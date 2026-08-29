# Demand Forecasting & Replenishment Agent

`Home › 05-use-cases › Demand Forecasting & Replenishment Agent`

**Primary Function:** [Supply Chain & Operations](../02-functions/supply-chain-operations.md)
**Primary Domains:** [Retail & CPG](../03-domains/retail-cpg.md), [Manufacturing](../03-domains/manufacturing.md)
**Also Applicable To:** [Insurance](../03-domains/insurance.md) (claims processing — structurally adjacent pattern, see domain notes)

## Problem / Trigger

Inventory replenishment decisions require synthesizing historical demand, seasonality, current stock levels, and lead times — done manually or with static rule-based systems that don't adapt well to changing patterns.

## Agentic Automation Opportunity

An agent continuously analyzes demand signals (sales history, seasonality, promotional calendar, current inventory position) across SKUs, generates replenishment recommendations with reasoning, and either queues them for planner approval or, for well-understood, low-risk SKUs, places routine reorders within pre-approved policy bounds.

## Automation Maturity

- **Realistic starting level:** L2 — agent recommends, planner approves
- **Potential ceiling:** L3–L4 — agent autonomously reorders well-understood, low-risk SKUs within policy bounds, with all actions logged and monitored; planner retains full control over new, seasonal, or high-value SKUs
- **Why this range:** Autonomous reordering commits real capital and physical supply — earn this ceiling incrementally, starting recommendation-only, per [Supply Chain & Operations](../02-functions/supply-chain-operations.md).

## Value Signal

- **Plausible outcome definition:** A replenishment recommendation or action that avoids a stockout or excess-inventory event, benchmarked against the prior forecasting approach.
- **Plausible value basis:** Cost avoided (stockout lost sales, excess inventory carrying cost), time saved (planner hours).

## Key Risks & Guardrails

- Forecasting errors compound across a supply chain — validate against a human-reviewed baseline before scaling to L3
- Autonomous reordering (L4) directly commits real money — start recommendation-only
- Data quality from upstream systems (POS, IoT) directly bounds achievable accuracy — see [Supply Chain & Operations risks](../02-functions/supply-chain-operations.md#key-cross-cutting-risks)

## Related Use Cases

- [Supplier Risk Monitoring Agent](supplier-risk-monitoring-agent.md)

---

**Back to:** [05-use-cases](.) · [Supply Chain & Operations](../02-functions/supply-chain-operations.md)
