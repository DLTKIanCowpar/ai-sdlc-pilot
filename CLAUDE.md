# AI SDLC Enablement Agent Team — Orchestrator

## Purpose

This system evaluates an AI Software Development Lifecycle (AI SDLC) training program
and produces three deliverables:

1. **AI SDLC Enablement Strategy** — rollout approach for two product organizations
2. **Adoption Measurement Framework** — metrics, indicators, and evaluation cadence
3. **Prioritized Recommendations** — ranked, actionable next steps with rationale

## Required Inputs (fill before running)

- `inputs/program-overview.md` — what the AI SDLC Camp teaches, session structure,
  target audience, duration, delivery format
- `inputs/org-context.md` — the two product orgs: size, structure, current AI maturity,
  any known adoption constraints or risks
- `inputs/success-definition.md` — what "good adoption" looks like to leadership

## Execution Sequence

Run agents in this order. Each writes its output to `outputs/` for downstream agents to read.

### Phase 1 — Parallel (no dependencies)

Run both simultaneously:

```
Agent: program-evaluator
→ reads: inputs/program-overview.md, inputs/org-context.md
→ writes: outputs/program-assessment.md

Agent: critical-reviewer (pass --mode=initial)
→ reads: inputs/program-overview.md, inputs/org-context.md
→ writes: outputs/initial-critique.md
```

### Phase 2 — Parallel (depends on Phase 1)

Run both simultaneously after Phase 1 completes:

```
Agent: adoption-strategist
→ reads: outputs/program-assessment.md, outputs/initial-critique.md, inputs/org-context.md, inputs/success-definition.md
→ writes: outputs/enablement-strategy.md

Agent: workflow-transformation-analyst
→ reads: outputs/program-assessment.md, inputs/org-context.md
→ writes: outputs/transformation-analysis.md
```

### Phase 3 — Sequential (depends on Phase 2)

```
Agent: measurement-architect
→ reads: outputs/enablement-strategy.md, outputs/transformation-analysis.md, inputs/success-definition.md
→ writes: outputs/measurement-framework.md
```

### Phase 4 — Final review (depends on Phase 3)

```
Agent: critical-reviewer (pass --mode=final)
→ reads: all outputs/
→ writes: outputs/final-critique.md
```

### Phase 5 — Synthesis (orchestrator, no agent)

Read all outputs and synthesize into `outputs/recommendations.md`.
Apply the final critique as a filter: flag any recommendation that the critical reviewer
identified as unsupported, vague, or assumption-laden.

## Reuse Instructions

To adapt this system for a different AI adoption initiative:

1. Replace all files in `inputs/` with materials for the new initiative
2. Clear `outputs/`
3. Run Phase 1 through Phase 5 in sequence

Agent definitions in `.claude/agents/` do not need to change — they are initiative-agnostic.

## Constraints

- Do not invent organizational information. All claims must trace to an input file.
- All strategic decisions remain subject to human review before implementation.
- Distinguish clearly between: facts (sourced from inputs), inferences (reasoned from inputs),
  and recommendations (judgment calls requiring human approval).
