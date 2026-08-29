# Purchase Requisition & Approval Agent

`Home › 05-use-cases › Purchase Requisition & Approval Agent`

**Primary Function:** [Purchasing & Procurement](../02-functions/purchasing-procurement.md)
**Primary Domains:** [Manufacturing](../03-domains/manufacturing.md), [Retail & CPG](../03-domains/retail-cpg.md)
**Also Applicable To:** All domains, generically

## Problem / Trigger

Purchase requisitions today are manually keyed, manually routed for approval, and frequently stall waiting on the right approver — especially for cross-department or over-threshold purchases requiring multiple sign-offs.

## Agentic Automation Opportunity

An agent receives a requisition (structured form or free-text email), validates it against budget and category rules via API to the ERP/procurement system, checks vendor status and contract terms, determines the correct approval chain based on amount and category, and routes it — following up on stalled approvals and flagging policy exceptions rather than silently blocking them.

## Automation Maturity

- **Realistic starting level:** L2 — automated validation and routing, human approves
- **Potential ceiling:** L3 — agent auto-approves within a pre-defined, low-risk threshold, escalating everything else
- **Why this range:** Approval authority is a segregation-of-duties control; automating routing is safe, automating the approval decision itself requires explicit, narrow policy bounds.

## Value Signal

- **Plausible outcome definition:** A requisition processed from submission to approved/rejected status without manual routing intervention, within policy.
- **Plausible value basis:** Time saved (procurement staff hours), cycle-time reduction (faster purchasing = faster operations).

## Key Risks & Guardrails

- Approval-routing errors that bypass segregation-of-duties controls — see [Purchasing & Procurement risks](../02-functions/purchasing-procurement.md#key-cross-cutting-risks)
- Category misclassification leading to incorrect approval chain
- Auto-approval thresholds must be reviewed periodically, not set once and forgotten

## Related Use Cases

- [Supplier Risk Monitoring Agent](supplier-risk-monitoring-agent.md)
- [Invoice Processing & 3-Way Match Agent](invoice-processing-3way-match-agent.md)

---

**Back to:** [05-use-cases](.) · [Purchasing & Procurement](../02-functions/purchasing-procurement.md)
