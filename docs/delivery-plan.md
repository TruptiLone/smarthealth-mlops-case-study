# Delivery plan and team process

The academic project and the hypothetical product rollout use different timelines. Course materials describe three academic sprints for proposal/report/pitch work; the later product plan describes four four-week sprints. The latter is a proposed delivery roadmap, not evidence of sixteen weeks of completed engineering.

## Personas and scope

| Persona | Role in the scenario | Core need |
|---|---|---|
| David Lee | Compliance and regulatory architect | Data protection controls and auditable handling |
| Alex Johnson | Tier-1 consultant | Category, priority, and resolution suggestions with human control |
| Jordan Miller | Resident field technician | Better onsite/remote distinction and fewer unnecessary dispatches |

Earlier persona drafts include additional stories and different numbering. This guide follows the later sprint milestone document.

## Proposed sprint sequence

| Sprint | Focus | Stories |
|---|---|---|
| 1 | PHI identification, sensitivity classification, redaction | 1.1–1.3 |
| 2 | Sanitized-only pipeline, PHI audit trail, first category/priority suggestions | 1.4–1.5, 2.1 |
| 3 | Resolution suggestions, confidence, accept/reject, decision logs | 2.2–2.5 |
| 4 | Onsite/remote distinction, routine-ticket filtering, escalation logs | 3.1–3.3 |

The key dependency is explicit: establish data-handling controls before expanding ML-assisted triage. Human rejection must not block manual ticket processing.

## Planning methods

The team used Kano categories, MoSCoW priority labels, Fibonacci-style sizing, and Weighted Shortest Job First (WSJF). The draft defines WSJF as business value plus time criticality plus risk reduction, divided by job size. Dependencies constrain execution order even when a later story has a higher score.

The pitch says 70 story points. The 13 story-level estimates shown in the earlier draft total 56 points (26 + 19 + 11). No reconciled estimate table establishing the increase was found, so neither number is presented as verified delivery velocity.

## Retrospective

The supplied retrospective reports that shared scope, architecture discussions, distributed responsibilities, and regular communication helped the team. It also records that DevOps/MLOps integration and technical dependencies took longer than expected.

The team's next-step actions were to break down larger stories, identify dependencies earlier, document architecture decisions sooner, keep a shared task board, and use regular check-ins.

## Contributions and attribution

The documents name Aryan Puranik, Maheshwari Bhandare, Senit Ghile, and Trupti Lone. Internal task notes associate Trupti with research, personas, user stories, sizing, testing, release planning, sprint milestones, and shared MLOps work. Role labels vary across proposal and pitch drafts; this collection credits the team without treating every working assignment as confirmed sole authorship.

Sources: [sprint milestones](originals/sprint-milestones.docx), [retrospective](originals/sprint-retrospective.docx), and the local annotated draft report.
