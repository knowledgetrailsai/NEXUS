# Function: Finance & Accounting

`Home › 02-functions › Finance & Accounting`

## Why This Function Is a Strong Fit

Structured documents, deterministic validation rules, and clear ground truth (does the math reconcile) make finance one of the most tractable functions for agentic automation — and one of the best-suited to the [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum) cost/value density model, since outcomes are usually unambiguous.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Invoice Processing & 3-Way Match Agent](../05-use-cases/invoice-processing-3way-match-agent.md) | Extraction & Structured Validation | L2 → L3 |
| [Expense Audit Agent](../05-use-cases/expense-audit-agent.md) | Continuous Monitoring & Flagging | L2 → L3 |

Other credible patterns (financial close reconciliation support, forecast variance commentary) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## Domain Applicability

| Domain | Notes |
|---|---|
| [Manufacturing](../03-domains/manufacturing.md), [Retail & CPG](../03-domains/retail-cpg.md) | Core — high transaction volume, PO-driven processes |
| [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md) | Core, with materially higher regulatory reporting requirements |
| [Technology & SaaS](../03-domains/technology-saas.md) | Core — subscription billing and revenue recognition add specific variants |
| [Healthcare](../03-domains/healthcare.md), [Public Sector](../03-domains/public-sector.md) | Applies generically, often with additional grant/fund accounting rules |

## Key Cross-Cutting Risks

- Errors compound silently in high-volume, low-unit-value transactions until an audit surfaces them — see [Value Leakage](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/03-value-economics/value-leakage.md)
- Threshold-based autonomy (L4) requires strong audit logging — never remove human traceability entirely
- Segregation-of-duties controls must be preserved even when a single agent could technically perform multiple steps

---

**Previous:** [HR & People](hr-people.md)
**Next:** [IT & Security](it-security.md)
