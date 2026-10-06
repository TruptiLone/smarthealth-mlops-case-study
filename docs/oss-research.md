# OSS research and selection

The team's research moved from broad OSS exploration to a narrowly scoped application of scikit-learn for ticket categorization and urgency prediction. The submitted proposal is the primary source for the selection decision.

## Selection rationale documented by the team

The team favored a focused Python ML component, a consistent API, a mature ecosystem, and the ability to integrate with the assumed service platform. The proposal treats explainability, internal control, and avoiding a wholesale platform replacement as important decision factors.

| Option considered | Role in the team's comparison | Scope conclusion |
|---|---|---|
| scikit-learn | ML classification and prediction component | Selected for the ticket intelligence layer |
| OpenEMR | EHR and practice-management platform | Broader than the chosen ticket-triage problem |
| Medplum | Healthcare application and interoperability platform | Addresses a different platform layer |

This is a comparison of possible project directions, not an algorithm benchmark between interchangeable ML libraries. Early research also explored infrastructure and language-model projects; those notes remain in the original archive rather than expanding the portfolio's final scope.

## OSS adoption concerns

The project research discusses dependency management, maintainability, community governance, licensing, and avoiding vendor dependence. The risk register proposes dependency pinning, monitoring changes, staged validation, and manual fallback. These are adoption and governance considerations; the collection contains no lockfile, dependency audit, or upstream contribution evidence.

The original proposal and draft include third-party statements and historical research links. This organizational pass did not revalidate external claims or current licensing details. Those claims are not presented as newly verified research here.

Source: [submitted proposal](originals/project-proposal.docx), supported by the annotated draft report and early OSS notes retained locally.
