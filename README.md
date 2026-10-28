
<div align="center"> <img src="assets/banner.png" alt="AICTE Grievance Intelligence System" width="100%" />
Integrated Institutional Grievance Intelligence, Monitoring and Cross-Bureau Coordination System
Smart India Hackathon 2026 · AICTE · Prototype

One institution. One connected grievance history. Better-informed coordination.

</div>
✦ The idea
Institutional complaints are often easier to understand together than as isolated tickets. This proposed platform connects student grievances, institution identities, officer assignments, and bureau workflows in one institution-centric workspace.

Complaints can be linked using an AICTE Permanent ID; official verification is a planned integration. Officers can explore complaint history, inspect potential duplicates, and review advisory coordination alerts across the Regulation Bureau (RB) and Public Grievance Redressal Cell (PGRC).

Project scope: Educational SIH prototype, not an official AICTE service. AI suggestions require officer review and do not automatically merge, escalate, or resolve cases.

✦ At a glance
Institution intelligence	Cross-bureau coordination	Human-in-the-loop AI
One institution profile links cases, statuses, and officers.	Potential RB–PGRC overlap alerts highlight coordination needs.	Advisory category and related-case suggestions support officer review.
✦ System architecture
<div align="center"> <a href="https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/"> <img src="assets/system-architecture.png" alt="Interactive technology architecture preview" width="100%" /> </a>
Open interactive technology architecture

</div>
The live link requires GitHub Settings → Pages → Deploy from a branch → main → /docs and an actual docs/index.html file committed to the main branch. You can also view the HTML source. GitHub README pages cannot execute interactive JavaScript.

<details> <summary><b>Architecture explanation</b></summary>
Users: Students, officers, institutions, and administrators.
Frontend: React + Vite for forms, dashboards, case views, and graphs.
Backend: Python + FastAPI for endpoints and workflows.
Intelligence & data: SQLite and rule-based complaint checks; SBERT and TF-IDF are proposed enhancements.
Outputs: Officer workspace, institution profiles, relationship graphs, reports, and alerts.
</details>
✦ Platform modules
<details open> <summary><b>01 — Student grievance portal</b></summary>
Students select an institution, submit grievance details, and track case status.

</details> <details> <summary><b>02 — Officer dashboard & case workspace</b></summary>
Authorized officers inspect cases, assignments, remarks, status changes, and action history.

</details> <details> <summary><b>03 — Institution intelligence profile</b></summary>
Institution records connect complaint history, categories, bureau assignments, and officers.

</details> <details> <summary><b>04 — RB–PGRC coordination alerts</b></summary>
Potentially overlapping active cases can be flagged for authorized officer review.

</details> <details> <summary><b>05 — Relationship graph & reporting</b></summary>
Visual relationships link institutions, complaints, bureaus, and officers; reporting summarizes case history.

</details>
✦ AI-assisted intelligence
Current prototype screenshots show rule-based category suggestions and potential duplicate detection. The following NLP methods are proposed enhancements, not verified deployed models.

Model / method	Intended role
Sentence-BERT (all-MiniLM-L6-v2)	Semantic complaint embeddings
TF-IDF	Keyword similarity baseline
Cosine similarity	Similarity scoring
Python rules	Institution, status, and bureau overlap checks
SLA rules	Deadline monitoring
✦ Technology stack
Layer	Technology	Purpose
Frontend	React + Vite	Interactive web interface
Backend	Python + FastAPI	REST endpoints and workflows
Database	SQLite	Prototype records
Current intelligence	Python rules	Advisory category and case checks
Proposed NLP	Sentence Transformers, scikit-learn	Semantic and keyword similarity
Access	Role-based permissions	Authorized workflows
✦ Demo journeys
Complaint to officer review: Student submits a grievance → case is stored → related-case checks run → officer reviews and records actions.

Potential cross-bureau overlap: Related RB and PGRC complaints → advisory flag → officer verification → documented coordination decision.

✦ Application screenshots
These screenshots show illustrative prototype records. Original screenshot files are used without resizing or alteration.

Complaint submission
<p align="center"><img src="assets/screenshots/case-submission.png" alt="Complaint submission" width="800" /></p>
Officer workspace and case assignment
<p align="center"><img src="assets/screenshots/officer-case-assignment.png" alt="Officer workspace and assignment" width="800" /></p>
Officer communication
<p align="center"><img src="assets/screenshots/officer-chat.png" alt="Officer chat" width="800" /></p>
File attachments
<p align="center"><img src="assets/screenshots/officer-chat-attachment.png" alt="Officer attachment" width="800" /></p>
Institution intelligence profile
<p align="center"><img src="assets/screenshots/institution-profile.png" alt="Institution profile" width="800" /></p>
Complaint relationship network
<p align="center"><img src="assets/screenshots/relationship-graph-institution.png" alt="Institution relationship graph" width="800" /></p> <p align="center"><img src="assets/screenshots/relationship-graph-case.png" alt="Complaint relationship graph" width="800" /></p>
AI-assisted case intelligence
<p align="center"><img src="assets/screenshots/ai-case-intelligence.png" alt="AI case intelligence" width="800" /></p>
Historical complaint reporting
<p align="center"><img src="assets/screenshots/historical-reporting.png" alt="Historical reporting" width="800" /></p> <p align="center"><img src="assets/screenshots/historical-reporting-status.png" alt="Historical reporting statuses" width="800" /></p>
✦ Repository layout
Integrated-Institutional-Grievance-Intelligence-.../
├── README.md
├── assets/
│   ├── banner.png
│   ├── system-architecture.png
│   └── screenshots/
│       ├── ai-case-intelligence.png
│       ├── case-submission.png
│       ├── historical-reporting.png
│       ├── historical-reporting-status.png
│       ├── institution-profile.png
│       ├── officer-case-assignment.png
│       ├── officer-chat.png
│       ├── officer-chat-attachment.png
│       ├── relationship-graph-case.png
│       └── relationship-graph-institution.png
└── docs/
    └── index.html
This tree documents the README assets and HTML page. Include frontend/, backend/, and other source folders only if they are actually committed to your repository.

✦ Details
Item	Details
Team	CYBRIXX
Hackathon	Smart India Hackathon 2026
Problem statement	SIH26264
Interactive architecture source	
index.html
Live interactive architecture	Open GitHub Pages
Repository	GitHub
✦ Responsible use
Student grievances may contain sensitive personal information. Do not commit real complaints, credentials, or private institution records to a public repository. Use synthetic records and enforce permissions on the backend. AI suggestions are advisory and require human review.

<div align="center">
AICTE GRIEVANCE INTELLIGENCE SYSTEM

Institutional visibility · Connected workflows · Responsible AI

<sub>Smart India Hackathon 2026 · Educational prototype · Not affiliated with or endorsed by AICTE</sub>

</div>
0.35 s
