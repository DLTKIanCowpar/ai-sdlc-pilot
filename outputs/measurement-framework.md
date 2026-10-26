# Adoption Measurement Framework
## Vantagepoint AI-SDLC Camp Rollout

---

## Framework Overview

This framework applies the Kirkpatrick model to measure whether the Vantagepoint AI-SDLC Camp is reaching the right people, changing behavior, and producing outcomes. Adoption is defined by four tests (Context, Connected, Gated, Measured) — not tool installs or session attendance. All claims are labeled FACT, INFERENCE, or RECOMMENDATION.

---

## Kirkpatrick Level Metrics

### Level 1 — Reaction

> Did participants find it relevant and valuable?

| Metric | Method | Timing | Owner | Meaningful Signal |
|---|---|---|---|---|
| Session relevance rating | 3-question pulse survey (1–5 scale) sent via Teams immediately post-cohort | Within 24 hrs of cohort completion | Dawn Gajewski | ≥ 4.0 average across roles; PDMs and QEs scoring < 3.5 triggers content review [RECOMMENDATION] |
| Setup completion rate by role | Count of participants who complete tooling setup (Claude Desktop + KnowledgeBase + role kit) before or during Day 1 | End of Day 1, per cohort | Saurendu (Teams channel owner) | ≥ 85% completion before learning begins; < 70% = setup is a dropout risk [INFERENCE] |
| Dropout point tracking | Log at which phase each incomplete participant stalled (setup, Framing, Capability Spec, Verifying) | End of cohort | Dawn Gajewski | Any single dropout cluster > 20% at the same phase = structural friction, not individual resistance [RECOMMENDATION] |
| Notion feedback log issues | Count and category of issues logged to Notion during camp | During and 48 hrs post-cohort | Dawn Gajewski | Recurring issue in same category across ≥ 3 participants = escalate to content fix before next cohort [RECOMMENDATION] |

---

### Level 2 — Learning

> Did participants acquire intended knowledge and skills?

| Metric | Method | Timing | Owner | Meaningful Signal |
|---|---|---|---|---|
| Applied sprint completion | Did each team run one real story from Framing to Verifying within 7 days of cohort? (Binary: yes/no per team) | 7 days post-cohort | Program Manager | ≥ 80% of cohort teams complete the applied sprint; < 60% = learning is not transferring to practice [RECOMMENDATION] |
| Capability Spec quality check | Manual review of 3–5 Capability Specs per cohort wave: does each spec include use cases traceable to ADO Acceptance Criteria? | Within 14 days post-cohort | PDM lead or program manager | ≥ 80% of reviewed specs meet the traceability standard [RECOMMENDATION]; dependency on ADO field usage [FACT] |
| Role-specific task demonstration | During applied sprint, each role completes their gate task (PDM: Framing write-back to Aha; Dev: `/code-review` before PR; QE: test case linked to spec) | Within 7 days post-cohort | Team lead per role | All three role gates demonstrated in ≥ 75% of teams [RECOMMENDATION] |
| KnowledgeBase domain coverage | Verify KnowledgeBase contains at least one source for each domain the pilot team works in | Before Phase 1 pilot and before each new team cohort | Program Manager + PDM | Zero gaps in domain coverage before cohort begins; any gap = prerequisite blocker, not a learning failure [INFERENCE] |

---

### Level 3 — Behavior

> Are participants applying what they learned on the job?

| Metric | Method | Timing | Owner | Meaningful Signal |
|---|---|---|---|---|
| Gate hold rate | Count features that advanced to next ADO column only after gate confirmation (observable in ADO board) | Weekly, per active team | Program Manager | ≥ 90% of feature transitions show gate confirmation; < 75% = gates are not holding under sprint pressure [RECOMMENDATION]; dependency on ADO column discipline [FACT] |
| PDM Aha write-back rate | Proportion of new features where Framing output is written back to Aha Acceptance Criteria field | Biweekly, per active PDM | PDM lead | ≥ 80% of new features post-cohort show write-back within one sprint of Framing [RECOMMENDATION] |
| Developer `/code-review` usage | PR review logs or team self-report: proportion of PRs where `/code-review` ran before submission | Per sprint, per team | Engineering lead | ≥ 70% of PRs show pre-submission review; dependency on PR log access or self-report honor system [FACT] |
| Manager 2-week check-in completion | Did the manager conduct the post-cohort check-in at 2 weeks? (Binary per team) | 14 days post-cohort | Program Manager | 100% completion; zero check-ins = managers are not engaged, which is an explicit failure signal [FACT from inputs] |
| Behavior regression signal | At 60 days: repeat gate hold rate and write-back rate measurement; compare to 30-day reading | 60 days post-cohort | Program Manager | Decline of > 15 percentage points from 30-day reading = sprint pressure is eroding behavior [RECOMMENDATION] |
| Cross-role team completion | Count of teams where PDM + developer + QE all completed the same camp cohort AND ran applied sprint together | Per cohort wave | Program Manager | Definition of "done" for adoption unit [FACT from inputs]; < 75% cross-role completion = adoption counting method must be revisited |

---

### Level 4 — Results

> Is behavior change producing measurable outcomes?

| Metric | Method | Timing | Owner | Meaningful Signal |
|---|---|---|---|---|
| Velocity signal (story points) | Compare story points delivered per sprint by cohort team vs. same team's pre-cohort baseline (same-team baseline required) | 60 and 90 days post-cohort | Mike Scopa + Team lead | Directional improvement vs. baseline on same team; 4x is the benchmark [FACT: ProPricer result]; no velocity number at 90 days = failure signal [FACT from inputs] |
| EVI Productivity Index movement | Read Mike Scopa's 10-signal EVI index; note whether pilot teams show upward movement from 3.08 baseline | Quarterly (next reading after 90 days) | Mike Scopa | Upward movement attributable to pilot cohorts; attribution requires pre/post isolation [RECOMMENDATION] |
| Feature cycle time (idea to GA) | Measure elapsed days from feature creation in Aha to GA for features run through AI-SDLC vs. comparable prior features | 90 days post-cohort, then quarterly | Program Manager + Engineering lead | Target: 25% shorter cycle time; dependency on Aha and ADO timestamps [FACT from inputs] |
| Late-stage requirement change rate | Count requirement changes logged after Capability Spec sign-off vs. same team's prior baseline | Per release cycle | PDM lead | Reduction from pre-cohort baseline; no agreed baseline = result is unmeasurable [RECOMMENDATION] |
| QE test case traceability rate | Proportion of QE test cases that link back to a Capability Spec use case | Per release cycle | QE lead | ≥ 80% traceability; Stage 5 content gap means this metric cannot be finalized until QE/Automation content is resolved [FACT from inputs] |
| Team-level adoption rate (rollout) | Count of in-scope Vantagepoint teams that have completed the adoption unit (PDM + dev + QE, one feature end-to-end) | Monthly | Program Manager | Target: 75% of in-scope teams by end 2026 [FACT from inputs] |

---

## Leading Indicators (by Rollout Phase)

Leading indicators are observable before outcome metrics can be read. At least two per phase.

### Phase 0 — Baseline (now–November)

1. **Baseline locked:** Same-team velocity baseline agreed and documented with Mike Scopa and Lisa before first cohort runs. Binary: yes/no. [RECOMMENDATION — this is a prerequisite, not a metric]
2. **KnowledgeBase domain coverage confirmed:** All domains covered for Phase 1 pilot team before camp begins. [RECOMMENDATION]
3. **Counting method agreed:** Definition of adoption unit (PDM + dev + QE, one feature end-to-end) documented and signed off. Binary: yes/no. [FACT: non-negotiable from inputs]

### Phase 1 — Pilot (November, one cross-functional team)

1. **Setup completion rate:** ≥ 85% of pilot participants complete tooling setup on Day 1 — predicts whether learning can begin. [INFERENCE]
2. **Applied sprint scheduled:** Team books the applied sprint session as a calendar event within 48 hrs of cohort end — calendar booking predicts follow-through better than intent. [INFERENCE]
3. **Gate events on ADO board:** At least one gate hold event visible in ADO board within 2 weeks of cohort — earliest observable behavior signal. [RECOMMENDATION]

### Phase 2 — Vantagepoint Rollout (December–January, 3–5 teams per wave)

1. **Manager check-in completion rate:** ≥ 90% of managers complete 2-week post-cohort check-in — predicts sustained behavior vs. regression. [INFERENCE]
2. **Cross-role cohort completion rate:** ≥ 75% of enrolled teams have all three roles (PDM, dev, QE) completing same cohort — predicts team-level adoption unit success. [RECOMMENDATION]
3. **PDM Aha write-back within first sprint:** PDM writes Framing output to Aha within one sprint of camp — earliest detectable PDM behavior change. [RECOMMENDATION]

### Phase 3 — Maconomy Rollout (January–March)

1. **Vantagepoint gate hold rate at ≥ 85%:** Confirms gates are holding before Maconomy rollout begins — prevents false attribution of results. [RECOMMENDATION]
2. **Maconomy setup completion rate by role:** Same metric as Phase 1, applied to Maconomy cohorts — Maconomy measured separately per inputs [FACT].

---

## Baseline Requirements

The following must be collected before the first cohort runs (Phase 0). Without these, no Level 4 result can be attributed to training. [FACT: inputs explicitly flag same-team baseline and counting method as non-negotiables]

| Baseline Data Point | Source | Collection Method | Responsible | Deadline |
|---|---|---|---|---|
| Story points delivered per sprint, by pilot team | ADO sprint history | Export last 3 sprints pre-cohort | Mike Scopa + Team lead | Before Phase 1 (November) |
| Feature cycle time (idea to GA), last 3–5 features | Aha + ADO timestamps | Manual pull from Aha and ADO | Program Manager | Before Phase 1 |
| Late-stage requirement change frequency | ADO change log or team estimate | Retrospective count from last 2 releases | PDM lead | Before Phase 1 |
| EVI Productivity Index current reading | Mike Scopa's index | Direct from Mike | Mike Scopa | Before Phase 1; current value: 3.08 [FACT] |
| Gate compliance rate (current, pre-camp) | ADO board column history | Manual ADO audit for pilot team's last release | Program Manager | Before Phase 1 |
| Adoption unit definition, documented and agreed | Internal agreement | Written document, signed by Lisa and Mike | Program Manager | Before Phase 1; non-negotiable [FACT] |

**Comparison method:** Use same-team pre/post comparison as primary isolation method. Cohort waves enrolling different teams in different months create a natural stagger — compare 90-day results from Wave 1 teams to Wave 2 teams at the same elapsed time, controlling for team size and feature complexity where possible. [RECOMMENDATION] Do not attribute velocity gains to training if a parallel organizational change (restructure, new tooling unrelated to AI-SDLC, release pressure) occurred in the same window — log confounders monthly. [RECOMMENDATION]

---

## 90-Day Measurement Calendar

| Milestone | What to Measure | Owner | Action if Signal is Weak |
|---|---|---|---|
| **30 days** | Setup completion rate; applied sprint completion rate; gate hold rate (first reading); manager check-in completion; PDM Aha write-back rate (first reading) | Program Manager | If setup < 70%: triage friction before next cohort. If applied sprint < 60%: investigate whether teams have capacity or support for application. If manager check-in < 80%: escalate to leadership — managers not engaged is an explicit failure signal. |
| **60 days** | Gate hold rate (second reading vs. 30-day); behavior regression check (compare write-back and `/code-review` rates to 30-day); developer PR review rate; first velocity signal vs. baseline | Program Manager + Mike Scopa | If gate hold rate dropped > 15 pp from 30-day: sprint pressure causing regression — convene manager check-in loop, not more training. If no velocity signal: confirm baseline was properly established; if baseline is solid and signal is absent, escalate. |
| **90 days** | All Level 3 metrics; velocity comparison (pilot team vs. baseline); feature cycle time comparison; team-level adoption rate (rollout count); QE traceability rate (if Stage 5 content resolved); January survey result (first read post-Phase 2) | Program Manager + Mike Scopa + PDM lead | If velocity signal absent: this is a failure signal per inputs — escalate, do not rationalize. If adoption rate < 50% of target: review cohort wave pacing. If QE traceability still unmeasurable: confirm Stage 5 content status and set a resolution date. |

---

## Failure Signals and Escalation Thresholds

The following are explicit failure signals drawn from the inputs [FACT] plus additional thresholds derived from analysis [INFERENCE/RECOMMENDATION].

| Failure Signal | Threshold | Escalation Action |
|---|---|---|
| No velocity number at 90 days | Absent entirely | Escalate to Lisa and Mike Scopa; halt expansion to new cohorts until signal is established [FACT from inputs] |
| People operating as triggers between gates | Any instance observed in gate audit | Flag to team lead and manager; repeat observation = structural issue, not individual — review gate design [FACT from inputs] |
| Counting tool installs or session attendance as adoption | Any reporting using these as primary metrics | Reject and replace with adoption unit definition; re-educate stakeholders on counting method [FACT from inputs] |
| Managers not conducting 2-week check-in | < 80% completion at 30 days | Escalate to program sponsor; manager engagement is a prerequisite for sustained behavior [INFERENCE] |
| Setup blocking non-developers | > 20% dropout at setup step among non-dev roles | Pause next cohort; fix setup path for PDMs and QEs before enrolling more [RECOMMENDATION] |
| Maconomy adoption near 10% | Maconomy-specific reading at 90 days | Treat Maconomy as separate rollout; do not blend with Vantagepoint results [FACT from inputs] |
| Gate hold rate < 75% at 30 days | First reading < 75% | Gates are not holding — convene facilitated retrospective with team leads within 1 week [RECOMMENDATION] |
| Cross-role cohort completion < 60% | Per cohort wave | Individual completion without cross-role coordination does not count as adoption; review scheduling and enrollment approach [INFERENCE] |
| January survey AI-SDLC adoption question returns no usable baseline | Survey result ambiguous or question not included | Treat as missing baseline — cannot use survey as rollout trigger; fall back to applied sprint completion as leading indicator [RECOMMENDATION] |

---

## Monthly Health Check (< 1 hour)

This checklist is designed to run without a data team. All inputs come from ADO, Aha, Notion, and direct team contact. Run on the first Monday of each month.

**Estimated time: 45–55 minutes**

---

**Step 1 — Setup and Completion Sweep (10 min)**
- Open the cohort log (Notion or spreadsheet): for each team that completed a cohort in the prior month, confirm whether all three roles (PDM, dev, QE) attended the same cohort. Mark complete/incomplete.
- Check whether each team's applied sprint is logged as complete (should be in Notion or a shared tracker). Count complete vs. incomplete.
- Record: (a) cross-role completion rate, (b) applied sprint completion rate.

**Step 2 — Manager Check-In Confirmation (5 min)**
- For each cohort completed in the prior month, confirm the manager check-in at 2 weeks was conducted. Email or Teams message to each manager is sufficient. Log yes/no per team.
- Flag any team where check-in did not happen.

**Step 3 — Gate Hold Audit (10 min)**
- Open ADO feature board for each active team. For features that advanced to a new column this month, spot-check 3–5 transitions: was there a gate confirmation documented before the move?
- Record gate hold rate (gates confirmed / total transitions checked). Note any features that jumped columns without visible gate event.

**Step 4 — Behavior Indicators (10 min)**
- PDM write-back rate: for each PDM in active teams, open Aha — do new features from this month show Framing output written to Acceptance Criteria? Count yes/no for 3–5 features per PDM.
- Developer review rate: ask engineering lead (Teams message or standing meeting): what proportion of PRs this sprint had `/code-review` run before submission? Log the number or estimate.

**Step 5 — Velocity / Outcome Read (10 min)**
- For teams ≥ 60 days post-cohort: pull sprint velocity (story points delivered) for current month. Compare to baseline documented in Phase 0.
- For teams < 60 days post-cohort: skip; record "too early."
- Log: velocity vs. baseline, direction (up/flat/down), any confounders noted by team lead.

**Step 6 — Signal Summary and Escalation Decision (5 min)**
Complete the monthly signal table:

| Indicator | This Month | Last Month | Trend | Escalate? |
|---|---|---|---|---|
| Cross-role completion rate | | | | |
| Applied sprint completion | | | | |
| Manager check-in rate | | | | |
| Gate hold rate | | | | |
| PDM write-back rate | | | | |
| Velocity vs. baseline | | | | |

Apply escalation thresholds from the Failure Signals section. If any indicator triggers an escalation threshold, note the action and owner before closing the check.

**Step 7 — Log and File (5 min)**
- Save the completed table to the shared program tracker (Notion or equivalent).
- Send a one-paragraph summary to Lisa and the program sponsor with: one green signal, one watch item, one action (if any).

---

## Labeling Key

| Label | Meaning |
|---|---|
| **FACT** | Directly stated in the program inputs; no interpretation added |
| **INFERENCE** | Derived from inputs using reasonable logic; may not hold in all conditions |
| **RECOMMENDATION** | A judgment call by this framework; should be confirmed with program lead before treating as a standard |

---

*Framework version: October 2026. Owner: Program Manager. Next review: After Phase 1 pilot (November 2026).*
