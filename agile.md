# Entrepreneurial WIL (eWIL) Portfolio: AquaLink

**Faith Adams** | Diploma in ICT (Applications Development) | PRP372S Project Presentation 3

[← Back to my portfolio home](README.md)

---

## Contents

1. [Project Overview](#project-overview)
2. [Agile Team Charter](#1-agile-team-charter)
3. [User Stories and Tasks](#2-user-stories-and-tasks)
4. [Product Backlog](#3-product-backlog)
5. [Sprint Backlog](#4-sprint-backlog)
6. [Agile Logbook](#5-agile-logbook)
7. [Graduate Attributes](#graduate-attributes-applied-to-the-ewil-project)
8. [Connecting It All Together](#connecting-it-all-together)

---

## Project Overview

**AquaLink: Connecting South African Villages to Clean, Reliable Water**

AquaLink is a community water supply and management platform that connects borehole owners directly to households through a permanent pipe network, subscription plans and a digital management system. The idea comes from Muraleni village in Makhado, Limpopo, where many households have no water at home and have to buy it from neighbours with boreholes. Residents sometimes find the seller unavailable, or face prices that keep rising.

**Team**

| Member | Role |
|---|---|
| Mologadi Dikgale | Team member |
| Uhmar Adams | Team member |
| Faith Adams | Team member: database design and technical design review, global stylesheet |
| Leeroy Chakanyuka | Team member |
| Phatushedzo Baloyi | Team member |

**Solution architecture:** the system has four layers.
1. **Presentation:** Household Portal, Supplier Dashboard and Administrator Dashboard.
2. **Application/API:** user, household, supplier, subscription, payment, water usage and alert management.
3. **Data:** a relational database (PostgreSQL in the example stack).
4. **Physical/IoT:** borehole, flow sensor, 500L buffer tank, HDPE pipe network and household taps.

![AquaLink Solution Architecture](images/Solution_Architecture.png)

**Timeline note:** I worked on the project sprints in July and early August 2026. On 8 September 2026 I was released to start in-service training at Alteram Solutions, so I am no longer working on AquaLink. The artefacts in this portfolio cover the period I was part of the team.

---

## 1. Agile Team Charter

### Evidence

An Agile team charter is a living social contract that defines a team's shared purpose, values, working agreements and boundaries (CPUT, 2026).

**Shared purpose** (from our project vision)
To give rural households a home tap and safe, reliable water: "one pipe, one street, one village at a time." Borehole owners earn a tracked income, and administrators can manage supply and payments.

**Working agreements our team followed** (visible in our taskboards and logbooks)

- A daily stand-up where each member answers three questions: what I completed, what I plan to do next, and what is blocking me.
- A taskboard with three columns (Product Backlog, In Progress, Completed), with every user story broken into tasks.
- A weekly walkthrough of the board using four questions: what do we need to do to advance the work, is anyone working on something that is not on the board, what do we need to finish as a team, and what is blocking the flow of work.
- New requirements found during a sprint are added to the Product Backlog.
- Design decisions that affect everyone (colour palette, typography, database structure, technical design) need team approval before implementation.

**Team members and roles:** see the team table in the Project Overview.

### Reflection (STAR)

**Situation:** Our team of five came together to build AquaLink, a real project for a real community. A team that size needs clear rules about how work is planned, shared and approved.

**Task:** My task was to understand the team's working agreements and follow them every day, so that my work fitted with everyone else's.

**Action:** I took part in the daily stand-ups and recorded my answers to the three questions in my logbook. I used the weekly walkthrough to check that what I was doing was on the board. When design decisions were still open, for example the colour palette in Sprint 3 and the relationships in the database in Sprint 4, I raised them as impediments and waited for team agreement. From the first sprint I applied these agreements in my own work and logged how they played out each day.

**Result:** The agreements gave us a shared way to work. My logbooks show the team repeatedly pausing for approval instead of building on unconfirmed decisions. I learned that a charter only works if the team keeps using it. After I left the project in September to start my internship, I saw the same habits (daily stand-up, tracked tasks, raising blockers early) in a workplace, which showed me they apply beyond a student project.

---

## 2. User Stories and Tasks

### Evidence

User stories describe a feature from the end user's perspective. Each story was broken into tasks and assigned to a sprint.

| # | User Story | Sprint | Tasks |
|---|---|---|---|
| 1 | As a Muraleni resident without reliable household water, I want a permanent connection so that I can access clean water without travelling long distances. | Sprint 2: Database Schema Design | Identify entities related to residents and households. Define the information needed for users and households. |
| 2 | As a household using AquaLink, I want my water usage, subscriptions and payments to be linked correctly so that my account information can be managed efficiently. | Sprint 2: Database Schema Design | Define relationships between all entities. Connect households, plans, purchases, tanks, alerts and payments. |
| 3 | As a borehole owner, I want my water supply information to be recorded so that available water resources can be monitored and managed through AquaLink. | Sprint 2: Database Schema Design | Identify supplier and borehole entities. Define attributes. Create the ERD. Document the database schema. |
| 4 | As a Muraleni resident using AquaLink, I want a consistent and easy-to-use interface so that I can access information without confusion. | Sprint 3: Global Stylesheet | Define CSS variables (colours, font sizes, spacing, border radius). Select typography. Create a reusable colour palette. |
| 5 | As a household using AquaLink, I want all buttons, forms and pages to have the same design so that the application is easy to use. | Sprint 3: Global Stylesheet | Style shared buttons. Style form inputs. Style tables and badges. Apply consistent spacing. |
| 6 | As a borehole owner using AquaLink, I want the web and mobile applications to have the same visual appearance so that I have a consistent experience on every device. | Sprint 3: Global Stylesheet | Style the sidebar, top navigation bar and footer. Test responsiveness on different screen sizes. |
| 7 | As a rural household resident, I want an easy way to access information about my water supply so that I can stay informed about availability and usage. | Sprint 4: US020 Review Technical Design | Review architecture. Review ERD. Review household-related entities and relationships. Document changes. Get team approval. |
| 8 | As a borehole supplier, I want to monitor water levels and supply information so that I can manage water distribution efficiently. | Sprint 4: US020 Review Technical Design | Same review tasks, applied to supplier-related entities. |
| 9 | As an administrator, I want to monitor water usage and community supply data so that I can manage resources effectively. | Sprint 4: US020 Review Technical Design | Same review tasks, applied to administrator-related entities. |

![Sprint 4 taskboard](images/sprint4-taskboard.png)

### Reflection (STAR)

**Situation:** AquaLink serves three very different users: households, borehole owners and administrators. At the start it was easy to think in terms of technical features instead of what each user needs.

**Task:** I needed to learn to describe work from the user's point of view, then break each story into tasks small enough to finish within a sprint.

**Action:** I worked with the team on stories written in the "As a… I want… so that…" format, each tied to a real person from our Muraleni research. In Sprint 2 I helped break the database stories into entity and relationship tasks. In Sprint 4 my task was **US020 Review Technical Design**, and I checked how the design supported households, suppliers and administrators.

**Result:** Writing the "so that" part of each story kept the work tied to a purpose. For example, "without travelling long distances" connected the data model back to the problem we found in the community. I learned that a good story makes the tasks obvious, and that vague tasks usually come from vague stories.

---

## 3. Product Backlog

### Evidence

The Product Backlog is the prioritised list of everything the product needs (Project Management Institute, 2017). We managed it on a Kanban-style taskboard (Product Backlog → In Progress → Completed).

| Area | Backlog items |
|---|---|
| Project foundations (listed on the Sprint 2 board) | Team Setup & Roles, GitHub Repository Setup, Development Environment Setup |
| Research and business (listed on the Sprint 2 board) | Community Research, Community Surveys, Business Case, Marketing, Feasibility & MVP |
| Design | Screen Design and Wireframes |
| Data (Sprint 2) | Database Schema Design: entities, relationships, ERD, schema documentation |
| UI (Sprint 3) | Global Stylesheet: CSS variables, typography, shared components, layout, responsiveness |
| Technical review (Sprint 4) | US020 Review Technical Design: architecture, ERD, entities, relationships, approval |
| Planned development (from our solution architecture) | Household Portal, Supplier Dashboard, Administrator Dashboard, sensor and flow data, subscriptions, payments and alerts |

**Taskboard:** our board followed the Kanban layout Trello is built around, with the three columns above.

![Taskboard](images/taskboard.png)

**Process rule from our walkthroughs:** any new requirement found during a sprint is added to the Product Backlog and is not worked on straight away.

### Reflection (STAR)

**Situation:** AquaLink has many parts, including research, a database, a UI, a dashboard for each user type and IoT sensors. Without a single ordered list, the team could easily have worked on the wrong thing first.

**Task:** Keep all required work visible in one place and decide what comes first.

**Action:** We used the taskboard to hold everything, and each walkthrough asked *"Is anyone working on anything that is not on the board?"* When new ideas came up in discussion, we added them to the backlog. I used the board each day to see what was in progress and what was complete.

**Result:** The backlog gave the project its order. The database came before the interface, and the interface came before development, so decisions that others depended on were made first. I learned that a backlog is a working document that has to be kept up to date, not something you write once.

---

## 4. Sprint Backlog

### Evidence

The Sprint Backlog is the part of the Product Backlog the team commits to finishing in one sprint.

### Sprint 2 (21 to 24 July 2026): Database Schema Design

**Goal:** agree the database structure and the entities for AquaLink.

| User story | Tasks |
|---|---|
| Resident / household | Identify resident and household entities. Define required information. |
| Household account | Define relationships between all entities. Connect households, plans, purchases, tanks, alerts and payments. |
| Borehole owner | Identify supplier and borehole entities. Define attributes. Create the ERD. Document the schema. |

### Sprint 3 (28 to 30 July 2026): Global Stylesheet

**Goal:** one consistent look across web and mobile.

| User story | Tasks |
|---|---|
| Consistent interface | CSS variables, typography, colour palette |
| Same design everywhere | Buttons, form inputs, tables, badges, spacing |
| Web and mobile match | Sidebar, top navigation bar, footer, responsiveness testing |

### Sprint 4 (4 to 7 August 2026): Technical Design Review (US020)

**Goal:** review and approve the architecture and database before development begins.

| Task | Status per logbook |
|---|---|
| Review the architecture | Done |
| Review the ERD | Done |
| Review entities and relationships | Done |
| Document changes | Done |
| Team approval | Prepared for final approval (7 Aug) |

![Sprint 2 taskboard](images/sprint2-taskboard.png)

![Sprint 3 taskboard](images/sprint3-taskboard.png)

![Sprint 4 taskboard](images/sprint4-taskboard.png)

### Reflection (STAR)

**Situation:** Each sprint lasted about one working week, and each had one clear focus.

**Task:** My job each sprint was to take the stories we had committed to and make real progress on the tasks within the week.

**Action:** In Sprint 2 I reviewed the proposed entities and prepared to define the relationships. In Sprint 3 I took part in planning the stylesheet and helped identify the reusable components (colours, typography, spacing). In Sprint 4 I reviewed the architecture, ERD, entities and relationships, documented the issues we found, and discussed the changes with the team.

**Result:** Each sprint's output fed the next one: the schema from Sprint 2 was reviewed in Sprint 4. Some work could only continue once the team agreed on design decisions, and that taught me that dependencies need to be raised at planning, not discovered mid-sprint. Next time I would list the decisions a sprint depends on during sprint planning and ask for them to be settled in the first days, so that work does not wait on them mid-week.

---

## 5. Agile Logbook

### Evidence

The logbook records the daily stand-up (what I completed, what I plan to do, impediments) together with a weekly walkthrough of the taskboard.

| Sprint | Week | Logbook |
|---|---|---|
| Sprint 2 | 21 to 24 July 2026 | [Agile Logbook 24-07-26](evidence/logbook-24-07-26.pdf) |
| Sprint 3 | 28 to 30 July 2026 | [Agile Logbook 05-08-26](evidence/logbook-sprint3.pdf) |
| Sprint 4 | 4 to 7 August 2026 | [Agile Logbook 05-08-26](evidence/logbook-sprint4.pdf) |

**Highlights**

| Date | What I completed | Impediment raised |
|---|---|---|
| 21 Jul | Joined Sprint 2 planning on the database schema | Task details still being clarified |
| 22 Jul | Reviewed the entities and how they serve each user type | Business rules not yet confirmed |
| 23 Jul | Discussed how the entities interact | Work depended on team decisions |
| 24 Jul | Prepared my task by reviewing the proposed structure | No major blockers |
| 28 Jul | Joined Sprint 3 planning for the Global Stylesheet | Design choices not yet final |
| 29 Jul | Reviewed palette and typography, organised reusable styles | Styles may need revision after review |
| 30 Jul | Styled the layout (sidebar, top bar, footer), checked responsiveness | No major blockers |
| 4 Aug | Joined Sprint 4 discussion, reviewed the architecture, started the ERD review | Some areas needed team discussion |
| 5 Aug | Reviewed ERD, entities and relationships | Some relationships needed clarification |
| 6 Aug | Completed the main review and documented issues | No major blockers |
| 7 Aug | Completed the review and confirmed readiness for approval | Waiting on final team approval |

### Reflection (STAR)

**Situation:** Three sprints ran across three weeks, and each day I had to account for my progress in front of the team.

**Task:** Keep a daily record that was honest and useful, not only a list of tasks.

**Action:** Every day I answered three questions: what I had completed, what I planned next and what was blocking me. I recorded real impediments, such as *business rules still needed confirmation* and *relationships need clarification*, instead of writing "none".

**Result:** Reading the logbooks back, I can see the project moving from uncertainty (Sprint 2, when decisions were still open) to confidence (Sprint 4, "no major blockers"). The log showed me that most of my blockers were about decisions, not code, and that raising them early let the team resolve them. It also gave me a habit I now use in my internship, where the daily stand-up is part of the programme. One example: on 5 August I logged that some relationships needed clarification before the design could be finalised. By 6 August the issues and changes had been documented and discussed with the team, and my log reads "no major blockers".

---

## Graduate Attributes Applied to the eWIL Project

| Attribute | How AquaLink demonstrates it |
|---|---|
| **Ubuntu** | The project is built from the community's needs. Two team members have grandparents in rural villages, and our survey and research in Muraleni informed the design. I worked with four teammates every day. |
| **Knowing, Technological Capability & Foresight** | We applied database design, IoT sensing, dashboards and a consistent web/mobile UI to the problem of unreliable water access. |
| **Resilience & Problem-Solving** | We handled open design decisions, relationships needing clarification, and review changes while keeping the sprints on track. We also planned the financials (R15,930 once-off infrastructure cost for the pilot) and an MVP to test the idea in real conditions. |
| **Ethical Capability & Respect** | I recorded real impediments in my logbook, such as business rules not yet confirmed and relationships needing clarification, instead of writing "none", so the team had an honest picture of progress. Our project presentation credits where at least one of its photos came from (the Gift of the Givers response in Limpopo, 2025) rather than presenting it as our own. Design decisions were only built after team approval, which respected every member's input. |

---

## Connecting It All Together

The five artefacts form one chain. The **Team Charter** set how we work. **User Stories** defined what each person needs. The **Product Backlog** ordered the work. The **Sprint Backlog** committed us to a week of it. The **Logbook** recorded how the week actually went, and its impediments often led to changes in the next sprint's plan.

My biggest learning is that Agile is about communication more than tools. The board, the stand-up and the walkthrough questions exist so that decisions and blockers are visible early. I could see this in my own logbook, which moved from "details still need to be clarified" in Sprint 2 to "no major blockers" in Sprint 4.

Because I moved to my internship in September, I also saw Agile in two settings: a student project where we set the rules ourselves, and a workplace where daily stand-ups and ticket-based first-line support were already established. The habits carried over directly.

---

## References

CPUT (2026) *PRP37XS Project Presentation III: Subject Guide and October 2026 Assessment Brief*. Cape Town: Cape Peninsula University of Technology.

Project Management Institute (2017) *Agile Practice Guide*. Newtown Square, PA: Project Management Institute.

Gift of the Givers (2025) Water relief response, Limpopo, as credited in the AquaLink project presentation.

---

*Faith Adams | PRP372S | October 2026*
