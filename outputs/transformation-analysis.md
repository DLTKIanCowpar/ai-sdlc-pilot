# Workflow Transformation Analysis

## Summary

The AI-SDLC Camp introduces meaningful workflow changes across five of six SDLC stages, with the largest transformations concentrated in Framing (PDM-led), Building (Developer-led), and Verifying (QE/Automation-led). The shift from individual skill acquisition to team-level coordination is the program's most structurally demanding requirement: a PDM who has completed the camp but is paired with an uncertified developer cannot run the new workflow. Three structural conditions must accompany the training to make behaviors stick: reliable tooling setup (particularly token management), resolved ambiguities in Stage 5, and explicit cross-role coordination rituals that async self-paced learning cannot install on its own. Maconomy faces a steeper adoption curve than Vantagepoint given its 10% AI maturity baseline and placeholder skill content.

---

## Current vs. Future State by SDLC Phase

| Phase | Current State | Future State (with AI) | Delta |
|-------|---------------|------------------------|-------|
| **Proposed** | PDM creates feature in Aha manually; team decides to frame it | Identical — no AI skills defined for this stage | None |
| **Framing** | PDM writes a brief alone, likely in a doc or Aha directly; UX may or may not be in the loop at this point | PDM runs `/frame` in Claude Desktop in a live session; AI reads Aha feature and generates a structured frame; PDM reviews and corrects each section; writes back to Aha Acceptance Criteria; UX is present; gate requires PDM and designer agreement | Significant transformation — from solo async writing to facilitated live session with structured output and a formal gate |
| **Exploring** | PDM writes requirements or specs using existing templates; developer estimates independently; QE may not see use cases until later | PDM runs `/capability-spec` iteratively through five session modes; spec drives UX mockups, developer's feature dev plan, and QE use-case review; spec becomes the ADO input | Significant transformation — from loosely connected artifacts to a single spec as the stage's canonical output with a formal gate |
| **Building** | Developer writes code, creates PR, does code review via standard team norms; no defined AI-assisted workflow | Developer runs sequential slash commands (`/tech-plan`, `/server-code`, `/client-code`, `/api-test`, `/code-review`, `/pr-create`) with eight-agent code review; proposes and confirms every change before write-back | Significant transformation — from conventional dev workflow to AI-augmented command sequence with new confirmation discipline |
| **Verifying** | QE writes test cases manually from requirements; automation scripted by hand or with ad hoc tooling; bug logging via team norms | QE runs `/test-case-creator` from spec use cases; Automation runs `/playwright` across four phases; QE signs off before release | Significant transformation — but incomplete: no worked example, automation trigger timing unresolved, preferred TC tool not confirmed |
| **Released** | Scrum master marks items done; release notes written manually or not at all; outcome tracking informal | Scrum master marks Done; PDM follows up against frame's success indicators; release notes skill not yet built; outcome measurement remains manual | Small adjustment — new PDM accountability for outcome follow-through is the primary behavioral addition |

---

## Role-by-Role Impact

### Product/Design Manager (PDM)

**Workflow change:** PDM moves from solo brief-writing to facilitating two live AI-assisted sessions (Framing and Exploring). The PDM's decision authority is preserved but now exercised through a structured review loop rather than open-ended drafting. PDM also gains a new post-release accountability: following up on outcomes against the frame's success indicators.

**New habits required:**
- Running `/frame` and `/capability-spec` in Claude Desktop as the primary means of producing framing and spec artifacts (FACT)
- Reviewing and correcting AI-generated content section by section rather than writing from scratch (FACT)
- Treating the capability spec as the authoritative input to Building — not email, not verbal handoff (INFERENCE)
- Closing the loop on outcome measurement post-release (FACT)

**Habits to unlearn:**
- Writing briefs solo and asynchronously without structured AI scaffolding (INFERENCE)
- Moving from Framing to Exploring without a formal gate requiring designer agreement (INFERENCE)
- Treating the feature spec as a living document that teams interpret independently (INFERENCE)

**Disruption level: High** — PDM role has the most changed workflow across the most stages. Framing and Exploring are both significant shifts, and the Released stage adds new accountability. (INFERENCE based on camp content scope)

---

### Developer (Software Engineer)

**Workflow change:** The Building stage is entirely restructured around sequential slash commands in Claude Code. The developer shifts from writing code with conventional tooling to proposing, reviewing, and confirming AI-generated technical plans and code via a defined command sequence.

**New habits required:**
- Running `/tech-plan`, `/server-code`, `/client-code`, `/api-test`, `/code-review`, `/pr-create` as the standard Building workflow (FACT)
- Confirming before every write-back — no changes committed without explicit review (FACT)
- Reading and acting on the capability spec as the primary input to planning (FACT)
- "Ground before you state" discipline: referencing KnowledgeBase and ADO wiki rather than coding from memory (FACT)

**Habits to unlearn:**
- Writing code directly without an AI-mediated review loop (INFERENCE)
- Estimating and planning from informal reading of requirements rather than the structured spec (INFERENCE)
- Relying on domain memory rather than grounding against authoritative sources (FACT — explicitly named as a difficult habit for experienced engineers)

**Disruption level: High** — Building is the developer's primary stage and it is fully restructured. The eight-agent code review and confirmation discipline represent a meaningful shift in daily working pattern. (INFERENCE)

**Gap:** The camp does not describe what the developer's workflow looks like when they have Claude Code access but their KnowledgeBase for their domain is incomplete. This is a known tooling gap. (FACT)

---

### Quality Engineer (QE)

**Workflow change:** QE moves from manual test case authoring to running `/test-case-creator` from the spec's use cases. Bug logging and RCA processes appear largely unchanged. QE's sign-off gate before release is preserved.

**New habits required:**
- Using `/test-case-creator` driven by the capability spec's use cases rather than writing cases from scratch (FACT)
- Reviewing the capability spec use cases at the end of Exploring as a QE-specific input step (FACT)

**Habits to unlearn:**
- Writing test cases independently of the spec, potentially from informal sources (INFERENCE)

**Disruption level: Medium** — Test case creation is changed; bug management and release sign-off are largely unchanged. However, the unresolved preferred TC tool question and absence of a worked Stage 5 example mean QE's new workflow is not fully defined. (FACT — gap explicitly noted)

**Gap:** The automation trigger (when Playwright scripting begins) is unresolved. QE cannot fully adopt the new workflow until this is decided. (FACT)

---

### Automation Engineer

**Workflow change:** Automation moves from hand-scripted test automation to a four-phase `/playwright` command sequence (Plan, Resolve, Script, Review and Debug).

**New habits required:**
- Running `/playwright` across all four phases as the standard automation scripting approach (FACT)
- Coordinating with QE on the handoff trigger point (ASSUMPTION — no process currently defined for this)

**Habits to unlearn:**
- Writing Playwright scripts directly without the structured four-phase sequence (INFERENCE)

**Disruption level: Medium-High** — The automation workflow is substantially restructured, but the incomplete Stage 5 content and unresolved trigger timing mean the full scope of change cannot be assessed. (FACT — gap explicitly noted)

**Gap:** No worked example exists for Stage 5. The automation engineer's new workflow is the least defined of any role in the camp. (FACT)

---

### UX / Designer

**Workflow change:** UX participates in the Framing live session (observer/collaborator role) and produces Level 1 mockups from the capability spec in Exploring. Their AI tooling (dvp plugin) is distinct from Engineering tooling.

**New habits required:**
- Being present in the Framing session, not receiving the brief after the fact (INFERENCE — current state assumed to be async)
- Producing mockups from the structured spec rather than from informal PDM briefs (INFERENCE)
- Gate: Designer must agree the frame is correct before Exploring begins — this requires a decision, not just presence (FACT)

**Habits to unlearn:**
- Starting design work from informal or incomplete requirements (INFERENCE)
- Operating independently of the Framing session (INFERENCE)

**Disruption level: Medium** — UX's tooling and primary workflow are less directly restructured than PDM or Developer, but the shift to spec-driven design and live session participation represent behavioral changes. (INFERENCE)

**Gap:** The camp does not specify whether UX uses AI tools during the Exploring stage to produce mockups, or whether mockup production remains manual. (FACT — gap)

---

### Scrum Master / Team Owner

**Workflow change:** Scrum Master's role is primarily operational: monitoring the Ready for Dev queue and tracking PR approvals in Building. In Released, they mark work Done. The nine-column ADO board is the primary management surface.

**New habits required:**
- Managing the Ready for Dev queue as a formal gate, not an informal handoff (INFERENCE)
- Recognizing PR approval as a stage gate in Building (FACT)
- Understanding the Feature → Capability Spec → PBI model well enough to support team flow (FACT)

**Habits to unlearn:**
- Treating ADO board management as administrative rather than as a workflow control mechanism (INFERENCE)

**Disruption level: Low** — The Scrum Master's workflow is the least changed of any named role. Their responsibility is operational continuity, not AI-augmented work product creation. (INFERENCE)

**Gap:** The camp does not specify whether Scrum Masters receive their own training module or whether their preparation is covered within the team-level content. (FACT — gap)

---

## Friction Hotspots

### 1. Setup as a Dropout Trigger (Pre-Camp)
Expired ADO personal access tokens are the most common single failure mode. (FACT) Plugin installation is manual and not automated. (FACT) KnowledgeBase content gaps mean some developers may complete setup but still be unable to ground their answers. (FACT) This friction occurs before any learning begins and is likely to disproportionately affect lower-AI-maturity participants (Maconomy at 10%, Philippines and India teams). (INFERENCE)

### 2. "Propose, Confirm, Write-Back" Discipline in Building
The confirmation loop in Building is structurally slower than conventional coding for individual tasks. (FACT) Experienced engineers who have built strong intuition about their codebase are the most likely to skip confirmation steps when under sprint pressure. (FACT — explicitly flagged as a difficult habit for experienced engineers) This is the most likely point of behavioral regression after training. (INFERENCE)

### 3. "Ground Before You State" in All AI-Assisted Stages
Stopping to retrieve grounding evidence (from KnowledgeBase, ADO wiki, or live code) rather than answering from memory is a high-discipline habit. (FACT) It requires practitioners to acknowledge uncertainty in front of peers and stakeholders — a social cost that increases in higher-stakes or time-pressured contexts. (INFERENCE) This friction applies across all roles but is highest for developers and architects who have the most domain expertise and therefore the strongest memory-based defaults. (INFERENCE)

### 4. Stage 5 Incompleteness (QE and Automation)
No worked example exists for Verifying. (FACT) The automation trigger is unresolved. (FACT) The preferred test case management tool is not confirmed. (FACT) QE and Automation engineers will exit the camp knowing the theory of their new workflow but unable to execute it reliably. This is the largest content gap in the program. (INFERENCE)

### 5. Cross-Role Coordination Not Installed by Async Training
The camp's success metric requires four roles to run a feature through all stages together. (FACT) Async self-paced training teaches individuals, not teams. (FACT) The live Framing session and stage gates create natural coordination points, but no cross-role scheduling mechanism, shared team calendar, or joint practice session is described in the camp content. (INFERENCE based on camp content absence) Teams that complete modules individually without synchronizing will be unable to run the workflow. (FACT)

### 6. dvp Persona Menu Routing to Deprecated Workflow
The dvp persona menu routes to a deprecated workflow. (FACT) This is a live UI risk that is hardest to mitigate for low-AI-fluency participants who are least likely to recognize the error. (FACT) This particularly affects Maconomy, where many skills are placeholders and the framework was built for Vantagepoint. (FACT)

### 7. Maconomy-Specific Structural Friction
Maconomy operates at 10% AI maturity with skills that are placeholders. (FACT) The framework was built for Vantagepoint and is being adapted. (FACT) Copenhagen and Philippines teams operate across two time zones, creating coordination challenges for the live Framing sessions. (FACT) Anders Hessellund is the sole named grassroots champion — single-point dependency for cultural momentum. (INFERENCE)

---

## Enabling Conditions

### 1. Centralized, Automated Token Management
ADO PAT expiry is the top dropout risk. A managed token renewal process — either automated or with a clear escalation path — would eliminate the most common pre-training failure. (INFERENCE) This is a structural fix, not a training fix.

### 2. Team Cohort Enrollment (Not Individual Enrollment)
Individual async completion cannot install cross-role coordination. Enrolling teams as a unit — with a shared cohort schedule, joint kickoff, and a defined window in which all four roles complete the camp — would allow live Framing sessions to be practiced together rather than described abstractly. (INFERENCE) This is the structural intervention most likely to translate individual learning into team behavior.

### 3. A Designated "First Feature" for Practice
Teams need a real but low-risk feature to run through all six stages using the new workflow immediately after training. Without a designated practice feature, the new behaviors will decay before they are reinforced by real work. (INFERENCE) The feature should be chosen before camp begins, not after.

### 4. Stage 5 Content Completion Before November Rollout
QE and Automation cannot adopt a workflow that is not defined. Resolving the automation trigger, confirming the preferred TC tool, and providing a worked Stage 5 example are prerequisites for those roles to participate meaningfully. (FACT — these are stated gaps; enabling condition is resolving them)

### 5. Manager Visibility into Workflow Adherence
If sprint pressure incentivizes skipping the confirmation loop or using memory rather than grounded sources, individual discipline will erode. Engineering leads and Scrum Masters need a lightweight mechanism to observe whether the new workflow is being followed — not to police it, but to surface early drift and address it in retros. (INFERENCE)

### 6. Maconomy Framework Completion Before Rollout
Placeholder skills that fail silently are worse than no skills. Maconomy participants who encounter broken or deprecated tooling in their first week will not return. Completing skill content for Maconomy's actual workflows before their November rollout is a hard dependency. (FACT — gaps are confirmed; enabling condition is resolving them)

### 7. Explicit Gate Ownership Assigned to Roles
The camp defines stage gates (frame agreed, spec finalized, PR approved, QE signed off) but does not specify how teams enforce them in practice. Assigning explicit gate ownership — naming who blocks and who unblocks — reduces ambiguity under sprint pressure. (INFERENCE)

---

## Observable Transformation Indicators

### Leading Indicators (early signals, before outcomes are measurable)

- **Tooling setup completion rate by role:** Are all four role types completing setup checks, including token validation, before entering the camp? Setup completion is a proxy for camp readiness. (INFERENCE)
- **Live Framing sessions scheduled (not just completed modules):** Individual module completion ≠ team coordination. Framing sessions booked as calendar events indicate teams are attempting the workflow together. (INFERENCE)
- **PDM using capability spec as the ADO artifact:** If the spec appears in ADO Acceptance Criteria and Description fields (not just in Notion), PDMs are completing the Exploring workflow. (FACT — this is the defined write-back target)
- **Developer running `/code-review` before PR submission:** Eight-agent review is a new step. Presence of AI-assisted code review output in PRs is a leading indicator that the Building workflow is being followed. (INFERENCE)
- **Stage gates blocking (not rubber-stamped):** If gates (frame agreed, spec finalized, PR approved) are visibly holding work — meaning features are not advancing without gate confirmation — the gating discipline is functioning. (INFERENCE)

### Lagging Indicators (outcome signals, requiring time to accumulate)

- **Features with all four roles completing the same camp cohort:** The defined success metric. (FACT)
- **Reduction in late-stage requirement changes:** If the spec is the canonical input to Building and Verifying, spec-driven development should reduce mid-sprint scope changes originating from ambiguous requirements. (INFERENCE)
- **QE test case coverage sourced from spec use cases:** Test cases that can be traced to capability spec use cases indicate the Verifying workflow is being followed. (INFERENCE)
- **PDM completing post-release outcome follow-through:** If PDMs are tracking Released features against the frame's success indicators, the Released stage accountability is functioning. (INFERENCE)
- **Maconomy workflow adoption parity:** Given the gap between Vantagepoint (50% AI maturity) and Maconomy (10%), measuring Maconomy adoption separately provides a leading signal on whether the framework transfer is working before the 27.2 cycle target. (INFERENCE)

---

## Labeling Key

- **FACT:** Sourced directly from camp content, program assessment, or critique inputs
- **INFERENCE:** Reasoned from the available inputs; stated as reasoned conclusions, not guesses
- **ASSUMPTION:** Plausible but not grounded in available data — used sparingly and flagged explicitly

---

## Noted Gaps (no data available to assess)

- Contractor roles (85 in Vantagepoint): AI maturity, tool access, and camp eligibility are unconfirmed. Transformation analysis for this group cannot be completed without this information.
- Architect role: Camp content does not describe specific workflows or slash commands for the 19 Vantagepoint and 25 Maconomy architects. Their transformation impact is unassessed.
- Scrum Master training path: Not specified whether Scrum Masters have their own camp module or receive joint team-level content.
- UX AI tool use in Exploring: Whether mockup production involves AI tooling or remains manual is not specified.
- Stage 5 (Verifying): Insufficient content to assess the full transformation scope for QE and Automation.
- Outcome measurement mechanism: "Read the Outcome Measurement dispositions" is named but not described. The mechanism for post-release tracking is unclear.
