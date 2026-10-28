
<p align="center">
  <img src="assets/banner.png" alt="AICTE Grievance Intelligence System Banner" width="100%">
</p>

<h1 align="center">AICTE GRIEVANCE INTELLIGENCE SYSTEM</h1>

<p align="center">
  <strong>Integrated Institutional Grievance Intelligence, Monitoring and Cross-Bureau Coordination System</strong>
</p>

<p align="center">
  Smart India Hackathon 2026 • AICTE • Artificial Intelligence • Institutional Monitoring • Cross-Bureau Coordination
</p>

---



# Table of Contents

- Overview
- Problem Statement
- Project Objectives
- Key Features
- Technology Stack
- Why Our Solution?
- System Architecture
- Project Modules
- Artificial Intelligence and Machine Learning
- System Workflows
- Application Screenshots
- Project Structure
- Running Locally
- Demonstration
- Future Enhancements
- Team 
- License

---

# Overview

The **AICTE Grievance Intelligence System** is an AI-assisted, institution-centric platform designed to support grievance monitoring, institutional analysis, and coordination between the **Regulation Bureau (RB)** and **Public Grievance Redressal Cell (PGRC)**.

The system connects complaints with verified institutional records using the **AICTE Permanent ID**.

It provides a centralized environment for student grievance submission, officer case management, institutional complaint history, AI-assisted similarity detection, cross-bureau alerts, and grievance analytics.

The platform is designed to help authorized officers identify related complaints, understand institutional grievance patterns, and coordinate case handling more effectively.

---

# Problem Statement

Institutional grievances can involve multiple students, officers, and administrative bureaus.

When records are managed separately, it becomes difficult to:

- Identify repeated complaints against the same institution.
- Detect related grievances across RB and PGRC.
- Access a consolidated institutional complaint history.
- Monitor complaint progress and deadlines.
- Coordinate actions between responsible officers.
- Analyze recurring grievance patterns.

A centralized grievance intelligence platform can address these challenges through structured case management and AI-assisted analysis.

---

# Project Objectives

The primary objectives are:

- Centralize institution-wise grievance records.
- Connect complaints through verified AICTE Permanent IDs.
- Identify potentially similar or duplicate complaints.
- Detect possible RB–PGRC case overlaps.
- Improve officer coordination and accountability.
- Monitor grievance status and resolution deadlines.
- Visualize institution–complaint–bureau–officer relationships.
- Generate institutional grievance reports and analytics.
- Maintain human oversight of AI-assisted suggestions.

---

# Key Features

| Student Services | Officer Management | AI Intelligence |
|------------------|--------------------|-----------------|
| Complaint Submission | Officer Dashboard | Semantic Similarity |
| Complaint Tracking | Case Assignment | Duplicate Suggestions |
| Status Updates | Case Transfers | Cross-Bureau Alerts |
| Institution Selection | Officer Remarks | Institution Matching |
| Complaint History | SLA Monitoring | Recurring Case Patterns |
| Supporting Details | Reports and Analytics | Priority Indicators |

---

# Technology Stack

| Category | Technology |
|----------|------------|
| Frontend | React.js, Vite |
| Backend | Python, FastAPI |
| Database | SQLite |
| Machine Learning | Sentence Transformers, Scikit-learn |
| Semantic Model | SBERT (`all-MiniLM-L6-v2`) |
| Text Similarity | TF-IDF, Cosine Similarity |
| Rule Engine | Python |
| API Communication | REST API, JSON |
| Security | Role-Based Access Control |
| Version Control | Git, GitHub |

The proposed stack uses free and open-source software. Cloud deployment may involve hosting costs.

---

# Why Our Solution?

Traditional grievance management workflows may provide complaint registration and tracking without presenting a consolidated view of related institutional cases across administrative bureaus.

Our solution combines:

- Institution-centric grievance records.
- AI-assisted semantic complaint matching.
- Cross-bureau coordination alerts.
- Centralized officer workspaces.
- Relationship-based grievance visualization.
- Deadline monitoring and reporting.

The platform emphasizes **human-reviewed AI intelligence** rather than automatic administrative decisions.

---

# System Architecture

<p align="center">
  <img src="assets/system-architecture.png" alt="AICTE System Architecture" width="95%">
</p>

## Architecture Flow

```text
                    SYSTEM USERS
                         |
        +----------------+----------------+
        |                |                |
     Students         Officers       Administrators
        |                |                |
        +----------------+----------------+
                         |
                    REACT + VITE
                         |
                    REST API / JSON
                         |
                    PYTHON FASTAPI
                         |
         +---------------+---------------+
         |               |               |
       SQLITE        AI / NLP        RULE ENGINE
         |               |               |
   Institution        SBERT          RB–PGRC
   Records            TF-IDF         Overlap
   Complaints         Cosine         Detection
   Case History       Similarity     SLA Rules
         |               |               |
         +---------------+---------------+
                         |
                   API RESPONSES
                         |
                    REACT FRONTEND
                         |
          +--------------+--------------+
          |              |              |
       Officer       Institution    Relationship
      Dashboard        Profile         Graph
                         |
                  Reports & Alerts
```

The React frontend renders dashboards, reports, and alerts using information returned by FastAPI.

---

# Project Modules

<details>
<summary><b>1. Student Grievance Portal</b></summary>

### Features

- Submit institutional complaints.
- Select or identify the concerned institution.
- Enter grievance descriptions.
- Provide relevant supporting information.
- Track complaint status.
- View complaint updates.

### Purpose

Provide students with a structured interface for grievance registration and tracking.

</details>

---

<details>
<summary><b>2. Officer Dashboard</b></summary>

### Features

- View assigned grievances.
- Access institution-wise complaint records.
- Review AI-assisted alerts.
- Update complaint status.
- Record officer remarks.
- Transfer or escalate cases.
- Monitor deadlines.

### Purpose

Support authorized officers in managing and coordinating grievance cases.

</details>

---

<details>
<summary><b>3. Institution Intelligence Profile</b></summary>

### Features

- AICTE Permanent ID.
- Institution details.
- Associated complaints.
- Complaint categories.
- Bureau assignments.
- Case statuses.
- Institutional grievance history.

### Purpose

Create a unified institution-centric view of grievance activity.

</details>

---

<details>
<summary><b>4. AI-Assisted Complaint Analysis</b></summary>

### Technologies

- SBERT
- `all-MiniLM-L6-v2`
- TF-IDF
- Cosine Similarity
- Python matching rules

### Features

- Semantic complaint comparison.
- Keyword similarity analysis.
- Potential duplicate suggestions.
- Related complaint identification.
- Institution-aware matching.

### Purpose

Help officers recognize related grievances even when complaint descriptions use different wording.

</details>

---

<details>
<summary><b>5. Cross-Bureau Coordination</b></summary>

### Features

- Identify complaints associated with the same institution.
- Check related active cases across RB and PGRC.
- Generate potential overlap alerts.
- Present linked case details for officer review.
- Support coordination through officer workflows.

### Alert Message

**Potential Overlapping Cases – Coordination Required**

### Purpose

Improve visibility into cases that may require coordination between administrative bureaus.

AI alerts do not automatically merge complaints or determine official outcomes.

</details>

---

<details>
<summary><b>6. Relationship Graph</b></summary>

### Relationships

```text
Institution
    |
    +--- Complaint A --- Regulation Bureau --- Officer A
    |
    +--- Complaint B --- PGRC --------------- Officer B
    |
    +--- Complaint C --- Regulation Bureau --- Officer C
```

### Purpose

Visually connect institutions, complaints, bureaus, and officers to reveal related cases and grievance patterns.

</details>

---

<details>
<summary><b>7. Reports and Analytics</b></summary>

### Features

- Institution-wise complaint analysis.
- Bureau-wise grievance reports.
- Regional grievance distribution.
- Complaint status summaries.
- Category-wise trends.
- Deadline monitoring.
- Recurring complaint indicators.

### Purpose

Support institutional monitoring and data-informed administrative review.

</details>

---

# Artificial Intelligence and Machine Learning

The AI/ML module is designed to analyze grievance descriptions and identify potential relationships between complaints.

## Models and Techniques

| Model / Technique | Function |
|-------------------|----------|
| SBERT | Semantic complaint representation |
| `all-MiniLM-L6-v2` | Pretrained sentence embeddings |
| TF-IDF | Keyword-based text representation |
| Cosine Similarity | Complaint similarity scoring |
| Python Rules | Institution and cross-bureau matching |
| SLA Rules | Deadline and priority indicators |

## AI Processing Workflow

```text
             Student Complaint
                    |
                    v
             Text Preprocessing
                    |
                    v
          Institution ID Matching
                    |
                    v
             Text Representation
                    |
          +---------+---------+
          |                   |
          v                   v
     SBERT Model            TF-IDF
          |                   |
          +---------+---------+
                    |
                    v
            Cosine Similarity
                    |
                    v
          Potential Related Cases
                    |
                    v
           RB–PGRC Rule Checking
                    |
                    v
           Advisory Alert Results
                    |
                    v
           Authorized Officer
                 Review
```

## Example

**Complaint A:**

"The college has not returned my admission fee."

**Complaint B:**

"I am still waiting for my refund after cancelling admission."

Although the complaints use different wording, semantic embeddings can help identify their potential relationship.

The system presents possible matches for officer review.

> Model selection, thresholds, and evaluation results must be verified during implementation. No specific detection accuracy is claimed here.

---

# System Workflows

<details>
<summary><b>Student Complaint Workflow</b></summary>

```text
Student Login
     |
     v
Select Institution
     |
     v
Submit Complaint
     |
     v
FastAPI Validation
     |
     v
Store Complaint in SQLite
     |
     v
AI-Assisted Analysis
     |
     v
Officer Dashboard
     |
     v
Complaint Status Updates
```

</details>

---

<details>
<summary><b>Cross-Bureau Coordination Workflow</b></summary>

```text
New Complaint
     |
     v
Verify Institution ID
     |
     v
Retrieve Existing Cases
     |
     v
Compare Complaint Descriptions
     |
     v
Check RB and PGRC Assignments
     |
     v
Potential Overlap Found?
     |
     +------ No ------> Continue Normal Workflow
     |
    Yes
     |
     v
Generate Advisory Alert
     |
     v
Authorized Officer Review
     |
     v
Record Coordination Decision
```

</details>

---

<details>
<summary><b>Officer Case Management Workflow</b></summary>

```text
Officer Dashboard
     |
     v
Open Assigned Case
     |
     v
View Institution Profile
     |
     v
Review Related Complaints
     |
     v
Inspect AI Suggestions
     |
     v
Update / Transfer / Escalate
     |
     v
Record Remarks and Audit Trail
     |
     v
Refresh Dashboard and Reports
```

</details>

---

# Application Screenshots

## Student Grievance Portal

<p align="center">
  <img src="assets/student-portal.png" alt="Student Grievance Portal" width="90%">
</p>

## Officer Dashboard

<p align="center">
  <img src="assets/officer-dashboard.png" alt="Officer Dashboard" width="90%">
</p>

## Institution Intelligence Profile

<p align="center">
  <img src="assets/institution-profile.png" alt="Institution Profile" width="90%">
</p>

## Cross-Bureau Coordination Alert

<p align="center">
  <img src="assets/cross-bureau-alert.png" alt="Cross-Bureau Alert" width="90%">
</p>

## Relationship Graph

<p align="center">
  <img src="assets/relationship-graph.png" alt="Relationship Graph" width="90%">
</p>

> Add your actual screenshots to the `assets/` directory. Remove screenshot sections for interfaces that are not yet available.

---

# Project Structure

```text
AICTE-Grievance-Intelligence-System/
|
├── assets/
│   ├── banner.png
│   ├── system-architecture.png
│   ├── student-portal.png
│   ├── officer-dashboard.png
│   ├── institution-profile.png
│   ├── cross-bureau-alert.png
│   └── relationship-graph.png
|
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── services/
│   └── package.json
|
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models.py
│   └── routes/
|
├── ai_engine/
│   ├── similarity.py
│   ├── duplicate_detection.py
│   └── overlap_detection.py
|
├── docs/
│   └── architecture.html
|
├── tests/
├── requirements.txt
├── .gitignore
├── README.md
└── LICENSE
```

This is the intended repository structure. Adjust it to match the actual implementation.

---

# Running Locally

The following commands assume the repository follows the structure above.

## Prerequisites

- Python 3.10 or later
- Node.js and npm
- Git

## Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

Replace the URL with your actual GitHub repository URL.

## Backend Setup

```bash
python -m venv .venv
```

Activate the virtual environment, then install dependencies:

```bash
pip install -r requirements.txt
```

Start FastAPI:

```bash
uvicorn backend.main:app --reload
```

Backend URL:

```text
http://127.0.0.1:8000
```

FastAPI API documentation:

```text
http://127.0.0.1:8000/docs
```

## Frontend Setup

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite.

> These are example setup commands. Verify them against the completed source code before submission.

---

# Demonstration

## Scenario 1: Student Complaint Submission

A student submits a grievance associated with a specific institution.

**Expected demonstration:**

- The complaint is received by the backend.
- The institution reference is validated.
- The complaint is stored.
- The complaint becomes visible in the authorized officer workflow.

## Scenario 2: Similar Complaint Detection

Two complaints describe a related issue using different wording.

**Expected demonstration:**

- The AI module compares the descriptions.
- A similarity score is calculated.
- Potentially related complaints are suggested.
- An officer reviews the suggestion.

## Scenario 3: RB–PGRC Coordination

Related active complaints concerning the same institution are associated with different bureaus.

**Expected demonstration:**

- The system identifies a potential overlap.
- An advisory coordination alert is generated.
- Authorized officers inspect the related cases.
- Any coordination decision is recorded.

## Scenario 4: Institution Monitoring

An officer opens an institution profile.

**Expected demonstration:**

- Associated complaints are displayed.
- Case statuses and bureau assignments are visible.
- Related records can be explored through the relationship graph.

---

# Future Enhancements

Potential future improvements include:

- Multilingual grievance analysis.
- Advanced institutional trend detection.
- Expanded reporting and visualization.
- Scalable production database infrastructure.
- Integration with authorized grievance platforms.
- Enhanced accessibility and mobile responsiveness.

---


**Team Name:** CYBRIXX



---

# License

Add the repository's chosen license here after selecting and including the appropriate `LICENSE` file.

---

# Disclaimer

This project is developed for educational and hackathon purposes.

It is not an official AICTE platform and does not imply authorization, endorsement, or deployment by AICTE.

---

<p align="center">
  <strong>AICTE GRIEVANCE INTELLIGENCE SYSTEM</strong>
</p>

<p align="center">
  <i>Institutional Intelligence • Transparent Monitoring • Coordinated Grievance Resolution</i>
</p>
