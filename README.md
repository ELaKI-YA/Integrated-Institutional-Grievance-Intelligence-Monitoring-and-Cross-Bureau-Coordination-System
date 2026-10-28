<div align="center">

<img src="assets/banner.png" alt="AICTE Grievance Intelligence System" width="100%" />


Integrated Institutional Grievance Intelligence, Monitoring and Cross-Bureau Coordination System
Smart India Hackathon 2026 · AICTE · Prototype

One institution. One connected grievance history. Better-informed coordination.
</div>

✦ The idea
Institutional complaints are often easier to understand together than as isolated tickets. Our proposed platform brings student grievances, institution identities, officer assignments, and bureau workflows into one institution-centric workspace.

Complaints can be linked to an institution using its AICTE Permanent ID; official verification is a planned integration. Officers can explore the full complaint history, inspect potential duplicates, and receive advisory coordination alerts when related active cases may span the Regulation Bureau (RB) and Public Grievance Redressal Cell (PGRC).
Project scope: An educational SIH prototype—not an official AICTE service. AI suggestions are reviewed by authorized officers; they do not automatically merge, escalate, or resolve cases.

✦ At a glance
Institution intelligence	Cross-bureau coordination	Human-in-the-loop AI
One institution profile connects related cases, statuses, and officers.	Potential RB–PGRC overlap alerts help officers identify coordination needs.	Advisory category and related-case suggestions support—not replace—officer review.


✦ System architecture
<div align="center">

<a href="https://ELaKI-YA.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/">
  <img src="assets/system-architecture.png" alt="Click to open the interactive AICTE technology architecture" width="100%" />
</a>


<a href="https://ELaKI-YA.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/">
  <img src="https://img.shields.io/badge/OPEN-INTERACTIVE_TECHNOLOGY_ARCHITECTURE-362822?style=for-the-badge" alt="Open interactive technology architecture" />
</a>

<br/>
<sub>Click the diagram or badge to explore the live HTML architecture, technology, features, purpose, and workflows.</sub>

</div>

Interactive page: Enable GitHub Pages with Deploy from a branch → main → /docs to activate the link above. GitHub README pages cannot run JavaScript directly. You can also [view the HTML source](docs/index.html).

<details>
<summary><b>Open the architecture explanation</b></summary>

01 · Users — Students submit and track complaints; officers review cases; institutions and administrators access permitted views.

02 · Frontend — React + Vite renders portals, dashboards, case pages, visualizations, and alerts.

03 · Backend — FastAPI provides REST endpoints, validation, case workflows, and controlled data access.

04 · Intelligence & data — SQLite stores structured records. Current case intelligence includes rule-based category suggestions and potential related-case checks; SBERT/TF-IDF are proposed enhancements. Python rules can examine institution IDs and bureau assignments.

05 · Outputs — Officer dashboards, institution profiles, relationship graphs, reports, and alerts appear in the React application.
</details>

✦ Platform modules
<details open>
<summary><b>01 — Student grievance portal</b></summary>

Students select an institution, submit complaint details, and follow status changes. Each submission is associated with an institution record for consistent tracking.
</details>

<details>
<summary><b>02 — Officer dashboard & case workspace</b></summary>


Authorized officers review assigned grievances, inspect related cases, add remarks, update statuses, transfer or escalate work, and maintain a chronological action trail.
</details>

<details>
<summary><b>03 — Institution intelligence profile</b></summary>


An AICTE Permanent ID anchors institution metadata, complaint history, categories, bureau assignments, officers, and case status summaries.
</details>

<details>
<summary><b>04 — RB–PGRC coordination alerts</b></summary>


Potentially related active cases involving the same institution across bureaus are flagged as “Potential Overlapping Cases – Coordination Required.” Authorized officers inspect the evidence and decide next steps.
</details>

<details>
<summary><b>05 — Relationship graph & reporting</b></summary>


A visual network links Institution → Complaint → Bureau → Officer. Reporting views summarize case volumes, statuses, categories, regions, and deadlines.
</details>

✦ AI-assisted intelligence
Current screenshots demonstrate rule-based category suggestions and potential duplicate detection. The NLP methods below are proposed extensions; do not describe them as deployed until implemented and tested.
Model / method	Role in grievance intelligence
Sentence-BERT · all-MiniLM-L6-v2	Create semantic complaint embeddings
TF-IDF	Provide a keyword-based similarity baseline
Cosine similarity	Score similarity between complaint representations
Python rules	Check institution IDs, active-case status, and RB–PGRC overlaps
SLA rules	Identify approaching or overdue case deadlines


```mermaid
flowchart TD
    A[New grievance] --> B[Validate AICTE Permanent ID]
    B --> C[Retrieve institution-linked complaints]
    C --> D[Normalize complaint text]
    D --> E[SBERT embeddings / TF-IDF baseline]
    E --> F[Cosine similarity scoring]
    F --> G[RB–PGRC overlap rules]
    G --> H[Advisory related-case alert]
    H --> I[Authorized officer review]
    I --> J[Decision and audit trail]
```
Example: “The college has not returned my admission fee” and “I am waiting for my refund after cancelling admission” may be semantically related even though the wording differs. A suggested match is not an official duplicate decision.
✦ Technology stack
Layer	Technology	Why it fits
Interface	React.js + Vite	Responsive, component-based frontend
API & workflows	Python + FastAPI	Typed REST endpoints and case logic
Prototype storage	SQLite	Simple relational institution/case records
NLP	Sentence Transformers	Local semantic embeddings
Text baseline	Scikit-learn	TF-IDF and cosine similarity
Coordination	Python rules	Transparent institution/bureau checks
Authorization	Role-based access control	Access based on authorized responsibilities


✦ Demo journeys
<details>
<summary><b>Journey A — Complaint to officer review</b></summary>

1. Student selects the institution and submits a grievance.
2. FastAPI validates the submission and institution reference.
3. SQLite stores the complaint and its institution relationship.
4. NLP and rule checks generate advisory signals.
5. An authorized officer reviews the case and records actions.
</details>

<details>
<summary><b>Journey B — Potential cross-bureau overlap</b></summary>

1. An active RB complaint and an active PGRC complaint reference the same institution.
2. Similarity analysis identifies a possible relationship.
3. Coordination rules produce a potential overlap flag.
4. Officers inspect both records; no automatic case merging occurs.
5. Any coordination action is recorded in the case history.
</details>

✦ 
## ✦ Application Screenshots

Explore the application interface and core grievance-management workflows.

### 1. Complaint Submission
![Complaint Submission](assets/screenshots/case-submission.png)

### 2. Officer Workspace and Case Assignment
![Officer Workspace](assets/screenshots/officer-case-assignment.png)

### 3. Officer Communication
![Officer Chat](assets/screenshots/officer-chat.png)

### 4. File Attachments
![File Attachments](assets/screenshots/officer-chat-attachment.png)

### 5. Institution Intelligence Profile
![Institution Profile](assets/screenshots/institution-profile.png)

### 6. Complaint Relationship Network
![Institution Relationship Graph](assets/screenshots/relationship-graph-institution.png)

![Complaint Relationship Graph](assets/screenshots/relationship-graph-case.png)

### 7. AI-Assisted Case Intelligence
![AI Case Intelligence](assets/screenshots/ai-case-intelligence.png)

### 8. Historical Complaint Reporting
![Historical Reporting](assets/screenshots/historical-reporting.png)

![Complaint Status History](assets/screenshots/historical-reporting-status.png)


✦ Repository layout
AICTE-Grievance-Intelligence-System/
├── assets/
│   ├── banner.png
│   ├── system-architecture.png
│   └── screenshots/           # 10 PNG screenshots
├── docs/
│   └── index.html               # GitHub Pages interactive architecture
├── frontend/                 # React + Vite application
├── backend/                  # FastAPI routes and case workflows
├── ai_engine/                # Similarity and overlap checks
├── tests/
├── requirements.txt
├── README.md
└── LICENSE
Implementation note: Sentence Transformers is a proposed enhancement. If added, the first model load may require internet access; cached model files can support later offline inference.
✦ Details


| Interactive architecture | [Open HTML source](docs/index.html) · Live interactive page |
| Team | CYBRIXX |
| SIH problem statement | SIH26264 |


✦ Responsible use
Student grievances may contain sensitive personal information. Do not commit real complaints, credentials, or private institution records to a public repository. Use synthetic demo records and enforce permissions in the backend. Model scores are advisory; accuracy and thresholds should be evaluated before operational use.
<div align="center">
  <b>AICTE GRIEVANCE INTELLIGENCE SYSTEM</b><br/>
  <sub>Institutional visibility · Connected workflows · Responsible AI</sub><br/><br/>
  <sub>Smart India Hackathon 2026 · Educational prototype · Not affiliated with or endorsed by AICTE</sub>
</div>
