# Agent Architecture

## How Claude Code Subagents Work

When Claude Code (the orchestrator) invokes a subagent, it spawns a fresh Claude instance.
That instance has no memory of prior conversations. Everything it knows comes from its
system prompt (defined in the agent file) plus whatever the orchestrator explicitly passes
in the invocation prompt.

This means:
- **Context is a parameter.** The orchestrator must pass prior agent outputs directly.
- **Agents cannot talk to each other.** All coordination happens through the orchestrator.
- **Outputs are text.** Agents write to files; the orchestrator reads those files and passes
  excerpts to the next agent.

## Agent Definitions

Each agent lives in `.claude/agents/<name>.md`. The frontmatter controls the runtime:

```yaml
---
name: agent-name
description: One-line description (used by Claude to select the right agent)
model: claude-sonnet-4-6   # or claude-haiku-4-5-20251001
tools: Read, Write          # what the agent can do
---
[system prompt body]
```

## Execution Graph

```
inputs/
  program-overview.md
  org-context.md
  success-definition.md
        │
        ├─────────────────────────────────┐
        ▼                                 ▼
  program-evaluator               critical-reviewer
  (Phase 1, parallel)             --mode=initial
        │                         (Phase 1, parallel)
        │                                 │
        ▼                                 ▼
  outputs/program-assessment.md    outputs/initial-critique.md
        │                                 │
        ├─────────────┐                   │
        ▼             ▼                   │
  adoption-       workflow-               │
  strategist  transformation-             │
  (Phase 2)     analyst                   │
                (Phase 2)                 │
        │             │                   │
        ▼             ▼                   │
  outputs/          outputs/              │
  enablement-       transformation-       │
  strategy.md       analysis.md           │
        │             │                   │
        └──────┬───────┘                  │
               ▼                          │
       measurement-architect              │
       (Phase 3)                          │
               │                          │
               ▼                          │
       outputs/measurement-               │
       framework.md                       │
               │                          │
               └──────────────────────────┤
                                          ▼
                                  critical-reviewer
                                  --mode=final
                                  (Phase 4)
                                          │
                                          ▼
                                  outputs/final-critique.md
                                          │
                                          ▼
                                  [orchestrator synthesizes]
                                          │
                                          ▼
                                  outputs/recommendations.md
```

## Agent Responsibilities

| Agent | Model | Runs | Purpose |
|-------|-------|------|---------|
| program-evaluator | Sonnet | Phase 1 | Structured assessment of training program quality and fit |
| critical-reviewer | Sonnet | Phase 1 + Phase 4 | Adversarial stress-test (twice: program first, strategy last) |
| adoption-strategist | Sonnet | Phase 2 | Rollout strategy grounded in assessment + critique |
| workflow-transformation-analyst | Sonnet | Phase 2 | Maps workflow delta and friction terrain |
| measurement-architect | Haiku | Phase 3 | Builds Kirkpatrick-based measurement framework |

## Model Selection Rationale

- **Sonnet** for agents where output quality is the foundation of downstream work,
  or where adversarial reasoning is required.
- **Haiku** for the measurement-architect: the task is formulaic
  (apply a known framework to specific inputs), risk to quality is low,
  and it runs on synthesized inputs rather than raw ambiguous source material.

## Claim Labeling Convention

All agents label their outputs:
- **FACT** — directly stated in input materials
- **INFERENCE** — reasoned from input materials
- **ASSUMPTION** — plausible but not grounded in available data
- **RECOMMENDATION** — judgment call requiring human approval
- **UNKNOWN** — not answerable from available inputs

This convention keeps the system epistemically honest and makes it clear
what decisions require human judgment before action.

## Reuse Pattern

The agents are initiative-agnostic. To adapt for a new AI adoption initiative:

1. Create a new project directory (e.g., `ai-champion-rollout/`)
2. Copy `.claude/`, `inputs/`, `outputs/`, `CLAUDE.md`, `README.md`
3. Replace `inputs/` contents with new initiative materials
4. Clear `outputs/`
5. Run phases 1–5

No agent system prompts need to change. The agents reason about whatever
program and org materials you give them.
