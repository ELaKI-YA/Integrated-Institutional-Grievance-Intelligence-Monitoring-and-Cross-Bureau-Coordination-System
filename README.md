<div align="center">

<img src="assets/banner.png" alt="AICTE Grievance Intelligence System" width="780" />

<h1>Integrated Institutional Grievance Intelligence, Monitoring and Cross-Bureau Coordination System</h1>

**Smart India Hackathon 2026 · AICTE · Prototype**

*One institution. One connected grievance history. Better-informed coordination.*

</div>

## ✦ The idea

Institutional complaints are often easier to understand **together** than as isolated tickets. This proposed platform connects student grievances, institution identities, officer assignments, and bureau workflows in one institution-centric workspace.

Complaints can be linked using an **AICTE Permanent ID**; official verification is a planned integration. Officers can explore complaint history, inspect potential duplicates, and review advisory coordination alerts across the **Regulation Bureau (RB)** and **Public Grievance Redressal Cell (PGRC)**.

> **Project scope:** Educational SIH prototype, not an official AICTE service. AI suggestions require officer review and do not automatically merge, escalate, or resolve cases.

## ✦ At a glance

| Institution intelligence | Cross-bureau coordination | Human-in-the-loop AI |
|:---|:---|:---|
| One institution profile links cases, statuses, and officers. | Potential RB–PGRC overlap alerts highlight coordination needs. | Advisory category and related-case suggestions support officer review. |

## ✦ System architecture

<div align="center">

<a href="https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/">
  <img src="assets/system-architecture.png" alt="Interactive technology architecture preview" width="680" />
</a>

**[Open interactive technology architecture](https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/)**

</div>

The live link requires **GitHub Settings → Pages → Deploy from a branch → main → /docs** and an actual `docs/index.html` file committed to the `main` branch. You can also [view the HTML source](docs/index.html). GitHub README pages cannot execute interactive JavaScript.

<details>
<summary><b>Architecture explanation</b></summary>

1. **Users:** Students, officers, institutions, and administrators.
2. **Frontend:** React + Vite for forms, dashboards, case views, and graphs.
3. **Backend:** Python + FastAPI for endpoints and workflows.
4. **Intelligence & data:** SQLite and rule-based complaint checks; SBERT and TF-IDF are proposed enhancements.
5. **Outputs:** Officer workspace, institution profiles, relationship graphs, reports, and alerts.

</details>

## ✦ Platform modules

<details open>
<summary><b>01 — Student grievance portal</b></summary>

Students select an institution, submit grievance details, and track case status.

</details>

<details>
<summary><b>02 — Officer dashboard & case workspace</b></summary>

Authorized officers inspect cases, assignments, remarks, status changes, and action history.

</details>

<details>
<summary><b>03 — Institution intelligence profile</b></summary>

Institution records connect complaint history, categories, bureau assignments, and officers.

</details>

<details>
<summary><b>04 — RB–PGRC coordination alerts</b></summary>

Potentially overlapping active cases can be flagged for authorized officer review.

</details>

<details>
<summary><b>05 — Relationship graph & reporting</b></summary>

Visual relationships link institutions, complaints, bureaus, and officers; reporting summarizes case history.

</details>

## ✦ AI-assisted intelligence

Current prototype screenshots show **rule-based category suggestions** and **potential duplicate detection**. The following NLP methods are **proposed enhancements**, not verified deployed models.

| Model / method | Intended role |
|:---|:---|
| Sentence-BERT (`all-MiniLM-L6-v2`) | Semantic complaint embeddings |
| TF-IDF | Keyword similarity baseline |
| Cosine similarity | Similarity scoring |
| Python rules | Institution, status, and bureau overlap checks |
| SLA rules | Deadline monitoring |

```mermaid
flowchart TD
    A[New grievance] --> B[Check institution ID]
    B --> C[Find related institution cases]
    C --> D[Rule-based checks]
    D --> E[Advisory related-case suggestion]
    E --> F[Authorized officer review]
    F --> G[Record action]
```

## ✦ Technology stack

| Layer | Technology | Purpose |
|:---|:---|:---|
| Frontend | React + Vite | Interactive web interface |
| Backend | Python + FastAPI | REST endpoints and workflows |
| Database | SQLite | Prototype records |
| Current intelligence | Python rules | Advisory category and case checks |
| Proposed NLP | Sentence Transformers, scikit-learn | Semantic and keyword similarity |
| Access | Role-based permissions | Authorized workflows |

## ✦ Demo journeys

**Complaint to officer review:** Student submits a grievance → case is stored → related-case checks run → officer reviews and records actions.

**Potential cross-bureau overlap:** Related RB and PGRC complaints → advisory flag → officer verification → documented coordination decision.

## Application screenshots

<details>
<summary><strong>🖼️ View all 10 application screenshots (click to expand / collapse)</strong></summary>

<p>Click the section heading above again to close and return to this position.</p>

<p align="center"><strong>Complaint submission</strong></p>
<p align="center"><img src="assets/screenshots/case-submission.png" alt="Complaint submission" width="440" /></p>

<p align="center"><strong>Officer workspace and case assignment</strong></p>
<p align="center"><img src="assets/screenshots/officer-case-assignment.png" alt="Officer workspace and case assignment" width="440" /></p>

<p align="center"><strong>Officer communication</strong></p>
<p align="center"><img src="assets/screenshots/officer-chat.png" alt="Officer communication" width="440" /></p>

<p align="center"><strong>File attachments</strong></p>
<p align="center"><img src="assets/screenshots/officer-chat-attachment.png" alt="File attachments" width="440" /></p>

<p align="center"><strong>Institution intelligence profile</strong></p>
<p align="center"><img src="assets/screenshots/institution-profile.png" alt="Institution intelligence profile" width="440" /></p>

<p align="center"><strong>Institution relationship network</strong></p>
<p align="center"><img src="assets/screenshots/relationship-graph-institution.png" alt="Institution relationship network" width="440" /></p>

<p align="center"><strong>Case relationship network</strong></p>
<p align="center"><img src="assets/screenshots/relationship-graph-case.png" alt="Case relationship network" width="440" /></p>

<p align="center"><strong>AI-assisted case intelligence</strong></p>
<p align="center"><img src="assets/screenshots/ai-case-intelligence.png" alt="AI-assisted case intelligence" width="440" /></p>

<p align="center"><strong>Historical reporting</strong></p>
<p align="center"><img src="assets/screenshots/historical-reporting.png" alt="Historical reporting" width="440" /></p>

<p align="center"><strong>Historical reporting by status</strong></p>
<p align="center"><img src="assets/screenshots/historical-reporting-status.png" alt="Historical reporting by status" width="440" /></p>

</details>

**[Open interactive screenshot gallery](https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/gallery.html)** (requires GitHub Pages to be enabled).

## ✦ Responsible use

Student grievances may contain sensitive personal information. Do not commit real complaints, credentials, or private institution records to a public repository. Use synthetic records and enforce permissions on the backend. AI suggestions are advisory and require human review.

---

<div align="center">

**AICTE GRIEVANCE INTELLIGENCE SYSTEM**

*Institutional visibility · Connected workflows · Responsible AI*

<sub>Smart India Hackathon 2026 · Educational prototype · Not affiliated with or endorsed by AICTE</sub>

</div>
