# Function: Research & Development

`Home › 02-functions › Research & Development`

## Why This Function Is a Strong Fit — With Caveats

R&D work is bimodal: a large share of it (literature review, protocol drafting, data tabulation, documentation) is exactly the kind of structured synthesis agentic AI handles well, while the actual scientific judgment — interpreting ambiguous results, deciding what to test next, forming a hypothesis — remains firmly human territory. The opportunity is compressing the surrounding work, not the thinking itself.

**In plain terms:** researchers spend a lot of time reading, summarizing, and writing up before and after the actual experiment — an agent can do a first pass on all of that, so the researcher spends more of their time on the part only they can do.

**For business readers:** research cycle time is frequently the real bottleneck to market — not the experiment itself, but the weeks spent on literature review before it and documentation after it. Compressing that surrounding work shortens time-to-decision without touching the part of the process that carries the most risk if rushed.

**For technical readers:** this typically means retrieval-augmented synthesis over literature databases and internal knowledge repositories with strict citation discipline, integration with electronic lab notebook (ELN) or lab information management system (LIMS) data for tabulation support, and drafting support for protocols and reports — never autonomous experimental design or result interpretation.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Literature Review & Research Synthesis Agent](../05-use-cases/literature-review-research-synthesis-agent.md) | Synthesis & Drafting | L1 |

Other credible patterns (experimental protocol drafting, results tabulation, regulatory/IP submission assembly) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## Domain Applicability

| Domain | Notes |
|---|---|
| [Scientific Research & Life Sciences R&D](../03-domains/scientific-research.md) | Core — this is the function's primary home |
| [Healthcare](../03-domains/healthcare.md) | Adaptable — clinical research and trials-adjacent documentation, kept separate from clinical care itself |
| [Technology & SaaS](../03-domains/technology-saas.md), [Manufacturing](../03-domains/manufacturing.md) | Applies generically — applied/product R&D and technical documentation |

## Key Cross-Cutting Risks

- **This function should stay at L1 as a near-permanent posture for anything feeding a publication, patent filing, or regulatory submission** — the cost of an unverified claim slipping through is high and often irreversible
- Literature synthesis is uniquely exposed to fabricated or misattributed citations — verification against the actual source is not optional
- Data provenance and reproducibility requirements are stricter here than in most business functions in this repository

---

**Previous:** [Claims Management](claims-management.md)
**Next section:** [03-domains](../03-domains/financial-services.md)
