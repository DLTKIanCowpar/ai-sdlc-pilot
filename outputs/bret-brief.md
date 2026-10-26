# AI-SDLC Camp — Analysis Brief for Bret
*Ian Cowpar · October 2026*
*V1 and V2 agent runs both complete.*

---

## What I Built and Why

While you were in V2, I built a multi-agent analysis system using Claude Code subagents and ran it against V1 of the camp. Then when V2 went live tonight, I fetched all seven modules directly from Railway and ran the same system again. Two full passes, side by side.

Here's the system, peer-to-peer.

---

## The Agent Architecture

Five specialized agents, running in sequence. No shared memory between them — each reads from files, writes to files, and the next agent reads those files before running. The orchestrator coordinates the phases and synthesizes the final output.

```
inputs/
├── program-overview.md     ← what I fed in about the camp
├── org-context.md          ← VP and Maconomy org profiles
└── success-definition.md   ← Lisa's targets, Dinakar's benchmark

Phase 1 (parallel — no dependencies):
  program-evaluator          → program-assessment.md
  critical-reviewer (initial) → initial-critique.md

Phase 2 (parallel — reads Phase 1):
  adoption-strategist            → enablement-strategy.md
  workflow-transformation-analyst → transformation-analysis.md

Phase 3 (sequential — reads Phase 2):
  measurement-architect → measurement-framework.md

Phase 4 (reads all outputs):
  critical-reviewer (final) → final-critique.md

Phase 5 (orchestrator synthesizes all six):
  → recommendations.md
```

**Why the critic runs twice.** The first pass stress-tests the program before any strategy is built. The second stress-tests the strategy itself. If the critic only runs at the end, it's reading its own team's work — an echo chamber. Two adversarial passes with the strategy built in between is the structural fix.

**Why Haiku for the measurement architect.** The Kirkpatrick framework, 90-day calendar, and monthly health check are formulaic work. Haiku is fast and cheap for templated output. Every agent doing analytical judgment gets Sonnet.

**Claim labeling.** Every substantive claim across all six agents is labeled FACT / INFERENCE / RECOMMENDATION / UNKNOWN. FACT means it's in the source files. INFERENCE means it's reasoned from source. RECOMMENDATION is a judgment call requiring human approval. This is how you audit the output — you can see the epistemic status of every sentence without having to trust that the agent was careful.

**The mandatory "What I Did Not Find" section.** The critical reviewer is required to list what it searched for and didn't find. Without this, a clean assessment is meaningless — you can't tell whether the agent tried hard or didn't look. With it, a clean bill of health carries weight.

**Reusability.** I ran the same agent team against the Make AI Work manager program this week. Swap inputs, clear outputs, run again. The agents are initiative-agnostic.

---

## What V1 Analysis Found

### The content is technically solid

No factual errors in skill invocations, field names, or ADO conventions. The Rate Table example is a genuine end-to-end artifact. Role differentiation is thoughtful. The critic looked hard for fabricated risks and didn't find any.

### What it's not: rollout-ready (V1 verdict)

**Setup will fail before learning begins.** Expired ADO tokens, manual plugin upload with admin rights pending, KB coverage gaps, token limits that blocked September testing. At scale, routing to a Teams channel is not a support path.

**Maconomy was invisible.** The word didn't appear in the camp. Their skills were placeholders. 10% AI maturity vs. VP's 50%. A Maconomy engineer following V1 would hit ADO paths, Aha workspace names, and skill names that don't exist in their environment.

**Async HTML cannot install cross-role coordination.** "Propose, confirm, write-back," "Ground before you state," "Never fabricate" — these are team behaviors. Browser-stored completion and knowledge checks deliver reference material. They don't change how a PDM, developer, and QE work together.

**Stage 5 QE/Automation content was incomplete.** The path QE and Automation engineers needed most was the least finished.

### The critic's two highest-severity findings

**The 75%-by-end-2026 target doesn't survive its own prerequisites.** Phase 0 through early November. Phase 1 pilot through November 27. ~20 December working days to reach 75% of VP teams across three time zones during year-end pressure. The strategy documented this as "tight" and built a Phase 2 schedule around the original target anyway. The critic called it "optimism masquerading as planning."

**Who facilitates?** Every structural reinforcement mechanism requires a named facilitator. None of the five agents could identify who that is or confirm their capacity. This was the highest-unaddressed structural risk across the full V1 output.

---

## V1 vs. V2: What the Agents Found

### What V2 genuinely resolved

| V1 Finding | V2 Status |
|---|---|
| SharePoint distribution risk | **Resolved.** GitHub/Railway is the right infrastructure call. Version-controlled, publicly accessible. |
| Maconomy invisible | **Partially resolved** (no longer a blocker for VP launch). Maconomy is named in Modules 1 and 3. A Maconomy engineer now knows they're unsupported before hitting it, rather than discovering it mid-exercise. That's better than silence. It is not a solution. |
| No role orientation for non-engineers | **Substantially improved.** Nine role-explainer videos. For UX, Documentation, and Scrum Master populations, this was the highest-value single V2 addition. |
| dvp persona menu defect (V1-specific) | **Not carried forward.** V2 restructured enough that the V1-specific defect is not identifiable in the new content. |

### What survives unchanged

Ten V1 findings are structurally the same in V2: setup dropout risk, Stage 5 incompleteness (all seven open items still open), async-cannot-install-cross-role-coordination, no backend progress tracking, 75% target implausibility, facilitation capacity unnamed, 4x ProPricer without transfer basis, no recovery protocol for a bad first cohort, single-point Bret dependency, gate discipline not measured at sprint crunch.

### What V2 introduces that V1 couldn't have found

**The "product-agnostic" claim is structurally false for Maconomy.** This is the agents' sharpest new finding. V2 uses "Your product" substitution throughout — but for a Maconomy engineer, "Your product" resolves to: zero KB domains, placeholder skills, scaffold plugin. The framing creates an expectation the content cannot meet. V1 was silent about Maconomy. V2 raises the expectation without the infrastructure to back it. The agents' read: *this is a step backward from V1's silence for Maconomy participants specifically* — because now they'll arrive expecting something.

**No recovery path from "scaffold today."** When a Maconomy participant hits a "Your product" note and finds a scaffold, the camp gives them nothing to do next — no named owner, no timeline, no "stop here" gate, no escalation. They either proceed and find skill failures, or disengage invisibly.

**Three-tier participant experience.** V2 now has three functionally distinct populations: (1) VP teams in 5 populated KB domains — fully operational; (2) VP teams in 83 empty domains — conceptual only, engineering skills degraded; (3) Maconomy — orientation only, no operational layer. Running a combined November launch without surfacing these tiers in the camp itself will produce visible asymmetry during Module 5 labs.

**Author hasn't reviewed it word-for-word — same condition as V1.** Same language in the V2 readiness summary as V1. Not a criticism of V2 specifically, but six of your own open questions suggest unreviewed content may contain errors or stale references. Before 377 engineers use this as an operating system, that review is the minimum quality bar.

---

## Top Recommendations (V2 synthesis)

### Before anything else: four decisions that change everything downstream

**D1. Is the 75% end-2026 target binding or directional?**
Scenario A: compress, accept shallow adoption risk, no time for Phase 1 findings to inform Phase 2.
Scenario B: 75% by Q1 2027 — Phase 1 runs November with real findings, Phase 2 starts January.
Owner: Lisa and Bret. Deadline: before any cohort is scheduled.

**D2. Maconomy November — in or out?**
If in: Modules 0-1 only, awareness track content assigned to a named owner, Henrik reviews it before distribution, Maconomy is never sent the full camp URL without a routing decision.
If out: no Maconomy communication in November, committed Phase 3 gate review date in 27.1.
The current default — send the full camp link with a verbal "stop at Module 1" — is not an awareness track.
Owner: Bret with Henrik. Deadline: before November kickoff is scheduled.

**D3. Who facilitates?**
Name the person(s), confirm availability for Phase 1 and at least two Phase 2 waves. If no confirmed facilitator, the reinforcement model must be revised.
Owner: Ian or designated program lead.

**D4. Are the six open questions resolved or explicitly deferred — each with a decision date?**
Q1 (does the plugin use the KB?) and Q6 (are ADO/TFS MCP connector instructions complete?) are blocking. The other four need a resolution or a named deferral. "We'll answer in the kickoff session" is a valid deferral. Silence is not.
Owner: Bret. Deadline: before camp is distributed.

### Immediate actions (pre-launch), ranked by consequence of inaction

1. **Author completes word-for-word review.** Minimum quality bar before distribution to 377 engineers.
2. **Three-person pilot before the org-wide kickoff.** One VP engineer new to the framework, one VP PDM, one Maconomy observer. Document every failure point. Fix before the kickoff is scheduled.
3. **Lock the velocity baseline before Phase 1.** Mike Scopa pulls last three sprints for the pilot team from ADO. No baseline = no result. Dinakar's standard is a before/after number.
4. **Confirm token guidance and AI gateway budget.** Token exhaustion blocked VP testing in September. Lab failures from quota exhaustion in Phase 1 will be attributed to the framework, not infrastructure.
5. **Assign KB domain owners for Phase 1 VP teams.** Teams in empty domains should know before they reach Module 5 labs, not during them.
6. **Pre-designate a practice feature for the Phase 1 pilot team.** Teams cannot run an applied sprint if they haven't designated a story before the sprint starts.
7. **Contractor access decision (85 VP engineers).** Written decision: in-scope with confirmed access, or formally descoped. Before Phase 1.
8. **Name a Maconomy awareness track owner.** If D2 is "in," someone needs to write a one-page status communication, get Henrik to review it, and scope what Maconomy participants actually receive.

### Rollout phasing

- **Phase 0 (now–October 31):** All eight actions above closed. D1–D4 resolved.
- **Phase 1 (November, weeks 1–2):** VP pilot — feature teams in the 5 populated KB domains only. QE participates as observer, not functional adopter (Stage 5 unresolved). Go/no-go gate with three explicit questions before Phase 2 is scheduled.
- **Maconomy awareness (November, conditional on D2):** Modules 0-1 only, written status comms, Henrik-reviewed.
- **Phase 2 (November week 3–December):** VP broader rollout, segmented by KB readiness. Each incoming team's domain must be populated or explicitly flagged before their camp link is sent.
- **Phase 3 (Q1 2027):** Maconomy operational rollout. Seven gate conditions named in the synthesis doc — each needs a named owner assigned before November or they remain a list of hopes.

---

## Where Anne and Janil Can Help

Based on what the agents surfaced, here's where your team's capacity is most load-bearing:

**KB domain population — highest leverage, most time-intensive.**
5 of 88 VP domains populated. The KB is the grounding layer the skills depend on. Without it, skills run "from live source with reduced grounding" and say so. Running `createdomainmap` across priority domains — starting with the domains the Phase 1 pilot team works in — is the single highest-leverage contribution before Phase 2 arrives. Anne and Janil doing this systematically converts the camp from a demonstration to a reliable operating system.

**Maconomy content scoping — gated on D2, but prep can start now.**
Someone needs to map what Maconomy-specific skills, KB domains, and "Your product" substitution content actually requires. This is a scoping exercise that doesn't wait for Henrik's commitment — it gives Henrik something real to react to. Anne or Janil doing that mapping before the November conversation with Henrik changes the quality of that conversation.

**Stage 5 QE/Automation open items — seven, all unresolved.**
Items 1-3 (Dev/QE coordination model, test case timing, QE review of AI-generated tests) are org-design questions, not content questions. They require a decision from whoever owns Dev/QE coordination in VP engineering. If Anne or Janil have that relationship with Sherelyn Natividad or the QE leads, they're well-positioned to drive those conversations to a resolution — or at minimum to a named decision-date — before QE is included in Phase 2 distribution.

**Phase 1 pilot logistics.**
Pre-flight setup verification for each pilot participant (connectors live, KB domain confirmed, ADO token valid, token budget confirmed) is structured, non-judgment work that prevents the exact setup dropout the agents flagged. Someone needs to own this systematically.

**Measurement cadence post-Phase 1.**
Gate hold rate monitoring, monthly health check, 30/60/90 day reads — none of this requires a data team. It requires a systematic person with 45 minutes a month and ADO/Aha access. If Anne or Janil can own this cadence, it frees you to run the strategic relationships (Lisa, Bret, Henrik, Dinakar readout).

---

## What the Agents Cannot Tell You

The agent team is a terrain map. It found:
- No factual errors in the camp's technical content (within what the overview covers — the word-for-word review may find more)
- No evidence the VP-first sequencing recommendation is wrong — the Maconomy gap is grounded in all available inputs
- No vanity metrics in the measurement framework's primary tracking set
- No conflict between the transformation analysis and the enablement strategy on role disruption levels or friction hotspots

What it cannot find — because these require humans:
- Whether the behavior-change ambition is calibrated to what VP teams at current AI maturity can absorb in one release cycle. The Phase 1 pilot — with a defined go/no-go gate — is the only mechanism that answers this.
- Whether Maconomy will reach Phase 3 gate conditions on any defined timeline. The default state is indefinite scaffold. Only organizational decisions change that.
- What the right answer is on the 75% target.
- Whether Henrik will commit.

Those are yours and Lisa's. The agents give you the argument; you make the call.

---

*V1 outputs: `/Users/iancowpar/Claude/ai-sdlc-pilot/outputs/`*
*V2 outputs: `/Users/iancowpar/Claude/ai-sdlc-v2-pilot/outputs/`*
*Make AI Work outputs: `/Users/iancowpar/Claude/make-ai-work-pilot/outputs/`*
*System architecture: `/Users/iancowpar/Claude/ai-sdlc-pilot/ARCHITECTURE.md`*
