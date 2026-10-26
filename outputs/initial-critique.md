# Critical Review — Initial Program Assessment

## Overall Assessment

The camp is technically thorough but organizationally naive. It teaches a process designed by and for Vantagepoint's most capable practitioners, then plans to drop it on a 145-person organization (Maconomy) with 10% AI maturity that had no hand in designing it. The most important issue is not any single content gap: it is that the program's behavior-change ambition is completely out of proportion to its delivery mechanism — async HTML, one video, and a lab nobody has piloted.

---

## Finding Summary

| # | Category | Severity | Finding |
|---|----------|----------|---------|
| 1 | Assumption Audit | High | Camp assumes participants can get the tooling working before learning matters; setup prerequisites are broken or pending for a significant share of the target audience |
| 2 | Assumption Audit | High | Camp assumes Maconomy will adopt a process it didn't design, with placeholders for its own skills and unknown leadership stance |
| 3 | Assumption Audit | High | Camp assumes prior AI fluency; seniority and experience baselines are completely unstated |
| 4 | Content Gap | High | No calibration of what "80 percent" leaves out; the 20 percent is assigned to teams without a scaffold for what that means |
| 5 | Content Gap | High | Stage 6 (Released) and outcome measurement are almost entirely manual stubs — the success benchmark (4x velocity) has no measurement path built |
| 6 | Content Gap | Med | Maconomy is mentioned exactly zero times in the camp content; it is being handed a Vantagepoint-labeled product |
| 7 | Content Gap | Med | The "humans make the decisions" principle is asserted but never taught; no cognitive framework for what a "good decision" looks like at each gate |
| 8 | Content Gap | Med | Contractor access (85 of 218 engineers) is unresolved; the camp says nothing about this |
| 9 | Adoption Risk | High | Monday-morning blockers — expired ADO tokens, admin rights pending for plugin install, token/gateway limits — are acknowledged in Module 0 setup steps but not solved |
| 10 | Adoption Risk | High | The program's own author had not read it at publication ("I have not read this myself yet"); no learner pilot means the labs are untested procedures |
| 11 | Adoption Risk | Med | KnowledgeBase readiness varies by domain and is described as "the formal prerequisite for the wider engineering rollout" — but the rollout is November and KnowledgeBases are team-built with no stated completion timeline |
| 12 | Adoption Risk | Med | The camp's success signal is Dinakar Hituvalli's "no humans as triggers between gates" standard, but the camp teaches a heavily human-gated process with no path from current state to that standard |
| 13 | Structural Weakness | High | Async self-paced HTML with one video and browser-stored completion is not a delivery format that produces behavior change; it produces checkbox completion |
| 14 | Structural Weakness | High | Labs are specified but entirely untested; the Rate Table example (the only worked example) stops before Verifying and Released, meaning the QE and Automation labs have no grounded precedent |
| 15 | Structural Weakness | Med | Cohort design is absent; no peer accountability, no facilitated practice, no structured debrief mechanism beyond "log it in the feedback log" |
| 16 | Structural Weakness | Med | The persona menu in the /dvp plugin actively misleads users into a deprecated workflow; this is a live landmine, not a footnote |
| 17 | Content Gap | Low | Token discipline is stated as a principle but never operationalized in the camp; participants have no framework for choosing scan levels or recognizing when they are burning tokens wastefully |

---

## Detailed Findings

### Finding 1 — Broken setup prerequisites (High)

**What it is.** Module 0's "Your first hour" section lists four connectors to authorize, a plugin to install (requiring admin rights "pending"), and ADO tokens known to expire. Module 6's "Not built yet" table notes that "Plugin distribution: GitHub-synced marketplace versus manual upload — manual upload in use; admin rights pending." The camp cites Saurendu Chakraborty as the single point of contact for connector failures.

**Why it matters.** Participants cannot learn a process they cannot access. If the first action in the camp — "confirm the dvp plugin shows as installed and On" — fails, they stop. The camp's response is "ask in the Agentic AI Teams channel." That is not a setup path; it is a support queue. In a November rollout to ~232 Vantagepoint staff plus an unknown share of 85 contractors, a single SME on a Teams channel is not a sustainable support model.

**What a fix would look like.** A verified setup runbook with tested fallback paths, a resolved admin-rights situation before rollout, and a setup validation step that must pass before camp content unlocks.

---

### Finding 2 — Maconomy is invisible (High)

**What it is.** The camp is Vantagepoint-labeled throughout: Aha VP2 workspace, tfs.deltek.com/tfs/Deltek/Vantagepoint, the dvp plugin, KnowledgeBases for Vantagepoint domains. The word "Maconomy" does not appear anywhere in the camp content. The program overview notes "Many Maconomy-specific skills are placeholders" and that Maconomy's AI maturity is 10% versus Vantagepoint's 50%.

**Why it matters.** Maconomy engineers and PMs will open this camp and immediately hit tool references, repo paths, Aha workspace names, and skill names that are not their environment. The camp's own admission that it "delivers about 80 percent of what you need" implicitly promises 80% applicability; for Maconomy it may be closer to 40%. Adopting a framework you didn't design, with 10% AI maturity and placeholder tooling, produces learned helplessness, not adoption.

**What a fix would look like.** Either a Maconomy-specific variant of the camp (minimum: different setup section, different connector instructions, explicit acknowledgment of which skills do not yet exist for their stack), or an explicit prerequisite that Maconomy rollout does not begin until skills are ready — not November.

---

### Finding 3 — No baseline for participant readiness (High)

**What it is.** The camp states no required prior AI experience, no required Claude proficiency, no required familiarity with agentic tools. The target audience includes roles as different as Scrum Masters and Automation Engineers. The January survey is described as a "baseline" — meaning the camp launches before any baseline exists.

**Why it matters.** A developer who has never had a multi-turn conversation with an AI coding assistant and a developer who uses Claude Code daily will have completely different experiences of Module 4's technical plan walkthrough. The camp treats them identically. The lab instruction "run /tech-plan on one small PBI with a finished spec" assumes fluency with the tool, with ADO, and with a finished spec existing — none of which are guaranteed.

**What a fix would look like.** A pre-camp readiness check and a remediation path for participants who do not yet have basic Claude fluency. At minimum, state the assumed baseline explicitly so managers can identify who needs prerequisite support.

---

### Finding 4 — The 20 percent gap has no scaffold (High)

**What it is.** Module 0 states: "This camp is built to deliver about 80 percent of what you need to start using the AI-SDLC on a real feature. The last 20 percent comes from your own team: the product area, the technical stack you touch, and the habits your scrum team settles on in the first few features."

**Why it matters.** "Your own team supplies the last 20 percent" is not a delivery plan. Teams have no framework for what that 20 percent is, no facilitation guide for the conversations that would produce it, and no timeline for when it needs to be settled. At 10% AI maturity (Maconomy), that 20 percent is likely to be 50 percent. The camp delegates the hardest, most team-specific adaptation work to the people least equipped to do it.

**What a fix would look like.** A structured team kickoff guide — a one-page facilitation template for the "how do we adapt this to our context" conversation — with three to five concrete decisions every team needs to make before their first feature.

---

### Finding 5 — Stage 6 and outcome measurement are hollow (High)

**What it is.** Stage 6 (Released) is described in Module 2 as: "The scrum master marks work complete. The frame's outcomes become the yardstick." The release notes skill is "not built." Outcome measurement is "read the Outcome Measurement dispositions" — a fully manual step. The success benchmark from the program overview is ~4x velocity, and Dinakar Hituvalli's standard is no humans as triggers between gates.

**Why it matters.** The program cannot demonstrate its own value. There is no instrumented measurement of velocity, throughput, or cycle time. The January survey is planned as a "baseline" — meaning the first data point arrives after rollout has already launched. Without measurement, the January survey will produce self-reported adoption, not outcome data. The 4x benchmark (from ProPricer, a different product) is being applied with no baseline and no measurement mechanism.

**What a fix would look like.** Define three to five measurable leading indicators that can be captured from existing tooling (ADO cycle time, PR turnaround, spec-to-In Dev time) before November rollout, so the January survey measures change against a pre-camp baseline, not against memory.

---

### Finding 6 — "Humans make the decisions" is asserted, not taught (Med)

**What it is.** The operating principle "Humans make the decisions, AI does the labor" appears in Module 0 and Module 1. Every gate description says "you decide." But the camp contains no instruction on what constitutes a good decision at each gate, what bad AI output looks like, or how to recognize when a skill has confidently produced something wrong.

**Why it matters.** For participants with low AI maturity, "you confirm" is meaningless if they cannot evaluate what they are confirming. The Rate Table example is instructive: the first draft of Current Behavior "understated how strong the existing workaround was" and had to be corrected by a PDM who already knew the system. New practitioners — especially in Maconomy — will not have that catch capability. The confirm gate becomes rubber-stamping.

**What a fix would look like.** For each major artifact (Frame, Capability Spec, Technical Plan), add a "red flags to check before you confirm" sidebar with two to three specific failure modes that practitioners at any skill level can recognize.

---

### Finding 7 — Contractor access is unresolved and undiscussed (Med)

**What it is.** The program overview states 85 of 218 Vantagepoint engineers are contractors with "unconfirmed tool access." The camp content says nothing about contractors. Module 1's "Getting set up" section provides no contingency for participants without Claude Desktop, without plugin install rights, or without Copilot access.

**Why it matters.** If 39% of engineering cannot access the tools, the process does not actually run at team level. A feature requiring server code, client code, tests, and a PR involves multiple engineers. If any of them cannot run the skills, the chain breaks.

**What a fix would look like.** An explicit access matrix stating which roles require which tool licenses, which skills degrade gracefully without full access, and who resolves access issues and by when.

---

### Finding 8 — Monday-morning blockers are acknowledged, not solved (High)

**What it is.** The camp acknowledges: expired ADO tokens (Module 1: "Expired personal access tokens are the common failure"); admin rights pending for plugin install (Module 6 "Not built yet"); token/gateway limits blocked testing (program overview); KnowledgeBase readiness varies (Module 1: "Check your domain's status with your team owner before you rely on grounded answers").

**Why it matters.** These are the exact conditions that will cause participants to open the camp, attempt the lab, hit a wall, and stop. The camp's response in each case is to route to a Teams channel or a named individual. When 232 people hit these walls simultaneously in November, those channels and individuals become the bottleneck.

**What a fix would look like.** A go/no-go checklist that must be signed off by team owners before camp access opens, covering: plugin installed, connectors live, ADO tokens active, KnowledgeBase status known, token limits cleared. Camp access does not open until the checklist passes.

---

### Finding 9 — The author had not read the camp at publication (High)

**What it is.** Bret Tushaus posted v1 on 21 September with the note "I have not read this myself yet." The program overview flags this as a signal that the content may be AI-generated. No learner pilot has been conducted. All feedback is from the internal working team.

**Why it matters.** An untested training program is a hypothesis. The labs — which are the primary behavior-change mechanism — are untested procedures. The Rate Table example (the only worked example) stops at Stage 4; QE and Automation lab content is entirely unvalidated. The camp teaches a process that has run exactly once end-to-end, on one small feature, by the people who designed it.

**What a fix would look like.** A structured pilot with three to five volunteers from outside the working team — ideally including one Maconomy participant — before November rollout. The pilot's purpose is to identify where the camp fails, not to validate that it works.

---

### Finding 10 — KnowledgeBase readiness blocks engineering rollout (Med)

**What it is.** Module 1 states: "Domain KnowledgeBases are the formal prerequisite for the wider engineering rollout. Team owners and dev leads, not the platform team, build their own domain with Saurendu's interactive domain and subdomain skill." KnowledgeBase readiness varies by domain; the camp does not state which domains are ready.

**Why it matters.** The rollout timeline is November. KnowledgeBases are team-built, require domain expert time, and have no stated completion deadline in the camp. If domains are not ready in November, engineering participants run the skills "from live source" with "reduced grounding" — which produces lower quality output and erodes confidence in the process. Teams whose KnowledgeBases are not ready will not see the benefit the camp promises.

**What a fix would look like.** A published KnowledgeBase readiness map by domain and team, with a deadline for pre-rollout completion. Teams whose domains are not ready by that deadline are explicitly scheduled for a later rollout cohort.

---

### Finding 11 — The gap between the process and Dinakar's standard is invisible (Med)

**What it is.** The program overview states Dinakar Hituvalli "will not accept humans as triggers between gates." The camp teaches a heavily human-gated process: the PDM confirms every write, the team decides carve-up, humans approve PRs, the scrum master marks Done. These are not defects — they are the design. But the gap between the current process and Dinakar's automation standard is never addressed.

**Why it matters.** Participants completing this camp will believe they are building toward the success benchmark. They are not. The camp teaches a first-generation process with heavy human gatekeeping; the ultimate goal is a process where humans set policy and AI executes. No roadmap connects the two. Without that roadmap, early adopters may over-invest in the current process and resist the next-generation one.

**What a fix would look like.** A one-page "where this is going" section that distinguishes phase-1 (current: humans in every gate) from phase-2 (target: humans set guardrails, AI executes), so participants understand which gates exist because of current AI capability limits, not permanent design intent.

---

### Finding 12 — Async delivery cannot produce behavior change at this depth (High)

**What it is.** Delivery is async self-paced HTML. Module completion is stored only in the browser. There is one companion video (4m47s, M2 only). The live kickoff is unscheduled. Knowledge checks are multiple-choice. The lab output (e.g., "bring the Update Summary to your team's retro") has no verification mechanism.

**Why it matters.** The camp is trying to install a new operating system across four roles. This requires repeated practice, feedback loops, and social accountability. Async HTML with browser-stored completion is the right format for reference material. It is the wrong format for "run one feature end to end and change your team's default behavior." The knowledge checks test recall, not capability. A participant who completes all six modules and all six knowledge checks may still be unable to run a framing session or review a technical plan.

**What a fix would look like.** Mandatory cohort sessions at the role level — not all-hands, role-specific — where participants attempt the lab with a facilitator present and debrief what failed. Async is the pre-read; the session is the actual learning.

---

### Finding 13 — The persona menu is a live user experience failure (Med)

**What it is.** Module 1 states: "About the persona menu. The menu that appears after /dvp still describes an older, generic workflow... that is not the Vantagepoint process. Until the persona files are rewritten, invoke skills by name as shown above. The persona menu is being corrected." Module 6 lists the personas as "Retire for VP."

**Why it matters.** New practitioners — especially those with lower AI fluency — will naturally use the menu the tool presents. The menu routes them into the wrong workflow. The camp warns them not to use it, but warnings in training material do not survive contact with a product UI. This will produce incorrectly executed framing sessions and misconfigured specs before anyone notices, because the output looks plausible.

**What a fix would look like.** The persona menu should be disabled or hidden in the plugin before the November rollout, not after. "Being corrected" is not a status compatible with launching to 232 people.

---

### Finding 14 — The Rate Table example ends before the hard parts (High)

**What it is.** Module 4 presents Rate Table as the only end-to-end worked example. The timeline shows Stages 1–4 with real artifacts. Stage 5 (Verifying) and Stage 6 (Released) read: "Rate Table's QE and automation pass, and its release, run through the same skills described in Module 2 and are not yet part of this record. When they complete... the test cases, the Playwright test, any bugs and their RCAs, and the outcome follow-through will be added here."

**Why it matters.** QE and Automation participants get no worked example. Their labs — "one PBI with a finished spec: test cases from its use cases, executed against the build, one bug logged, one RCA" — have no grounded precedent in the camp. They are asked to run a four-phase Playwright skill (Plan, Resolve, Script, Review and Debug) with no example of what success looks like. The only precedent is a stub.

**What a fix would look like.** Either complete the Rate Table example through Stage 6 before launching the camp, or explicitly remove the QE and Automation labs from v1 and describe them as "coming with v2."

---

### Finding 15 — No peer accountability or cohort mechanism (Med)

**What it is.** The camp has no cohort design. Completion is individual and browser-stored. Feedback goes to a Notion log reviewed by Dawn Gajewski. The lab output is self-directed ("bring to your team's retro"). There is no mechanism for teams to share what worked, adapt the process together, or escalate blockers that require platform team action.

**Why it matters.** Adoption research consistently shows that peer visibility and team-level accountability are stronger drivers of behavior change than individual completion. A process that requires Product, UX, Engineering, and QE to coordinate differently will not be adopted by individuals in isolation. If a PDM completes the camp but their developer has not, framing produces an artifact nobody picks up. The process is only as adopted as the least-adopted role on the team.

**What a fix would look like.** A team-level adoption unit: the camp is "done" when the PDM, at least one developer, and at least one QE on the same team have run one feature end-to-end together, not when individuals complete six modules.

---

## What I Would Do Differently

**Run a structured two-week pilot with one cross-functional team before November rollout — and define "pass" in advance.**

The pilot team should include a PDM, two developers (one senior, one mid-level), one QE, and one Automation engineer — none of them from the camp's working group. Give them v1 of the camp, no hand-holding, and a real 2027.2 feature. Define in advance what "the camp worked" means: the feature reaches In PR with a complete technical plan, at least three test cases, and a closed consideration audit. Observe where they stall, which setup steps fail, and which lab instructions produce confusion.

The output of the pilot is not a success story — it is a punch list of the ten highest-friction points, ranked by how many November participants will hit them. Fix the top five before November. Defer the rest to v2.

The reason this is the single most important change: every other finding in this critique is a hypothesis. The pilot converts hypotheses into facts.

---

## What I Did Not Find

**Searched for and did not find:**

- Evidence that the "propose, confirm, write-back" principle has caused data loss or incorrect writes in practice (the camp documents one near-miss with placeholder shorthand, and it was caught and fixed).
- Evidence that the six-stage artifact chain is over-engineered for a 2-week sprint PBI — the Rate Table example (a small, well-scoped feature) did run the full chain in a reasonable time, suggesting the process is appropriately sized for MVP-grade features.
- Factual errors in the technical content (skill invocations, field names, ADO path conventions, test framework requirements) — what is described matches the specificity expected of real tooling documentation.
- Outright contradiction between the camp's operating principles and the Rate Table worked example — the example is consistent with the principles as documented.
- Evidence that the 45-minute per-role time estimate for Module 2 is wildly wrong — for experienced practitioners it may be accurate; for new practitioners it is likely a significant underestimate, but that is an assumption audit issue, not a factual error.

The camp's technical depth is genuine. The failure mode is organizational and pedagogical, not technical.
