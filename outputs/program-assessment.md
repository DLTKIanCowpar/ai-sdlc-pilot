# Program Assessment

## Summary

The Vantagepoint AI-SDLC Camp v1 is a substantive, role-differentiated training program covering a real operational workflow with genuine tooling behind it — most engineering and QE skills are live as of the camp's publication date. Its biggest strength is fidelity: the curriculum teaches an actual implemented system, grounded in a real end-to-end example (Rate Table), not a conceptual framework. Its biggest risk is rollout readiness: the program has never been piloted with learners, carries approximately 20 unbuilt items it acknowledges explicitly, depends on infrastructure prerequisites (KnowledgeBases, connector tokens, admin rights for plugin installation) that are not yet in place for all teams, and was written to completion without the author having read the final version — all of which means that v1 should be treated as a near-complete draft requiring one structured review cycle before wide rollout, not a release candidate. The November target for Maconomy adoption is particularly at risk given that org's 10% AI maturity and the fact that most Maconomy-specific skills are placeholders.

---

## Content Fit

**Coverage of AI SDLC stages.** FACT: The camp addresses all six stages of the defined lifecycle — Proposed, Framing, Exploring, Building, Verifying, Released — with step-by-step procedures for each. Coverage depth is uneven by design: Building and Verifying are the most technically complete (live in repo since 16 Sep, full slash-command inventory, four testing layers, eight-agent code review), while Proposed and Released are explicitly manual with no AI skills in use.

**Learning objectives.** INFERENCE: No formal, enumerated learning objectives list exists in the camp. The context summary notes this explicitly ("inferred — no formal list exists"). Objectives can be reconstructed from the module structure and role playbooks, but the camp does not open with a measurable outcomes statement learners or facilitators can use to assess completion.

**Concrete, measurable outcomes.** INFERENCE: The lab exercises in Module 5 (one per role) are the closest the camp comes to measurable outcomes — each ends with a concrete artifact to produce (a framed feature, a tested PBI, a Playwright test). These are workable as completion proxies. The knowledge checks (2–6 questions per module) test recall, not applied skill.

**Difficulty calibration.** INFERENCE: The camp assumes learners can navigate Claude Desktop or Claude Code, connect four external systems (Aha, ADO/TFS, Notion, M365), interpret JSON, and understand terms like filterHash, DescriptionHtml, xUnit, and FluentAssertions. For the engineering audience these are reasonable assumptions. For PDMs and UX designers, the technical density of Modules 2 and 3 (especially the field-level technical facts and sync rules) may exceed what is needed for their role. The role filter addresses this partially — learners see only their relevant content — but the shared modules (0, 1, 3, 4) are written at a consistent level that skews technical.

**Accuracy concerns.** FACT: The camp itself discloses that the plugin repository snapshot used during development carried an older skill body that wrote capability specs to the first PBI instead of the ADO Feature. Working-team feedback (Saurendu) identified 14 additional spots where the document is behind the current repo. FACT: The camp was flagged by its poster (Bret Tushaus) with the note "I have not read this myself yet" at publication. INFERENCE: The combination of unconfirmed content accuracy and no learner pilot means that content errors will surface during rollout rather than before it.

**Module 4 (Rate Table) as an anchor.** FACT: Module 4 provides a complete, real end-to-end example through Building, with actual artifact excerpts for Stages 1–4. Stages 5 and 6 (Verifying and Released) are explicitly noted as incomplete in the record. INFERENCE: This is the camp's strongest content asset and the clearest evidence the process has been run, though the example is incomplete at the stages QE and Automation participants care most about.

---

## Audience Alignment

**Stated audience.** FACT: The camp targets six roles: PDM, Developer, QE, Automation, UX, Scrum Master/Team Owner. Seniority level is not stated. Prior AI experience is not stated.

**Role differentiation.** FACT: The camp implements a role filter ("I am" selector) that hides content irrelevant to the selected role. Module 2 is scoped to 45 minutes for your role or 90 minutes for all stages. Module 5 provides one printed quick-card per role with a first-week plan and a lab. INFERENCE: The role differentiation is well-designed for self-paced learning but has not been tested to confirm that the filtering is accurate and complete.

**Vantagepoint-only framing.** FACT: The camp is explicitly scoped to Vantagepoint. Most Maconomy-specific skills are described in the context summary as placeholders. The camp never mentions Maconomy. INFERENCE: Maconomy engineers, QEs and PDMs attempting to use this camp will encounter Vantagepoint-specific tool paths, connector endpoints, repo locations, and example artifacts that do not apply to their environment. The gap between Maconomy's stated AI maturity (10%) and the Vantagepoint-first content is a material audience mismatch for a November rollout targeting both orgs.

**Offshore and contractor audiences.** FACT (from context): 75 of Vantagepoint's ~218 engineers are in the Philippines, 22 in India. 85 are contractors whose tool access is unconfirmed. The camp does not acknowledge geographic distribution, time zones, or contractor access constraints. UNKNOWN: Whether offshore team members have confirmed access to Claude Desktop, Claude Code, or the Vantagepoint repo's .claude/ folder. UNKNOWN: Whether contractors will be in-scope for this rollout.

**Scrum Master/Team Owner role.** INFERENCE: The Scrum Master card (Module 5) is the thinnest of the six role cards — it focuses on board column visibility and flow, with limited guidance on how to coach developers and QEs through their first features. Given that Team Owners are described as "near-mandatory" in spec authoring, the program likely under-prepares this role for its actual influence function.

**UX.** FACT: The UX role card explicitly warns against using the generic UX persona or "add ui requirements" invocations. INFERENCE: UX participants have the least scaffolded path — Level 2 mockups are not built, the placement of synthetic personas is an open item owned by Dawn and Alex, and UX's own skill is still being defined. This role may exit the camp with less actionable capability than the others.

---

## Delivery Readiness

**Format.** FACT: The camp is async, self-paced HTML with browser-only completion tracking. One companion video exists for Module 2 only (4m47s). A live kickoff is referenced as planned but unscheduled. A hybrid video approach is proposed but not built.

**Facilitation requirements.** INFERENCE: The camp requires no live facilitator for basic completion, but the lab exercises (Module 5) assume access to live tooling, a real 2027.2 feature, and presumably some team support for the first run. No facilitation guide, cohort structure, or rollout ceremony is described in the camp itself.

**Infrastructure prerequisites.** FACT: The following must be in place before a learner can complete the camp's hands-on components:
- dvp plugin installed with admin rights (admin rights pending as of 21 Sep)
- All four connectors authorized with valid personal access tokens (ADO tokens expire; this is the most common failure)
- SharePoint access to the ProductResearch site
- Claude Code with the Vantagepoint repo pulled and .claude/ folder resolved
- ADO MCP tools resolving in the Claude Code session
- KnowledgeBase present for the engineering domain (described as the formal prerequisite for wider engineering rollout)
- Token/gateway access (token guidance noted as a rollout prerequisite)

INFERENCE: A learner who hits setup friction on Day 1 and has no support path will disengage. The camp's support path (Agentic AI Teams channel, Saurendu as connector owner) is real but not integrated into the camp flow as a guided rescue.

**Completion tracking.** FACT: Completion is stored in the browser only — it does not persist across devices and is not visible to facilitators or managers. INFERENCE: This makes it impossible to report on program completion centrally, which is a meaningful gap for a rollout with a stated November target and a leadership expectation that 100% of in-scope teams adopt the process in the 2027.2 cycle.

**Version currency.** FACT: The camp acknowledges approximately 20 "Not built yet" items in Module 6 and notes that content goes out of date quickly as tools change. The readiness table at the bottom of Module 0 is dated 21 Sep 2026 and may already be stale given that Saurendu identified 14 documentation gaps. FACT: v2 is needed before rollout readiness is confirmed per the status note.

---

## Adoption Risk Factors

**Setup friction as a dropout point.** INFERENCE: The highest-risk moment in the learner journey is the setup sequence in Module 0 and Module 1. Expired ADO tokens, manual plugin upload requiring admin rights, SharePoint access issues, and KnowledgeBase availability all have the potential to block a learner before they reach the first skill. If setup fails with no immediate support, the learner stops and may not return.

**The 80/20 framing creates ambiguity.** FACT: The camp explicitly states it delivers "about 80 percent of what you need; your team supplies the rest." INFERENCE: For teams without a strong Team Owner or without an adjacent experienced practitioner, the 20% is undefined. This is an intentional design choice, but it means that isolated teams — particularly offshore or lower-maturity ones — may not know what they are missing.

**Behavior change that requires reinforcement.** INFERENCE: Several operating principles taught in the camp represent significant behavioral shifts that will not stick after a single self-paced pass: "Ground before you state" (no claims without a source), "Propose, confirm, write-back" (slower per write, requires patience), and "Never fabricate" (discipline to stop rather than guess). These principles exist because their alternatives failed in the POC — which means the failure mode is real and likely to recur without reinforcement.

**QE and Automation may wait for stable tooling.** FACT: The camp explicitly states the automation trigger (when to start Playwright automation) is still being decided between Dev and QE. FACT: QE agents still run in Copilot, and the preferred tool for several overlapping TC-generation scenarios (test-case-creator, qe-tc-generation, qe-bug-tc-generation) is described as "QE-lead guidance" — meaning the right answer is not in the camp. INFERENCE: QE and Automation participants may finish the camp uncertain about basic workflow decisions, which increases the chance of local improvisation that diverges from the intended process.

**Content that will feel irrelevant by role.** INFERENCE: The Proposed stage (Stage 1) contains no AI skills and is identical to current practice; developers, QE, and Automation may experience it as overhead. The Released stage (Stage 6) is largely manual; for anyone not a PDM or Scrum Master, it is a brief read. Module 3 (work items) is marked "essential for Scrum Masters and Team Owners" but is required for everyone — the depth of sync rules and field-level technical facts may feel excessive to PDMs focused on Framing and Exploring. FACT: The persona menu in the dvp plugin is explicitly labeled as describing an older, generic workflow that learners should not follow — an active friction point for anyone who does not read this warning carefully.

**The Rate Table example is incomplete.** FACT: Module 4 explicitly states that Stages 5 and 6 (Verifying and Released) are not yet part of the record. INFERENCE: QE and Automation participants — who work primarily in Stage 5 — do not have a complete real-world example to anchor their learning. This is the gap most likely to be felt in the lab.

---

## Gaps and Unknowns

1. UNKNOWN: What is the actual completion time for each role, including setup? The estimated times (M0: 10 min, M1: 20 min, etc.) appear to exclude setup friction and may exclude the lab duration entirely.

2. UNKNOWN: Will contractors (85 of ~218 Vantagepoint engineers) be in-scope for this rollout, and do they have confirmed access to all required tooling?

3. UNKNOWN: What is the plan for Maconomy-specific content? The camp is Vantagepoint-only, and most Maconomy skills are placeholders. No Maconomy-adapted version of the camp is described.

4. UNKNOWN: How will rollout completion be tracked? Browser-only completion tracking cannot support any form of centralized reporting or manager visibility.

5. UNKNOWN: What is the facilitation model for the lab? The lab exercises assume access to live tooling and a real feature — is any structured support (office hours, a cohort kickoff, a pairing model) planned?

6. UNKNOWN: What is the v2 scope and timeline? The context notes that v2 needs review before rollout readiness is confirmed, but does not specify what changes are required or who will make them.

7. UNKNOWN: Whether offshore participants (Philippines, India) face any tooling, access, or network constraints that would block them from completing the camp.

8. UNKNOWN: The 2027.2 adoption expectation has not been stated by Bret. The camp teaches the process but cannot tell learners what their actual adoption commitment is.

9. UNKNOWN: Technical framing guidance (for technical features, spikes, platform work) is described as in-progress (Hardik and Jessica) with guidance due before feature reviews close. This gap affects Developer and QE participants who work on non-functional features.

10. UNKNOWN: Whether QE and Automation participants who complete the camp will receive clarity on the automation trigger and preferred TC-generation tool selection in time for the 2027.2 cycle.

11. UNKNOWN: Whether the KnowledgeBase readiness state per domain is documented anywhere a learner can check before they begin their first feature.

12. FACT stated, implication UNKNOWN: The developer agent's exact step list is described as "to be confirmed here after the first team runs" — meaning the camp's representation of the agent may not match its actual behavior.

---

## Labeling Key

- FACT: directly stated in program materials (camp content or context summary)
- INFERENCE: reasoned from program materials without direct statement
- UNKNOWN: not answerable from available inputs
