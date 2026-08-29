# Markdown & Promotional Pricing Recommendation Agent

`Home › 05-use-cases › Markdown & Promotional Pricing Recommendation Agent`

**Exclusive domain:** [Retail & CPG](../03-domains/retail-cpg.md)
**Primary Function:** [Data & Analytics](../02-functions/data-analytics.md)

## Who This Is For

- **In plain terms:** deciding when and how much to mark down slow-moving inventory, or how deep a promotion should run, means weighing sell-through speed against margin loss across thousands of SKUs — more than a merchandiser can systematically evaluate by hand. This agent recommends markdown timing and depth per SKU with the reasoning shown, and the merchandiser approves.
- **For business readers:** markdown decisions made too late waste margin on clearance fire-sales, and decisions made too early leave money on the table — getting the timing and depth right, consistently, across a full SKU range is where the value sits, not in a single big pricing call.
- **For technical readers:** this means integration with the POS/sales data system, current inventory position, and a documented markdown policy (margin floors, timing rules by category) — producing a ranked recommendation set for merchandiser approval, never an autonomous price change.

## Problem / Trigger

Markdown timing and depth decisions require weighing sell-through velocity, inventory age, and margin impact across a large SKU range, and merchandisers typically manage this with broad category-level rules rather than SKU-specific analysis, leaving value on the table in both directions (too-early and too-late markdowns).

## Agentic Automation Opportunity

The agent analyzes sell-through velocity and inventory age per SKU against the documented markdown policy, recommends specific markdown timing and depth with the supporting rationale, and queues recommendations for merchandiser approval — never changing a price autonomously.

## Boundary, Maturity & Value

- **Starting / ceiling:** L1 / L2. Agent recommends with rationale; merchandiser approves every price change. L3 (bounded auto-execution within policy) is achievable for very low-risk, well-validated categories once the recommendation quality is proven.
- **Outcome:** Markdown decisions applied at the right time and depth more consistently than category-level manual rules achieve, recovering margin without slowing sell-through.
- **Value basis:** Revenue influenced (margin recovered from better-timed markdowns), cost avoided (reduced end-of-season clearance losses).
- **Exceptions:** New or novel SKUs without sufficient sales history, and any recommendation that would breach the documented margin floor, escalate to the merchandiser.

_Indicative scale:_
`L1 (assist) ●○ — L2 (automate, reviewed) — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## KPIs Influenced

- **Leading:** Recommendation acceptance rate, SKU coverage (percentage actively analyzed), time-to-markdown-decision.
- **Lagging:** Sell-through rate at season end, gross margin recovered versus prior-period markdown approach, end-of-season clearance inventory value.

## Key Risks & Guardrails

- A pricing recommendation is still a revenue-impacting decision at scale — margin-floor breaches must be a hard constraint, not a soft preference
- Sell-through models trained on historical patterns can misfire on genuinely novel products or unusual demand shocks — flag low-confidence recommendations rather than presenting them with false certainty
- Autonomous price execution (even bounded) requires strong monitoring given the direct revenue exposure

## Related Use Cases

- [Demand Forecasting & Replenishment Agent](demand-forecasting-replenishment-agent.md) — related inventory-and-demand pattern
- [Returns & Refund Adjudication Agent](returns-refund-adjudication-agent.md) — related retail policy-application pattern

---

**Back to:** [Retail & CPG](../03-domains/retail-cpg.md)
