# SmartHealth — Integrating Machine Learning into CI/CD

A software project management case study exploring how a fictional healthcare IT consultancy could introduce **scikit-learn–assisted ticket triage** through an existing DevOps delivery process.

The team took a research-lab approach: experiment with machine learning in a research environment, transfer validated models and pipelines to engineering, and manage releases through CI quality gates, staging, production promotion, and monitoring.

**Project status:** academic research, architecture, and delivery planning. This repository contains the team's documentation and diagrams, with a curated reading guide. The supplied materials do not include executable training code, CI/CD configuration, deployment logs, or measured model results. Business benefits are scenario estimates and targets.

## The business problem

SmartHealth is a roleplay consultancy of approximately 80–100 employees supporting hospitals and clinics. Its existing service platform uses Salesforce for support cases and service-level tracking. Tier-1 staff manually interpret ticket descriptions, assign category and urgency, and choose a resolution path. The proposed automation adds machine learning assistance to that workflow while keeping consultants responsible for final decisions.

## What this project showcases

- Selecting an OSS component for a defined business problem and examining alternatives.
- Connecting research experimentation with DevOps and MLOps responsibilities.
- Designing a training, validation, model registry, serving, and monitoring lifecycle.
- Planning controlled releases through feature and ML experiment branches.
- Translating personas into user stories, sprint milestones, test criteria, and risk controls.
- Evaluating an automation business case while documenting assumptions and limitations.

## Product management highlights

The team's OSS Project draft report (slides) frames the work the way a product team would: problem → measurable goals → prioritized backlog → milestone roadmap → business case → risk and change management. The highlights below are drawn from that deck.

### Problem, current state, and target state

Support tickets arrive omni-channel into a single Salesforce queue with inconsistent categories, urgency levels, and free-text descriptions. Tier-1 staff manually review, reclassify, and route every ticket across internal, vendor, remote, and onsite teams — slowing initial response, increasing routing errors and cognitive load, and (because unstructured tickets may contain PHI) raising compliance risk. The target state: incoming tickets are automatically analyzed and categorized with ML-assisted sorting, high-impact and clinically sensitive issues are escalated faster, and IT teams focus on resolution quality rather than manual triage — with every ML suggestion remaining advisory under human control.

### SMART goals

| Goal | Target (within 8–12 weeks of deployment) |
|---|---|
| Reduce manual triage time | ≥ 50% reduction in average ticket triage time via automated classification at intake |
| Improve routing accuracy | 30% reduction in ticket misrouting and reassignment |
| Increase critical issue response | 25% faster response for high/critical clinical tickets |

### Product roadmap

Four milestones, deliberately sequenced so compliance comes first and ML authority is earned incrementally — read-only suggestions before human-approved actions, and filtering only after trust is established:

| Milestone | Expected outcome | Success measures |
|---|---|---|
| **M1 — Compliance-Safe Ticket Ingestion Foundation** | All tickets cleaned and sanitized before storage or ML use; PHI automatically identified, masked, and logged; compliance and audit controls in place | 100% of tickets sanitized before storage; PHI detection/masking logs available; audit logs include timestamps and actions |
| **M2 — ML-Assisted Ticket Triage (Read-Only)** | ML suggests category, priority, and resolution path with confidence scores; ML does not auto-route | ≥ 30% reduction in manual triage time; suggestions shown for most tickets; no tickets auto-routed by ML |
| **M3 — Human-in-the-Loop ML Control** | Users accept or reject ML suggestions; accepted suggestions update the ticket; all triage decisions recorded | ≥ 80% of routine tickets accepted without changes; accept/reject actions logged with user ID; no workflow blocked by ML |
| **M4 — Smart Filtering & Onsite Escalation** | Tickets marked onsite vs. remote; low-priority issues filtered from onsite queues; only high-confidence issues sent onsite | Fewer unnecessary onsite escalations; faster response to real physical issues; escalation decisions fully logged |

### Backlog and delivery

- **Prioritization:** user stories across three epics (compliance-safe ingestion, ML-assisted service desk triage, smart filtering & onsite escalation) scored with **KANO**, **MoSCoW**, and **WSJF** (value, time criticality, risk vs. job size) — audit logging and human accept/reject controls consistently ranked as Must-haves ahead of ML suggestion features.
- **SDLC:** a blended **Scrum + XP** model — Scrum governs planning, prioritization, and sprint reviews; XP practices (pair programming on ML classification logic and Salesforce integrations, small testable increments, continuous integration) govern execution.
- **Sprint plan:** three program-level sprints — Discovery & Design (problem clarity, architecture, OSS selection, backlog), Implementation (data pipeline, scikit-learn classification, routing logic, PHI detection/redaction, validation), and Release Planning (deployment, rollout, monitoring, adoption strategy) — tracked with a cumulative story-point burnup.

### Business case (scenario estimates)

Modeled on assumed volumes (~40,000 tickets/year): **≈ $94,300 estimated annual savings** across triage labor, SLA breach reduction, misrouting rework, onsite dispatch reduction, and critical-incident downtime, against a **≈ $35,000 one-time investment** — a **~4.5-month payback** and **~169% first-year ROI**. See [Business case and evidence limits](docs/business-case.md) for assumptions and conflicting drafts; these are targets, not measured results.

### Risk and change management

- **Risk analysis:** likelihood × impact scoring with mitigations mapped to specific user stories — e.g., operational scalability (20) mitigated by ML-assisted categorization with human accept/reject; clinical misclassification (10) by conservative confidence thresholds and manual override; PHI exposure (5) by automated detection, mandatory redaction, and sanitized-only ML pipelines.
- **OSS software-disaster plan:** version pinning of scikit-learn and upstream dependencies, CVE monitoring, staged deployments with regression tests, model/version traceability per prediction, manual fallback mode, and rollback to last-known-stable — with all ML outputs remaining advisory.
- **Change management:** a Lewin Unfreeze–Change–Refreeze adoption plan — leadership and compliance buy-in, phased rollout (recommend-only before acting), training with a "critical vs. routine" cheat sheet, then standardizing the new triage process and reinforcing with tracked wins at sprint reviews.

## Start here

| Document | What it covers |
|---|---|
| [Project report](docs/project-report.md) | Company context, research approach, architecture, and conclusions |
| [Pipeline and release design](docs/pipeline-and-releases.md) | Original diagrams, CI/CD integration, ownership, and testing |
| [OSS research](docs/oss-research.md) | Why the team chose scikit-learn and how alternatives were considered |
| [Delivery plan](docs/delivery-plan.md) | Personas, 13-story scope, four proposed sprints, and retrospectives |
| [Business case and evidence limits](docs/business-case.md) | Scenario inputs, conflicting ROI figures, and unresolved assumptions |

## ML pipeline design

![Original SmartHealth ML pipeline showing research, CI, training, registry, serving, and monitoring](assets/diagrams/mlops-pipeline.png)

Extracted unchanged from the team's DevOps/MLOps workflow document. It describes the proposed operating model; it is not a record of a deployed system.

## Original documents

The team's eight source documents, retained unchanged with descriptive filenames. Open the PDF to read in the browser, or download the original Word file. They preserve the team's original diagrams, tables, references, and wording; the curated guides above explain where drafts conflict.

| Document | What it covers | Open |
|---|---|---|
| Project proposal | Submitted business context and OSS selection | [PDF](docs/originals/project-proposal.pdf) · [DOCX](docs/originals/project-proposal.docx) |
| Technical workflow | Primary CI/CD, MLOps, release, and testing source | [PDF](docs/originals/devops-mlops-release-and-testing.pdf) · [DOCX](docs/originals/devops-mlops-release-and-testing.docx) |
| Sprint milestones | Later 13-story roadmap and acceptance criteria | [PDF](docs/originals/sprint-milestones.pdf) · [DOCX](docs/originals/sprint-milestones.docx) |
| Retrospective | Team process and lessons | [PDF](docs/originals/sprint-retrospective.pdf) · [DOCX](docs/originals/sprint-retrospective.docx) |
| Company and platform | Roleplay service and platform assumptions | [PDF](docs/originals/company-and-platform-overview.pdf) · [DOCX](docs/originals/company-and-platform-overview.docx) |
| Risk register | Risk scoring and mitigation planning | [PDF](docs/originals/risk-register.pdf) · [DOCX](docs/originals/risk-register.docx) |
| Project pitch | Executive presentation dated March 11, 2026 | [PDF](docs/originals/project-pitch.pdf) |
| ROI scenario | Later financial assumptions, subject to reconciliation | [PDF](docs/originals/roi-scenario.pdf) · [DOCX](docs/originals/roi-scenario.docx) |

### Figure sources

| Image | Source |
|---|---|
| [MLOps pipeline](assets/diagrams/mlops-pipeline.png) | Technical workflow document, Figure 1 |
| [Release workflow](assets/diagrams/release-workflow.png) | Technical workflow document, Figure 2 |
| [Earlier ML lifecycle](assets/diagrams/early-ml-lifecycle.png) | Annotated draft report (slides) |
| [Organization structure](assets/diagrams/organization-structure.png) | Annotated draft report (slides) |

Images were extracted directly from the source files without redrawing or changing labels.

## Team

Trupti Lone · Aryan Puranik · Maheshwari Bhandare · Senit Ghile 

Course context: ISBA 2408 OSS project. SmartHealth, its staff personas, customer scenarios, service volumes, and financial projections are part of the academic simulation. The project is about applying an OSS library; it does not claim contributions to the upstream scikit-learn project.

## Repository contents

```text
assets/diagrams/       Original figures extracted from team documents
docs/                 Curated Markdown report and supporting guides
docs/originals/        Essential source documents, retained unchanged (PDF + DOCX)
```

Original documents preserve the team's historical wording, including draft claims and inconsistent estimates. Use the curated guides for the current portfolio framing. No license has been assigned to the team's documents; scikit-learn's license does not automatically license this collection.
