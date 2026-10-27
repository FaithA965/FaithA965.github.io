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
9. [References](#references)

---

## Project Overview

**AquaLink: Connecting South African Villages to Clean, Reliable Water**

AquaLink is a community water supply and management platform that connects borehole owners directly to households through a permanent pipe network, subscription plans and a digital management system. The idea comes from Muraleni village in Makhado, Limpopo, where many households have no water at home and have to buy it from neighbours with boreholes. Residents sometimes find the seller unavailable, or face prices that keep rising.

**Team**

| Member | Role (from our team charter) |
|---|---|
| Mologadi Dikgale | Project Manager |
| Uhmar Adams | Lead Developer |
| Leeroy Chakanyuka | Backend Developer |
| Faith Adams | UI/UX Designer |
| Phatushedzo Baloyi | QA Tester |

**Solution architecture:** the system has four layers.
1. **Presentation:** Household Portal, Supplier Dashboard and Administrator Dashboard.
2. **Application/API:** user, household, supplier, subscription, payment, water usage and alert management.
3. **Data:** a relational database.
4. **Physical/IoT:** borehole, flow sensor, 500L buffer tank, HDPE pipe network and household taps.

- [View the AquaLink solution architecture diagram](/Solution_Architecture.png)
- [View the AquaLink project presentation](/AquaLink_Presentation.pdf)

**Timeline note:** I worked on the project sprints from 14 July to 7 August 2026. On 8 September 2026 I was released to start in-service training at Alteram Solutions, so I am no longer working on AquaLink. The artefacts in this portfolio cover the period I was part of the team.

---

## 1. Agile Team Charter

### Evidence

An Agile team charter is a living social contract that defines a team's shared purpose, values, working agreements and boundaries (CPUT, 2026).

- [Download the full Agile Team Charter (PDF)](/Agile_Team_Charter.pdf) (student numbers removed for privacy)

**Purpose.** The charter states that the team exists to design and build a digital platform that brings structure and fairness to the water supply system in Muraleni, replacing an informal system with one that is transparent, reliable and easy to use. Its vision is a community where access to water is guaranteed, predictable and affordable.

**Roles and responsibilities**

| Name | Role | Responsibilities |
|---|---|---|
| Mologadi Dikgale | Project Manager | Leads sprint planning and retrospectives, manages the backlog, tracks progress, removes blockers |
| Uhmar Adams | Lead Developer | Owns the technical architecture, code reviews, development standards, integration |
| Leeroy Chakanyuka | Backend Developer | Builds REST APIs, designs the database schema, implements business logic |
| **Faith Adams** | **UI/UX Designer** | **Creates wireframes and user flows, designs the dashboards, ensures a clear and accessible user experience** |
| Phatushedzo Baloyi | QA Tester | Test plans, functional and regression testing, bug documentation, acceptance criteria |

**Core values:** Community first, Transparency, Accountability, Respect, Fairness, Reliability and Simplicity.

**Agile principles the team committed to:** frequent delivery in short sprints, welcoming changing requirements, trusting motivated individuals, face-to-face conversation for complex issues, working software as the measure of progress, a sustainable pace, good design as part of "done", and regular retrospectives.

**Working agreements**

| Area | Agreement |
|---|---|
| Channels | WhatsApp for daily check-ins (response within two hours), Microsoft Teams or in-person sessions for planning, reviews and retrospectives, GitHub for code |
| Daily stand-up | A short message each morning: what was completed, what is planned, and whether anything is blocked |
| Sprint planning, review, retrospective | Held every sprint. Attendance at planning is mandatory |
| Design and backend syncs | Short ad hoc sessions to align on interface requirements before implementation |

**SMART goals** (owners from the charter)

| Goal | Measure | Deadline | Owner |
|---|---|---|---|
| Admin Portal | All admin CRUD functions pass QA with zero critical bugs | Week 2 | Uhmar Adams, Leeroy Chakanyuka |
| Borehole Owner Portal | Owners complete all key tasks without assistance in UAT | Week 3 | Leeroy Chakanyuka, Faith Adams |
| Backend APIs | 100% of planned endpoints documented and passing integration tests | Week 4 | Leeroy Chakanyuka |
| Test Coverage | Zero critical bugs outstanding at deployment | Week 6 | Phatushedzo Baloyi |
| UAT | Sign-off from three real stakeholders | Week 8 | Mologadi Dikgale, Faith Adams |

### Reflection (STAR)

**Situation:** Early in the project our team of five wrote a charter for the "Village Water Supply" idea, which at that stage was a water delivery service for Muraleni. As we researched, the concept developed into AquaLink, a permanent pipe network with household, supplier and administrator users. Our sprints also settled into one week each, while the charter had planned for two-week sprints.

**Task:** My task was to work within the charter in my role as UI/UX Designer, and to notice where real practice and the written charter were drifting apart.

**Action:** I followed the stand-up agreement by answering the three questions in my logbook every day. I lived the Transparency and Accountability values by recording real impediments, such as unclear scope in Sprint 1 and unconfirmed business rules in Sprint 2, instead of writing "none". My design role showed up in Sprint 3, when I worked on the global stylesheet (colour palette, typography, sidebar, top bar, footer and responsiveness). I also compared the charter with my logbooks and saw two differences: the sprint length, and the user groups, because the charter names two (administrators and borehole owners) while AquaLink serves three (households, suppliers and administrators).

**Result:** The charter's principle of welcoming changing requirements gave the team permission to change direction without breaking our agreements. The comparison taught me that a charter is a "living" document only if someone updates it. If I did this again, I would revisit the charter at the end of Sprint 1, once the scope was clearer, and update the sprint length, the user groups and the milestone plan so that it matched what we were actually doing.

---

## 2. User Stories and Tasks

### Evidence

User stories describe a feature from the end user's perspective. Each story was broken into tasks and assigned to a sprint (CPUT, 2026).

| # | User Story | Sprint | Tasks |
|---|---|---|---|
| 1 | As a Muraleni resident without reliable household water, I want a permanent connection so that I can access clean water without travelling long distances. | Sprint 1: Research | Research the water-access situation. Identify the challenges residents face. Determine households' main water needs. Document the main problem AquaLink addresses. |
| 1 (cont.) | Same story | Sprint 2: Database Schema | Identify entities for residents and households. Define the information needed for users and households. |
| 2 | As a household that needs water, I want to request a connection to the AquaLink network so that I can receive water at my home. | Sprint 1: Requirements | Identify requirements for connecting a household. Determine the information needed from customers. Explore the request process. Map the customer journey. |
| 3 | As a borehole owner, I want to make my available water supply known through AquaLink so that it can be used to support households in the community. | Sprint 1: Requirements | Identify potential borehole owners. Determine the information needed from suppliers. Explore how available water can be monitored. Consider how suppliers will be managed. |
| 4 | As a household using AquaLink, I want my water usage, subscriptions and payments to be linked correctly so that my account information can be managed efficiently. | Sprint 2: Database Schema | Define relationships between all entities. Connect households, plans, purchases, tanks, alerts and payments. |
| 5 | As a borehole owner, I want my water supply information to be recorded so that available water resources can be monitored and managed through AquaLink. | Sprint 2: Database Schema | Identify supplier and borehole entities. Define attributes. Create the ERD. Document the schema. |
| 6 | As a Muraleni resident using AquaLink, I want a consistent and easy-to-use interface so that I can access information without confusion. | Sprint 3: Global Stylesheet | Define CSS variables. Select typography. Create a reusable colour palette. |
| 7 | As a household using AquaLink, I want all buttons, forms and pages to have the same design so that the application is easy to use. | Sprint 3: Global Stylesheet | Style shared buttons, form inputs, tables and badges. Apply consistent spacing. |
| 8 | As a borehole owner using AquaLink, I want the web and mobile applications to have the same visual appearance so that I have a consistent experience on every device. | Sprint 3: Global Stylesheet | Style the sidebar, top navigation bar and footer. Test responsiveness. |
| 9 | As a rural household resident, I want an easy way to access information about my water supply so that I can stay informed about availability and usage. | Sprint 4: US020 Review Technical Design | Review architecture, ERD, household-related entities and relationships. Document changes. Get team approval. |
| 10 | As a borehole supplier, I want to monitor water levels and supply information so that I can manage water distribution efficiently. | Sprint 4: US020 Review Technical Design | The same review, applied to supplier-related entities. |
| 11 | As an administrator, I want to monitor water usage and community supply data so that I can manage resources effectively. | Sprint 4: US020 Review Technical Design | The same review, applied to administrator-related entities. |

Taskboards for each sprint (page 1 of each logbook):
### Sprint 1 Taskboard
![Sprint 1 Taskboard](./evidence/Taskboard_Sprint1.png)

### Sprint 2 Taskboard
![Sprint 2 Taskboard](./evidence/Taskboard_Sprint2.png)

### Sprint 3 Taskboard
![Sprint 3 Taskboard](./evidence/Taskboard_Sprint3.png)

### Sprint 4 Taskboard
![Sprint 4 Taskboard](./evidence/Taskboard_Sprint4.png)

### Reflection (STAR)

**Situation:** AquaLink serves three very different users: households, borehole owners and administrators. At the start it was easy to think in terms of technical features instead of what each user needs.

**Task:** I needed to learn to describe work from the user's point of view, then break each story into tasks small enough to finish within a sprint.

**Action:** I worked with the team on stories in the "As a… I want… so that…" format, each tied to a real person from our Muraleni research. In Sprint 1 the stories turned our research into tasks, such as mapping the customer journey and identifying what information we need from suppliers. In Sprint 2 the first story came back with new tasks, this time about database entities. In Sprint 4 my task was **US020 Review Technical Design**, where I checked how the design supported each type of user.

**Result:** Writing the "so that" part of each story kept the work tied to a purpose, for example "without travelling long distances" connected the data model back to the problem we found in the community. I also learned that one story can be worked on in several sprints from different angles (research first, then data). Vague stories lead to vague tasks, and clear stories made the tasks obvious.

---

## 3. Product Backlog

### Evidence

The Product Backlog is the prioritised list of everything the product needs (Project Management Institute, 2017). We managed it on a Kanban-style taskboard (Product Backlog → In Progress → Completed).

| Area | Backlog items |
|---|---|
| Research and requirements (Sprint 1) | Water-access research in Muraleni, household needs, customer connection process, supplier information, MVP scope |
| Project foundations (listed on the Sprint 2 board) | Team Setup & Roles, GitHub Repository Setup, Development Environment Setup |
| Research and business (listed on the Sprint 2 board) | Community Research, Community Surveys, Business Case, Marketing, Feasibility & MVP |
| Design | Screen Design and Wireframes |
| Data (Sprint 2) | Database Schema Design: entities, relationships, ERD, schema documentation |
| UI (Sprint 3) | Global Stylesheet: CSS variables, typography, shared components, layout, responsiveness |
| Technical review (Sprint 4) | US020 Review Technical Design: architecture, ERD, entities, relationships, approval |
| Planned development (from our solution architecture) | Household Portal, Supplier Dashboard, Administrator Dashboard, sensor and flow data, subscriptions, payments and alerts |

The Sprint 2 taskboard shows the Product Backlog column most fully: [Sprint 2 taskboard and logbook](evidence/Logbook_Sprint2_21-24Jul.pdf)

**Process rule from our walkthroughs:** any new requirement found during a sprint is added to the Product Backlog and is not worked on straight away.

### Reflection (STAR)

**Situation:** AquaLink has many parts, including research, a database, a UI, a dashboard for each user type and IoT sensors. Without one ordered list, the team could easily have worked on the wrong thing first.

**Task:** Keep all required work visible in one place and decide what comes first.

**Action:** We used the taskboard to hold everything, and each walkthrough asked *"Is anyone working on anything that is not on the board?"* In Sprint 1 the answer was to add new research findings and new ideas to the board. When Sprint 1 raised open questions, such as how water usage would be measured and how subscriptions and supplier payments would work, they went into the backlog and shaped the tasks of later sprints.

**Result:** The backlog gave the project its order. Research came before the database, the database before the interface, and the technical design review before development, so decisions that others depended on were made first. I learned that a backlog is a working document that has to be kept up to date, not something you write once.

---

## 4. Sprint Backlog

### Evidence

The Sprint Backlog is the part of the Product Backlog the team commits to finishing in one sprint (Project Management Institute, 2017). Each of our sprints lasted one working week.

### Sprint 1 (14 to 17 July 2026): Research and Requirements

**Goal:** understand the water problem in Muraleni and define the scope and main requirements for AquaLink.

| User story | Tasks |
|---|---|
| Resident without reliable water | Research the situation, identify challenges, determine household needs, document the main problem |
| Household connection request | Identify connection requirements, determine customer information, explore the request process, map the customer journey |
| Borehole owner | Identify potential owners, determine supplier information, explore water monitoring, consider supplier management |

### Sprint 2 (21 to 24 July 2026): Database Schema Design

**Goal:** agree the database structure and entities for AquaLink.

| User story | Tasks |
|---|---|
| Resident / household | Identify resident and household entities. Define required information |
| Household account | Define relationships between all entities. Connect households, plans, purchases, tanks, alerts and payments |
| Borehole owner | Identify supplier and borehole entities. Define attributes. Create the ERD. Document the schema |

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

Sprint taskboards and logbooks:
[Sprint 1](/Logbook_Sprint1_14-17Jul.pdf) | [Sprint 2](/Logbook_Sprint2_21-24Jul.pdf) | [Sprint 3](/Logbook_Sprint3_28-30Jul.pdf) | [Sprint 4](/Logbook_Sprint4_04-07Aug.pdf)

### Reflection (STAR)

**Situation:** Each sprint lasted about one working week and had one clear focus, which moved the project from research to data, then to design, then to technical review.

**Task:** My job each sprint was to take the stories we had committed to and make real progress on the tasks within the week.

**Action:** In Sprint 1 I helped define the main users and the information we needed about them. In Sprint 2 I reviewed the proposed entities and prepared to define the relationships. In Sprint 3 I took part in planning the stylesheet, helped identify the reusable components (colours, typography, spacing) and styled the layout. In Sprint 4 I reviewed the architecture, ERD, entities and relationships, documented the issues we found, and discussed the changes with the team.

**Result:** Each sprint's output fed the next one: the requirements from Sprint 1 shaped the schema in Sprint 2, which was then reviewed in Sprint 4. Some work could only continue once the team agreed on design decisions, which taught me that dependencies need to be raised at sprint planning, not discovered mid-week. Next time I would list the decisions a sprint depends on during planning and ask for them to be settled in the first days.

---

## 5. Agile Logbook

### Evidence

The logbook records the daily stand-up (what I completed, what I plan to do, impediments) together with a weekly walkthrough of the taskboard.

| Sprint | Dates | Logbook |
|---|---|---|
| Sprint 1 | 14 to 17 July 2026 | [Logbook Sprint 1](/Logbook_Sprint1_14-17Jul.pdf) |
| Sprint 2 | 21 to 24 July 2026 | [Logbook Sprint 2](/Logbook_Sprint2_21-24Jul.pdf) |
| Sprint 3 | 28 to 30 July 2026 | [Logbook Sprint 3](/Logbook_Sprint3_28-30Jul.pdf) |
| Sprint 4 | 4 to 7 August 2026 | [Logbook Sprint 4](/Logbook_Sprint4_04-07Aug.pdf) |

**Highlights**

| Date | What I completed | Impediment raised |
|---|---|---|
| 14 Jul | Contributed to understanding the community water-access problem | Scope and requirements not yet clear |
| 15 Jul | Discussed how a pipe network could connect households with suppliers, and the types of users | Team still deciding which features are essential for the first version |
| 16 Jul | Worked through the service from customer and supplier views: subscriptions, usage monitoring, supplier payments | Questions on how infrastructure and platform work together and how usage is measured |
| 17 Jul | Reviewed the week and helped consolidate direction; the pilot idea became clearer | Technical and operational aspects still to be reviewed |
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

**Situation:** Four sprints ran across four weeks, and each day I had to account for my progress to the team.

**Task:** Keep a daily record that was honest and useful, not only a list of tasks.

**Action:** Every day I answered three questions: what I had completed, what I planned next and what was blocking me. I recorded real impediments, such as *the final scope was not yet clear*, *business rules still needed confirmation* and *relationships need clarification*, instead of writing "none".

**Result:** Reading the logbooks back, I can see the project moving from uncertainty (Sprint 1, when the scope was still forming) to confidence (Sprint 4, "no major blockers"). Most of my blockers were about decisions, not code, and raising them early let the team resolve them. One example: on 5 August I logged that some relationships needed clarification before the design could be finalised. By 6 August the issues and changes had been documented and discussed with the team, and my log reads "no major blockers". The log also gave me a habit I now use in my internship, where the daily stand-up is part of the programme.

---

## Graduate Attributes Applied to the eWIL Project

| Attribute | How AquaLink demonstrates it |
|---|---|
| **Ubuntu** | The project is built from the community's needs. Two team members have grandparents in rural villages, and our research in Muraleni informed the design. Our charter's values of Community first and Respect shaped how we worked, and I worked with four teammates every day. |
| **Knowing, Technological Capability & Foresight** | We applied database design, IoT sensing, dashboards and a consistent web/mobile UI to the problem of unreliable water access. |
| **Resilience & Problem-Solving** | The concept developed from a delivery service into a pipe network, and we handled open decisions in every sprint while keeping the work moving. We also planned the financials (R15,930 once-off infrastructure cost for the pilot) and an MVP to test the idea in real conditions. |
| **Ethical Capability & Respect** | I recorded real impediments in my logbook instead of writing "none", which is the Transparency and Accountability our charter asks for. Our project presentation credits where at least one of its photos came from (the Gift of the Givers response in Limpopo, 2025) rather than presenting it as our own. Design decisions were only built after team approval, which respected every member's input. |

---

## Connecting It All Together

The five artefacts form one chain. The **Team Charter** set how we work and who does what. **User Stories** defined what each person needs. The **Product Backlog** ordered the work. The **Sprint Backlog** committed us to a week of it. The **Logbook** recorded how the week actually went, and its impediments often led to changes in the next sprint's plan.

My biggest learning is that Agile is about communication more than tools. The board, the stand-up and the walkthrough questions exist so that decisions and blockers are visible early. I could see this in my own logbook, which moved from "the final scope was not yet clear" in Sprint 1 to "no major blockers" in Sprint 4. I also learned that a charter has to keep up with the project: ours described a delivery service in two-week sprints, and by Sprint 4 we were designing a pipe network in one-week sprints.

Because I moved to my internship in September, I also saw Agile in two settings: a student project where we set the rules ourselves, and a workplace where daily stand-ups and ticket-based first-line support were already established. The habits carried over directly.

---

## References

CPUT (2026) *PRP37XS Project Presentation III: Subject Guide and October 2026 Assessment Brief*. Cape Town: Cape Peninsula University of Technology.

Project Management Institute (2017) *Agile Practice Guide*. Newtown Square, PA: Project Management Institute.

Gift of the Givers (2025) Water relief response, Limpopo, as credited in the AquaLink project presentation.

---

*Faith Adams | PRP372S | October 2026*
