
AI-SDLC Camp
VANTAGEPOINT · V1 · SEPT 2026
I AM

Everyone

PDM

Developer

QE

Automation

UX

Scrum Master / Team Owner
0
Start here
1
Why, what and how
2
The lifecycle, step by step
3
Work items through the lifecycle
4
Rate Table, end to end
5
Role playbooks and labs
6
Reference
Skill catalog
Glossary
Not built yet
Support and feedback
VANTAGEPOINT PRODUCT AND TECHNOLOGY · ENABLEMENT
The AI-SDLC, from idea to released feature
One operating system for Product, UX, Engineering and QE. Humans make the decisions, AI does the labor. This camp gets you to the point where you can run your part of it on a real feature, and it shows you one that already went end to end.
Six stages Proposed · Framing · Exploring · Building · Verifying · Released
Two doors Claude Desktop for Product and UX · Claude Code in the Vantagepoint repo for Engineering
Example Rate Table Status field (VP2-445)
MODULE 0
Start here
10 minutes
This camp is built to deliver about 80 percent of what you need to start using the AI-SDLC on a real feature. The last 20 percent comes from your own team: the product area, the technical stack you touch, and the habits your scrum team settles on in the first few features.
Use the I am selector at the top to filter the camp to your role. Everything that applies to everyone stays visible; blocks that belong to another role are hidden. Switch back to Everyone when you want the whole picture, which is worth doing once, because the point of this process is that Product, UX, Engineering and QE work from the same artifacts.
Each module ends with a short knowledge check and a completion box. Completion is stored only in your browser.
The six modules

MODULE 1 · 20 MIN
Why, what and how
The problem the AI-SDLC solves, the six stages, the two doors, the operating principles, and how to get set up.
MODULE 2 · 45 MIN FOR YOUR ROLE
The lifecycle, step by step
Every stage as an ordered procedure: who is in the room, what you say to Claude, what the AI does versus what you decide, what comes out, and the gates.
MODULE 3 · 20 MIN
Work items through the lifecycle
Aha, Notion, ADO and the repo: which record holds what, how they link, the board columns, who moves what, and the living-document conventions.
MODULE 4 · 30 MIN
Rate Table, end to end
The first feature that ran the whole way, with the real artifacts and what to notice in each one.
MODULE 5 · 20 MIN + LAB
Role playbooks and labs
Your first week, your prompt card, your checklist, and a hands-on lab on one 2027.2 feature.
MODULE 6 · REFERENCE
Reference
The skill catalog, the glossary, what is not built yet, and where to get help.
Readiness by stage and role as of 21 Sep 2026

This table is the honest state of the tooling on the day this camp was published. The camp teaches the process as designed and marks where a step is manual, partial, or still being wired. Owners update this table when something ships.
STAGE	PDM	UX	DEVELOPER	QE	AUTOMATION	SCRUM MASTER / TEAM OWNER
Proposed	Manual (Aha, today's practice)	·	·	·	·	·
Framing	Live framing v2.8	Live lo-fi wireframe, PDM-initiated	Reads the frame	Reads the frame	·	·
Exploring	Live capability spec v1 check plugin version	Partial in the room; Level 1 mockups in the spec	Manual feature dev plan, estimates	In the room; use cases drive TCs	·	Manual board, PBIs, estimates
Building	Answers open items	Reviews UI	Live in repo since 16 Sep: dev agent, tech plan, code, tests, review, PR	Live in repo test cases in parallel	·	Ready for Dev queue, PR approvals
Verifying	Dev demo, spec updates	·	Live in repo fix, RCA support, PR	Live in repo TCs, bugs, RCA, release-found, certification	Live in repo Playwright skill; PW agents in Copilot	Flow, bottlenecks
Released	Manual release notes, outcome follow-through	·	·	·	·	Manual marks Done
One thing to check before you rely on the spec skill
The decision of record is that the capability spec lives on the ADO Feature (Acceptance Criteria plus Description) with one automatic child PBI. The plugin repository snapshot used for this camp still carried an older skill body that wrote to the first PBI. If your spec lands on a PBI instead of the Feature, stop, do not fix it by hand, and log it in the feedback log (Module 6). The camp teaches the Feature-level model.
Your first hour

PRODUCT AND UX · CLAUDE DESKTOP
Confirm the dvp plugin shows as installed and On (Claude Desktop, profile icon, Settings, Capabilities or Plugins). Install steps came from Melissa and Saurendu in the Agentic AI Teams channel.
Connect the four connectors in Settings, Connectors: Aha (deltek1.aha.io, VP2), Azure DevOps (on-prem TFS, tfs.deltek.com/tfs/Deltek), Notion (Framing Documents teamspace), Microsoft 365 (SharePoint ProductResearch site).
Open a new chat, type check connectors. All four live means framing and capability spec are ready.
Type /dvp, then say what you are working on in plain English. You will invoke skills by name in this camp (for example let's frame VP2-1234); Module 1 explains why.
Read Module 1, then your stages in Module 2 (Framing and Exploring), then Module 4.
ENGINEERING · CLAUDE CODE IN THE VANTAGEPOINT REPO
Pull the latest Vantagepoint repo. The skills live in .claude/skills/, the developer agent in .claude/agents/, the framework rules in agentic_ai/, and the QE guides in tests/QEGuides/. Jessica's 16 September drop is announced in the GenTech AI channel.
Open the repo in Claude Code. Skills are slash commands: /tech-plan, /server-code, /client-code, /api-test, /code-review, /pr-create, /test-case-creator, /playwright.
Check whether your domain has a KnowledgeBase yet (Module 1, Getting set up). Without one the skills still run, from live source, with reduced grounding.
Prefer Claude over Copilot for token efficiency (engineering direction, 17 Sep). Copilot remains the home of the QE agents until they are ported.
Read Module 1, then your stages in Module 2 (Building and Verifying), then Module 4 from the technical plan onward.
SCRUM MASTERS AND TEAM OWNERS
Read Module 1 and Module 3 first. Your job in this process is flow: the board columns, the Ready for Dev queue, PR approvals, and marking Done.
Learn the artifact chain in Module 2 well enough to spot a feature entering In Dev without a finalized capability spec or dev plan.
Plan the feature reviews: the first draft capability spec is the input, not a slide deck.
Knowledge check
2 questions

What does this camp promise to deliver?
About 80 percent of what you need; your team supplies the rest
Everything, including every team-specific convention
Only the Product side of the process
Where does the capability spec live, per the decision of record?
In a Notion page
On the ADO Feature's Acceptance Criteria and Description fields, with one default child PBI
On the first PBI's Description field
Mark Module 0 complete
MODULE 1
Why, what and how
20 minutes · everyone
Why we are doing this

A feature's context used to live in people's heads, a Feature Review slide deck, a PBI template with fifteen sections nobody filled in, and a chain of meetings. Every handoff lost some of it. Engineering rebuilt intent from a thin user story; QE tested from the same thin story; the "why" was gone by the time code shipped.
The AI-SDLC replaces that with a small number of durable artifacts that carry the feature from idea to release, and with AI skills that do the retrieval, drafting, interrogation and write-back so people spend their time on judgment. It is a new operating system for how we build, not a set of AI tools bolted onto the old ceremonies.
"We're not just applying AI on top of the way we've always done things."
Bret Tushaus, executive sponsor, on the recurring challenge to the team
Three phrases from the charter describe the destination and are worth memorizing, because every design decision in the process traces back to one of them:
Humans make the decisions, AI does the labor. Claude retrieves, drafts, challenges, assembles and documents. The PDM, the engineer, the QE and the UX designer decide scope, resolution, approval and carve-up at every gate. Nothing is written to Aha, ADO or Notion without an explicit confirm.
Same operating system, two doors in. One repository of skills, agents, instructions and context, versioned like code. Engineers pull it into Claude Code (or Copilot) as part of the Vantagepoint repo; Product and UX install it as a Claude Desktop plugin. Same procedure, same artifacts, either door.
Standard model, divergent content. The lifecycle, the artifacts and the discipline are the same across products. What differs is the content: Vantagepoint's terminology, architecture, help content and conventions, held in a KnowledgeBase the skills read.
What changes from today's practice
AREA	TODAY	UNDER THE AI-SDLC
Framing the problem	Ad hoc, in the Aha description or in meetings	A formal 18-section Frame per Feature in Notion, produced by the framing skill and grounded in help content, ADO architecture and customer evidence
Feature Review deck	A PowerPoint authored by hand for the ceremony	Retired. The frame and the first-draft capability spec are what the room discusses
Where the spec lives	Spread across a 15-section PBI template, the parent PBI carrying the weight informally	One capability spec per Feature on the ADO Feature record. PBIs are thin slices that point at spec sections
Considerations (Screen Designer, Mobile, Cloud, Gainsight, and about 25 more)	Walked from memory by experienced PDMs; often missed	A systematic pass at spec time; every item gets a disposition recorded in an audit block
PBI carve-up	PDM decides alone, adjusted in Feature Review	The team decides during spec work; the skill creates PBIs on confirmation
Technical planning	In the developer's head, or a PBI comment	A Research Findings document and a Technical Plan per PBI, produced from the spec against the real codebase, attached to the PBI
Code, tests, review, PR	Hand-written against a thin story	Skills that load the framework rules and app context first, honor the plan's out-of-scope and regression guards, generate tests, run a multi-agent review, and raise the PR
Test cases and automation	Written after the fact from the PBI	Generated from the spec's use cases, in parallel with development; Playwright automation once code and test cases are stable
"Slide decks are the absolute worst for capturing context."
Bret Tushaus. The frame and the spec exist so context is never in a deck again.
What it is: six stages, one chain of artifacts

Each stage produces one artifact that the next stage consumes. AI involvement is heaviest in the middle four stages. Module 2 walks each stage step by step; this is the map.
RELEASE PLANNING
RELEASE EXECUTION
1
Proposed
Aha idea and Feature; ADO Feature created by sync
Outside the AI-SDLC skills. PDM prep and prioritization.
2
Framing
Frame Artifact in Notion, wireframe optional
Board: Framing
3
Exploring
Capability Spec on the ADO Feature, PBIs, feature dev plan
Board: Feature Review, then Requirements Collab
4
Building
Technical plan, code, tests, approved PR
Board: Ready for Dev, In Dev, In PR
5
Verifying
Executed test cases, automation, bugs fixed
Board: In Testing, In Bug Fixing
6
Released
Done; outcomes measured against the frame
Board: Done
THE FOUR AI FUNCTIONS
Discovery reads Aha, ADO, Notion, help content and the codebase so nothing starts from memory.
Context keeps the durable record: the frame, the spec, the KnowledgeBase, the update history.
Generator drafts the frame, the spec, the technical plan, the code, the tests, the test cases, the PR.
Verifier interrogates for gaps, runs the considerations pass, reviews code with specialist agents, checks coverage.
These are roles the skills play, not files you install.
THE ARTIFACT CHAIN
Frame (Notion): the scope contract. Problem, current behavior, proposed change, evidence, outcomes, scope in and out, related capabilities, decisions, open questions, prototype direction.
Capability Spec (ADO Feature): the implementation contract. Build-ready content in Acceptance Criteria; human reference in Description.
PBIs: shippable slices that reference spec sections. One default child PBI is created automatically.
Research Findings and Technical Plan (per PBI): what the code is today and exactly how to change it, with tests and a definition of done.
Code, tests, PR, test cases, automation, bugs: the outputs of Building and Verifying, each produced by a named skill.
Two doors, one operating system

DOOR 1 · CLAUDE DESKTOP · PRODUCT AND UX
The dvp plugin
One installable plugin, Deltek Vantagepoint AI (dvp). Type /dvp to start. It bundles the Framing and Capability Spec skills, the lookups they delegate to (Aha, Azure DevOps, Notion Frame Home, Vantagepoint Help), the Outcome Grid Builder, the Mockup skill, and a connector check. It ships no product data; grounding comes from the connectors and the KnowledgeBase.
How to invoke work. Say the skill's job in plain English: let's frame VP2-1234 start capability spec for VP2-1234 update the spec based on this transcript. The router sends a named task straight to the right skill.
About the persona menu. The menu that appears after /dvp (PM, UX, Developer, QA, Auto Tester, Repo-Native) still describes an older, generic workflow (context brief, spec to Notion, code to GitHub) that is not the Vantagepoint process. Until the persona files are rewritten, invoke skills by name as shown above. The persona menu is being corrected.
DOOR 2 · CLAUDE CODE (COPILOT FOR QE AGENTS) · ENGINEERING
Skills that live with the code
The Vantagepoint repo carries the engineering skills in .claude/skills/, the developer agent in .claude/agents/, and the framework knowledge every skill loads first in agentic_ai/ (framework overviews, coding rules, review rubrics, app context files, build and PR guides). QE guides and certification templates live in tests/QEGuides/.
How to invoke work. Slash commands in Claude Code: /tech-plan /server-code /client-code /server-unit-test /client-unit-test /api-test /code-review /pr-create /test-case-creator /playwright /bug-create /bug-rca. Or describe the task and let the developer agent sequence them.
Copilot. The QE agents (PW Script Writer, PW Script Reviewer, PW Debugger, QE Analyst, QE Bug Creator, QE TC Author, QE RF and RCA Investigator, QE Release Certification, SQL Performance Analyst) live in .github/agents/ and run in Copilot Chat. Engineering direction is to prefer Claude Code for token efficiency; use Copilot where those agents are.
THE BRIDGE
Repo-Native Agentic
A persona in the plugin that discovers the repo's own skills through a cheap catalog and asks before preferring a repo skill over a bundled one. It is why the plugin does not need a copy of every engineering skill, and why the repo stays the source of truth for engineering work.
BRAIN AND MEMORY
dvp plus the KnowledgeBase
The plugin is the brain: pure capability, the same for everyone. The KnowledgeBase is the memory: real Vantagepoint facts (work items, bugs, test cases, help topics, code references) organized by domain and subdomain. Skills read the smallest index that answers the question first, full records second, live source as final proof. Swap in a bigger KnowledgeBase and the skills get smarter without a plugin update. Without one, the skills still run from live source and say so.
Operating principles

These are not style preferences. Each one is enforced somewhere in a skill, and each one exists because the alternative failed in a POC.
Propose, confirm, write-back
Every write to Aha, ADO or Notion is proposed in plain language (record, field, old value, new value), waits for your go, then reports what was written. Reads need no confirmation. It is slower per write and it is the reason nothing has been written to the wrong place.
Never fabricate
No invented IDs, URLs, field values, file paths, method names or behaviors. If a skill cannot find something, it says so, or writes NOT FOUND in a technical plan. Empty search results mean "broaden and retry", not "does not exist".
Ground before you state
"How it works today" comes from the official help content on the ProductResearch SharePoint site, architecture from the ADO wiki, and code facts from the live repo. Never from the model's memory. The Rate Table frame had to be corrected on exactly this point.
AC is build-ready, Description is human reference
The organizing principle of the spec. If removing a section would make the feature unbuildable or untestable, it belongs in Acceptance Criteria. If humans would only lose the "why", it belongs in Description. AI, dev and QE build from AC.
One frame, one spec, per Feature
Same-Feature work, story splits and follow-up PBIs share the parent frame and spec. Only a materially different problem statement or new personas justify a new Feature. Prefer smaller features; large ones increase rework and reduce AI accuracy.
Unresolved stays visible
[OPEN] markers for anything not yet decided, strikethrough instead of deletion so history survives, dated update markers, and a Design Considerations audit that shows "considered and not applicable" as distinct from "forgot".
Humans hold the gates
The PDM approves every frame section and every spec write. The team decides carve-up. PR review is human, with the review skill as an aid. The scrum master marks Done. The AI proposes; it never closes a gate on its own.
Token discipline
Pick a scan level before retrieving: L1 indexes, L2 full records, L3 live source. Write finished artifacts to their home and keep only a pointer. Use the cheap model tier for scans and the strong tier for judgment. Never downgrade a live-source correctness check to save tokens.
PDM is not PM
PDM is the product management team. PM is the project manager: the customer persona Vantagepoint serves, and a separate internal delivery role. Every skill keeps them distinct; so should you.
Getting set up

CLAUDE DESKTOP DOOR
Install the plugin. Claude Desktop, profile icon, Settings, Capabilities (or Plugins), Upload plugin, choose dvp.plugin. It must show On. Remove any older deltek-core or deltek-vantagepoint plugins; they cause menu conflicts. Start a new chat after installing.
Authorize connectors in Settings, Connectors: Aha (deltek1.aha.io, VP2 workspace), Azure DevOps (tfs.deltek.com/tfs/Deltek, on-prem TFS, not ADO cloud), Notion (with access to the Framing Documents teamspace), Microsoft 365 (SharePoint ProductResearch site). Your own account must already have access to each system.
Check readiness in a new chat: check connectors. The reply names each connector Live or Missing and which skills are ready.
No Claude Project is needed. The earlier setup that pasted project instructions and uploaded skill files into a shared Claude Project is retired. Output lives in Notion and ADO where the whole team can see it.
If a connector fails
Expired personal access tokens are the common failure, especially for Azure DevOps. The skill will stop and name the connector; it never falls back to memory. Reconnect it in Settings, Connectors. Connector setup and maintenance is owned by Saurendu Chakraborty (handover from Francesco, 17 Sep). Ask in the Agentic AI Teams channel.
CLAUDE CODE DOOR
Repo checkout. The skills, agent and rules travel with the Vantagepoint repo. Pull the latest main. Nothing to install separately for Claude Code; the .claude/ folder is discovered when you open the repo.
Framework rules load first. Every coding skill reads agentic_ai/framework/*.md and agentic_ai/rules/*.md before writing code, and an app context file from agentic_ai/apps/ when one exists for your area. If your area has none, ask for one with the repo open (create an app context for <app>, the plugin's vp-create-app-context skill); it writes agentic_ai/apps/<app>.md and asks you for the TFS area path.
ADO access. The PR, test case, bug and RCA skills call the Azure DevOps MCP tools. Confirm they resolve in your Claude Code session before you need them.
KnowledgeBase. A KnowledgeBase is any folder with both manifest.json (with a knowledgeBase key) and START-HERE.md. Skills probe $DVP_KB_PATH, then KnowledgeBase/ and code/KnowledgeBase/ under the product root ($VP_HOME, default C:\Development\Vantagepoint), then the working directory. If none is found the skills say so once and continue from live source.
Copilot (QE agents). The repo's .github/ folder already carries the agents, instructions and prompts. Open the repo in VS Code and pick the agent in Copilot Chat.
KNOWLEDGEBASE READINESS
Domain KnowledgeBases are the formal prerequisite for the wider engineering rollout. Team owners and dev leads, not the platform team, build their own domain with Saurendu's interactive domain and subdomain skill, because domain correctness needs a domain expert. Product framing and spec work do not wait on it; accuracy is lower without it. Check your domain's status with your team owner before you rely on grounded answers, and say "No KnowledgeBase connected" is expected output, not an error.
Which features go through it

GOOD FIT TODAY
A releasable customer capability, MVP-sized, that fits within one release. Same sizing guidance as today's process, to be re-evaluated after the first group of features runs through.
Most 2027.2 features. Melissa reviewed the full list in Aha on 17 September and found the majority a good fit.
Any PBI or bug, for the engineering and QE skills. Every engineering role is expected to use the skills for defect fixing and testing whether or not the feature ran end to end.
EXCEPTIONS AND EDGES
Too big for one pass: scenario planning, draft invoice approvals. Split into releasable features first.
SST-dependent features where the underlying service is not yet defined: frame the desired customer outcome; the spec waits on the service.
Large features already in flight stay on their current path.
Technical and framework features: a subset is a poor fit for the functional capability spec. Jessica is defining a technical framing and spec variant focused on customer value (performance, quality). Guidance is due before feature reviews close.
Small quick wins may not need full framing. The Rate Table frame skipped the outcomes grid and competitive research for exactly this reason, by explicit PDM decision.
The 2027.2 expectation
Leadership's expectation for how many 2027.2 features run end to end (full adoption with a named exception list, or one feature per team as an intermediate step) is being set by Bret and will be stated here. Until then: every PDM runs at least one 2027.2 feature through Framing and Capability Spec, starting now.
Knowledge check
4 questions

Which statement matches the accountability model?
Claude writes to Aha and Notion once it is confident
Claude proposes every write; a person confirms before anything is written
The PDM writes; Claude only reads
Where do "how it works today" statements come from?
The model's knowledge of ERP software
Official help content on the ProductResearch SharePoint site, plus the ADO wiki for architecture
The Feature Review deck
A section of the spec, if removed, would still let the feature be built correctly. Where does it belong?
Acceptance Criteria
Description
A separate Notion page
Why should you invoke Vantagepoint skills by name rather than following the /dvp persona menu today?
The persona files still describe an older generic workflow; naming the skill routes directly to the correct Vantagepoint procedure
Personas cost more tokens
Skills cannot be invoked from personas
Mark Module 1 complete
MODULE 2
The lifecycle, step by step
45 minutes for your role · 90 for all six stages
Companion video · 4 min 47 s
Prefer to watch first? The lifecycle, step by step walks the six stages at overview depth, with narration and captions. It lives in the AI SDLC Enablement folder under Module 2 Video, next to this file, with its caption file (.vtt) and the storyboard. This module remains the full procedure.
Each stage below is written as a procedure: who is in the room, what has to be true to start, the ordered steps, what you say to Claude, what the AI does versus what you decide, what comes out, and the gate that ends the stage. The board columns each stage maps to are shown so you can find the same work on the Kanban.
Legend: AI does retrieval, drafting, interrogation, write-back. You do judgment, confirmation, decisions. Live built and in use. Live in repo shipped in the Vantagepoint repo on 16 September. Manual a real step with no skill yet. Not built designed, not yet available.
Stage 1 · Proposed 
PDM

Board: before Framing (release planning)
Manual, today's practice
An idea enters Aha from the ideas portal or from a PDM, is promoted to an Aha Feature in the VP2 workspace, and the Aha to ADO sync creates the matching ADO Feature automatically. Prioritization and release targeting happen here as they do today. No AI-SDLC skill runs in this stage, but two things it produces matter downstream.
A Feature record exists, with its idea linked
Framing starts from an Aha Feature reference (VP2-####). It does not matter which release the Feature targets. The linked idea carries the customer language, votes and organizations that framing reads, so promote the idea rather than creating a Feature with no idea behind it. If framing finds no linked idea it stops and asks how the Feature originated.
The Feature has a plain-language roadmap description
Convention: two to four sentences written for a non-technical audience (firm principals, project managers, finance leads). Framing later replaces this with a short-form summary and a link to the Notion frame.
Status is one that framing accepts
VP2 features use a customized workflow: New, Approved, Committed, Done, Released, Rejected. Framing proceeds for New, Approved or Committed and asks before touching anything Done, Released or Rejected.
Sync rules you should know
Aha and ADO Features are bidirectionally synced. The Feature Name flows Aha to ADO. The Description does not flow Aha to ADO once a capability spec exists on the ADO Feature, because that would overwrite the spec; the spec skill mirrors a User Story summary back to Aha instead. Aha's Integrations field holds the link to the ADO Feature.
Stage 2 · Framing 
PDM
UX

Board: Framing (release planning)
Live · framing v2.8
Claude Desktop
Framing takes a Feature from idea to a well-scoped, evidence-grounded problem statement with outcomes and a prototype direction. It is the deeper version of storytime prep, done before the room is full. The output is the Frame Artifact: one Notion page per Feature, 18 sections, Decisions Made and Open Questions included. The frame is the scope contract for everything downstream.
Who runs it: the PDM, alone with Claude, typically before release planning. Who reads it: product leadership for review, then the whole scrum team in Exploring. UX joins when a wireframe is wanted; engineering's technical reality check arrives through the ADO wiki and related work items the skill reads, not by attendance.
Entry: an Aha Feature reference; Aha, Azure DevOps, Microsoft 365 and Notion connectors live.
Say: let's frame VP2-1234 frame this feature start framing generate frame brief
Retrieve the Feature and its signal context
AI does
deltek-aha-lookup
Feature title, description, tags, initiative links, notes, and the linked ideas (read through the feature's ideas association, which Aha omits by default). For each idea: description, submitter, date, PM notes, portal comments, vote count, and voting organizations. Any org with more than 3,000 employees or more than $1M revenue is flagged High-Value Org. Incomplete org data is flagged by name, never assumed. The status gate runs here.
Competitive research prompt
You decide
Claude asks whether to include competitive research, and if so whether to search the web or synthesize research you provide. The default competitor set is BST, Unanet, Workday, Microsoft Dynamics and QuickBooks; you can add, remove or replace (Mosaic is a candidate for resource planning features). Web search never runs without your explicit confirmation. Declining is a valid answer and is recorded in the frame.
Read the context sources
AI does
deltek-azure-devops-lookup
vantagepoint-help-lookup
Aha wiki business-significance pages for the functional area (often absent; not a blocker), the ADO wiki and PRD for architecture and integration constraints, and the official Vantagepoint help content for how the functionality works today. Gaps are noted in Open Questions, never filled from general knowledge.
Map related capabilities
AI proposes
You confirm
Searches Aha (demand side) and ADO (in-flight and built work) for related items and classifies each as Dependency (predecessor or successor), Overlap (duplication risk or collision risk) or Replacement (elimination or consolidation), with a one-line reason. This lands in the brief as a proposal you confirm, recategorize or dismiss with a reason, so overlaps surface before scope is set. Rate Table surfaced its own engineering-side twin (ADO Feature 1953408) this way.
Generate the Frame Brief
AI drafts
A 16-section working document: feature reference, idea summary with High-Value Org votes, what we know from customers (customer language, grouped by theme), current behavior (grounded and cited), proposed change (a delta, not a solution), initiative connections, functional and architectural context, competitive research, draft problem statement ("[user type] needs to [goal] but currently [obstacle], which results in [consequence]"), scope in (outcomes, not features), scope out (with reasons), related capabilities, open questions, stakeholders (Documentation / Writer is always included), prototype direction.
Review the brief with Claude, section by section
You decide
AI challenges
Claude pushes back on scope items that read like solutions, on vague problem statements, on a proposed change that reads like a spec, and on architectural conflicts (project-based billing, resource management, time entry, AP/AR, project accounting). One open question at a time. Gate: you confirm the problem statement, scope and related capabilities, or explicitly proceed with known open items.
Build the outcomes grid
pm-outcome-grid-builder
You confirm inputs first
Claude shows the three inputs the grid inherits (confirmed problem statement, customer validation, competitive benchmark) and pauses. Corrections go into the frame first and are logged in Decisions Made. Then the grid builder runs in embedded mode and interrogates only the elements it owns: primary outcome, secondary outcome, leading indicators, baseline measured, measurement method, business impact (Revenue, Margin, Risk). Target is hypothesis grade: every element present, numbers labeled Hypothesis or SME Estimate. Where no baseline exists the skill produces a User Simulation Request for UX instead of inventing a number. A PDM may skip the grid for a quick win, as Rate Table did; the decision is recorded.
Assemble the Frame Artifact
AI assembles
You approve
The 18-section permanent record: 1 Feature Reference, 2 Associated Idea Summary, 3 Problem Statement, 4 Current Behavior, 5 Proposed Change, 6 Customer Evidence, 7 Competitive Research, 8 Outcomes, 9 Initiative Alignment, 10 Functional Area Context, 11 Architectural Context, 12 Scope In, 13 Scope Out, 14 Related Capabilities, 15 Decisions Made, 16 Open Questions, 17 Stakeholders, 18 Prototype Direction. Nothing is written until you approve it.
Confirm the prototype direction; wireframe if you want one
vantagepoint-mockup
PDM-initiated
Section 18 names the single most important question a prototype must answer. Once confirmed, Claude offers a lo-fi HTML wireframe that uses real Vantagepoint regions and layout conventions, checked against three criteria: does it answer the direction question, does it stay inside Scope In, does it surface the right decision without solving the problem prematurely. Iterate directly; after three cycles the issue is probably the frame, not the wireframe. Framing can close without one. Higher-fidelity design stays with UX in Exploring.
Write the frame to Notion and back-link Aha
deltek-notion-frame-home
deltek-aha-lookup
Confirm each write
7.1 Find-or-update the one page for this Aha Feature # in the Framing Documents database (never a duplicate); properties Feature Name (mirrors the live Aha name), Aha Feature #, links, ADO Feature # when known, PDM = you. 7.2 Update the Aha description with a 2 to 4 sentence plain-language summary, the one-sentence problem statement, current behavior and proposed change, and the Notion URL. Each write is proposed and confirmed.
Close
You decide the status
Claude confirms what was written and asks whether to change the Feature's Aha status and to which one. It never picks a status for you. A dedicated "Framed" status is planned. Stakeholder notifications from section 17 are yours to send. Then "Framing is complete for [feature]".
AI OWNS
Retrieval, High-Value Org flagging, competitor list presentation, context reads, related-capability search and classification, brief and artifact drafting, outcomes hand-off, wireframe generation, Notion and Aha writes after confirmation.
YOU OWN
The feature reference, every judgment call on current behavior and proposed change, the competitor set and method, problem statement, scope-out reasoning, related-capability dispositions, inherited outcome inputs, approving the artifact, whether and when to wireframe, every write, the closing status, stakeholder notifications.
After framing: review, and the manual pre-think
Manual
Gotchas seen in real runs
Stage 3 · Exploring 
PDM
DEV
QE
UX
SM

Board: Feature Review (release planning)
then Requirements Collab (release execution)
Live · capability spec v1
Claude Desktop
Exploring turns the frame into the Capability Spec, the implementation contract that dev, QE, UX and the downstream AI skills build and verify from, and gets the team to an agreed carve-up into PBIs. It spans two board columns. Feature Review sets direction: the PDM brings the frame and a first-draft spec, the whole team discusses, PBIs are anticipated and estimated. Requirements Collab is the deeper pass inside the release: the same assets are refined until the spec and the feature dev plan are final and design review per PBI has happened. Engineering is in every whole-team conversation; the skill accelerates the artifacts, the conversations stay team-owned.
Who is in the room: the feature owner (PDM), developers, QE, the Team Owner (near-mandatory), UX most of the time, Documentation as a stakeholder. Who runs the skill: the PDM, between meetings. The skill does not sit in the meeting; it processes what the meeting produced.
Entry: the Aha Feature exists; a completed frame exists in Notion (the skill checks and offers to run framing first if not); all four connectors live.
Say: start capability spec for VP2-1234 update the spec for VP2-1234 based on these notes walk considerations for VP2-1234 prep for next meeting on VP2-1234 close the spec for VP2-1234 You can use the feature name instead of the number; the skill confirms the match before proceeding.
The spec: 16 sections in two fields
ACCEPTANCE CRITERIA · BUILD-READY · AI, DEV AND QE CONSUME THIS
User Story, rich: persona, goal, benefit, business rationale, customer motivation, expected outcomes. Not one line.
Summary (optional), one exec-friendly paragraph.
Existing Behavior: how the system works today, that this feature changes.
Existing Configuration and Security: external dependencies only (module ownership, existing settings, existing Opt-Ins, existing permissions).
Capabilities and Requirements: numbered Req N.M blocks; includes an Enable Mechanism subsection when the feature introduces a new Opt-In, Setting or Security permission.
Mockups: Level 1 text descriptions of the UI plus Figma or Notion references.
Use Cases: UC-# with actor, preconditions, trigger, main flow, expected outcomes, alternate flows, error flows, post-conditions.
Out of Scope, with reasons.
Outcome Measurement: one disposition per frame outcome.
Documentation and Tracking: Doc ID, notes for documentation, Gainsight.
DESCRIPTION · HUMAN REFERENCE · CONTEXT, HISTORY, AUDIT
Feature References: Feature #, Aha #, Notion frame URL, PDM, iteration, effort, tags, implementing PBIs.
Update Summary: dated log of meaningful changes.
Related Work Items: sibling Features, dependencies.
References: external research, standards, legal frameworks.
Team Follow-ups: the team's in-flight work during Exploring (item, category, owner as Role (Name), related section, status).
Design Considerations audit: one line per consideration walked, with its disposition.
Requirements and use cases carry numbers (Req 6.4, UC-3) so the room can say "let's talk about Req 6.4" without counting bullets.
How a spec session runs
Every session starts the same way: the skill resolves the Feature, checks the entry gates, reads the frame and the current spec, confirms the connectors, and infers which of five modes you want from how you phrased the request. You can switch modes mid-session by rephrasing.
Mode a · Initial authoring, before the Feature Review
AI drafts
You shape, then approve the write
Say start capability spec for VP2-1234. The skill drafts Feature References, then inherits from the frame: problem statement, proposed change, evidence and outcomes become the rich User Story; current behavior and dependency-type related capabilities become Existing Behavior; scope out becomes Out of Scope; prototype direction seeds Mockups and Use Cases; outcomes seed the Outcome Measurement stub. You can refine before the team sees it or take the first cut as is; there is no approval gate before the room, only before the write. Then, on your confirmation, it writes AC and Description to the ADO Feature, creates the default child PBI (a thin reference titled after the Feature, the item dev will pick up), and checks the Aha to ADO Integrations link.
You do not need the whole solution figured out. Leave open items as [OPEN]; the skill surfaces them so they land in the Feature Review conversation instead of forcing a guess.
Feature Review meeting
Team conversation
Feature dev plan and estimates are manual
Inputs: the frame and the first-draft spec, not a deck. The PDM facilitates; developers, QE, UX and the Team Owner discuss scope, requirements, use cases, considerations and the anticipated carve-up. Outputs on the board: frame, spec draft, Feature Dev Plan draft (how the work breaks into stories), Feature estimated, PBIs created and estimated. Capture the meeting as a transcript or notes; that record is the input to the next step. Today the dev plan and estimates are produced by the team by hand; a PBI breakdown and estimation skill is being defined.
Mode b · Process the meeting record
AI extracts and proposes
Accept, edit or reject each proposal
Say update the spec for VP2-1234 based on these notes and paste or attach the transcript, notes or Miro export. The skill reports which sections the meeting touched, the Team Follow-ups it extracted (with proposed owner from speaker attribution, category and related section), the decisions it identified, and anything unresolved or reversed. Clear decisions become content. Maybe-decisions become [OPEN] markers with a note ("verify decision: I heard auto-approve, please confirm"); nothing is silently written as fact. Reversed decisions are struck through with the new content added beneath and a dated marker. Phrases like "what if", "edge case" and "alternatively" become candidate use case flows. Section by section it shows current content, the proposed update and where in the record it came from; you accept, edit or reject. Follow-ups are reconciled, mockup references captured, and if the team agreed a carve-up ("let's make mobile its own PBI") the PBI creation subflow fires. Then one atomic write to the Feature.
Mode c · Work the gaps, including the considerations pass
AI interrogates
You disposition
Say walk considerations for VP2-1234 or update the use cases for VP2-1234. The skill lists what is open: empty sections, [OPEN] markers, open follow-ups, undispositioned considerations and outcomes. You pick; it asks the questions needed to draft or resolve; each accepted update is written on confirmation.
The considerations pass walks the PDM Considerations checklist (about 30 items from the canonical SharePoint document) in five groups: UI and Design (Screen Designer, Mobile, Info Bubbles and iButtons, Row Tools, Paging, Search UI); Data and Reporting (Cubes, Dashboard Bases, Search and Replace, Key Convert); Integration and External Coordination (Cloud Impact, Gainsight fields, Gainsight actions, Transfer Settings Utility, Outlook Integration, Public API, Private API); Documentation (Doc ID, Help topics, Release Notes); Other (Security, Auditing, Localization, Accessibility, Performance). Each item shows an applicability signal (Likely, Possibly, Unlikely, Pre-populated from frame) to help you prioritize attention; every item is still walked. Dispositions use a controlled vocabulary: Yes, in spec §X.Y; Yes, new PBI [ID] (fires PBI creation); Yes, existing PBI [ID]; No, with a one-line reason; Deferred, with context. Items that need someone told (Cloud: Shirley and Brent; Gainsight fields: Charles K.; Gainsight actions: Teresa; Transfer Settings: Team 4; Cubes: Team 10 / Ellen; Doc ID: Documentation) are marked NOTIFICATION NEEDED in the audit block and you send them. A public API is not optional: it must be made available to Ask Dela, and the exact requirement text is a placeholder pending Brent's spec. A private API is optional; the skill asks.
The outcome measurement review walks each frame outcome: Measurable today (mechanism), Folded into existing PBI, New PBI (creates it), Deferred, or Cannot be measured with reasoning.
Enable mechanism. The skill asks whether the feature introduces a new way to activate or gate itself. New Opt-In: a 10-field block (area, name, title, description, enabled by default, hidden, reversible, help topic, module dependency, release automatically enabled, release removed), and the two follow-up PBIs (Hide/Enable, Remove) that you create by hand for now. New Setting: 8 fields. New Security permission: 7 fields. Existing mechanisms the feature depends on are line items in Existing Configuration and Security instead.
Use cases are interrogated against coverage domains: happy path, boundaries, permissions, data state, concurrency, integration failure, reversal. They are what QE and automation build from.
Requirements Collab and Design Review
Team, inside the release
Modes b and c between meetings
The deeper pass. Open questions left after Feature Review are resolved, the feature dev plan and PBIs are finalized, and each PBI's implementation slice is reviewed against the spec (Design Review). All detail stays at the Feature level; PBIs stay thin. The spec skill is the between-meeting tool throughout: process each session's record in Mode b, work remaining gaps in Mode c. Exit: finalized capability spec and finalized feature dev plan.
Mode d · Prep for the next meeting
Read-only summary
Say prep for next meeting on VP2-1234. The skill produces a paste-ready state summary: sections complete, in progress and not started; open questions; considerations and outcomes without disposition; follow-ups needing the team; recent changes. It writes nothing.
Mode e · Close
Runs the gates
You decide it is ready
Say close the spec for VP2-1234. Gates: every outcome dispositioned; every consideration dispositioned; every Team Follow-up resolved, deferred with reason, or converted to a PBI (In progress and Blocked are acceptable); every [OPEN] resolved, with [SPIKE-#] and [DEPENDS ON SPIKE-#] the one exception when the spike has its own PBI; all required AC and Description sections populated. Use case coverage of requirements is checked and reported as advisory. Then a final PBI verification (each PBI references the spec, has an iteration, sits in the Feature's swimlane, follows the naming pattern), the final atomic write, and a write-back to the frame: a "Considerations and Outcomes Resolved (Exploring)" section, one line per disposition, so the frame stays the durable record of everything ever considered. Post-close, by hand for now: Notion frame status to Complete, external notifications, the Aha status you choose.
PBI creation: when it happens and what a PBI looks like
Living-document conventions and what is manual today
AI OWNS
Entry checks, frame and spec reads, drafting from the frame, parsing meeting records, section-by-section proposals with attribution, PBI proposals, walking considerations and outcomes with applicability signals, capturing follow-ups, running the close gates, every write after confirmation, the frame write-back.
YOU OWN (WITH THE TEAM)
Scope and requirements, every accept, edit or reject, dispositions, carve-up and estimates, owners of follow-ups, sending notifications, deciding when the spec is ready to close, the Aha and Notion statuses.
UX in Exploring
UX joins spec authoring for anything with a real interface. Mockups in the spec are Level 1 today: text descriptions of the affected screens, fields, states and interactions in Acceptance Criteria, plus Figma or Notion references. Higher-fidelity mockups are produced by UX outside the skill and referenced; UX work in progress is tracked as a Team Follow-up with a UX owner. A Level 2 mockup skill callable from the spec is planned. Where synthetic personas belong and whether UX needs its own skill are open items owned by Dawn and Alex.
Engineering and QE in Exploring
Your job in the room is the implementation shape: the carve-up, technical considerations (data model boundaries, API surface, sequencing, spikes), and testability. Read the User Story and Use Cases closely; thin user stories caused QE to focus on the wrong things in the first POC, which is why the story is now rich. If a requirement cannot be written with confidence until a spike resolves, ask for a [SPIKE-#] and its investigation PBI rather than letting the requirement be written as fact.
Stage 4 · Building 
DEV
QE
SM

Board: Ready for Dev
In Dev
In PR
Live in repo · 16 Sep
Claude Code
Building turns the spec and the dev plan into an approved PR. The developer works PBI by PBI. Each PBI first gets a Technical Plan (and a Research Findings document describing the code as it is today), both produced against the real codebase and attached to the PBI; then the plan is executed task by task with the coding skills, tests are generated at three layers, the multi-agent review runs, and the PR is raised. QE writes test cases in parallel from the spec's use cases. Team Owners make sure reviews and approvals happen quickly.
Ready for Dev is a queue column with no tasks. It exists so the scrum master can see bottlenecks moving work into development. Entry to In Dev: a finalized capability spec on the Feature and a finalized feature dev plan; the PBI is in the sprint.
Say (Claude Code, repo open): /tech-plan 2808724 /server-code code/server/VB/LaborRateTableSetup/Server/RateTableSetup.metadata.vb /client-code labor_rate_tables /api-test RateTableController /server-unit-test LaborRateTableBO /code-review /pr-create 2808724
Load the framework knowledge (every skill does this first)
AI reads
The coding and test skills load agentic_ai/AI_Agent_Routing.md and the guides it routes to, the framework overview (agentic_ai/framework/server.md or client.md), the rules (agentic_ai/rules/server-rules.md, client-rules.md, the testing rules), and an app context file from agentic_ai/apps/ when one exists for the feature area (code locations, API routes, tables, related projects). If your area has no app context file, have one created before the first feature; it saves exploration time on every later task.
Technical plan and research findings for the PBI
tech-plan
AI researches and drafts
You answer 3 to 5 questions
The skill locates the spec (attached file, the PBI or Feature's Acceptance Criteria and Description, or a linked item), reads the framework rules, and extracts capabilities, UI elements, endpoints, fields, enums, out-of-scope items and edge cases. Then two mandatory steps that cannot be skipped: it asks you 3 to 5 targeted clarifying questions in one message (continuation scope, endpoint parameters, field composition, enum reuse, cleanup, dependencies on other PBIs, testing constraints) and waits; and it researches the codebase so every file path, route string, method, field, enum and parameter in the plan comes from source. Anything it cannot find is written as NOT FOUND, never guessed.
The plan has a fixed shape: summary; carry-over decisions (for continuation PBIs); numbered objectives and a user flow; endpoints and data contracts with file and line references; tasks A, B, C, each naming its files and the skill to execute it with (/server-code, /client-code, or both) and including paste-ready snippets; testing in four subsections (server unit, API/integration, client Karma/Jasmine, regression guards), each present even if empty with a reason; a How to Execute table mapping every task and test layer to a skill; a Before Coding checklist; a binary Definition of Done. Out-of-scope items from the spec become explicit "do not implement" guards. Both documents are attached to the PBI. Module 4 shows the real ones for Rate Table.
Implement the plan, task by task
server-code
client-code
You steer and review
Give the coding skill the plan. Step 0: it reads the plan and holds two lists for the whole session, the out-of-scope guards it will not implement no matter what, and the regression guards it must not break. Steps 1 to 3: framework, rules, app context, references on demand (server reference, query-group patterns, long-running transaction guide, client reference, testing references). Step 4: the change, following the pattern of the nearest existing code (server: the BO hierarchy BaseClass, BaseBO, VisionBaseBO and the save flow PersistRecord, ImportRecordValidateChanges, ImportRecordCommitChanges, Save; client: the feature folder structure, models extending BaseModel, API route matching resourceRoute). Then the regression guard check. Step 5: targeted build (msbuild ... WebApiAndTest.slnf), dotnet test for the affected project, npm run test:headless for client tests.
Database changes go through the standard DCR process. Server and client code can be developed in parallel with the DCR; integration tests need the DCR applied to the dev database.
Tests at three layers
server-unit-test
client-unit-test
api-test
Server unit tests (xUnit, FluentAssertions, Moq): the skill locates the class and its partials, audits raw SQL string literals for misaligned closing delimiters and adds the --ClassName-MemberName comment prefix every query needs for stable mocking (fixing the source where needed), then writes the test class in the matching test project. Client unit tests (Karma/Jasmine) live beside the source. API tests use the TestHarness, authenticate through TestHarnessOptions, assert status codes before bodies, use FluentAssertions, and call DbMock.Verify() after any mocked database interaction. Distinguish first: a unit test mocks at the BO level; an API test exercises controller to BO to database.
QE in parallel: test cases from the spec
test-case-creator
QE
While code is being written, QE generates test cases for the PBI from the spec's use cases (procedure in Stage 5). Automation waits for working code and stable test cases.
Review before you raise the PR
code-review
Eight agents in parallel
You decide what to fix
On a feature branch, the review orchestrator detects the base branch, lists changed .cs, .vb and .js files (excluding generated files), warns about uncommitted changes, and runs specialist reviewers in parallel, each against its own rule file in agentic_ai/reviews/: Security, Framework Conventions, Dependency Injection, Modern C#, Unit Testing, JavaScript Frontend, Performance, General. Findings come back as Critical, Warning and Info with a suggested fix, deduplicated into one report with a verdict: BLOCK (any Critical), PASS WITH WARNINGS, or CLEAN. Large changesets suppress Info unless you ask for thorough. Run it before the PR and again after changes.
Raise the PR
pr-create
The skill loads agentic_ai/PullRequest.md and follows it exactly: repository coordinates, work item linkage, title and description conventions, the ADO MCP call, and the fallback if the call fails. Output on the board: PR code raised, performance test complete where applicable, unit tests, API tests, manual test cases complete.
In PR: human review and approval
Reviewers approve
SM
The review skill is an aid to the reviewer, not a replacement. Human approval is mandatory. Team Owners ensure code reviews occur and PRs are approved quickly. Output: approved PR, checked-in code. A dev demo to the PDM follows.
The developer agent
The deltek-developer agent in the repo (shipped 16 September) sequences this chain for you: a questions gate, the plan, the code, the API, unit and performance tests, and the review, announcing each hand-off. Use it when you want the whole chain driven; use the individual slash commands when you want to run one step. Its exact step list is maintained in the repo and will be confirmed here after the first team runs.
AI OWNS
Loading rules and context, codebase research, the plan and research documents, the code change within the plan's guards, test generation at three layers, the multi-agent review report, the PR mechanics.
YOU OWN
Answering the plan's questions, confirming risky steps (migrations, high-risk changes), the DCR, reading the diff, deciding which findings to fix, the review approval, the demo.
Manual today, or still being defined
Stage 5 · Verifying 
QE
AUTO
DEV

Board: In Testing
In Bug Fixing
Live in repo
Claude Code · Copilot for QE agents
Verifying proves the feature does what the spec says. QE executes the test cases written during Building, logs bugs, and developers fix them through the same code, test, review and PR chain. Automation engineers convert stable test cases into Playwright tests. Root cause analysis and release-found triage keep the quality signal honest. Exit: fully tested code, all bugs fixed.
Say: /test-case-creator 2808724 /bug-create /bug-rca 1234567 /release-found 1234567 /playwright /tc-identify-performance 2808724 /final-certification
Test cases from the PBI or bug
test-case-creator
QE
Approve the JSON before creation
The skill loads the AI Test Case Generation Guide in full, then asks which output you need: Manual QA Tester (step-by-step UI instructions), Automation Developer (complete automation script), or Hybrid. It fetches the work item, and before generating anything runs duplicate detection in TFS by linked work item, module plus title keywords, and area path. Existing duplicates stop it and you choose: update, create a distinct scenario, or skip. It generates the test case in the exact JSON structure the guide specifies, presents it, and creates it only after your approval. Rules: one scenario per test case (Deltek.ScenarioCount = 1, so comprehensive coverage means several TCs), the @DBFlavor parameter is mandatory (from MasterDBFlavor when the work item names a database), titles carry the AI-generated prefix, UI element names and navigation paths are verified against the Vantagepoint Applications Reference and never invented, and HTML fields use HTML.
The repo also carries qe-tc-generation, qe-bug-tc-generation and qe-tc-review, and Copilot has the QE TC Author agent. Which is preferred for which case is QE-lead guidance.
Execute and log bugs
bug-create
QE
Manual testing runs against the spec's use cases and the test cases. To log a bug the skill needs eight things from you and will not invent any: module, exact issue, version tested, reproduction steps, expected versus actual, severity 1 (Critical) to 5 (Cosmetic), evidence, and the related PBI if any. It runs the five-phase duplicate detection against active bugs (New, In Development, In Testing, Committed), loads the right template (General Bug, or New Feature Bug when tied to a PBI), completes a pre-flight checklist (all four content fields populated: DescriptionHtml, ReproSteps, AcceptanceCriteria, Deltek.testSteps; title starting "AI Generated Bug:"; RelFound a real version or empty; area path validated; severity confirmed), presents the JSON, and after approval creates the bug and links it to the PBI with an Affects relationship. It never sets Regression, Blocked, Assigned To or Priority; those are human calls. Deltek.testSteps holds post-fix regression areas, not repro steps.
Automation with Playwright
playwright
AUTO
PW agents in Copilot
The framework is TypeScript on Playwright under tests/qe/web/playwright/, layered: the Session (u) is the actor and owns browser context, login, locale and i18n; page objects own selectors and UI interactions; API objects own endpoints and typed responses; business objects own data shape (Zod schema first, type inferred); Forge generates test data with dependency resolution; the Localizer resolves every user-visible string; pre-conditions skip cleanly with u.require(). Four phases: Plan (fetch the work item, decompose into atomic steps, pick sanity, CRUD or feature test, name the area path); Resolve (find existing page objects, APIs and BOs; if missing, build in order schema, API, page object, test); Script (every string through u.i18n(), every created entity torn down through TeardownStack, step titles written as repro steps, pre-conditions first); Review and Debug (a three-agent review with Mandatory, Recommended and Advisory findings; failure diagnosis from terminal output and artifacts with an RCA before any code changes). The skill's reference files carry conventions that are not in general training data; it reads the matching reference in full before answering.
When to start automation: after code works and the test cases are stable. The exact trigger is being decided between Dev and QE; until then, do not automate against an unstable slice.
In Bug Fixing
DEV
server-code · client-code · code-review · pr-create
Developers fix bugs with the same coding skills, giving the bug as input, then tests, review and PR. Root cause analysis runs alongside.
Root cause analysis
bug-rca
QE
The skill loads the QE RCA guide and four mapping files (14 defect migration categories, 5 missed-scenario subcategories, 4 missed-execution subcategories, the RCA notes template) and tolerates no value outside them. It fetches the bug, verifies source code through PRs when the bug is Done or In Testing, and runs a mandatory test case research pass in TFS (eight or more area paths, full steps read, PBI coverage verified) before any classification. Then it classifies defect migration, determines the subcategory, generates the QE RCA Notes in HTML, updates the required TFS fields (never empty), re-reads to verify, and updates related bugs with the same title. Breaking Change bugs additionally require Deltek.BuildFoundIn.
Release-found bugs and performance fixes
release-found
tc-identify-performance
Release-found: is the bug new, a regression, or pre-existing; which PR introduced it (changed files against the affected functionality); what is the blast radius (modules and shared components); what is the immediate action (hotfix, RCA, more regression testing); is it a Breaking Change. Performance fixes: a query or index change that fixes one scenario can break another, so the skill maps blast radius (SQL layer, BO layer, shared utilities), fetches linked test cases, filters by state and usage, finds gaps (the original slow scenario, adjacent operations, concurrency, boundaries) and prioritizes P1 to P3.
Release certification, M1 to M6
final-certification
Copilot Chat today
Routes to the certification template for each milestone in tests/QEGuides/Final Certification Analysis Templates/: M1 tech debt and quality gaps, M2 areas with changes (runs the joined PR export), M3 end-to-end and intermodule, M4 areas without changes, M5 tablet test case selection, M6 bug-fix test case analysis with a GO or NO-GO recommendation. Each names its inputs (release version, target branch derived as releases/production plus the version digits, area path, CSV exports).
AI OWNS
Duplicate detection, test case and bug drafting in the exact TFS structures, RCA classification within the allowed values, Playwright planning, resolution, scripting and review, blast-radius mapping, certification analysis.
YOU OWN
Test execution and judgment, the eight bug inputs, severity, approving every TFS write, regression and priority calls, the automation trigger, the GO or NO-GO.
Open questions QE should know about
Stage 6 · Released 
SM
PDM

Board: Done
Manual today
The scrum master marks work complete. The frame's outcomes become the yardstick: each outcome was dispositioned during Exploring (measurable today, a measurement PBI, deferred, or qualitative), so the follow-through is already written down.
Done on the board
SM
PBIs and the Feature move to Done. In Aha the PDM chooses the Feature's status (Done, then Released) through the Aha lookup's propose, confirm, write-back.
Close the frame and the record
PDM
Manual
Set the frame's status to Complete once the Notion Status property exists (today: your team's signal). The spec's "Considerations and Outcomes Resolved" section already lives on the frame from spec close, so the frame remains the durable record of everything considered.
Release notes and documentation
PDM
RelNotes skill not built
Customer-facing release notes are drafted by the PDM into the ADO RelNotesDescription field; a release-notes skill that drafts from the spec's Summary and key requirements is designed for later. Documentation was a standing stakeholder from the frame onward; confirm the Doc ID and help-topic updates flagged in the spec's Documentation and Tracking section landed.
Measure outcomes
PDM
Read the Outcome Measurement dispositions: existing Gainsight events, reports or telemetry, or the measurement PBIs that shipped with the feature. Outcome confidence matures from Hypothesis toward Validated here.
Feed the loop
Everyone
Bugs found after release run through /release-found. Anything that was confusing, wrong or slow in the skills goes into the PDM Skill Feedback and Enhancement Log (Module 6) or the engineering channel, so the next feature is easier than this one.
Knowledge check
6 questions

Framing's Step 4.5 pauses before building outcomes. Why?
The grid inherits the problem statement, customer validation and competitive benchmark; an error there propagates through every outcome
To ask which competitors to research
To write the frame to Notion first
A meeting transcript says "I think we agreed on auto-approve, right?" What does the spec skill do with it?
Writes auto-approve into Requirements
Proposes an [OPEN] marker asking you to verify the decision
Ignores it
Which of these blocks spec close?
A requirement with no matching use case
A consideration with no disposition
A Team Follow-up in Blocked status
Which step of the technical plan skill can be skipped when you are in a hurry?
The 3 to 5 clarifying questions
The codebase research
Neither
What does the review orchestrator's verdict BLOCK mean?
At least one Critical finding; fix before merge
The branch is master
Too many files to review
How many scenarios go in one test case?
As many as needed for full coverage
One; write more test cases for more scenarios
Two, a positive and a negative
Mark Module 2 complete
MODULE 3
Work items through the lifecycle
20 minutes · everyone, essential for Scrum Masters and Team Owners
Four systems hold the record: Aha for demand, Notion for the frame, ADO (on-prem TFS) for the Feature, the spec, PBIs, bugs and test cases, and the Vantagepoint repo for plans, code and automation. This module is the map of which record holds what, how they link, how the board reads, and who moves what.
Systems of record

AHA · DELTEK1.AHA.IO · VP2
Demand
Ideas (VP2-I-####): customer language, votes, organizations, portal comments
Features (VP2-####): the unit of scope and of specification
Epics, initiatives, releases
Feature description carries the short-form frame summary and the Notion link
Integrations field links the ADO Feature
NOTION · FRAMING DOCUMENTS DATABASE
Scope contract
One page per Feature, keyed by Aha Feature #
The 18-section Frame Artifact, Decisions Made and Open Questions inside
Properties: Feature Name (mirrors Aha), Aha Feature #, links, ADO Feature #, PDM
Gains "Considerations and Outcomes Resolved" at spec close
Status property: designed, not yet added
ADO · TFS.DELTEK.COM/TFS/DELTEK · VANTAGEPOINT
Implementation contract and delivery
Feature: Acceptance Criteria (build-ready spec) and Description (human reference)
PBIs: thin slices under the Feature swimlane
Bugs, Test Cases, PRs
The Kanban board and iteration paths
Wiki and PRD: architecture context framing reads
VANTAGEPOINT REPO
Where the code and the engineering brain live
Research Findings and Technical Plan per PBI (attached to the PBI)
Code, unit, API and client tests, Playwright automation
.claude/skills, .claude/agents, .github/
agentic_ai/ framework rules and app context
tests/QEGuides/ and the KnowledgeBase folder
The board

Two phases, nine columns. Framing and Feature Review are release planning; everything from Requirements Collab onward is release execution. Ready for Dev is a wait state with no tasks. The scrum master watches the whole flow for bottlenecks.
COLUMN	PHASE	STAGE	WHO	APPLICABLE SKILLS	OUTPUT WHEN THE CARD LEAVES
Framing	Release planning	Framing	PDM owns it, early in the planning cycle, ahead of Feature Reviews	framing; wireframe (vantagepoint-mockup)	Frame in Notion; wireframe if applicable; Feature exists in TFS
Feature Review	Release planning	Exploring	PDM facilitates; whole team	framing; capability-spec; UX (placement being defined); feature dev plan and PBI creation (manual today)	Frame; capability spec draft; feature dev plan draft; Feature estimated; PBIs created and estimated
Requirements Collab	Release execution	Exploring	PDM and scrum team	capability-spec (modes b, c, d, e); feature dev plan and PBI creation	Finalized capability spec; finalized feature dev plan
Ready for Dev	Release execution	Building	Scrum master watches for bottlenecks	None (holding column)	Nothing; the card waits here
In Dev	Release execution	Building	Assigned developer; QE and automation create test cases in parallel	developer agent; tech-plan; server-code; client-code; server-unit-test; client-unit-test; api-test; performance-analysis; test-case-creator; code-review; pr-create	PR raised; unit tests; API tests; performance test where applicable; manual test cases complete
In PR	Release execution	Building	Reviewers; Team Owners ensure reviews occur and approvals are quick	code-review	Approved PR; checked-in code
In Testing	Release execution	Verifying	Assigned QE; automation	test-case-creator; bug-create; playwright; tc-identify-performance	Fully tested code
In Bug Fixing	Release execution	Verifying	Assigned developers; QE for RCA	server-code; client-code (fix); bug-rca; release-found; code-review; pr-create	All bugs fixed
Done	Release execution	Released	Scrum master marks work complete	None	Released; outcomes measured
Column names versus ADO state names
The columns above are the process view Janna maintains. The exact ADO work item states behind each column, and whether a column maps to one state or several, are being written down as part of the process map clean-up. Until that lands, treat the columns as the authoritative vocabulary and check the board for the state names your team uses.
Feature, spec and PBIs: the model

One Feature, one frame, one spec, many PBIs
The Feature is the unit of scope and of specification. The frame and the spec both attach to it.
The spec lives on the Feature record: Acceptance Criteria holds the build-ready sections; Description holds the human-reference sections. Both fields are owned by the spec skill and overwritten on each write. Dev and QE notes go in Discussion comments.
Every Feature gets one default child PBI at first write: a thin reference titled after the Feature, no spec content of its own. This is what dev picks up.
Additional PBIs are created as the team agrees the carve-up, each a thin reference to the spec sections it implements, parented to the Feature, in the Feature's swimlane, defaulting to the Feature's target release iteration, effort blank until the team estimates, state New.
Naming: [Feature Name] - [Scope descriptor]. Spikes: [Feature Name] - Spike: [topic] (an investigation-only PBI; the title convention is a proposed default, confirm against your team's practice).
Story splits and delta PBIs share the same frame and spec. A materially different problem or new personas means a new Feature, new frame, new spec.
Field-level facts engineers and QE need
Acceptance Criteria field: Microsoft.VSTS.Common.AcceptanceCriteria.
Description field as rendered on Deltek's template: Microsoft.VSTS.Common.DescriptionHtml. The generic description parameter writes System.Description, which the form does not render; the write succeeds silently and the item looks empty. Every skill that writes descriptions targets DescriptionHtml explicitly and reads back to verify.
Content is authored in markdown and converted to HTML: headings, lists, tables, bold, strikethrough as <s>, the [OPEN] tag as bold red, dated markers in blue.
Opt-In features need two follow-up PBIs (Hide/Enable, Remove) created by the PDM by hand for now.
Bugs link to their PBI with an Affects relationship. Test cases link to the work item they verify.
Links and sync rules

LINK	DIRECTION AND RULE	MAINTAINED BY
Aha Feature to ADO Feature	Bidirectional sync creates the ADO Feature. Feature Name flows Aha to ADO. Description never flows Aha to ADO once a spec exists (it would destroy the spec).	The Aha integration; verified by the spec skill
Aha Integrations field	Holds the link to the ADO Feature. Checked every spec session; set or corrected on your confirmation.	capability-spec via deltek-aha-lookup
ADO Feature to Aha description	The User Story mirrors to the top of Aha's description (idempotent). Other content reconciles Replace, Keep or Append; never a silent overwrite. Remaining field list still being confirmed.	capability-spec via deltek-aha-lookup
Aha Feature to Notion frame	Aha description carries the Notion URL. Notion page carries the Aha Feature # (the key) and the Aha link. Notion title always mirrors the live Aha name.	framing via deltek-notion-frame-home and deltek-aha-lookup
Notion frame to ADO Feature	ADO Feature # and link stored as properties on the frame page when known. The spec inherits the frame's content one way; at close it writes the resolution section back.	framing; capability-spec
PBI to spec	PBI Description names the parent Feature's spec and the sections it implements. Listed in the Feature's Feature References and Related Work Items.	capability-spec
PBI to plan	Research Findings and Technical Plan attached to the PBI.	tech-plan (developer)
Bug to PBI	Affects relationship for bugs found while testing a PBI.	bug-create
Statuses, and who moves what

AHA FEATURE WORKFLOW (VP2, CUSTOMIZED)
New, Approved, Committed, Done, Released, Rejected
Framing proceeds for New, Approved, Committed
At framing close the PDM chooses whether to change status and to which; the skill never picks
Planned: a "Framed" status set automatically at close
Moved by: PDM, through propose, confirm, write-back
NOTION FRAME STATUS (DESIGNED, NOT ADDED)
Draft, Under Review, Approved, In Exploring, Complete
Framing would set Under Review at close; PDM flips to Approved after sign-off; the Bridge would set In Exploring; spec close sets Complete
Today: signal review status the way your team agrees until the property exists
ADO BOARD
Framing, Feature Review, Requirements Collab, Ready for Dev, In Dev, In PR, In Testing, In Bug Fixing, Done
Iteration path assigned at PBI creation (Feature's target release by default)
Feature swimlane groups the PBIs
Moved by (typical, confirm on your team): PDM through Framing, Feature Review and Requirements Collab; developer into In Dev and In PR; QE into In Testing and In Bug Fixing; the scrum master marks Done. The only owners stated in the process records are the PDM for Framing and the scrum master for Done.
Living-document conventions on the spec

[OPEN] for anything unresolved, tag bold red caps, note text normal. Kept even at Done when deferral is intentional.
Strikethrough preserves reverted decisions. Never delete a struck bullet.
Blue dated marker (updated MM/DD/YYYY initials) at each change point.
Update Summary at the top of Description: one dated line per type of change.
"No new work for us" marks requirements that ride on existing framework so dev does not estimate them.
Team Follow-ups are transient: as each resolves it leaves the table and its result shows up in the spec section it affected, or as a PBI.
UPDATE SUMMARY, GOOD AND BAD
Good: "Removed real-time updates decision; clarified overnight generation via Refresh Project Summary Tables."
Good: "Updated multiple bullets in the iButton text."
Bad: five lines for five iButton edits. Bad: one line saying "changes made".
Notifications are manual for now. The audit block marks who needs telling with NOTIFICATION NEEDED; the PDM sends. A discussion comment on the Feature that tags stakeholders is the planned mechanism.
How work gets seen at the right time

MECHANISM	WHERE	PURPOSE
Aha workflow status	Aha	Signals the Feature's position in the product workflow
Notion Framing Documents views	Notion	Frames pending review, once the Status property exists
Iteration path (for example Vantagepoint\2026.4\Team 2\Sprint 3)	ADO	Sprint assignment; visible on team boards
Feature swimlane (emoji prefix plus Feature name)	ADO Kanban	Groups the PBIs under their Feature
Board columns	ADO	Standard work-tracking transitions; bottleneck visibility in Ready for Dev
ADO Discussion comments	ADO	Dev and QE notes on the Feature or PBI; planned home for stakeholder-tagged change notices
Agentic AI Teams channel (Vantagepoint space)	Teams	Announcements, rollout instructions, questions and support
Why the frame and the spec live in different tools
Dev, QE and storytime already live in ADO; forcing spec review into Notion adds friction. Framing stays in Notion because the frame reads better there and PDMs review it there. The team has agreed to revisit co-locating frames with the code repo later; for now, the Notion database is a review artifact, not just storage.
Knowledge check
3 questions

Where does a developer add a persistent note about the spec?
In the Feature's Description field
In an ADO Discussion comment; AC and Description are owned by the spec skill and overwritten
In the Notion frame
What happens in the Ready for Dev column?
The technical plan is written
Nothing; it is a queue that makes bottlenecks visible
The feature review
Which direction never syncs?
Feature Name from Aha to ADO
Description from Aha to ADO once a spec exists
User Story from ADO to Aha
Mark Module 3 complete
MODULE 4
Rate Table, end to end
30 minutes · everyone
"Add Rate Table Status Field" was picked on 23 June as the first feature to run the whole process. It is small, it touches server, client, database, three lookups, search and the public API, and it had a three-year-old ADO decomposition to reconcile. What follows is the real record: the Aha feature and idea, the frame written on 7 July, the research findings and technical plan written on 16 July, and the end-to-end run on 17 July. Read the artifacts, then the "what to notice" note under each one.
Timeline

2022-05-11
Idea VP2-I-2492 "Inactivate old rate tables"
Submitted by Craig Miller (Synterra Corp). "We should be able to mark old rate tables inactive, so they can't be used on current projects. This creates billing issues since Project Managers choose the wrong rate table and have lower billing rates than should be." It gathered roughly 538 votes and endorsements.
2023-05-11
Feature VP2-445 "Add Rate Table Status Field"
Created by Judith Murphy: "Users would like a Status field added to rate tables so that these tables could be marked Active, Inactive or Dormant. Impacts of each status should mirror those assigned to Unit Tables." Synced to ADO Feature 1953408 on 2023-06-20, later decomposed into five PBIs (effort 26) assuming three tiers.
2026-06-23
Selected as the first end-to-end POC feature
Chosen to exercise UI plus the full process. Owners: Hardik Shah, Jessica Abiles, Melissa Coffey, Dawn Gajewski.
2026-07-07
Framed in Notion (Melissa Coffey)
Two-tier Active/Inactive chosen over three tiers; Current Behavior corrected to the real admin workaround; outcomes grid and competitive research skipped by explicit decision; wireframe produced; seven open questions logged.
2026-07-16
Research findings and technical plan for PBI 2808724 (Jessica Abiles)
Written against main from the capability spec authored on ADO earlier that week. The same day, the team resolved that spec data lives on the ADO Feature, not the PBI.
2026-07-17
Technical plan to code to tests to PR, end to end, for the first time
Server and client code, client unit test, API test and PR ran through the chain; the run validated the pipeline. Confirmed again on 21 July.
Stage 1 · Proposed: the demand record

Aha Feature VP2-445 · Idea VP2-I-2492 · ADO Feature 1953408
Status New · Parking lot, Team 6 · Assigned to Judith Murphy
IDEA, IN THE CUSTOMER'S WORDS
"We should be able to mark old rate tables inactive, so they can't be used on current projects. This creates billing issues since Project Managers choose the wrong rate table and have lower billing rates than should be."
FEATURE DESCRIPTION AS IT STOOD BEFORE FRAMING
"Users would like a 'Status' field added to rate tables so that these tables could be marked Active, Inactive or Dormant. Impacts of each status should mirror those assigned to Unit Tables." Plus a link to a December 2023 Feature Review recording.
What to notice. The feature description encoded a solution (three tiers mirroring Unit Tables) that the customer never asked for. The idea asks for one thing: stop stale tables being selected. Framing caught the difference. Also: the Aha connector could not return the idea's portal comments, and the frame recorded that as a tooling gap rather than concluding there were none.
Stage 2 · Framing: the Frame Artifact

Notion Framing Documents · "Rate Table Status Field Added" · Aha VP2-445 · ADO 1953408
Framed 2026-07-07 · 18 sections
3 · PROBLEM STATEMENT
Billers and PMs need an obvious way to retire a stale rate table so it can't be selected on new billing terms, but today that requires discovering and assembling a two-screen, admin-level workaround that isn't discoverable from the Rate Tables screen itself, so most firms never build it, and stale tables keep getting selected, resulting in either under-billing (if the error isn't caught before the invoice goes out) or delayed billing (if it is caught and must be corrected first).
4 · CURRENT BEHAVIOR (GROUNDED IN HELP CONTENT)
Rate tables have no native status field. Firms can approximate one today via a real, working admin-level mechanism: set the free-text Code property on a rate table, then configure Record Level View on the relevant Security Role to filter out tables carrying that code. Grounded in the "Record Access Tab of the Roles Form" help article, which says Record Level View controls the list of records displayed in search results for lookup fields when working in other applications, so this fully excludes coded tables from that role's lookups everywhere, including Billing Terms. The gap is not capability; it is that the mechanism is not discoverable from the Rate Tables screen, requires stitching a Labels-and-Lists field to a Roles-form security configuration the help content itself calls a system administrator task, and cannot express a graduated warn-but-allow tier.
5 · PROPOSED CHANGE
Add a self-service, table-level Status field (Active / blocked state) directly on rate tables, making the retirement action obvious and immediate rather than requiring an admin-level security workaround. Two-tier, hard block, not three-tier Active/Inactive/Dormant.
7, 8 · COMPETITIVE RESEARCH AND OUTCOMES
Competitive research: not conducted (declined by the PDM). Outcomes grid: skipped; the PDM determined a formal grid is not warranted for a Quick Win, parity-scope fix. Both recorded as decisions, not omissions.
12, 13 · SCOPE IN, SCOPE OUT
In: self-service, table-level Status field on rate tables; selection blocked at Billing Terms and other selection points once a table is marked blocked; status visible and reportable natively. Out: a graduated warn-but-allow tier (Unit Tables style Inactive), explicitly rejected; ADO 1602719 (Active-only filtering on Employee, Vendor and Account lookups within Rate Tables) stays separate; any ADO writes or links during framing.
14 · RELATED CAPABILITIES
ADO Feature 1953408 plus five child PBIs: Overlap, duplication risk, the existing unlinked engineering-side twin, scoped for three tiers, will need re-scoping for two. ADO Feature 1602719: Overlap, collision risk, same screens, adjacent motivation, different mechanism, kept separate.
15 · DECISIONS MADE (SELECTED)
Corrected Current Behavior to reflect the real Code plus Record Level View workaround, reversing an earlier draft that understated its enforcement strength. Retracted two claims ("no reporting visibility", "per-table security maintenance burden") that were wrong per PDM correction.
Reframed the problem from "missing capability" to "discoverability and self-service gap".
Chose two-tier over three-tier: matches the literal customer ask, fits Quick Win sizing, avoids building an unvalidated graduated-warn capability. Revisitable if engineering disagrees at the collaboration stage.
Logged a process-improvement item: the framing and help-lookup skills should ground Current Behavior claims before stating them, not infer from general software patterns.
16 · OPEN QUESTIONS (SELECTED)
Idea comments unretrievable via the connector: tooling gap, not confirmed absence on a 538-vote idea.
Naming for the blocked state must avoid colliding with Unit Tables' "Inactive", which means warn-but-allow there. Needs UX and PDM input.
ADO 1953408's five-PBI breakdown assumed three tiers and needs re-scoping before reuse.
18 · PROTOTYPE DIRECTION
Where does the Active/Inactive toggle live on the Rate Table form, and how obvious is the block at selection time, without requiring security or admin setup? A lo-fi wireframe answering it shows two screens: the Rate Table form with the new self-service Status field, and the Billing Terms rate table lookup with an Inactive table excluded from selection.
What to notice. The frame's most valuable content is a correction. The first draft understated how strong the existing workaround was and the PDM fixed it against the help article; the decision log shows the reversal instead of hiding it. The related-capabilities step found a three-year-old duplicate decomposition before anyone re-estimated it. And the PDM skipped two steps on purpose and said so, which is what a Quick Win should look like in this process.
Stage 3 · Exploring: the capability spec

ADO Feature 1953408 (Acceptance Criteria and Description) · PBI 2808724
Authored July 2026 · Feature-level storage decided 2026-07-16
The spec text is held in ADO and is not reproduced here yet; this panel will carry excerpts of the User Story, Existing Behavior, Requirements, Use Cases and the Design Considerations audit once exported. What the downstream technical plan tells us the spec required:
A Status field on all seven billing rate table types, binary Active (Y) or Inactive (N), default Active, fully independent of the existing AvailableForPlanning checkbox.
Status shown in the list view and on the detail form for all seven types, and searchable and filterable in Find and Advanced Search.
Inactive tables removed from rate table lookups on new selections in Billing Terms, Project Plans and Service Estimates; existing references unaffected; the Rate Tables screen itself shows all statuses.
Status exposed in the public REST API metadata and GET endpoints; opt-in filter, backward compatible.
Out of scope, carried straight from the frame: no graduated warn-but-allow tier; no bundling of ADO 1602719; no relinking or clean-up of the prior five-PBI decomposition; no Status on Cost and Pay rate tables.
Documentation notified to update help articles for all seven table types; release notes copy drafted.
What to notice. Every out-of-scope line in the frame reappears in the spec and then in the technical plan as a "do not implement" guard. That chain is the point. Note also that this feature ran while the storage model was being settled: the spec went to a PBI first and the decision to keep it on the Feature was made the same week. New features start Feature-level.
Stage 4 · Building: research findings and the technical plan

Repo, attached to PBI 2808724 · rate_table_research_findings_2808724.md
Researched 2026-07-16 against main
CODE STRUCTURE, AS FOUND
Server: BaseClass to BaseBO to VisionBaseBO to LaborRateTableBO under code/server/VB/LaborRateTableSetup/Server/, split into RateTableSetup.vb (core), .metadata.vb (GetMetadata) and .query.vb (GetQuery, filter expressions). One BO handles all seven table types (BTEA, BTEC, BTEV, BTRCT, BTRLT, BTROT, BTRRT) through a Table property; each has a detail table for rate lines. RateTableController exposes /vision/Metadata/RateTable/{RateMethod}, /vision/RateTable/{RateMethod} and a public /api/ variant restricted to four labor methods.
Client: one application and one layout serve all seven types (laborRateTableSetup_application.js, _layout.js), type resolved from the RateMethod route parameter; a model per type. Three lookup areas: Billing Terms (direct model.getAll by billing method, currency filter only), Resource Planning (RateTableDropdown, already filters AvailableForPlanning through filterHash), Service Estimates (RateTableDropdown, no filterHash). Advanced Search fields defined in labor_rate_tables_search_fields.js.
DEPENDENCIES, SCHEMA, FLAGS, PERMISSIONS
Framework: VisionBaseBO, QueryRoutines, ParameterizedQueryBuilder, CheckboxField (varchar(1) Y/N to checkbox), BaseBOController, BaseModel, ComponentDefinition, RateTableDropdown. Seven header tables in DeltekVantagepointCreateSchema.sql; no FK constraints from rate tables to projects or billing terms, so Inactive does not cascade. AvailableForPlanning already follows the exact varchar(1) default pattern Status will use. No feature flags gate Status; standard record-level security applies through RateSecurity.
EXISTING TEST COVERAGE
Integration tests exist for basic CRUD and metadata but nothing verifies filterHash behavior; no dedicated BO unit test project; a client test exists for RateTableDropdown but not for filterHash propagation; Nightwatch UI smoke tests exist per table type and are QE's to update post-development.
ANTIPATTERNS AND TECH DEBT, EACH WITH AN IN-SCOPE VERDICT
Inconsistent AvailableForPlanning presence across the seven tables: not in scope; Status is added consistently regardless. Track separately.
No enum for Y/N status values: not in scope; framework convention, not a magic number.
Public API restriction hardcoded to four methods: partially; Status is added to metadata for all seven, the restriction is unchanged.
Vestigial filterHash extraction in GetQuery: no action; the framework's GetOrgFilterExpression is the real mechanism.
No in-use validation before a Status change: not in scope; intentional soft-delete behavior per spec; low risk.
What to notice. This document is what the technical plan skill's mandatory research step produces. Every file path is real, every gap in test coverage is named, and every tech-debt observation ends with an explicit scope verdict so the developer neither fixes the world nor forgets that it was seen. The research also found that one client change covers all seven table types, which changed the plan's size.
Repo, attached to PBI 2808724 · rate_table_technical_plan_2808724.md
Produced by the tech-plan skill · 8 tasks · 4 test layers
OBJECTIVE (SEVEN NUMBERED OUTCOMES) AND USER FLOW
Add Status (varchar(1), default Y) at database, metadata and UI levels for all seven types; show it in list and detail views; make it searchable in Find and Advanced Search; filter Inactive tables from lookups in Billing Terms, Project Plans and Service Estimates via client-passed filterHash; expose it in public API metadata and GET; keep Status and AvailableForPlanning fully independent; update test data. User flow: a biller creates a table Active by default, later marks it Inactive, and from then on it no longer appears in rate table dropdowns for new setup while existing references and the Rate Tables screen are unchanged.
OUT OF SCOPE, AS "DO NOT IMPLEMENT" GUARDS
No three-value Active/Inactive/Dormant tier. No ADO 1602719 work. No relinking of the prior decomposition (Feature 1953408 plus PBIs 588776, 2122055, 2122065, 2122067, 2122068). No Status on Cost and Pay tables (COSTRT, COSTCT, COSTLT).
ENDPOINTS AND DATA CONTRACTS
Metadata GET returns Status as a CheckboxField with default Y for the given RateMethod. GetMany returns Status in the result set and honors an optional filterHash: [{name:"Status", opp:"=", value:"Y"}]; lookups pass the filter, the Rate Tables screen does not.
TASKS A TO H, EACH WITH "EXECUTE WITH"
Database: create the DCR for the Status column on seven tables (ALTER TABLE ... ADD Status varchar(1) DEFAULT ('Y') NOT NULL, after TableName); update the schema script after execution. Standard DCR process; parallel with code.
Server metadata: add CheckboxField("Status", 1) with caption, default Y and Searchable true to all seven cases; add the resource string. Execute with /server-code.
Server query: add Status to the SELECT of all seven header queries; add a Status case to GetOrgFilterExpression so a client filterHash becomes {table}.Status = 'Y'. Do not hardcode a WHERE clause; filtering is client-controlled. Execute with /server-code.
Client UI: add Status to list-view default columns and to the detail form after TableName; add the i18n string. One change covers all seven types. Execute with /client-code.
Billing Terms lookup: add the Status filterHash before the billing-method switch. Execute with /client-code.
Project Plans lookup: add Status to the existing AvailableForPlanning filterHash array on every rate table dropdown; both filters apply. Execute with /client-code.
Service Estimates lookup: add additionalParams with the Status filterHash to each RateTableDropdown; extend the component if it does not pass additionalParams through. Execute with /client-code.
Advanced Search: add Status to the default search result fields. Execute with /client-code.
TESTING, FOUR LAYERS
Server unit tests: none required, with the reason (no dedicated test project; additive metadata and query change) and what they would verify if added. API tests (/api-test RateTableController): metadata returns Status; GetMany returns Status; GetMany honors the Status filter; GetMany without the filter returns all statuses; a regression guard that pre-upgrade calls still work. Client tests: list-view default columns include Status; Billing Terms passes the Status filter; RateTableDropdown propagates the filter. Regression guards: existing references unchanged; AvailableForPlanning independent; print and export unaffected; public API backward compatible.
HOW TO EXECUTE, BEFORE CODING, DEFINITION OF DONE
A twelve-row table maps every task and test layer to its skill and argument, ending with "Verify Definition of Done". Before coding: read the routing file and guides, read the research findings, create and track the DCR, confirm resource keys, verify the line numbers the plan cites (patterns, not guarantees). The Definition of Done has sixteen binary items, from "DCR created" to "release notes copy drafted".
What to notice. The plan is a prompt for a coding agent, not a design document. It says which skill executes each task, pastes snippets exact enough to use, names the enum and field conventions, and turns every out-of-scope line into an instruction. Two things the plan flags as uncertain are flagged as uncertain (verify line numbers; confirm resource keys), which is the no-assumptions rule working.
Repo and ADO · code, tests, PR
2026-07-17 and 2026-07-21
On 17 July the plan was executed through the chain: server code, client code, client unit test, API test and PR, with the review and PR skills. This was the first time the technical-plan-to-PR chain ran end to end for a real feature; it was repeated on 21 July with the updated skills. The PR link and the generated tests will be added to this panel from ADO.
What to notice. The DCR ran in parallel with code, exactly as the plan said it could, and integration tests waited for it, exactly as the plan said they must. Whether a feature "needs a DCR" turned out to matter less than whether the plan sequenced it correctly.
Stages 5 and 6 · Verifying and Released

Rate Table's QE and automation pass, and its release, run through the same skills described in Module 2 and are not yet part of this record. When they complete, the test cases, the Playwright test, any bugs and their RCAs, and the outcome follow-through will be added here so the example is complete through Done.
What the first run taught the team

Delegation beats direct access
Once framing stopped calling Aha, ADO and Notion directly and routed every read and write through the lookup skills, consistency and error handling both improved.
One load-bearing principle beats many rules
The AC versus Description split did more to keep the spec coherent than any amount of formatting guidance.
Propose, confirm, write-back is worth the friction
Slower per write, and the reason nothing has been written to the wrong place.
Real usage surfaces what review cannot
Dev building against a spec surfaced the PBI structure question; a long session surfaced a data-loss bug when placeholder shorthand ("[Unchanged.]") replaced real content on a full-field write. The fix is a rule, a pre-write self-check, and re-reading the record before every write.
Ground before you state
The frame's Current Behavior had to be corrected against a help article. That became an explicit rule in the skills: no claims about today's behavior without a source.
Terminology drift is a real cost
Metadata became Feature References, Preconditions became Existing Behavior, Working Items became Team Follow-ups. Each rename was necessary and each rippled through several documents. Agree names early.
Knowledge check
3 questions

Why did the frame choose two tiers instead of the three tiers in the original feature description?
The customer asked for one thing (stop stale tables being selected); three tiers was an unvalidated solution and did not fit Quick Win sizing
Engineering said three tiers was impossible
Unit Tables were being changed at the same time
What did the research findings do with the five tech-debt observations?
Fixed them all in the same PBI
Gave each an explicit in-scope verdict so it was seen but not silently expanded into the work
Left them out of the plan
How does the frame's "scope out" reach the developer?
It does not; the developer reads the frame
The spec carries it into Out of Scope and the technical plan turns each item into a "do not implement" guard the coding skills hold for the session
Through the PBI title
Mark Module 4 complete
MODULE 5
Role playbooks and labs
20 minutes plus the lab · filtered to your role
One card per role: what changes for you, the phrases you will actually type, the checklist that keeps you out of trouble, your first week, and a lab on a real feature. Print your card and keep it next to you for the first few features.
Print all quick cards Each card also has its own print button.
PDM
Product Development Manager Print this card
WHAT CHANGES FOR YOU
You frame before release planning, alone with Claude, from an Aha Feature.
You write the first-draft capability spec before the Feature Review and bring it instead of a deck.
Between meetings you feed the transcript to the skill and accept, edit or reject its proposals.
You disposition every consideration and outcome, and the audit block proves it.
The team decides the carve-up in the room; the skill creates the PBIs on your confirmation.
You send the notifications the audit block flags, and you close the spec when the gates pass.
WHAT YOU SAY (CLAUDE DESKTOP, AFTER /DVP)
check connectors
let's frame VP2-1234
generate wireframe
start capability spec for VP2-1234
update the spec for VP2-1234 based on these notes
walk considerations for VP2-1234
update the use cases for VP2-1234
prep for next meeting on VP2-1234
close the spec for VP2-1234
what's the status of feature VP2-1234
BEFORE THE FEATURE REVIEW
Frame written to Notion and read by product leadership
Aha description carries the summary and the Notion link
First-draft spec on the ADO Feature; default child PBI exists
Aha Integrations field points at the ADO Feature
Your own pre-think of anticipated PBIs and considerations (the Bridge is not built)
Someone is capturing a transcript or notes
BEFORE YOU CLOSE
Every consideration and outcome has a disposition
Follow-ups resolved, deferred with reason, or converted to PBIs
Every [OPEN] resolved, spikes have their PBI
NOTIFICATION NEEDED items sent
Aha status chosen; frame status signaled
YOUR FIRST WEEK
Install the plugin, connect Aha, ADO, Notion and M365, run the connector check.
Frame one 2027.2 feature you own. Correct Current Behavior against the help content Claude cites.
Start its capability spec; leave open items open.
Bring frame and draft to the Feature Review; capture the record.
Process the record; walk considerations; prep the next meeting.
Log every bug, friction point and idea in the feedback log.
LAB
Run one 2027.2 feature through Framing and Capability Spec end to end, up to the first Mode b pass. Bring the Update Summary and the considerations audit block to your team's retro.
PDM questions the team has already answered
DEV
Developer Print this card
WHAT CHANGES FOR YOU
You are in the Feature Review and Requirements Collab; the carve-up and the spikes are yours to shape.
Every PBI starts with a technical plan built against the real code. You answer three to five questions; the skill does the research.
You execute the plan with skills that load the framework rules first and hold the plan's guards for the whole session.
Tests at three layers are generated, not deferred. The review runs before the PR, and again after changes.
Bugs go through the same chain with the bug as input.
Claude Code is the preferred door; Copilot only where the QE agents live.
WHAT YOU TYPE (CLAUDE CODE, REPO OPEN)
/tech-plan 2808724
/server-code code/server/VB/<App>/Server/<File>.vb
/client-code <app-name>
/server-unit-test <ClassName>
/client-unit-test
/api-test <Controller>
/performance-analysis <query or area>
/code-review
/pr-create 2808724
Or describe the task and let the deltek-developer agent sequence the chain.
PER PBI CHECKLIST
Spec finalized on the Feature; dev plan finalized
Technical plan and research findings attached to the PBI
All plan questions answered; every NOT FOUND resolved or accepted
DCR created and tracked if the schema changes
Out-of-scope guards honored; regression guards verified
Unit, API and client tests present or explicitly not required with a reason
Review verdict CLEAN, or every Warning judged
PR linked to the work item; Definition of Done binary-complete
YOUR FIRST WEEK
Pull the repo; confirm the skills and the agent resolve in Claude Code; confirm ADO tools resolve.
Check whether agentic_ai/apps/ has a context file for your area; if not, have one created.
Run /tech-plan on one small PBI with a finished spec. Answer the questions honestly.
Execute one task with /server-code or /client-code; generate its tests.
Run /code-review on the branch; read the report before fixing anything.
LAB
One PBI: plan, one task, its tests, the review. Compare the plan's file references with what you would have looked up by hand, and note where it saved time and where it was wrong.
Developer questions
QE
Quality Engineer Print this card
WHAT CHANGES FOR YOU
You are in the room from Feature Review on; the spec's Use Cases are written to be testable and you help make them so.
Test cases are generated from the PBI in parallel with development, one scenario each, with duplicate detection and your approval before anything is created in TFS.
Bugs, RCA and release-found triage each have a skill with strict field rules; the skill never fills a field it cannot ground.
Release certification templates for M1 to M6 are routed by one skill.
WHAT YOU TYPE (CLAUDE CODE, REPO OPEN)
/test-case-creator 2808724
/bug-create
/bug-rca 1234567
/release-found 1234567
/tc-identify-performance 2808724
/final-certification
In Copilot Chat: the QE TC Author, QE Bug Creator, QE Analyst, QE RF and RCA Investigator and QE Release Certification agents.
TEST CASE CHECKLIST
Output role chosen: manual, automation or hybrid
Duplicates searched by linked item, module and title, area path
One scenario per test case (ScenarioCount = 1)
@DBFlavor set from MasterDBFlavor when a database is named
Navigation and field names verified, never invented
JSON reviewed and approved before creation; linked to the work item
BUG CHECKLIST
All eight inputs provided by you
Five-phase duplicate detection done
Right template; pre-flight checklist passed; JSON approved
Affects link to the PBI; Regression, Blocked, Assigned To and Priority left for humans
YOUR FIRST WEEK
Read one finished spec's Use Cases and Requirements before its Feature Review.
Generate test cases for one PBI; compare against what you would have written.
Log one real bug through the skill.
Run an RCA on one recently closed bug and check every required field landed.
LAB
One PBI with a finished spec: test cases from its use cases, executed against the build, one bug logged, one RCA. Bring the coverage gaps you found back to the PDM as Use Case proposals.
QE questions
AUTO
Automation Engineer Print this card
WHAT CHANGES FOR YOU
Automation starts from stable test cases and working code, not from the PBI title.
The Playwright skill carries the framework's conventions in reference files and reads the matching one in full before every task; so should you.
Four phases: Plan, Resolve, Script, Review and Debug. Enter at the phase the task needs.
Layer discipline: Session, page objects, API objects, business objects, Forge, Localizer, settings. Each owns one thing.
WHAT YOU TYPE
/playwright
automate test case 1234567
create a page object for <area>
debug the test failure
review this e2e test
In Copilot Chat: PW Script Writer, PW Script Reviewer, PW Debugger.
CHECKLIST
Work item fetched; steps decomposed; test type chosen (sanity, CRUD, feature); area path named
Existing page objects, APIs and BOs resolved; missing ones built in order schema, API, page object, test
Every user-visible string through u.i18n(); every created entity torn down through TeardownStack
u.require() pre-conditions first; test.step titles readable as repro steps
Three-agent review run; Mandatory findings fixed
Failures diagnosed from artifacts with an RCA before code changes
YOUR FIRST WEEK
Run the Project Setup reference so tooling is in place.
Write one sanity test for your area following the example.
Trace one page object back to its front-end layout file with the Code Navigation reference.
Review the test with the review reference.
LAB
Automate one stable test case from a finished PBI. Note which framework pieces already existed and which you had to build.
Automation questions
UX
UX Designer Print this card
WHAT CHANGES FOR YOU
A lo-fi wireframe can exist at framing, generated from the frame's Prototype Direction and Vantagepoint UI patterns, before you are asked for design. It is for scope confirmation, not design.
You are in the room for spec authoring on anything with an interface. The spec's Mockups section is Level 1: text descriptions in Acceptance Criteria plus references to your work.
Your in-progress mockups are tracked as Team Follow-ups with a UX owner, so nothing is lost between meetings.
Accessibility, localization and mobile impact are considerations the PDM must disposition; you are the input.
WHAT YOU SAY (CLAUDE DESKTOP)
generate wireframe for VP2-1234
build mockup
how does <screen> work in vantagepoint
Do not use the generic UX persona or "add ui requirements"; they write to a Notion spec that does not exist in the Vantagepoint process.
CHECKLIST
The Prototype Direction question is specific enough to draw
Wireframe stays inside Scope In and shows nothing from Scope Out
Three criteria met: answers the question, within scope, surfaces the decision without solving it
Mockup references added to the spec; follow-ups carry UX (Name)
Naming collisions with existing Vantagepoint states raised early (Rate Table's "Inactive" versus Unit Tables)
YOUR FIRST WEEK
Iterate one framing wireframe with a PDM.
Sit in one spec session and write the Level 1 mockup text for one screen.
Log what a Level 2 mockup skill would need to produce for you.
LAB
For one 2027.2 feature: review the wireframe against the three criteria, then author the Mockups section text and references in the spec with the PDM.
UX questions
SM
Scrum Master and Team Owner Print this card
WHAT CHANGES FOR YOU
Two pre-release columns, Framing and Feature Review, sit to the left of the board; Requirements Collab is new inside the release.
Ready for Dev is a queue with no tasks; your job is to see what stalls there and why.
PBIs are thin references to a spec on the Feature; the spec and the dev plan must be final before a card enters In Dev.
Team Owners ensure code reviews happen and approvals are fast; the review skill report is your friend.
You mark Done.
WHAT YOU SAY (CLAUDE DESKTOP)
what's the status of feature 1953408
find the work item
check Aha for VP2-1234
open the frame for VP2-1234
PER FEATURE CHECKLIST
Frame exists in Notion; Aha description links it
Spec on the Feature; default PBI plus agreed PBIs in the swimlane with iteration paths
Estimates on PBIs; spikes have their own PBIs; Opt-In follow-up PBIs created
Dev plan finalized before Ready for Dev
PR review turnaround inside the team's target
Done criteria met before you mark Done
YOUR FIRST WEEK
Map one feature's cards to the nine columns.
Check what is sitting in Ready for Dev and why.
Agree the PR review expectation with your Team Owner.
Confirm who moves cards between which columns on your team.
LAB
Walk one feature from Feature Review to In PR on the board with the artifacts open next to it. Note every point where the card moved without its artifact being ready.
Scrum Master questions
Mark Module 5 complete
MODULE 6
Reference
Keep open while you work
Skill catalog

Every skill in the operating system, where it runs, what you say, what it reads and writes, and its status on 21 September 2026. Names differ slightly between the plugin and the repo where noted (the repo name is what you type in Claude Code). Use the filter to narrow by role or stage.
Filter by stage
Filter by door
Filter by status
SKILL	STAGE	RUNS IN	SAY	READS	WRITES	STATUS
connector-check
Run first. Names each of Aha, ADO/TFS, Notion, M365 as Live or Missing and which skills are ready.
Any	Claude Desktop	check connectors	Tools available in the session	Nothing	Live
framing
v2.8, locked. Eight steps, 18-section artifact.
Framing	Claude Desktop	let's frame VP2-1234 frame this feature start framing generate frame brief	Aha feature and ideas, ADO wiki, help content (via lookups)	Notion frame page; Aha description and back-link; optional status change	Live
pm-outcome-grid-builder
Nine elements. Embedded mode inherits 1, 7 and 8; interrogates 2 to 6 and 9. Hypothesis grade.
Framing	Claude Desktop	build the outcome grid review my outcome grid build the outcomes for this feature	The frame's problem statement, evidence, competitive read	Outcomes section of the frame (via framing)	Live
vantagepoint-mockup
Level 1, scope confirmation. Level 2 (embedded in the spec) not built.
Framing	Claude Desktop	generate wireframe build mockup wireframe this feature	Frame sections 1, 3, 4, 5, 12, 13, 18; bundled UI patterns	One self-contained lo-fi HTML wireframe	Live
capability-spec
v1. Five modes. Decision of record: Feature-level storage. Check your installed version writes to the Feature, not a PBI.
Exploring	Claude Desktop	start capability spec for VP2-1234 update the spec for VP2-1234 based on these notes walk considerations for VP2-1234 prep for next meeting on VP2-1234 close the spec for VP2-1234	Frame (Notion), Aha feature, ADO Feature AC and Description, help content	ADO Feature AC and Description; default child PBI and additional PBIs; Aha Integrations link and User Story mirror; frame resolution section at close	Live
deltek-aha-lookup
Reads the ideas association explicitly. Keeps PDM and PM distinct.
Any	Claude Desktop	check Aha what's the status of feature VP2-1234 find the idea about ...	Ideas, features, epics, initiatives, releases, votes, orgs	Feature description, status, Integrations field (propose, confirm, write-back)	Live
deltek-azure-devops-lookup
Knows the DescriptionHtml pitfall and reads back to verify.
Any	Claude Desktop	check ADO find the work item what's the status of feature 1953408 look in the ADO wiki	Work items, boards, queries, wiki	Feature AC and DescriptionHtml, PBIs (on behalf of the spec skill)	Live
deltek-notion-frame-home
v3. Find-or-update; read frame body; append or update a named section.
Framing	Claude Desktop	save the frame to Notion open the frame for this feature where's the framing doc	Framing Documents database by Aha Feature #	The one frame page per feature; a single named section on request	Live
vantagepoint-help-lookup
Ignores personal OneDrive copies. Reads the full article before answering. Needs Microsoft 365.
Any	Claude Desktop	how does <X> work in vantagepoint look up vantagepoint help for <X>	Help content on the ProductResearch SharePoint site only	Nothing	Live
repo-native
Asks before preferring a repo skill over a bundled one. Refresh the catalog from your checkout once per session.
Any	Claude Desktop	use the repo's own skill what skills does the repo have	A catalog of the Vantagepoint repo's .claude and .github skills	Nothing in the repo	Live
domain-context-bootstrap
Seven gated phases with two human gates; maturity L0 to L4. Team owners run Saurendu's interactive domain and subdomain skill for their domain.
Any	Claude Desktop	bootstrap a domain build the context map for <domain> context bootstrap status	Product repo, work items	KnowledgeBase artifacts in the product repo, never the plugin	Live
tech-plan
Mandatory 3 to 5 questions; mandatory codebase research; NOT FOUND instead of guesses.
Building	Claude Code	/tech-plan <PBI> create a technical plan turn the spec into a technical plan	Spec (attached, PBI or Feature fields, or linked item); agentic_ai routing and rules; the codebase	Technical Plan (and Research Findings) attached to the PBI	Live in repo
server-code
Holds out-of-scope and regression guards for the session. Builds with the solution filter.
Building	Claude Code	/server-code <app, class or file> add a server feature fix the server bug	Plan guards; agentic_ai/framework/server.md; server rules; app context	C# and VB.NET under code/server/VB/	Live in repo
client-code
Step 5 checks whether a client test is required.
Building	Claude Code	/client-code <app or file> add a client feature fix the frontend bug	Plan guards; agentic_ai/framework/client.md; client rules; app context	JavaScript under code/client/DeltekNavigator/Web/src/; Karma/Jasmine tests when needed	Live in repo
server-unit-test (dvp: vp-unittest)
Audits raw string literal alignment; adds --Class-Member prefixes.
Building	Claude Code	/server-unit-test <ClassName> write vp unit tests add xUnit tests for this class	Class and partials; test project structure	xUnit tests with FluentAssertions and Moq; SQL comment prefixes in source where missing	Live in repo
client-unit-test
Repo only; not bundled in the plugin.
Building	Claude Code	/client-unit-test write client unit tests	Client component, model, layout	Karma/Jasmine tests beside the source	Live in repo
api-test
Unit test versus API test decided first. DbMock.Verify after mocked DB calls.
Building	Claude Code	/api-test <Controller or endpoint> write api tests add integration tests	Server testing rules and reference; app context	Integration tests using TestHarness	Live in repo
performance-analysis
Actual execution plans, not estimated. Verify logical reads decreased.
Building	Claude Code	/performance-analysis <query or area> diagnose a slow query investigate a deadlock	Query performance and deadlock guides; server rules	Fix proposals and code	Live in repo
code-review (dvp: vp-review)
Eight specialist agents in parallel. Human approval remains mandatory.
Building	Claude Code	/code-review review my changes check my branch before merging	Changed .cs, .vb, .js files on the branch; agentic_ai/reviews/*	A unified report with a verdict	Live in repo
pr-create (dvp: vp-pr-create)
Follows the PR guide exactly, including the fallback.
Building	Claude Code	/pr-create <work item> create a PR open a pull request	agentic_ai/PullRequest.md	An ADO pull request linked to the work item	Live in repo
vp-create-app-context
Bundled in the plugin; run it in the repo. Ask for the TFS area path when prompted.
Building	Claude Code	create an app context for <app>	Client and server directories, controllers, tables, manifest	agentic_ai/apps/<app>.md, a UI test stub, the apps INDEX	Live
deltek-developer (agent)
Shipped 16 September. Exact step list confirmed in the repo.
Building	Claude Code	Describe the PBI work; the agent sequences the chain	The skills above	Plan, code, tests, review, PR through the skills	Live in repo
test-case-creator (dvp: vp-tc-create)
One scenario per TC. @DBFlavor mandatory.
Verifying	Claude Code	/test-case-creator <PBI, Bug or TC> create a test case generate test cases	AI Test Case Generation Guide; the work item; TFS for duplicates	Test cases in TFS after JSON approval	Live in repo
qe-tc-generation · qe-bug-tc-generation · qe-tc-review
Repo only. QE-lead guidance decides when to use these versus test-case-creator.
Verifying	Claude Code	per the QE guides	QE guides	Test cases and reviews	Live in repo
playwright
Four phases. Reads the matching reference in full before acting.
Verifying	Claude Code	/playwright write a playwright test automate this test case debug the test failure	Bundled references (test scripts, page objects, APIs, test data, i18n, config, navigation, debug, review, setup)	Tests, page objects, API and BO classes under tests/qe/web/playwright/	Live in repo
PW Script Writer · PW Script Reviewer · PW Debugger (agents)
Copilot agents in .github/agents. Reference format to Claude.
Verifying	Copilot	Pick the agent in Copilot Chat	Playwright framework and instructions	Tests, reviews, failure investigations	Live in repo
bug-create (dvp: vp-bug-create)
Eight inputs from you; never sets Regression, Blocked, Assigned To, Priority.
Verifying	Claude Code	/bug-create log a bug file a bug	Bug creation overview and templates; TFS for duplicates	A bug in TFS after JSON approval, linked to the PBI	Live in repo
bug-rca (dvp: vp-bug-rca)
Mandatory TC research before classification. Values only from the mapping files.
Verifying	Claude Code	/bug-rca <Bug> root cause analysis fill in QE RCA notes	RCA guide; four mapping files; the bug; TFS test cases	Defect migration, subcategory and QE RCA Notes fields in TFS	Live in repo
release-found (dvp: release-coverage)
New, regression or pre-existing; introducing PR; blast radius; Breaking Change flag.
Verifying	Claude Code	/release-found <Bug> which PR introduced this assess the blast radius	Release-found investigation guide; the bug; PRs	Triage output; bug updates when warranted	Live in repo
tc-identify-performance
P1 to P3 by blast radius.
Verifying	Claude Code	/tc-identify-performance <PBI or Bug> what tests verify this performance fix	Feature regression testing analysis guide; linked TCs	Prioritized TC list and new TC drafts	Live in repo
final-certification
M1 to M6 routing. Runs in Copilot Chat today.
Verifying	Copilot	/final-certification M2 2026.3 Vantagepoint\Accounting	Certification templates per milestone; CSV exports; the joined PR export	Analysis and recommendations (GO or NO-GO at M6)	Live in repo
QE Analyst · QE Bug Creator · QE TC Author · QE RF and RCA Investigator · QE Release Certification · SQL Performance Analyst (agents)
Copilot agents in .github/agents. Claude equivalents exist for TC creation, bug creation and RCA.
Verifying	Copilot	Pick the agent in Copilot Chat	QE guides and instructions	Per agent	Live in repo
pm · ux · developer · qa · autotester (personas)
Describe an older generic chain. Invoke the Vantagepoint skills by name instead. Files being rewritten.
Any	Claude Desktop	(the /dvp menu)			Retire for VP
gather-context · ux-frame · code-generator · test-author · auto-test
Use framing and capability-spec; the spec session with UX; tech-plan plus server-code and client-code; test-case-creator; playwright.
Any	Claude Desktop	do not use for Vantagepoint		Notion specs, GitHub PRs, tests/automated (not the Vantagepoint systems)	Retire for VP
Bridge
PDM pre-thinks the breakdown by hand.
Exploring	Claude Desktop	(not available)		Proposed Work Breakdown and Considerations for Exploring on the frame	Not built
Feature dev plan and PBI breakdown skill
Being defined; owner to be named. Team authors the plan today.
Exploring	Claude Desktop	(not available)		PBIs and estimates	Not built
Release notes (RelNotesDescription) skill
PDM drafts by hand today.
Any	Claude Desktop	(not available)		Customer-facing release notes field	Not built
Glossary

AC / Acceptance Criteria. The ADO Feature field holding the build-ready spec sections. What AI, dev and QE build and test from.
Aha Feature (VP2-####). The unit of scope and of specification. Synced to an ADO Feature.
Ask Dela / Dela. Deltek's AI assistant. Public APIs must be made available to it; private APIs optionally.
Bridge. Designed skill that would append a Proposed Work Breakdown and Considerations for Exploring to the frame. Not built.
Capability Spec. The implementation contract for a Feature, on the ADO Feature's AC and Description fields. One per Feature.
Considerations / Disposition. The roughly 30-item PDM checklist walked at spec time; each item gets one disposition: Yes in spec, Yes new PBI, Yes existing PBI, No with reason, Deferred.
DCR. Database change request; the standard process for schema changes, run in parallel with code.
Default child PBI. The one thin PBI created automatically with the spec; what dev picks up.
Description. The ADO Feature field holding human-reference spec sections. Rendered from DescriptionHtml, not System.Description.
dvp. Deltek Vantagepoint AI, the Claude Desktop plugin. Type /dvp.
Enable Mechanism. How a feature is activated: new Opt-In (formal three-release rollout, two for tech debt), new Setting, new Security permission, or none.
Exploring. Stage 3. On the board: Feature Review then Requirements Collab.
Feature Dev Plan. How the feature breaks into PBIs, with estimates. Team-authored today.
Frame / Frame Artifact. The 18-section scope contract in Notion, one page per Feature.
High-Value Org. A voting organization with more than 3,000 employees or more than $1M revenue, flagged during framing.
KnowledgeBase / context map. The domain evidence layer (work items, help, code references) skills read; the plugin ships the protocol, the repo holds the data.
L1 / L2 / L3. Scan levels: indexes, full records, live source. Pick before retrieving; escalate only when needed.
[OPEN]. Inline marker for anything unresolved in the spec.
Outcome grid. The nine-element customer outcome grid built during framing at hypothesis grade.
PBI. Product Backlog Item in ADO; the unit of implementation work; a thin slice of the spec.
PDM. Product Development Manager, the product management team. Not PM.
PM. Project manager: the customer persona, and a separate internal delivery role. Never the PDM team.
Propose, confirm, write-back. The write discipline in every skill.
Related capabilities. Framing's Dependency, Overlap and Replacement classification of related features and work items.
Repo-Native. The plugin persona that discovers and uses the Vantagepoint repo's own skills.
Research Findings / Technical Plan. The two per-PBI documents the tech-plan step produces: what the code is today, and exactly how to change it.
Spike. An investigation PBI; [SPIKE-#] marks the requirement waiting on it, [DEPENDS ON SPIKE-#] marks dependents.
Team Follow-ups. The spec's table of in-flight work during Exploring (formerly Working Items).
Team Owner. The engineering lead accountable for a scrum team's reviews and approvals; near-mandatory in spec authoring.
Use case (UC-#). A testable scenario in the spec: actor, preconditions, trigger, flows, outcomes, post-conditions.
Not built yet, and open decisions

Everything here is intentionally tabled or genuinely undecided, not forgotten. Each item has an owner or a tracker entry. The camp says what is manual today wherever one of these touches a step.
ITEM	STATE	WHAT YOU DO TODAY	WHERE IT IS TRACKED
Feature dev plan and PBI breakdown skill (including estimation)	Not built owner to be named	Team authors the plan and estimates in Feature Review and Requirements Collab	AI-SDLC Decisions and Actions; 10 Sep decisions
Bridge skill	Not built	PDM pre-thinks anticipated PBIs; considerations pass covers the rest	Process doc §5; punch list 32
PBI splitting as its own skill; carve-up by use case or requirement	Under consideration; second POC planned	Team decides; spec skill records; [POTENTIAL PBI-#] marks candidates	MVP tabled items tracker
Atomic update (inline markers, Update Summary, ADO @-mention in one write)	v0.2	Skill overwrites fields with re-read protection; PDM notifies by hand	Punch list 23
Auto-drafted external notifications (Cloud, Gainsight, Transfer Settings, Cubes, Doc ID)	v0.2	NOTIFICATION NEEDED in the audit block; PDM sends	Punch list 29
Opt-In follow-up PBIs (Hide/Enable, Remove) auto-created	v0.2	PDM creates the two PBIs by hand	Punch list 28
State-transition scaffolding cleanup; story-split and delta PBIs; red-text convention	v0.2	Manual	Punch list 24, 27, 30, 31
Level 2 mockups (Alex's mockup skill callable from the spec)	v0.2+	Level 1 text descriptions plus references	Tracker; owner Alex
UX skills and synthetic personas placement	Open	Wireframe at framing; UX in the spec session	PDM AI-DLC Guidance; owners Dawn and Alex
Release notes (RelNotesDescription) skill	Later	PDM drafts release notes copy	Process doc §12 item 6
Notion frame Status property; Aha "Framed" status	Designed	Team signal for review; PDM picks the Aha status at close	Punch list 14, 15; framing v2.8 notes
Public API to Ask Dela requirement content	Blocked on Brent's spec	Skill writes an [OPEN] placeholder requirement and flags Brent	Tracker
Considerations list sync with the SharePoint canonical document	Manual discipline	Skill owner updates the hardcoded list when the doc changes	Design outline
Technical capability spec guidance (which technical feature types, steps, examples)	In progress, Hardik and Jessica	Functional features use the spec as-is; ask before a technical one	17 Sep rollout actions
Developer agent step list confirmed for training	Shipped 16 Sep; to be confirmed here	Use the agent or the slash commands	Repo .claude/agents
QE involvement model, automation trigger, manual versus automated cadence	Open, Dev and QE	Automate only against working code and stable test cases	11 Sep decisions
Meeting transcript storage, taxonomy and sync skill	Design agreed; Bret owns the sync skill	Upload the transcript to the spec skill by hand	17 Sep rollout actions
ADO state names behind the board columns; transition owners	Being written	Columns are the vocabulary; check your board	Janna's process map
Plugin distribution: GitHub-synced marketplace versus manual upload	Manual upload in use; admin rights pending	Install from the Teams channel file; updates announced there	17 Sep rollout actions
Persona files in the plugin still describe the generic chain	To be rewritten	Invoke skills by name	This camp's source analysis
Frames in Notion versus co-located with the code repo	Deferred; revisit later	Notion	17 Sep decisions
Relationship to the corporate AI-DLC framework	Under evaluation; benchmark pending	dvp is the Vantagepoint operating system today	Leadership
2027.2 end-to-end adoption expectation	To be stated by Bret	Every PDM runs at least one 2027.2 feature through Framing and Capability Spec now	AEPS P&T leadership
Support and feedback

ASK AND ANNOUNCE
Agentic AI Teams channel
In the Vantagepoint space. Rollout instructions, install files, questions and support all live here. No new channel.
LOG IT, DO NOT JUST MENTION IT
PDM Skill Feedback and Enhancement Log
Notion database for bugs, challenges, enhancement ideas and open questions on the Product-side skills. Title, your name, skill, type, description; Aha # and priority optional. Dawn reviews and updates status.
Open the log
WHO OWNS WHAT
Framing and Capability Spec skills: Dawn Gajewski
Engineering and QE skills, developer agent: Jessica Abiles
Plugin, KnowledgeBase, connectors and MCP: Saurendu Chakraborty
Process map and trackers: Janna Courter
Engineering direction and the enablement camp: Hardik Shah
Product direction: Melissa Coffey
Executive sponsor: Bret Tushaus
Sources and versions

This camp was built from: the AI-SDLC Framing to Exploring process document v0.8; the Capability Spec design outline v0.5, punch list v0.6, smoke test guide v0.3 and MVP tabled items tracker v1.2; the Framing Skills Registry v0.8; the Vantagepoint PM project instructions v1.5 (retired setup model); the dvp plugin repository at v0.8.0 (every skill, the router, the context map, the Copilot pack); the PM walkthrough deck of 17 September; the Work Items Flow Diagram and the framing mind map; the Rate Table research findings and technical plan for PBI 2808724; the live Aha record for VP2-445 and VP2-I-2492; the Rate Table frame in Notion; the PDM AI-DLC Guidance page and the AI-DLC Quick-Start Guide for PDM v1; and the rollout, process-mapping and status records of 10, 11, 17 and 18 September 2026.
Vantagepoint AI-SDLC Camp · v1 · published 21 September 2026 · Readiness and the Not-built register are dated and should be updated by the owners above when something ships.