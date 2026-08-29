# Returns & Refund Adjudication Agent

`Home › 05-use-cases › Returns & Refund Adjudication Agent`

**Exclusive domain:** [Retail & CPG](../03-domains/retail-cpg.md)
**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)

## Problem / Trigger

Return and refund requests require checking purchase history, return-window and condition policy, and fraud/abuse signals (serial returners, mismatched items) — high volume, mostly routine, but costly when policy is applied inconsistently.

## Agentic Automation Opportunity

The agent verifies the purchase and return eligibility against policy, checks the customer's return history for abuse patterns, processes the refund or exchange for compliant, low-risk requests, and routes policy exceptions or flagged abuse patterns to a human for a decision — rather than auto-approving or auto-denying them.

## Boundary, Maturity & Value

- **Starting / ceiling:** L2 / L3. Agent processes clear, within-policy returns autonomously; exceptions, high-value items, and suspected abuse route to a human.
- **Outcome:** Faster refund turnaround for legitimate returns and more consistent policy application at full coverage instead of a sample.
- **Value basis:** Cost avoided (return-fraud losses caught), time saved (support/finance staff hours), and improved customer experience from faster resolution.
- **Exceptions:** Suspected serial-return abuse, high-value or non-standard items, and policy-ambiguous cases escalate to a human reviewer.

## Evaluation & Guardrails

Measure refund accuracy against policy, abuse-pattern detection precision/recall, customer friction (appeal/complaint rate), and processing time. Cap autonomous refund value, log the policy version and evidence behind every decision, and validate abuse-detection rules against a human-reviewed baseline before raising thresholds.

## Related Use Cases

- [Expense Audit Agent](expense-audit-agent.md) — related policy-based approve/flag pattern
- [Churn Prevention Agent](churn-prevention-agent.md)

---

**Back to:** [Retail & CPG](../03-domains/retail-cpg.md)
