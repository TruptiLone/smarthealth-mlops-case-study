# Business case and evidence limits

All figures are assumptions or estimates for the fictional SmartHealth scenario. The source files contain multiple versions; they are preserved as historical evidence rather than silently combined into a measured result.

## Later pitch scenario

| Input or estimate | Value stated in the source |
|---|---:|
| Annual ticket volume | 40,000 |
| Manual / assisted triage | 6 / 4 minutes per ticket |
| One-time setup | $35,000 |
| Annual operating expense | $57,000 |
| First-year combined cost | $92,000 |
| Annual benefit estimate | $208,320 |
| Net first-year benefit | $116,320 |
| Reported ROI | Approximately 126% |

The arithmetic `(208,320 − 92,000) / 92,000` is approximately 126.4%. This checks the stated arithmetic only, not whether the benefits would occur.

## Findings from reviewing the drafts

- **Cost labeling:** the pitch calls $92,000 an initial investment, while its breakdown and ROI document identify $35,000 setup plus $57,000 annual operation. The guide uses “first-year combined cost.”
- **Triage target:** six to four minutes is a 33.3% reduction. The proposal's 50% target and the test strategy's 30% target are different planning versions.
- **Time saved:** 40,000 × two minutes is 80,000 minutes, or 1,333.33 hours. The source rounds this to 1,333 and then values it at $53,320 using $40/hour. This is time saved, not total baseline triage time.
- **Potential double counting:** labor productivity value and capacity expansion both use the same recovered hours. The $208,320 headline should not be treated as validated economic value until the benefit categories are reconciled.
- **Revenue versus profit:** the later ROI narrative describes $5 per extra ticket as profit contribution; the pitch labels the resulting $100,000 as new revenue. The basis is inconsistent.
- **SLA and rework:** the later ROI file uses $12,000 and $16,000 as savings, while an earlier working document describes those same amounts as baselines before applying reductions. The versions imply different benefits.
- **Payback:** the reported 9.5 months divides first-year combined costs by monthly net benefit after those first-year costs. It is not supported by a consistent, fully specified cash-flow schedule. The repository does not endorse a payback claim.
- **Research dependency:** later planning excludes research costs from the CIO/CDTO budget. That is a scope assumption, not zero economic cost for research.

Other drafts show $80,000 costs and 160% or 201% ROI. Those alternatives remain in the local review materials. A reconciled financial model would require explicit decisions about the baseline, ramp-up, benefit overlap, cost timing, and research cost boundary.

## Unverified outcomes

No experiment output, held-out model score, operational before/after dataset, executed release evidence, or completed compliance assessment was supplied. Claims such as fully automated compliance, achieved response improvements, and guaranteed savings are therefore not adopted as portfolio outcomes.

Sources: [pitch](originals/project-pitch.pdf) and [later ROI scenario](originals/roi-scenario.docx). This review evaluates internal consistency in the supplied material; it does not validate its external market benchmarks.
