# Invoice Processing & 3-Way Match Agent

`Home › 05-use-cases › Invoice Processing & 3-Way Match Agent`

**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)
**Primary Domains:** [Manufacturing](../03-domains/manufacturing.md), [Retail & CPG](../03-domains/retail-cpg.md)
**Also Applicable To:** All domains with meaningful PO-based purchasing volume

## Problem / Trigger

Accounts payable teams manually match invoices against purchase orders and receiving documents (the "3-way match") — a high-volume, rules-based task that's tedious for humans but well-suited to structured validation.

## Agentic Automation Opportunity

An agent extracts invoice line items, retrieves the corresponding PO and receiving record via API, validates that quantities, prices, and terms match within tolerance, and approves the invoice for payment — routing any mismatch above a defined threshold to a human for review rather than auto-rejecting or silently accepting it.

## Workflow Boundary

**Trigger and inputs:** Invoice email, portal upload, or AP capture event; supplier, invoice number, line items, currency, tax, PO reference, and terms.

**Systems and evidence consulted:** AP/ERP, purchase-order system, goods-receipt record, supplier master, tolerance policy, and duplicate-invoice index.

**Outputs and allowed actions:** Structured invoice, match result, evidence links, and payment-workflow submission. Release is allowed only where ERP policy explicitly permits it.

**Human owner / approval point:** AP exception owner for mismatches, duplicates, new suppliers, and invoices above authority thresholds.

**Exception paths:** Missing PO/receipt → request evidence; mismatch → route with line-level explanation; duplicate signal → hold; tool failure → preserve in manual queue.

**Out of scope:** Creating suppliers, changing bank details, overriding tolerances, or releasing payment without evidence.

## Automation Maturity

- **Realistic starting level:** L2 — agent matches and validates, human reviews mismatches
- **Potential ceiling:** L3 — agent processes all within-tolerance matches autonomously, only genuine mismatches reach a human
- **Why this range:** Ground truth is unambiguous (numbers either match or they don't), making this one of the safer functions to push toward L3 — see [Finance & Accounting](../02-functions/finance-accounting.md).

## Value Signal

- **Plausible outcome definition:** An invoice matched and approved for payment without manual intervention, within policy tolerance.
- **Plausible value basis:** Time saved (AP staff hours), cost avoided (late-payment penalties from faster processing).

## Evaluation Plan

- **Offline test set:** Historical invoices covering clean matches, partial receipts, split lines, tax/currency variation, duplicates, scans, and missing references.
- **Quality measures:** Field extraction accuracy, match precision, false-approval rate, duplicate recall, routing accuracy, and cycle time.
- **Launch gates:** Zero unauthorized releases in testing; every autonomous release has retrievable evidence; false approvals stay below the finance owner's tolerance.
- **Rollout path:** Shadow → AP assist → bounded release for low-risk matches → monitored scale.

## Implementation Notes

- **Data dependencies:** Supplier and PO masters, receipts, tolerance tables, and historical exception labels.
- **Integration dependencies:** Idempotent ERP APIs and a durable retry queue.
- **Permissions / audit:** Separate read, draft, approve, and release permissions; retain source, policy version, evidence, and actor.
- **Likely failure modes:** OCR line merging, duplicate invoices with changed numbers, partial receipts, stale supplier records, and asynchronous ERP updates.
- **Open discovery questions:** Which entities permit auto-release? How are non-PO invoices governed? What tolerance applies by category and currency?

## Key Risks & Guardrails

- Errors compound silently in high-volume, low-unit-value transactions until an audit surfaces them — see [Finance & Accounting risks](../02-functions/finance-accounting.md#key-cross-cutting-risks)
- Segregation-of-duties controls must be preserved even at higher automation levels
- Autonomy requires strong audit logging — never remove human traceability

## Related Use Cases

- [Expense Audit Agent](expense-audit-agent.md)
- [Purchase Requisition & Approval Agent](purchasing-requisition-approval-agent.md)

---

**Back to:** [05-use-cases](.) · [Finance & Accounting](../02-functions/finance-accounting.md)
