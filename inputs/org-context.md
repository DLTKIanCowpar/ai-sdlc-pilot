# Organization Context

Source: Copilot research via company directory, AI-SDLC check-in meeting chat, Teams channels,
and adoption status slide shared by Lisa Rabideau (9 Oct 2026). Researched October 2026.

Both organizations report to Bret Tushaus (VP, Product Management), who reports to
Dinakar Hituvalli (EVP, CPTO).

---

## Organization 1: Vantagepoint

### Leadership
- Engineering: Hardik Shah, VP Engineering
- Product: Melissa Coffey, Sr Dir Product Management (directs: Ed Zanaty, Dawn Gajewski, Brent Johnson)

### Headcount
- Engineering: 218 (includes 85 contractors)
- Product management: 14
- **Total: ~232**
- UX and scrum masters not counted (UX likely sits in Lisa Rabideau's org — unconfirmed)

### Structure (Hardik's directs)
- June Cruzate, Dir Engineering (Philippines): 117 people, all 85 contractors, 4 senior managers
- Andy Woodcock-Squires, Dir Engineering: 29 people
- Shirley Tang, Sr Dir Engineering: 24 people
- Sherelyn Natividad, Dir QC Engineering: 22 people
- Jessica Abiles, Dir Engineering: 14 people (also owns engineering and QE AI skills)

### Role Mix
- Engineering: 52 software engineers, 39 QE, 19 architects, 12 engineering leaders, 8 help desk
- Contractors: 85 (titles say "Contractor" only — roles unknown)
- Product management: 14

### Locations
- Philippines: 75; India: 22; US remote: 23
- Contractors: ~47 Asia, ~36 US

### AI Maturity
- **Status:** 50% per Lisa's adoption slide ("building and piloting live")
- Pilot org — owns and built the AI-SDLC framework
- Tooling in use: dvp plugin in Claude Desktop (Product/UX), Claude Code skills in Vantagepoint repo (Engineering), Copilot for QE agents
- Engineering skills live in repo from 16 Sep 2026
- Note: slide percentages are reported to Roper and are directional; treat as external-facing signal

### Prior Enablement
- Working team and reviewers have used camp v1
- Melissa's team planned plugin install and initial training (confirmed in earlier check-in)
- No formal training found for wider engineering org

### Adoption Risks
- **Contractor tool access (HIGH):** Whether 85 contractors are licensed for Claude or the dvp plugin is unconfirmed — potentially the largest single access gap
- **Token and gateway limits:** Blocked testing in September; Saurendu exhausted gateway budget in August; token guidance still listed as a rollout prerequisite as of 15 Oct
- **Setup friction:** Plugin requires manual upload (admin rights pending); Azure DevOps tokens expire
- **KnowledgeBase coverage:** Varies by domain — formal prerequisite for wider engineering rollout
- **Rollout terms undefined:** 2027.2 adoption expectation "to be stated by Bret"; kickoff date and attendance expectations open

### Key Stakeholders
Hardik Shah, Melissa Coffey, June Cruzate (manages contractors), Sherelyn Natividad (QE),
Jessica Abiles, Dawn Gajewski, Saurendu Chakraborty, Janna Courter

---

## Organization 2: Maconomy

### Leadership
- Engineering: Henrik Rosenstand, Sr Dir Engineering (Copenhagen)
- Product: Dan DiStefano, Sr Dir Product Management

### Headcount
- Engineering: 135 (includes 4 contractors)
- Product management: 10
- **Total: ~145**

### Structure (Henrik's directs)
- Mary Joy Deniega, Dir QC: 20 people
- Sigrun Halla Gisladottir, Dir Engineering: 19 people
- Dan Jørgensen, Dir Engineering: 18 people
- Chris Horne, Help Desk: 12 people
- Peter Hemmingsen, Dir Engineering: 11 people
- Anders Hessellund, Dir Engineering: 11 people
- Carla Bervano, Sr Mgr: 10 people
- WorkBook managers: Daniel Lykkegaard, Brent Frialde

### Role Mix
- Engineering: 56 software engineers, 30 QE, 25 architects, 10 help desk, 9 engineering leaders, 4 contractors
- Product management: 10 (Dan DiStefano + 4 Product Directors + Mike Mclean covering WorkBook)

### Locations
- Copenhagen: 54; Philippines: 55; India: 10; scattered Europe and Australia

### AI Maturity
- **Status:** 10% per Lisa's adoption slide ("joins more fully in November")
- Early stage on the AI-SDLC framework; more mature on AI in the product (Maconomy Extender team has integrated AI into Extender, bringing Dela directly into it)
- Grassroots champion: Anders Hessellund gave an internal tech talk on Skills (Aug 2026); noted many skills are still placeholders for Maconomy
- No formal AI-SDLC training found for the org

### Adoption Risks
- **Framework built elsewhere (HIGH):** The framework, KnowledgeBase, and skills were built around Vantagepoint. Maconomy will adopt a framework it didn't design. Slide language: "implementing Vantagepoint framework."
- **Two hubs, two time zones (INFERENCE):** Copenhagen and Philippines split may complicate live session scheduling
- **Leadership stance unknown:** No statement found from Henrik Rosenstand or Dan DiStefano on AI adoption — significant gap
- **Skills placeholders:** Anders noted many Maconomy skills are not yet built out, which affects engineering workflow viability

### Key Stakeholders
Henrik Rosenstand, Dan DiStefano, Mary Joy Deniega (QE), Anders Hessellund (likely champion — unconfirmed), Mike Mclean

---

## Shared Context

### Shared Leadership
- Bret Tushaus leads both orgs. His four direct reports: Hardik Shah, Henrik Rosenstand, Melissa Coffey, Dan DiStefano
- Lisa Rabideau has named AI-SDLC rollout the #1 priority for the enablement team
- Dinakar Hituvalli (EVP, CPTO) is the executive sponsor; Bret describes the ProPricer readout as showing "where Dinakar's interests are and what the expectations are"

### Shared Framework
- Status slide describes the relationship as: Vantagepoint "piloting with Maconomy team riding shotgun"
- Maconomy participants (Anders Hessellund, Mike Mclean) participate in VP AI-SDLC check-in chat
- ProPricer readout debrief was framed for the "VP and Maconomy AI-SDLC Team"

### Shared Delivery Base
- Both orgs have large engineering and QE teams in the Philippines

### Plugin / Admin Access
- A person referenced as "Gaurav" or "GK" in meeting notes handles plugin distribution and admin access
- Possibly Gaurav Jetly, VP Cloud Ops — unconfirmed

---

## Rollout Timing and Constraints

- **Target:** November 2026 for initial rollout
- **Milestone from Ian's 28 Sep note:** Minimum bar = Vantagepoint and Maconomy trained on the framework and using it for at least some 2027.2 work
- **Cycle targets (per Lisa's slide):** 27.1 cycle covers Maconomy onboarding; 100% of in-scope teams on AI-SDLC in 27.2 cycle (1H 2027)
- **Camp v2 not ready:** 15 Oct check-in confirmed training is at v1; v2 needs review before rollout readiness is confirmed
- **Kickoff date not set:** Full-team kickoff planned once next training round is ready; date and attendance expectations open
- **Token guidance:** Still a rollout prerequisite as of 15 Oct

---

## Gaps in Available Information

- Survey data (491 responses, Jul–Aug) groups by job function, not by product org — cannot split by Vantagepoint vs. Maconomy
- Scrum masters and UX designers not identified or counted per org
- Contractor roles (85 in VP) unknown from directory data
- Claude licensing and tool access status not confirmed for either org
- No leadership stance on AI from Henrik Rosenstand or Dan DiStefano
