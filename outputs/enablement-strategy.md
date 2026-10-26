# Enablement Strategy
## Vantagepoint AI-SDLC Camp — Cross-Org Rollout
*Prepared: October 2026 | Status: Draft for Human Review*

---

## Executive Summary

The Vantagepoint AI-SDLC Camp is technically sound but not yet pilot-ready: it has never run with real learners, contains approximately 20 unbuilt items, and carries setup friction that can block participants before they encounter any content. [FACT] A simultaneous November launch across both orgs carries high risk of shallow adoption that satisfies the checkbox but fails Lisa's four adoption tests — tool use alone does not count. [INFERENCE] The highest-leverage intervention before any broad rollout is a tightly scoped pilot with one cross-functional Vantagepoint team (PDM, developer, QE), run before the November target, to surface real blockers and prove the learning model. [RECOMMENDATION] Maconomy should not launch until Vantagepoint's framework is stable, Maconomy-specific content exists (currently placeholder), and Henrik Rosenstand's leadership stance is confirmed. [RECOMMENDATION] Every recommendation in this document requires human review and organizational authority before implementation; open questions are surfaced explicitly rather than papered over.

---

## Recommended Sequencing

### Why Not Simultaneous Launch

A simultaneous November launch across both orgs is not recommended for the following reasons:

- **Content mismatch:** The camp is Vantagepoint-built, Vantagepoint-specific, and the word "Maconomy" does not appear in it. Maconomy-specific skills are placeholders. Launching Maconomy participants into this content before it reflects their context will produce disengagement and reinforces the org's current 10% AI maturity baseline. [FACT]
- **Leadership stance unknown:** Henrik Rosenstand's and Dan DiStefato's stance on the program is unconfirmed. Manager activation (see section below) is a prerequisite for adoption — not a follow-on. Launching without confirmed manager engagement is a documented failure signal. [FACT, INFERENCE]
- **Maturity gap:** Vantagepoint is at 50% AI maturity with a live framework, live skills since 16 September 2026, and a working team that has already reviewed the camp. Maconomy is at 10% and has had one internal tech talk. These are not equivalent starting points. [FACT]
- **Diluted signal:** Running pilots simultaneously means problems discovered in one org cannot inform the other. Sequencing preserves learning.

### Recommended Phasing

#### Phase 0 — Readiness Gating (Now through early November 2026)
*Duration: ~3–4 weeks. Runs in parallel with Phase 1 preparation.*

Prerequisites that must be true before Phase 1 can begin:

1. Camp v2 content complete and reviewed — do not launch on content out of date with the repo. [FACT — stated non-negotiable]
2. Setup friction resolved or documented workarounds confirmed: expired ADO tokens, manual plugin upload, admin rights, token limits. The person responsible (Gaurav/GK) and their scope must be confirmed. [FACT — blocker identified]
3. Contractor tool access for Vantagepoint's 85 contractors confirmed or explicitly out-of-scope with a documented decision. [FACT — unresolved]
4. KnowledgeBase readiness assessed per domain. A published completion deadline must exist; teams whose KBs are not ready should be scheduled for a later cohort, not blocked in November. [RECOMMENDATION, consistent with Input 4]
5. Baseline measurement approach agreed: the counting method, same-team baseline, and survey instrument must be locked before rollout starts. The January survey is too late if rollout has already begun. [FACT — failure signal identified; RECOMMENDATION to act now]
6. dvp persona menu fixed — currently routes to deprecated workflow. [FACT]

#### Phase 1 — Vantagepoint Pilot Cohort (November 2026)
*Duration: 2–3 weeks. Gate: one cross-functional team completes end-to-end.*

- **Who:** One cross-functional team — one PDM, one developer, one QE — drawn from Vantagepoint US or India-based staff (where timezone and async logistics are most manageable for rapid iteration). [RECOMMENDATION]
- **Why this team, not broader cohort:** Team-level adoption is the right unit of measurement. The camp is "done" when a PDM, developer, and QE on the same team have run one feature end-to-end together. Every finding from the assessment is a hypothesis until piloted. [FACT — from Input 4]
- **Facilitated, not async:** This pilot must be run with live facilitation, not as a solo async pass. Behavior change goals — "Ground before you state," "Propose, confirm, write-back," "Never fabricate" — cannot be developed through a single async HTML walkthrough. [FACT — from Input 4]
- **Deliverable:** A documented feature run through Framing to Verifying, a setup issue log, a content gap log, and a revised readiness assessment for Phase 2. Pilot findings gate Phase 2 launch.
- **Gate to Phase 2:** Pilot team completes end-to-end. Blockers categorized as resolved, workaround-documented, or descoped. Camp content updated with findings.

#### Phase 2 — Vantagepoint Broader Rollout (December 2026 — January 2027)
*Duration: 4–6 weeks. Target: 75% of in-scope Vantagepoint teams by end 2026, as per Lisa's target.*

- Run cohorts of 3–5 teams. Prioritize teams with KB-ready domains first.
- Philippines and India teams need timezone-appropriate facilitation or a supported async model with live office hours. [INFERENCE — based on location data]
- QE/Automation path needs a decided automation trigger and preferred TC tool before these participants run their lab. This is an unresolved content gap. [FACT]
- UX and Scrum Master roles need additional scaffolding before their cohorts run. [FACT]
- Contractors: if tool access is confirmed, add a cohort; if not, formally descope with documented decision.

#### Phase 3 — Maconomy Onboarding (January — March 2027)
*Duration: 6–8 weeks. Target: Maconomy "joins more fully" — 100% of in-scope teams by 1H 2027.*

Prerequisites specific to Maconomy before Phase 3 can begin:

1. Maconomy-specific content added to camp — skills, worked examples, personas. Placeholder content is not sufficient. [FACT]
2. Henrik Rosenstand and Dan DiStefato have confirmed their leadership stance and have completed the manager activation sequence (see section below). [RECOMMENDATION]
3. Anders Hessellund confirmed as in-scope champion and briefed on his role in Phase 3. [RECOMMENDATION]
4. Vantagepoint pilot findings incorporated into camp. Maconomy teams benefit from Vantagepoint's learning.
5. Maconomy-specific KnowledgeBase domains assessed and scheduled.

---

## Audience Segments and Approach

### Segment 1: Product Managers (PDMs) — Highest Priority
*14 Vantagepoint, 10 Maconomy*

Highest-leverage first cohort. Lisa's success definition requires every PDM to run at least one 2027.2 feature through Framing and Capability Spec. [FACT] PDMs are the upstream gate — if they don't adopt, downstream engineering and QE adoption has nothing to connect to.

- **Rollout approach:** Include a PDM in the Phase 1 pilot team. Cohort PDMs early in Phase 2 alongside their paired developers, not separately.
- **Support needed:** Framing and Capability Spec walkthroughs with Maconomy/Vantagepoint domain context. The 20% gap ("your team supplies the rest") is unscaffolded — PDMs with low AI maturity cannot fill this without support. [FACT — from Input 4]
- **Timing:** Must precede or co-launch with developer cohorts. A developer cohort without an AI-SDLC-capable PDM upstream cannot demonstrate connected adoption.

### Segment 2: Software Engineers — Core Delivery
*52 Vantagepoint, 56 Maconomy, plus contractors TBD*

The engineering skills have been live in Vantagepoint's repo since 16 September 2026. [FACT] Some engineers may have already explored them. This creates uneven baseline — some will come in with partial exposure, others cold.

- **Rollout approach:** Cohort with paired PDM and QE. Avoid engineering-only cohorts that cannot demonstrate end-to-end connected adoption.
- **Setup prerequisite:** ADO token refresh, plugin installation, and admin rights must be resolved before cohort scheduling. Engineers who hit setup blockers in the first session have high dropout risk. [FACT — from Input 3]
- **Timing:** Phase 2 core track after pilot findings incorporated.

### Segment 3: QE / Automation Engineers — Deferred Until Content Ready
*39 Vantagepoint, 30 Maconomy*

The QE/Automation path has an unresolved content gap: the automation trigger and preferred TC tool are undecided, and the Rate Table example stops before Verifying. The QE lab has no worked precedent. [FACT] Scheduling QE cohorts before this is resolved will produce an incomplete experience and undermine credibility.

- **Rollout approach:** Deferred within Phase 2 until QE content gap is resolved. One QE included in the Phase 1 pilot specifically to identify what is missing.
- **Decision required:** Who decides the automation trigger and preferred TC tool, and by when?

### Segment 4: Architects — Enabler Track
*19 Vantagepoint, 25 Maconomy*

Architects are disproportionately represented in Maconomy (25 of 135). [FACT] They are likely to be the technical skeptics or champions — their early endorsement accelerates adoption across teams.

- **Rollout approach:** Brief architects before their team cohorts. Frame the camp in terms of design integrity and gate ownership, not tool use. Architects need to see the "humans at gates" model, not "humans as triggers." [INFERENCE]
- **Timing:** Early in each org's Phase 2/3.

### Segment 5: Engineering Leaders — Manager Activation Track (see next section)
*12 Vantagepoint, 9 Maconomy*

### Segment 6: UX and Scrum Masters — Scaffolding Required
These roles are under-scaffolded in current content. [FACT] Do not cohort them until scaffolding is added. Include in a later Phase 2 wave.

### Segment 7: Contractors (85 Vantagepoint, 4 Maconomy)
Tool access is unconfirmed for the 85 Vantagepoint contractors. [FACT] Camp content says nothing about this population. This requires an explicit organizational decision — include with documentation of access, or formally descope with rationale. [RECOMMENDATION] Do not schedule contractor cohorts until this decision is made.

### Segment 8: Help Desk (8 Vantagepoint, 10 Maconomy)
No information exists in the inputs about whether help desk roles are in scope for AI-SDLC. [GAP] Treat as out of scope until confirmed otherwise.

---

## Manager and Leader Activation Plan

Managers not engaged is a documented failure signal. [FACT — from Input 2] Manager activation is not a downstream communication — it is a prerequisite to cohort scheduling.

### What Managers Need to Know
- The four adoption tests (Context, Connected, Gated, Measured) — tool installs do not count. [FACT]
- Dinakar's standard: humans at gates, not triggers. This is a process change, not just a tool change.
- What their team's KnowledgeBase readiness looks like and what they are accountable for.
- The Phase 1 pilot findings before their team's cohort runs.

### What Managers Need to Do
- Confirm KB domain readiness for their teams before cohort scheduling.
- Protect time for their team's cohort and post-training application sprints.
- Run at least one check-in with their team after the cohort to discuss real-work application.
- Escalate setup blockers they cannot resolve locally.

### What Managers Need to Model
- Use AI-SDLC language in team conversations (Framing, Capability Spec, gates).
- Reference the velocity benchmark in sprint reviews where applicable.
- Be visible in the program — if engineering leaders skip the orientation, teams will treat the camp as optional.

### Activation Sequence

| Step | Who | When | Action |
|------|-----|------|--------|
| Executive alignment | Bret Tushaus, Dinakar | Before Phase 1 | Confirm 2027.2 expectation is actively communicated by Bret to Hardik, Melissa, Henrik, Dan |
| Engineering leader briefing | Hardik Shah, Henrik Rosenstand | Before Phase 1 pilot | Dedicated session on adoption tests, manager role, KnowledgeBase accountabilities |
| PM leader briefing | Melissa Coffey, Dan DiStefato | Before Phase 1 pilot | PDM expectations, Framing/Capability Spec requirement, cohort scheduling |
| Henrik and Dan stance confirmation | Henrik Rosenstand, Dan DiStefato | Before Phase 3 gate | Must confirm active sponsorship before Maconomy cohorts are scheduled |
| Pre-cohort manager briefing | All team managers | 1 week before each cohort | Team KnowledgeBase status, time protection, post-training check-in expectation |
| Post-cohort manager follow-up | All team managers | 2 weeks after each cohort | Did team apply? What blocked them? Escalation path? |

### Maconomy-Specific

Henrik Rosenstand's leadership stance is unconfirmed. [FACT] This is the single highest organizational risk for Phase 3. The recommendation is to engage Henrik with a leadership briefing (not a participant onboarding) in November 2026, before Maconomy content is built, to confirm his active sponsorship. If sponsorship is not confirmed, Maconomy Phase 3 should be reconsidered at the schedule level, not managed around. [RECOMMENDATION]

Anders Hessellund is a credible grassroots champion. [FACT] He should be formally acknowledged and given a role — champion peer support, office hours facilitation, or internal evangelist — with Maconomy leadership's visible endorsement. Without that endorsement, his reach is limited to the technically curious, not the mainstream. [INFERENCE]

---

## Reinforcement and Transfer Strategy

A single async pass through the camp content will not produce the behavior changes the program claims to deliver. [FACT — from Input 4] The following structures are needed after each cohort.

### Immediate Post-Training (within 1 week of cohort completion)

- **Applied sprint:** Each cohort team identifies one real story from their current backlog and runs it through Framing and Capability Spec using the AI-SDLC workflow. This is not optional — it is the "done" criterion for team-level adoption. [RECOMMENDATION]
- **Setup verification:** Confirm every cohort member has a working setup before the cohort closes. Participants who exit with broken setup will not return to it independently.

### Short-Term Reinforcement (weeks 2–6 post-cohort)

- **Peer cohort channels:** A shared channel (Teams or Slack) per cohort for questions, examples, and friction logging. A champion or facilitator monitors with SLA of same business day. [RECOMMENDATION]
- **Bi-weekly office hours:** Open Q&A sessions, 30 minutes, with a facilitator who can address both process (AI-SDLC gates) and tool (skills, KnowledgeBase, token limits). Not a lecture — bring real problems. [RECOMMENDATION]
- **Champions network:** Identify one champion per team (not just one per org). Champions are the first line of peer support. For Maconomy, Anders Hessellund is the confirmed starting point. [FACT + RECOMMENDATION]

### Sustained Reinforcement (ongoing, into 2027)

- **Sprint review integration:** Encourage teams to reference AI-SDLC gate status in sprint reviews (which gates ran, what velocity signal emerged). This normalizes the measurement expectation. [RECOMMENDATION]
- **Productivity index feedback:** Mike Scopa's EVI productivity index should produce visible output for participating teams. Teams that cannot see their own velocity signal will not believe the 4x benchmark is achievable. [FACT — benchmark exists; RECOMMENDATION — make it visible per team]
- **Cohort graduation gate:** Define what "done" looks like for a team: one feature, end-to-end, PDM through QE, with a velocity or throughput signal. Publish this gate before Phase 2 begins so teams know what they are working toward. [RECOMMENDATION]
- **January survey as baseline only:** The January adoption survey should be treated as the first data point, not the rollout trigger. By January, Phase 1 and early Phase 2 cohorts will have already run. The survey establishes pre-Phase 3 baseline for Maconomy and confirms Phase 2 stickiness for Vantagepoint. [INFERENCE]

### The 20% Team Gap

The camp assigns 20% of implementation to teams themselves. Teams with low AI maturity cannot fill this gap independently. [FACT — from Input 4] Each cohort should receive a structured "team supplement" guide covering: how to assess their own KnowledgeBase, how to identify their first real story for end-to-end application, and who to call when they are blocked. This is not optional scaffolding — it is the bridge between learning and doing. [RECOMMENDATION]

---

## Risk Register

| Risk | Early Warning | Mitigation |
|------|---------------|------------|
| Setup friction blocks cohort before content is reached | >20% of participants report setup issues in first session; facilitator time spent troubleshooting not learning | Pre-flight setup verification session (30 min) the week before each cohort; documented workarounds for known blockers; Gaurav/GK identity and scope confirmed before Phase 1 |
| Camp v2 not ready before November launch | Phase 1 pilot date set but v2 completion date not confirmed | Gate Phase 1 pilot on v2 completion; do not schedule cohorts against an unconfirmed content date |
| Maconomy leadership does not confirm sponsorship | Henrik and Dan are not present at leadership briefing; no response to Phase 3 planning communications | Escalate to Bret Tushaus before scheduling any Maconomy cohorts; do not build Maconomy content ahead of sponsorship confirmation |
| KnowledgeBase gaps block teams from meaningful application | Cohort teams report they cannot apply AI-SDLC to their domain because KB does not cover it | KB readiness assessment per domain published before Phase 2 scheduling; teams without ready KBs scheduled to later cohorts |
| QE cohort runs before automation path is decided | QE participants complete the camp but the Verifying phase is incomplete or omits their preferred tool | Defer QE-specific cohorts until tool decision is made and QE lab has a worked precedent |
| Contractor tool access never resolved | Contractors reach camp intake with no confirmed access; ad-hoc workarounds cause inequity | Force organizational decision before Phase 2: include contractors with confirmed access documentation, or formally descope with rationale |
| Shallow adoption — tool installs counted as done | Manager reports say "team is on the program" but no velocity signal exists; no end-to-end feature run documented | Publish team-level graduation gate (one feature, end-to-end) before Phase 2; train managers on four adoption tests; adoption question in January survey |
| PDM adoption lags, breaking connected adoption | Developers run skills but no upstream Framing or Capability Spec from PDMs | PDMs cohorted with developers, not separately; Melissa and Dan briefed on PDM expectation before Phase 1 |
| Async HTML completion without behavior change | 100% "completion" rates but teams cannot describe their gate ownership in retrospect | Facilitated cohorts, not solo async; pilot uses live facilitation as the test; post-cohort applied sprint required |
| Maconomy stays at 10% after November | No Phase 3 cohorts scheduled; November communications do not lead to team enrollment | Phase 3 gate is explicit (Henrik stance confirmed, content ready, KB assessed); absence of these gates surfaces the stall early |
| Philippines and India teams face timezone exclusion | Facilitator availability does not cover UTC+8 sessions; these cohorts start later than US cohorts | Phase 2 scheduling must include timezone-appropriate facilitation slots or documented async-with-office-hours model before Philippines cohorts begin |
| dvp deprecated workflow routed in participant experience | Participants follow dvp persona menu, use deprecated workflow, report confusion | Fix dvp persona menu before Phase 1 pilot — this is a known, documented defect |
| No velocity baseline before results are reported | Dinakar receives a velocity number with no agreed counting method; comparison is invalid | Lock same-team baseline, counting method, and agreed metric before first cohort completes; Mike Scopa confirms EVI scope |

---

## Timeline (High Level)

*Durations are estimates. Assumptions are noted. All dates require human confirmation against actual org calendars.*

### Phase 0 — Readiness (Now — Early November 2026) | ~3–4 weeks

**Assumed:** Camp v2 can be completed in this window. If not, Phase 1 is delayed.

| Week | Actions |
|------|---------|
| Oct 16–23 | Confirm Gaurav/GK identity and scope; initiate contractor tool access decision; publish KB readiness assessment template to domain leads |
| Oct 23–30 | Executive alignment session (Bret + Hardik, Melissa); Henrik and Dan leadership briefing scheduled; dvp persona menu fix confirmed; baseline measurement approach agreed with Lisa and Mike Scopa |
| Oct 30 — Nov 6 | Camp v2 completion confirmed; KB readiness reports due from domain leads; Phase 1 pilot team identified; pre-flight setup verification session run with pilot team |

**Gate to Phase 1:** v2 complete, pilot team identified, setup verified, baseline agreed.

---

### Phase 1 — Vantagepoint Pilot (November 2026) | ~2–3 weeks

**Assumed:** One cross-functional team (PDM, developer, QE) drawn from Vantagepoint. Live facilitation, not async. Week 1 is learning + setup; Week 2–3 is applied sprint on a real story.

| Week | Actions |
|------|---------|
| Nov 6–13 | Facilitated pilot cohort — camp content with live facilitator; setup issue log running in parallel |
| Nov 13–20 | Applied sprint: pilot team runs one real story through Framing to Verifying |
| Nov 20–27 | Pilot retrospective; content gap log produced; Phase 2 cohort schedule revised with findings; readiness report to Bret/Lisa |

**Gate to Phase 2:** Pilot team completes end-to-end. Blockers categorized. Camp updated.

---

### Phase 2 — Vantagepoint Broader Rollout (December 2026 — January 2027) | ~6 weeks

**Assumed:** 3–5 teams per cohort wave; KB-ready domains go first; QE path deferred until content decision made. Philippines and India timezone cohorts require facilitation scheduling.

**Target:** 75% of in-scope Vantagepoint teams by end 2026 (Lisa's target — this is aggressive if Phase 1 runs through November 27).

*Note: If the 75% by end-2026 target is to be met, Phase 2 must begin no later than December 1 and cohorts must run in parallel where KB readiness allows. This requires Phase 0 to hold and Phase 1 to complete on time. The timeline is tight. Human judgment required on whether to compress or adjust the target.*

| Cohort Wave | Timing | Segments |
|-------------|--------|----------|
| Wave 2a | Dec 1–12 | PDMs + developers, KB-ready domains, US/India |
| Wave 2b | Dec 8–19 | PDMs + developers, KB-ready domains, Philippines (timezone-appropriate sessions) |
| Wave 2c | Jan 5–16 | QE cohorts (if automation path decided); architects; UX (if scaffolding added) |

**Gate to Phase 3:** Vantagepoint pilot findings incorporated into camp; Maconomy-specific content added; Henrik and Dan sponsorship confirmed; Maconomy KB readiness assessed.

---

### Phase 3 — Maconomy Onboarding (January — March 2027) | ~6–8 weeks

**Assumed:** Maconomy-specific content ready, Henrik and Dan confirmed, Anders Hessellund in champion role.

| Wave | Timing | Segments |
|------|--------|----------|
| Mac Wave 1 | Jan 19 — Feb 6 | Pilot cohort: 1 PDM, 1 developer, 1 QE from Copenhagen or Philippines |
| Mac Wave 2 | Feb 9 — Mar 6 | Broader Maconomy rollout by domain and KB readiness |
| Mac Wave 3 | Mar 9 — Mar 27 | Remaining teams; QE if path resolved; architects |

**Target:** 100% of in-scope teams by end of 1H 2027.

---

## Open Questions for Human Decision

These questions cannot be resolved from available inputs and require organizational authority or information not present in the inputs provided.

1. **Contractor tool access (85 Vantagepoint):** Are contractors in scope for AI-SDLC adoption? If yes, what is the path to confirmed tool access and who owns it? If no, document the rationale. Decision owner: [unknown — likely Hardik Shah + procurement/IT].

2. **Gaurav/GK identity and scope:** Who is responsible for plugin distribution and admin rights? What is their capacity and timeline for resolving Phase 0 blockers? Decision owner: [unconfirmed].

3. **Henrik Rosenstand and Dan DiStefato's stance:** Will they actively sponsor Phase 3? What do they need to confirm their commitment? Who should facilitate this conversation and when? Decision owner: Bret Tushaus.

4. **QE automation trigger and preferred TC tool:** Who decides this, and by what date? Without this decision, QE/Automation cohorts cannot be scheduled. Decision owner: [unknown — likely Hardik Shah + QE lead].

5. **75% by end-2026 target — is it binding?** Given that Phase 1 pilot runs through late November and Phase 2 requires KB readiness assessment per team, 75% of Vantagepoint teams by December 31 is achievable only under favorable assumptions. Is this target a hard commitment or a directional goal? Decision owner: Lisa Rabideau / Bret Tushaus.

6. **Baseline measurement and counting method:** Who confirms the same-team baseline and counting method before the first cohort completes? This must be decided before Phase 1 pilot — not after January survey results arrive. Decision owner: Lisa Rabideau, Mike Scopa.

7. **Camp v2 completion date:** When will v2 be complete? Who confirms it is ready before the Phase 1 pilot is scheduled? Decision owner: Ian / program owner.

8. **Facilitation model for Philippines and India:** Will cohorts have live facilitation or an async-with-office-hours model? If async, what is the office hours schedule and who staffs it? Decision owner: Ian / program owner + Hardik Shah.

9. **Help desk in scope?** Are the 8 Vantagepoint and 10 Maconomy help desk roles expected to go through AI-SDLC camp? Decision owner: Hardik Shah, Henrik Rosenstand.

10. **Champions role formal or informal?** Should champions (Anders for Maconomy, identified champions per team for Vantagepoint) have a formal role with time allocation, or is this expected to be on top of existing responsibilities? Decision owner: Bret Tushaus / respective engineering leads.

---

## Labeling Key

- **FACT:** Sourced from program assessment, org context, success definition, or initial critique inputs as provided.
- **INFERENCE:** Reasoned from inputs; logical but not explicitly stated. Requires human validation.
- **RECOMMENDATION:** Judgment call based on inputs; requires human review and approval before implementation.
- **GAP:** Information required to make a decision that is absent from all inputs provided.

---

*All recommendations in this document require human review before implementation. This document is an analytical input to human decision-making, not an authorization to proceed.*
