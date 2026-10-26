# AI SDLC Camp — Program Overview

Source: Vantagepoint AI-SDLC Camp v1 (interactive HTML, PS Product Management Leadership
SharePoint, AI SDLC › Enablement). Supplemented by AI-SDLC check-in meeting chat (Bret
Tushaus and working team). Researched via Copilot, October 2026.

---

## Program Name and Description

**Name:** Vantagepoint AI-SDLC Camp (v1, published 21 September 2026)
Also referenced as: "AI-SDLC enablement camp," "AI DLC camp"

**Description:** The camp describes itself as training for "one operating system for
Product, UX, Engineering and QE. Humans make the decisions, AI does the labor."
Goal: get each participant "to the point where you can run your part of it on a real feature."

**Scope:** Vantagepoint only. Delivers "about 80 percent of what you need"; each scrum team
supplies the remaining 20 percent.

**Org placement:** Vantagepoint Product and Technology · Enablement

---

## Learning Objectives

No formal list of objectives exists in the program. Inferred from module descriptions:

- Explain why the AI-SDLC replaces today's practice, and name its six stages:
  Proposed, Framing, Exploring, Building, Verifying, Released
- Set up through the correct "door": Claude Desktop (dvp plugin) for Product and UX,
  or Claude Code in the Vantagepoint repo for Engineering
- Apply nine operating principles, including "Propose, confirm, write-back,"
  "Never fabricate," "Ground before you state," and "Humans hold the gates"
- Run role-specific stage procedures (what to say to the AI tool, what you decide,
  what gates end each stage)
- Track work items across Aha, Notion, Azure DevOps, and the repo
- Complete a lab running one real 2027.2 feature through your role's procedures

---

## Target Audience

**Roles (via "I am" filter):** PDM, Developer, QE, Automation, UX, Scrum Master / Team Owner.
Each role has its own playbook card.

**Seniority:** Not stated.

**Prior AI experience assumed:** Not stated explicitly. Learners must have access to Aha,
Azure DevOps, Notion, and SharePoint. Engineering requires a Vantagepoint repo checkout.
Whether any prior AI experience is expected is unconfirmed.

---

## Session Structure and Time Commitment

Self-paced; no scheduled sessions. Completion tracked in learner's browser only.

| Module | Title | Time |
|--------|-------|------|
| 0 | Start here | 10 min |
| 1 | Why, what and how | 20 min |
| 2 | The lifecycle, step by step | 45 min (your role) / 90 min (all six stages) |
| 3 | Work items through the lifecycle | 20 min |
| 4 | Rate Table, end to end (worked example) | 30 min |
| 5 | Role playbooks and labs | 20 min + lab |
| 6 | Reference | No time given (reference only) |

**Total (estimated):** ~2 hr 25 min following your own role; ~3 hr 10 min covering all stages.
Lab duration unstated — requires running a real 2027.2 feature, likely multi-sitting.

---

## Delivery Format

- **Current:** Async, self-paced interactive HTML. Bret's 21 Sep message: each person goes
  through it on their own.
- **Video:** One companion video exists for Module 2 only (4 min 47 sec). Team has discussed
  adding video walkthroughs; Bret proposed a hybrid approach (video + content to read).
  Concern raised about ongoing video maintenance cost as tooling changes.
- **Live kickoff:** Supported in 16 Oct meeting recap; date unconfirmed.
- **Cohort format:** No evidence found.

---

## Curriculum Outline

**M0 — Start here:** Readiness table by stage and role; "your first hour" checklist per door.

**M1 — Why, what and how:** What changes from today's practice; six stages and their artifact
chain; two doors; nine operating principles; setup; which features are a good fit.

**M2 — The lifecycle, step by step:** Stage-by-stage procedures. Includes 16-section capability
spec, spec-session modes a–e, technical plans, tests and PRs, QE test cases, Playwright
automation, root-cause analysis, and release certification.

**M3 — Work items:** Systems of record; 9-column board; Feature → spec → PBI model;
sync rules; statuses; who moves what.

**M4 — Rate Table example:** First feature run end-to-end with real artifacts and lessons learned.

**M5 — Role playbooks and labs:** Printable card per role; first-week plan; lab.

**M6 — Reference:** Skill catalog; glossary; "Not built yet" register; support and ownership contacts.

---

## Prerequisites and Pre-work

**Product and UX:** Install dvp plugin in Claude Desktop; connect Aha, Azure DevOps, Notion,
and Microsoft 365; run a "check connectors" test.

**Engineering:** Pull latest Vantagepoint repo; confirm Azure DevOps tools work; check whether
your domain has a KnowledgeBase.

**Account access:** Learners must already have access to each connected system.

**Formal prerequisites:** None stated beyond the above setup steps.

---

## Who Developed It and When

**Author:** Bret Tushaus (executive sponsor) posted v1 on 21 Sep 2026.
His note at posting: "I have not read this myself yet" — suggests AI-generated content
(unconfirmed).

**Sources cited in camp footer:** AI-SDLC process documents, skills registry, dvp plugin
repository at v0.8.0.

**Named owners:**
- Engineering direction and enablement camp: Hardik Shah
- Skills: Saurendu Chakraborty
- Plugin: Jessica Abiles
- Process map: Dawn Gajewski
- Product direction: Janna Courter and Melissa Coffey

**Ownership status:** Open. Jessica flagged: "We probably need to assign an owner that is not you."

---

## Pilot Results and Feedback

**No learner pilot conducted.** All feedback is from the internal working team reviewing content.

**Working team feedback:**
- Saurendu: Found 14 spots where the doc is behind the current repo
- Jessica: Reviewed engineering roles; flow makes sense, content not too verbose
- Melissa: Flagged gaps on technical features, spikes, manual status updates, release notes ownership
- Janna: Raised QE automation impact and inconsistent "Feature Dev Plan vs. Tech-Plan" terminology
  (resolved in 12 Oct check-in)
- Ian (26 Sep): Suggested splitting video by step for easier maintenance

Feedback consolidated in Notion and a Gap Register document (not accessible to researcher).
Dawn deferred her review to v2.

**Current status (15 Oct check-in):** Version 1. Version 2 still needs review before
rollout readiness is confirmed.

---

## Known Constraints on Delivery

- **Content currency:** Tools change faster than the camp. Readiness table dated 21 Sep;
  approximately 20 "Not built yet" or open items in M6 (e.g., feature dev plan skill,
  relationship to corporate AI-DLC).
- **Video maintenance:** Bret has concerns about maintaining video walkthroughs as tooling evolves.
- **Setup friction:** Expired Azure DevOps tokens; plugin install requires manual upload
  (admin rights pending); SharePoint access issue raised 16 Oct.
- **Token and budget limits:** Gateway budgets and token limits have blocked testing.
  Token guidance is listed as a rollout prerequisite.
- **KnowledgeBase readiness:** Varies by domain — formal prerequisite for wider engineering rollout.
- **Undecided rollout terms:** 2027.2 adoption expectation "to be stated by Bret." Kickoff date
  and attendance expectations for feature teams are still open.

---

## Gaps in Available Information

- Notion feedback pages and Gap Register document not accessible
- AI-DLC Process Overview not accessed
- No data on seniority targeting, learner pilot, or cohort model
- Ian's own UX Enablement ownership proposal exists but was excluded as a source
  (it is Ian's proposal, not a description of the camp)
