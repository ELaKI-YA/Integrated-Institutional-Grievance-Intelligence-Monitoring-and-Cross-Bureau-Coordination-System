<div align="center">

<img src="assets/banner.png" alt="AICTE Grievance Intelligence System" width="780" />

<h1>Integrated Institutional Grievance Intelligence, Monitoring and Cross-Bureau Coordination System</h1>

<p><strong>Smart India Hackathon 2026 · AICTE · Prototype</strong></p>
<p><em>One institution. One connected grievance history. Better-informed coordination.</em></p>

</div>

## ✦ The idea

Institutional complaints are often easier to understand **together** than as isolated tickets. This proposed platform connects student grievances, institution identities, officer assignments, and bureau workflows in one institution-centric workspace.

Complaints can be linked using an **AICTE Permanent ID**; official verification is a planned integration. Officers can explore complaint history, inspect potential duplicates, and review advisory coordination alerts across the **Regulation Bureau (RB)** and **Public Grievance Redressal Cell (PGRC)**.

> **Project scope:** Educational SIH prototype, not an official AICTE service. AI suggestions require officer review and do not automatically merge, escalate, or resolve cases.

## ✦ At a glance

| Institution intelligence | Cross-bureau coordination | Human-in-the-loop AI |
|:---|:---|:---|
| One institution profile links cases, statuses, and officers. | Potential RB–PGRC overlap alerts highlight coordination needs. | Advisory category and related-case suggestions support officer review. |

## ✦ Interactive architecture & application gallery

<div align="center">

<a href="https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/" title="Explore the interactive architecture and screenshot gallery">
  <img src="assets/system-architecture.png" alt="Open interactive architecture and animated application gallery" width="680" />
</a>



</div>

<details>
<summary><b>Architecture explanation</b></summary>

<ol>
<li><strong>Users:</strong> Students, officers, institutions, and administrators.</li>
<li><strong>Frontend:</strong> React + Vite for forms, dashboards, case views, and graphs.</li>
<li><strong>Backend:</strong> Python + FastAPI for endpoints and workflows.</li>
<li><strong>Intelligence &amp; data:</strong> SQLite and rule-based complaint checks; SBERT and TF-IDF are proposed enhancements.</li>
<li><strong>Outputs:</strong> Officer workspace, institution profiles, relationship graphs, reports, and alerts.</li>
</ol>

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

## ✦ Application screenshots

<div align="center">
<a href="https://elaki-ya.github.io/Integrated-Institutional-Grievance-Intelligence-Monitoring-and-Cross-Bureau-Coordination-System/#screenshots">
<img src="assets/stacked-gallery-preview.png" alt="Application screenshot gallery" width="680" />
</a>
</div>


## ✦ Responsible use

Student grievances may contain sensitive personal information. Do not commit real complaints, credentials, or private institution records to a public repository. Use synthetic records and enforce permissions on the backend. AI suggestions are advisory and require human review.

---

<div align="center">

<p><strong>AICTE GRIEVANCE INTELLIGENCE SYSTEM</strong></p>
<p><em>Institutional visibility · Connected workflows · Responsible AI</em></p>

<sub>Smart India Hackathon 2026 · Educational prototype · Not affiliated with or endorsed by AICTE</sub>

</div>
