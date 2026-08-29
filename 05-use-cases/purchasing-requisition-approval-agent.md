# Purchase Requisition & Approval Agent

`Home › 05-use-cases › Purchase Requisition & Approval Agent`

**Primary Function:** [Purchasing & Procurement](../02-functions/purchasing-procurement.md)
**Primary Domains:** [Manufacturing](../03-domains/manufacturing.md), [Retail & CPG](../03-domains/retail-cpg.md)
**Also Applicable To:** All domains, generically
**Capability:** Classification & Routing
**Outcome Categories:** Time Saved, Risk Reduced
**Business Outcome Category:** Efficiency

## Problem / Trigger

Purchase requisitions today are manually keyed, manually routed for approval, and frequently stall waiting on the right approver — especially for cross-department or over-threshold purchases requiring multiple sign-offs.

## Agentic Automation Opportunity

An agent receives a requisition (structured form or free-text email), validates it against budget and category rules via API to the ERP/procurement system, checks vendor status and contract terms, determines the correct approval chain based on amount and category, and routes it — following up on stalled approvals and flagging policy exceptions rather than silently blocking them.

## Benefits

- **For the requester:** faster time from submission to approved/rejected status, without a requisition stalling for lack of the right approver being found.
- **For procurement:** less time spent manually determining and chasing the correct approval chain for each requisition.
- **For the business:** fewer segregation-of-duties errors from ad hoc, human-determined routing, since the approval chain is applied consistently by documented rule.

## Agentic Design

- **Inputs read:** the requisition (structured form or free-text email), budget and category rules, vendor status and contract terms.
- **Reasoning steps:** validate the requisition against budget and category rules via API → check vendor status and contract terms → determine the correct approval chain based on amount and category → route it → follow up on stalled approvals and flag policy exceptions rather than silently blocking them.
- **Tools/actions available:** read access to the ERP/procurement system and vendor master; write access limited to routing the requisition and sending follow-up notifications — no autonomous approval outside a pre-defined, low-risk threshold.
- **Output produced:** a routed requisition with the applied approval chain, or a flagged policy exception.

## Multi-Agent Design (where relevant)

Not needed as a default — validation and routing are one coherent sequence, and splitting them risks the routing decision being made on a requisition that wasn't fully validated first.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Automated validation and routing | Human approves | Faster, more consistent routing; approval authority stays fully human |
| L3 (automate, exception-routed) | Auto-approves within a pre-defined, low-risk threshold | Human handles everything else | Faster processing for the low-risk majority, procurement time concentrated on higher-value/higher-risk requisitions |

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
