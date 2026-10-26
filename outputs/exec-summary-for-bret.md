# AI SDLC Camp Rollout — Analysis and Recommendations
*Prepared for Bret Tushaus | October 2026*

---

## What We Built and Why

To evaluate the AI SDLC Camp rollout and produce an enablement strategy, I built a multi-agent analysis system using Claude Code subagents. Five specialized agents ran in sequence — each with a distinct mission, defined inputs, and structured outputs — coordinated by an orchestrator that passed findings downstream and synthesized the results.

The agents, their models, and what each produced:

| Agent | Model | Output |
|---|---|---|
| Program Evaluator | Sonnet | Structured assessment of camp quality, audience fit, and delivery readiness |
| Critical Reviewer (initial pass) | Sonnet | Adversarial stress-test of the camp itself — what is wrong before strategy is built |
| Adoption Strategist | Sonnet | Phased rollout strategy across both orgs |
| Workflow Transformation Analyst | Sonnet | Role-by-role mapping of what actually changes and where friction is highest |
| Measurement Architect | Haiku | Kirkpatrick-based measurement framework with 90-day calendar and monthly health check |
| Critical Reviewer (final pass) | Sonnet | Adversarial stress-test of the strategy and recommendations — 18 findings applied as a filter |

The critical reviewer ran twice: once before strategy was built (to find problems in the program), and once after (to find problems in the strategy itself). Its final-pass findings are applied as a filter throughout the recommendations — anything unsupported, vague, or contradicted is flagged rather than carried forward.

The system is reusable. Swap the input files for a different initiative and run it again.

---

## What the Agents Found

### The camp is technically solid. It is not rollout-ready.

The camp teaches a real, implemented workflow — the engineering skills have been live in the repo since September 16, the Rate Table example is a genuine end-to-end artifact, and the role-differentiation model is thoughtful. The agents found no factual errors in skill invocations, field names, or ADO conventions.

What they found instead:

**It has never been run by real learners.** Every lab procedure is untested. The Rate Table example — the only worked example — stops before Verifying, which is exactly where QE and Automation participants need it. You published it with the note "I have not read this myself yet." That is not a criticism; it is a condition that must change before November.

**Setup will fail before learning begins.** Expired ADO tokens, manual plugin upload with admin rights pending, KnowledgeBase coverage varying by domain, and token limits that blocked testing in September — all of these are acknowledged in the camp, none are resolved. At scale, a Teams channel routing to Saurendu is not a support path.

**Maconomy is invisible in a program it is supposed to adopt.** The word "Maconomy" does not appear in the camp. Their skills are placeholders. Their AI maturity is 10% vs. Vantagepoint's 50%. Their framework was designed around a different product, a different codebase, and a different tool surface. A Maconomy engineer opening this camp will encounter ADO paths, Aha workspace names, and skill names that are not their environment.

**Async HTML cannot install the behavior change the program claims to deliver.** The camp is trying to install a new operating system across four roles. "Propose, confirm, write-back," "Ground before you state," "Never fabricate" — these are team behaviors, not individual knowledge. Browser-stored module completion and multiple-choice knowledge checks are reference material delivery. The process requires Product, UX, Engineering, and QE to coordinate differently. That cannot happen through individual async completion.

---

## Two Decisions That Change Everything Downstream

**Decision 1: Is 75% of in-scope VP teams by December 31 a hard target or a directional goal?**

Phase 0 prerequisites run through early November. Phase 1 pilot runs through November 27. That leaves roughly 20 working days in December — during end-of-year vacation and release pressure — to reach 75% of VP teams with live-facilitated cohorts across US, Philippines, and India. The agents documented this as implausible and then built a Phase 2 schedule around it anyway. That was the critic's highest-severity finding.

Two scenarios for your conversation with Lisa:
- **Scenario A:** Compress to meet December 31. Accept higher risk of shallow adoption and measurement gaps. Phase 1 findings do not inform Phase 2.
- **Scenario B:** Redefine as 75% by end of Q1 2027. Phase 1 runs November with real findings. Phase 2 begins January. The strategy actually describes this scenario — it just doesn't say so.

Every downstream recommendation changes depending on which scenario you are optimizing for.

**Decision 2: Who facilitates the cohorts?**

Every structural reinforcement mechanism — applied sprint, office hours, post-cohort check-ins — requires a facilitator. None of the five agents could identify who that is, what their capacity is, or whether simultaneous December waves across three time zones are achievable by one person. If facilitation capacity does not exist, the behavior-change ambition of the program must be revised.

---

## The Top Recommendations

**1. Do not launch both orgs simultaneously.**
Vantagepoint first, then Maconomy — gated on three things that do not yet exist: Maconomy-specific content, Henrik Rosenstand's confirmed sponsorship, and VP pilot findings incorporated. This is the most well-supported recommendation in the package. The agents looked for evidence it is wrong and did not find any.

**2. Run a structured pilot with one cross-functional VP team before any broad rollout.**
One PDM, one developer, one QE. A real 2027.2 feature. Live facilitation. A defined pass/fail criterion. Every other finding in this analysis is a hypothesis — the pilot converts hypotheses to facts. This is not a suggestion; it is the load-bearing recommendation the strategy depends on.

**3. Lock the baseline before the first cohort, not in January.**
Same-team velocity baseline from ADO (last 3 sprints for the pilot team), adoption unit definition agreed with Lisa and Mike Scopa, counting method locked. The January survey is the Maconomy baseline, not the VP rollout trigger.

**4. The team is the unit of adoption, not the individual.**
"Done" = a PDM, developer, and QE on the same team run one feature end-to-end. Not individual module completion. Not tool installs. The measurement framework is built around this definition — it is the strongest document in the set.

**5. Get explicit about Henrik and Dan.**
The Maconomy gate requires their confirmed sponsorship. But confirmation before seeing content is a nominal commitment. The recommendation: bring Henrik a brief — the VP pilot results, the content gap, what Maconomy-specific content would require — and get a real commitment from that conversation, not a leadership briefing alone.

**6. The 4x ProPricer benchmark is a reference, not a gate.**
4x came from one team, one product, one moment. Applied as a pass/fail threshold to teams at different maturity levels without a transfer basis, it will demoralize teams showing real improvement at a different multiplier. Use it directionally.

---

## What the Agents Did Not Find

The analysis looked hard for these and did not find them:
- Factual errors in the camp's technical content
- Evidence that the no-simultaneous-launch recommendation is wrong
- Vanity metrics in the measurement framework's primary tracking set
- Conflict between the transformation analysis and the strategy — both agree on role disruption levels and friction hotspots
- Any recommendation across five agents that QE/Automation should launch before Stage 5 content is resolved

The failure mode here is organizational and capacity-based, not technical. The camp's content is genuine. The execution assumptions are the problem.

---

## On the Multi-Agent Approach

This system is worth describing because it reflects what agentic workflows can and cannot do.

What worked: each agent produced outputs that went beyond what a single-context analysis would catch. The critical reviewer's final pass surfaced 18 findings against the strategy — including the facilitation capacity gap that no other agent named, and the internal contradiction in including a QE in the Phase 1 pilot while simultaneously deferring QE content. The measurement architect independently produced a monthly health check that is genuinely runnable (45 minutes, no data team) from the same inputs that grounded the strategy.

What the system cannot do: it cannot tell you whether Henrik will commit, whether the camp is worth the friction at current AI maturity levels, or whether the behavior change ambition is calibrated to what VP teams can absorb in one release cycle. Those judgments require the Phase 1 pilot result and the humans in the room with you.

The system is designed to give you the terrain map. You navigate it.

---

*Full outputs: `/Users/iancowpar/Claude/ai-sdlc-pilot/outputs/`*
*System architecture: `/Users/iancowpar/Claude/ai-sdlc-pilot/ARCHITECTURE.md`*
