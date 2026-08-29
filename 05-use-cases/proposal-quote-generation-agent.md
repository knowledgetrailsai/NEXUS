# Proposal & Quote Generation Agent

`Home › 05-use-cases › Proposal & Quote Generation Agent`

**Primary Function:** [Sales](../02-functions/sales.md)
**Primary Domains:** [Manufacturing](../03-domains/manufacturing.md), [Technology & SaaS](../03-domains/technology-saas.md)
**Also Applicable To:** Any domain with configurable product/service offerings

## Problem / Trigger

Generating an accurate quote or proposal for a configurable product/service requires pulling pricing rules, discount policy, and product configuration into a coherent document — a slow, error-prone manual process, especially for complex configurations.

## Agentic Automation Opportunity

Given deal parameters (product configuration, volume, term), an agent generates a compliant quote by querying the pricing/CPQ system directly, applies discount policy correctly, and drafts the accompanying proposal document — flagging any configuration or discount request outside standard policy for human approval rather than silently applying it.

## Automation Maturity

- **Realistic starting level:** L2 — agent generates full quotes within standard policy, human approves exceptions
- **Potential ceiling:** L3 — agent handles full standard-policy quote lifecycle end-to-end, only exceptions reach a human
- **Why this range:** Pricing errors have direct revenue impact but standard-policy quotes are well-bounded and low-risk once validated.

## Value Signal

- **Plausible outcome definition:** An accurate, policy-compliant quote generated and sent without manual pricing rework.
- **Plausible value basis:** Time saved (sales ops hours), cycle-time reduction (faster quote turnaround improving win rate).

## Key Risks & Guardrails

- Pricing/quote errors in configurable, high-value proposals — see [Sales risks](../02-functions/sales.md#key-cross-cutting-risks)
- Discount policy exceptions applied without the appropriate approval
- Configuration errors that create unfulfillable commitments

## Related Use Cases

- [Sales Development Rep (SDR) Agent](sales-development-rep-agent.md)
- [Invoice Processing & 3-Way Match Agent](invoice-processing-3way-match-agent.md)

---

**Back to:** [05-use-cases](.) · [Sales](../02-functions/sales.md)
