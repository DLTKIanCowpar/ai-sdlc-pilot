# Prioritized Recommendations
## AI SDLC Camp Rollout — Vantagepoint and Maconomy

*Synthesized: October 2026 | Applies final critique as a filter | All claims labeled FACT / INFERENCE / RECOMMENDATION*

---

## Before Anything Else: Two Decisions Required

Every downstream recommendation changes depending on these two questions. They cannot be resolved analytically — they require organizational authority.

**Decision 1: Is 75% by December 31 a hard target or a directional goal?**

FACT: Lisa Rabideau set 75% of in-scope Vantagepoint teams by end 2026.
FACT (from program assessment): The camp has never been piloted, carries ~20 unbuilt items, and has setup prerequisites unresolved as of today.
CRITIC FLAG (HIGH): The enablement strategy flags this target as "tight" and proceeds to build a Phase 2 schedule around it anyway. This is the strategy's most damaging omission. Phase 0 runs through early November. Phase 1 pilot runs through November 27. That leaves ~20 working days in December — during end-of-year vacation and release pressure — to reach 75% of Vantagepoint teams with live-facilitated cohorts across US, Philippines, and India. The strategy cannot achieve both speed and depth simultaneously.

RECOMMENDATION: Before Phase 0 work begins, present Lisa and Bret with two explicit scenarios:
- **Scenario A:** Compress to meet 75% by December 31. Accepts higher risk of shallow adoption, measurement gaps, and a Phase 1 pilot that does not have time to inform Phase 2 design.
- **Scenario B:** Redefine as 75% by end of Q1 2027. Phase 1 runs November. Phase 2 begins January with pilot findings incorporated. This is what the strategy actually describes, despite claiming to meet the December target.

Do not build anything else until this conversation happens. Bret must be in the room.

---

**Decision 2: Who facilitates the cohorts?**

FACT (from enablement strategy): Facilitated, live cohorts are prescribed as the primary delivery model. Every structural reinforcement mechanism — applied sprint, bi-weekly office hours, post-cohort check-ins — requires a facilitator.
CRITIC FLAG (HIGH): None of the five agent outputs names the facilitator, assesses their current availability, or establishes that this capacity exists. "Facilitation" as currently written is a placeholder, not a plan. If Ian is the sole facilitator, simultaneous December waves across US, Philippines, and India are not simultaneously facilitatable.

RECOMMENDATION: Name the facilitator(s), assess their capacity, and determine whether the Phase 2 wave schedule is achievable before scheduling any cohort. If capacity does not exist for live facilitation, the reinforcement model — and therefore the behavior-change ambition of the entire program — must be revised.

---

## Immediate Actions (Phase 0, before November)

Ranked by consequence of inaction. Each includes a definition of "done" and a suggested owner.

**1. Lock the 75% vs. Q1 2027 scenario (Decision 1 above)**
Owner: Ian initiates; Lisa and Bret decide.
Done: Written record of which scenario the program is optimizing for, communicated to Hardik Shah, Melissa Coffey, Henrik Rosenstand.

**2. Confirm facilitation capacity and name the facilitator(s)**
Owner: Ian.
Done: Named person(s) with confirmed availability for Phase 1 and at least two Phase 2 waves.

**3. Resolve dvp persona menu defect**
FACT: The dvp plugin persona menu currently routes learners to a deprecated workflow. Any participant who does not read the warning carefully will follow the wrong process.
Owner: Plugin owner (Gaurav/GK — identity unconfirmed; confirming this identity is itself a Phase 0 action).
Done: Deployed fix confirmed in the plugin before Phase 1 pilot date.

**4. Establish the camp v2 completion date with a named author**
FACT: Camp v2 is required before rollout readiness can be confirmed. The poster (Bret Tushaus) noted at publication "I have not read this myself yet." Saurendu identified 14 documentation gaps. ~20 items are explicitly "not built yet."
Owner: Ian / program owner.
Done: v2 published with a confirmed review sign-off before Phase 1 cohort is scheduled.

**5. Force the contractor decision (85 Vantagepoint engineers)**
FACT: Tool access for the 85 Vantagepoint contractors is unconfirmed. The camp does not address this population.
Owner: Hardik Shah + procurement/IT.
Done: Written decision — in-scope with confirmed access path, or formally descoped with rationale.

**6. Lock the baseline measurement approach**
FACT: The measurement framework identifies the same-team baseline and counting method as hard prerequisites before the first cohort completes. The January survey is too late if Phase 1 has already run.
Owner: Lisa Rabideau, Mike Scopa.
Done: Adoption unit definition documented and signed ("PDM + dev + QE, one feature end-to-end"); story points baseline for Phase 1 pilot team pulled from ADO for last 3 sprints.

**7. Assess KnowledgeBase readiness per domain**
FACT: KB readiness is explicitly listed as the formal prerequisite for wider engineering rollout. Teams whose KBs are not ready cannot run a meaningful applied sprint.
Owner: Program manager + domain leads.
Done: Published list of which domains are KB-ready, by November 1.

**8. Designate a practice feature for the Phase 1 pilot team**
INFERENCE (from transformation analysis): Teams cannot run a meaningful applied sprint if they do not have a suitable story pre-identified. Identifying one under sprint pressure is how this fails.
Owner: PDM on pilot team + their Scrum Master.
Done: One real 2027.2 story from the pilot team's backlog chosen and confirmed before Phase 1 begins.

---

## Rollout Approach

RECOMMENDATION: Do not launch both orgs simultaneously. Sequence VP first, then Maconomy.

**Why this is the right call:**
FACT: The camp never mentions Maconomy. Most Maconomy-specific skills are placeholders. Maconomy's AI maturity is 10% vs. Vantagepoint's 50%. Henrik Rosenstand and Dan DiStefato have not confirmed their sponsorship stance. Launching Maconomy participants into Vantagepoint-specific content before their context is represented will produce disengagement and reinforce the org's current low baseline. The critic found no evidence this sequencing recommendation is wrong — it is the strongest recommendation in the package.

**Sequencing:**
- Phase 0 (now–early November): Prerequisites listed above.
- Phase 1 (November): One cross-functional VP pilot — one PDM, one developer, one QE — live facilitation, one real feature end-to-end. Pilot findings gate Phase 2.
- Phase 2 (December or January, depending on Decision 1): VP broader rollout in cohort waves. QE deferred until Stage 5 content and automation trigger decision resolved. Philippines/India timezone-appropriate facilitation required.
- Phase 3 (January–March 2027): Maconomy. Gated on: Maconomy-specific content built, Henrik confirmed, VP findings incorporated, Maconomy KB assessed.

**The internal contradiction the critic flagged (MED):**
The strategy defers QE/Automation to Phase 2 because Stage 5 content is incomplete — then includes one QE in the Phase 1 pilot "specifically to identify what is missing." If Stage 5 is incomplete, the Phase 1 QE experiences the same incomplete content the strategy is trying to avoid for the broader cohort. The learning from including a QE in Phase 1 ("Stage 5 is incomplete") is already known without running a person through it. RECOMMENDATION: Either fix Stage 5 before Phase 1 so the QE experience is meaningful, or exclude QE from Phase 1 and document Stage 5 gaps directly from the content review.

**Maconomy sponsorship sequencing (critic flag, MED):**
The strategy recommends confirming Henrik's sponsorship before building Maconomy content. The critic notes this is backward — Henrik needs to see what he is sponsoring to make an informed commitment. RECOMMENDATION: Prepare a brief (not the full camp) showing Henrik the VP pilot results, the content gap, and what Maconomy-specific content would require. Use that briefing to get a real commitment, not a nominal one.

---

## Reinforcement Model

A single async pass through the camp will not produce the behavior changes the program claims to deliver. FACT (confirmed by both the program assessment and the initial critique). The following are structural interventions, not a wishlist.

**What must happen, in order:**

1. **Pre-cohort:** Practice feature pre-designated. Every cohort participant's setup verified before Day 1. KnowledgeBase domain coverage confirmed for the cohort team.

2. **During cohort:** Live facilitation, not async. The behavior-change goals — "Ground before you state," "Propose, confirm, write-back," "Never fabricate" — require live correction, not self-discovery.

3. **Within 7 days:** Cohort team runs the pre-designated story through Framing to Verifying. This is the "done" criterion for team-level adoption. CRITIC FLAG (MED): This assumes teams have sprint slack and a suitable low-risk story available within a 2-week sprint cycle. Pre-designating the practice feature (Phase 0 action 8 above) is what makes this achievable, not a training outcome.

4. **At 14 days:** Manager conducts post-cohort check-in. CRITIC FLAG (MED): "Manager check-in mandatory" with no defined consequence is a wish, not a mandate. What happens if it does not happen? The escalation path ("escalate to program sponsor") must name a consequence that changes manager behavior, not just notifies someone. Define this before Phase 2.

5. **Ongoing:** Gate hold rate monitored in ADO. PDM write-back confirmed in Aha. The monthly health check (measurement framework) is the mechanism — run it on the first Monday of each month.

**What is excluded from the reinforcement model:**
- Vanity metrics: session attendance, module completion rates, "awareness" survey scores.
- Activity-based success signals: number of cohorts run, number of participants enrolled.
- The 4x ProPricer benchmark as a pass/fail threshold. CRITIC FLAG (MED): 4x comes from a different product, different team, different maturity level. Using it as a target for VP or Maconomy teams without establishing a transfer basis risks demoralizing teams who show real improvement at a different multiplier. Use it as a directional reference, not a gate.

---

## Measurement: What to Lock Before You Start

The measurement framework is the strongest document in this package. Its Kirkpatrick structure is sound, it correctly weights Level 3 (behavior) most heavily, and its failure signals are specific enough to be observable. Three non-negotiables before the first cohort runs:

**Non-negotiable 1 (FACT):** Same-team velocity baseline — last 3 sprints for the pilot team — pulled from ADO and documented with Mike Scopa before Phase 1 begins. No baseline, no result.

**Non-negotiable 2 (FACT):** Adoption unit definition documented and signed: "PDM + developer + QE on the same team, one feature run end-to-end." This definition determines what counts as adoption for reporting. Lock it before counting anything.

**Non-negotiable 3 (FACT):** Counting method agreed with Lisa and Mike before the January survey is fielded. The survey is the Maconomy baseline, not the VP rollout trigger.

**Two metrics the critic flagged as potentially unmeasurable — resolve these before Phase 2:**
- CRITIC FLAG (HIGH): Developer `/code-review` usage depends on PR log access or self-report. Neither is confirmed. If PR log access cannot be granted, this metric cannot be reliably measured and should be replaced or dropped before it becomes a reporting gap.
- CRITIC FLAG (HIGH): No metric currently captures whether gate discipline holds under the first high-pressure release. The 90-day measurement cadence will miss the sprint crunch moment. Add a gate hold rate spot-check tied to the first VP release cycle after each cohort — not just to the 30/60/90 calendar.

**Drop from the measurement plan:**
- EVI Productivity Index as an attributable rollout metric. CRITIC FLAG (LOW): In a multi-change environment, movement in the EVI index cannot be attributed to this program specifically. Track it as context; do not report it as a program result.

---

## What the Agent Team Did Not Find

This section gives the recommendations their credibility. The analysis searched for these and did not find them:

- No internal contradiction between the measurement framework's Kirkpatrick structure and the behavior-change goals of the program. The framework correctly weights Level 3 and its leading indicators are behavioral, not activity-based.
- No evidence that the "no simultaneous launch" recommendation is wrong. The sequencing rationale is well-grounded in all available inputs.
- No fabricated risks in the risk register. All 13 risks trace to something in the inputs.
- No conflict between the transformation analysis and the enablement strategy. Both documents agree on role disruption levels, friction hotspots, and enabling conditions.
- No recommendation in any document that QE/Automation be launched before content is ready. All five documents are consistent on this point.
- No factual errors in skill invocations, field names, or ADO conventions in the camp content.
- No vanity metric in the measurement framework's primary tracking set. The metrics chosen are genuinely behavioral.

**What the agent team found but could not resolve:**
- Whether the program's behavior-change ambition is calibrated to what VP teams at current AI maturity can absorb in a single release cycle. This is a judgment call that requires the Phase 1 pilot result — and a recovery protocol if the result is net-negative.

---

## Open Questions (Organizational Authority Required)

The critic's single highest-priority recommendation applies to question 5 below. All others are downstream of it.

1. **Contractor tool access (85 VP):** In or out of scope? Who owns the decision and by when? [Owner: Hardik Shah + IT/procurement]

2. **Gaurav/GK identity and scope:** Who resolves Phase 0 plugin and admin-rights blockers? What is their confirmed availability? [Owner: Hardik Shah to confirm]

3. **Henrik Rosenstand and Dan DiStefato stance:** What do they need to confirm active Maconomy sponsorship — and who facilitates that conversation? [Owner: Bret Tushaus]

4. **QE automation trigger and preferred TC tool:** Who decides, and by what date? QE cohorts cannot be scheduled until this is resolved. [Owner: Hardik Shah + QE lead]

5. **75% by end-2026 — binding or directional? (CRITIC PRIORITY — HIGH):** This is the decision that changes everything downstream. Present Scenarios A and B to Lisa and Bret before any Phase 0 work proceeds. The strategy documents the tension; it does not resolve it. [Owner: Lisa Rabideau, Bret Tushaus]

6. **Baseline measurement and counting method:** Confirmed by whom and by what date? Must be locked before Phase 1 begins. [Owner: Lisa Rabideau, Mike Scopa]

7. **Camp v2 completion date:** When is it confirmed ready? Who signs off? [Owner: Ian / program owner]

8. **Philippines and India facilitation model:** Live or async-with-office-hours? If async, who staffs office hours and when? [Owner: Ian + Hardik Shah]

9. **Help desk roles in scope?** Eight VP, ten Mac. No input documents address this. [Owner: Hardik Shah, Henrik Rosenstand]

10. **Champions role — formal or informal?** Time allocation, recognition, and scope for Anders Hessellund (Maconomy) and equivalent VP champions. If it is on top of existing responsibilities with no acknowledgment, it will not hold. [Owner: Bret Tushaus / respective engineering leads]

**Note on question 5 and the critic's finding:** The strategy retains the 75% target while documenting it as implausible. The critic's single actionable recommendation is to surface this contradiction explicitly before committing to a Phase 2 schedule. Every other question above is conditional on the answer.

---

*This document synthesizes outputs from five analytical agents. All recommendations require human review before implementation. Organizational decisions marked above cannot be resolved analytically — they require the authority of the named decision owners.*
