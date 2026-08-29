# Domain: Insurance

`Home › 03-domains › Insurance`

## Domain Context

Document- and rules-heavy by nature (policies, claims, underwriting guidelines), with a regulatory and fairness overlay similar to financial services. Claims processing is the domain's flagship agentic opportunity — structurally similar to the [Supply Chain & Operations](../02-functions/supply-chain-operations.md) pattern of structured intake, validation, and exception routing.

## Most Relevant Functions

| Function | Relevance | Notes |
|---|---|---|
| [Claims Management](../02-functions/claims-management.md) | Core | This domain's flagship function — see note below |
| [Data & Analytics](../02-functions/data-analytics.md) | Core | Underwriting risk-data assembly |
| [Customer Relations & Support](../02-functions/customer-relations-support.md) | Core | High ticket volume around policy and claims questions |
| [Legal & Compliance](../02-functions/legal-compliance.md) | Core | High contract volume, heavy regulatory overlay |
| [Sales](../02-functions/sales.md) | Adaptable | Suitability/disclosure rules constrain outreach |

## Domain-Exclusive Opportunities

- [Claims Intake & Triage Agent](../05-use-cases/claims-intake-triage-agent.md)
- [Underwriting Risk Data Assembly Agent](../05-use-cases/underwriting-risk-data-assembly-agent.md)

## Claims Processing — A Domain-Specific Note

Insurance claims processing is a distinct business function in its own right — see [Claims Management](../02-functions/claims-management.md) — not a variant of physical-goods supply chain or generic operations, given its own regulatory fairness and appeal-rights obligations. First-notice-of-loss intake and triage is detailed in [Claims Intake & Triage Agent](../05-use-cases/claims-intake-triage-agent.md); full adjudication and settlement automation is not yet written up as a standalone use case and should be scoped with the risk posture of [oasis-fulcrum's claims processing sector guidance](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/09-sector-specific-finops/claims-processing.md), which treats evaluation depth as proportional to claim value and risk. Contributions welcome — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## Regulatory Considerations

Claims decisions carry fairness and appeal-rights obligations in most jurisdictions — see [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI) fairness guidance before treating any claims automation as autonomous.

## Typical Automation Posture

L2–L3 for standard, low-value claims; L1–L2 with mandatory human approval for high-value or ambiguous claims.

---

**Previous:** [Manufacturing & Industrial](manufacturing.md)
**Next:** [Telecom & Media](telecom-media.md)
