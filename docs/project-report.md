# SmartHealth project report

This curated report consolidates the supplied academic project materials. The project examines how an existing healthcare IT service organization could operationalize machine learning through its established CI/CD process. Its contribution is the research, architecture, project planning, and governance design documented by the team.

## Company and existing service model

SmartHealth is a fictional healthcare IT consultancy based in Silicon Valley with approximately 80–100 employees. It supports hospital and clinic IT operations through remote service desks and onsite technicians. The scenario includes clinical application support, infrastructure, vendor escalation, and service continuity.

The platform documents describe Salesforce Service Cloud as the case system of record and Experience Cloud as a customer portal. PostgreSQL stores structured ticket and ML metadata; object storage holds datasets, model artifacts, and logs. These are architectural assumptions in the roleplay company.

## Problem and scope

Manual interpretation of free-text tickets creates a bottleneck. Staff must determine the category, urgency, responsible team, and whether resolution requires a vendor, remote support, or an onsite technician. The project proposes an intelligence layer that recommends these attributes using historical ticket patterns.

The selected OSS is scikit-learn. The project scope is ticket decision support and its delivery lifecycle. The initial workflow keeps recommendations advisory, exposes confidence information, allows human acceptance or rejection, and records decisions. Early notes occasionally suggest automatic routing; the later sprint and test documents provide the clearer human-review scope.

## Research-to-product approach

The workflow document describes an HP Labs-inspired transition model. Researchers under the CDO experiment with data preparation, features, classification models, and evaluation. Engineering under the CIO operationalizes the research artifacts through version control, automated validation, release promotion, and service monitoring.

The distinction matters because a promising research model alone is not the complete service. The proposed handoff includes preprocessing logic, model artifacts, validation procedures, experiment metadata, and deployment integration. Research effort is treated as an external dependency in the later operating-budget scenario.

## Extending the existing CI/CD process

The assumed existing DevOps process supplies Git branching, CI builds and tests, staging, controlled production releases, and operational monitoring. The ML extension adds dataset preparation, feature engineering, model training and evaluation, a model registry, prediction serving, and feedback-driven retraining.

Application changes and ML experiments pass through shared quality controls. The release design separates DevTest, staging, and production and describes protected production access, patch releases, and hotfixes. [Pipeline and release design](pipeline-and-releases.md) contains the original figures and a stage-by-stage explanation.

## Project management approach

Scrum supplies planning, prioritization, reviews, and retrospectives; XP supplies the proposed engineering practices, including test-first development, pair programming, small increments, and continuous integration. Personas anchor the backlog in service desk, field technician, and data-protection needs.

The later plan organizes 13 stories into four proposed four-week delivery sprints. This product plan is distinct from the academic project's three-sprint reporting schedule. The available retrospective records strong scope alignment and collaboration, alongside underestimated integration dependencies and a need for earlier architecture documentation.

## Validation and risk

The test strategy specifies checks for data sanitization, classification, routing recommendations, confidence boundaries, human review, audit logging, and monitoring. Its numeric thresholds are acceptance targets, not observed results. The risk register covers incorrect critical-ticket classification, data quality, sensitive-data exposure, integration failure, adoption, downtime, and OSS dependencies.

The source documents frame PHI detection and redaction as an intended control. They do not establish a working redaction implementation or independently validated compliance. The portfolio therefore does not reproduce claims of guaranteed or fully automated compliance as achieved outcomes.

## What the evidence supports

The supplied work supports a case study of OSS adoption, MLOps architecture, release governance, and software project management. It includes a submitted proposal, an annotated draft report, a pitch, technical workflow and testing documentation, sprint materials, and business analysis. No final consolidated report or executable SmartHealth implementation was identified in the inspected folder.

The principal lesson documented by the retrospective is that moving ML research into an existing delivery process introduces coordination and integration dependencies that must be reflected in scope, estimates, ownership, and release criteria.

Sources: [proposal, platform overview, workflow, sprint milestones, retrospective, and risk register](source-index.md). The local review collection preserves the annotated draft report separately.
