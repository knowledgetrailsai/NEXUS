# Function: Purchasing & Procurement

`Home › 02-functions › Purchasing & Procurement`

## Why This Function Is a Strong Fit

Procurement is document-heavy, rule-bound, and high-volume — three traits that make it consistently one of the earliest and highest-ROI targets for agentic automation across nearly every industry.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Purchase Requisition & Approval Agent](../05-use-cases/purchasing-requisition-approval-agent.md) | Classification & Routing | L2 → L3 |
| [Supplier Risk Monitoring Agent](../05-use-cases/supplier-risk-monitoring-agent.md) | Continuous Monitoring & Flagging | L1 → L2 |

Other credible patterns (spend classification/budget reconciliation, RFP/RFQ response drafting) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md). Contract-term extraction is closely related to [Legal & Compliance: Contract Review](legal-compliance.md).

## Domain Applicability

| Domain | Notes |
|---|---|
| [Manufacturing](../03-domains/manufacturing.md) | Core — high PO volume, tight supplier integration, JIT sensitivity |
| [Retail & CPG](../03-domains/retail-cpg.md) | Core — high SKU count, seasonal supplier volume swings |
| [Healthcare](../03-domains/healthcare.md) | Adaptable — added complexity from regulated/clinical procurement categories |
| [Public Sector](../03-domains/public-sector.md) | Adaptable — procurement rules are often statutory, reducing agent discretion |
| [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md), [Technology & SaaS](../03-domains/technology-saas.md), [Telecom & Media](../03-domains/telecom-media.md) | Applies generically — lower volume, standard patterns apply |

## Key Cross-Cutting Risks

- Approval-routing errors that bypass segregation-of-duties controls
- Supplier risk signals sourced from low-quality or biased external data
- Contract term extraction missing a materially unfavorable clause

See [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI) for full control guidance, particularly around financial approval workflows.

---

**Next:** [Sales](sales.md)
