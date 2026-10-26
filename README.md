# AI SDLC Enablement Agent Team

A reusable multi-agent system built with Claude Code subagents.
Evaluates AI training programs and produces an enablement strategy, measurement framework,
and prioritized recommendations.

## First Use Case

AI Software Development Lifecycle (AI SDLC) Camp rollout across two Deltek product organizations.

## Quick Start

1. **Fill in the inputs** (the system produces nothing useful without them):
   - `inputs/program-overview.md` — the AI SDLC Camp materials
   - `inputs/org-context.md` — the two product organizations
   - `inputs/success-definition.md` — what leadership considers good adoption

2. **Open this project in Claude Desktop** (or Claude Code CLI from this directory)

3. **Run Phase 1** — ask Claude to run the program-evaluator and critical-reviewer agents simultaneously

4. **Continue through phases** — orchestrator instructions are in `CLAUDE.md`

5. **Review outputs** — all agent outputs land in `outputs/`

## What It Produces

| Output | Produced by |
|--------|------------|
| `outputs/program-assessment.md` | program-evaluator |
| `outputs/initial-critique.md` | critical-reviewer (mode=initial) |
| `outputs/enablement-strategy.md` | adoption-strategist |
| `outputs/transformation-analysis.md` | workflow-transformation-analyst |
| `outputs/measurement-framework.md` | measurement-architect |
| `outputs/final-critique.md` | critical-reviewer (mode=final) |
| `outputs/recommendations.md` | orchestrator synthesis |

## Reuse for Other Initiatives

Replace the contents of `inputs/` and clear `outputs/`. The agent definitions
in `.claude/agents/` are initiative-agnostic and do not need to change.

## Project Structure

```
ai-sdlc-pilot/
├── CLAUDE.md                        ← orchestrator instructions and execution sequence
├── README.md                        ← this file
├── ARCHITECTURE.md                  ← how the system works (for onboarding)
├── .claude/
│   └── agents/
│       ├── program-evaluator.md
│       ├── adoption-strategist.md
│       ├── workflow-transformation-analyst.md
│       ├── measurement-architect.md
│       └── critical-reviewer.md
├── inputs/                          ← you fill these in
│   ├── program-overview.md
│   ├── org-context.md
│   └── success-definition.md
└── outputs/                         ← agents write here
```
