# Function: Customer Relations & Support

`Home › 02-functions › Customer Relations & Support`

## Why This Function Is a Strong Fit

High volume, well-documented resolution paths, and a clear success signal (resolved without escalation) make support one of the most mature and widely deployed agentic AI functions today — see the fully worked [oasis-fulcrum case study](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/10-case-studies/customer-support-agent.md) built on this exact pattern.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Tier-1 Support Resolution Agent](../05-use-cases/tier1-support-resolution-agent.md) | Classification & Routing | L2 → L3 |
| [Churn Prevention Agent](../05-use-cases/churn-prevention-agent.md) | Forecasting & Pattern Detection | L1 → L2 |
| [Student Services Case Routing Agent](../05-use-cases/student-services-case-routing-agent.md) | Classification & Routing | L2 → L3 |
| [Constituent Service Request Routing Agent](../05-use-cases/constituent-service-request-agent.md) | Classification & Routing | L2 → L3 |

Other credible patterns in this function (sentiment monitoring, post-interaction summarization, complaint triage) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md) to add one.

## Domain Applicability

| Domain | Notes |
|---|---|
| [Telecom & Media](../03-domains/telecom-media.md), [Retail & CPG](../03-domains/retail-cpg.md) | Core — very high ticket volume, well-structured resolution paths |
| [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md) | Core, with added disclosure/compliance requirements on communications |
| [Technology & SaaS](../03-domains/technology-saas.md) | Core — often the first function automated in this domain |
| [Healthcare](../03-domains/healthcare.md) | Adaptable — patient-facing communication has materially higher stakes; keep clinical questions out of agent scope |
| [Public Sector](../03-domains/public-sector.md), [Manufacturing](../03-domains/manufacturing.md) | Applies generically — citizen services and B2B account support respectively |

## Key Cross-Cutting Risks

- Incorrect resolutions that satisfy the immediate ticket but recur (see [Value Leakage](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/03-value-economics/value-leakage.md))
- Financial actions (refunds, credits) issued without proportional evaluation
- Sensitive account or health information handled outside approved boundaries

---

**Previous:** [Sales](sales.md)
**Next:** [Marketing](marketing.md)
