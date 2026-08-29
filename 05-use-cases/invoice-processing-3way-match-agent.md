# Invoice Processing & 3-Way Match Agent

`Home › 05-use-cases › Invoice Processing & 3-Way Match Agent`

**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)
**Primary Domains:** [Manufacturing](../03-domains/manufacturing.md), [Retail & CPG](../03-domains/retail-cpg.md)
**Also Applicable To:** All domains with meaningful PO-based purchasing volume
**Capability:** Extraction & Structured Validation (secondary: Classification & Routing, for exceptions)
**Outcome Categories:** Time Saved, Cost Avoided, Coverage & Consistency Improved
**Business Outcome Category:** Efficiency

## Who This Is For

- **In plain terms:** every invoice should match what was ordered and what actually arrived — someone has to check that, line by line, before the bill gets paid. This agent does that checking automatically and only bothers a person when something genuinely doesn't line up.
- **For business readers:** this is one of the most well-proven agentic automation patterns in any industry because the ground truth is unambiguous — the numbers either match within tolerance or they don't — which is exactly the kind of decision that's safe to push toward higher autonomy.
- **For technical readers:** this is a classic multi-source structured-validation pattern: extract, retrieve two corroborating records, compare within tolerance, act. It's a good candidate for a single well-scoped agent rather than a multi-agent decomposition — see Agentic Design below.

## Problem / Trigger

Accounts payable teams manually match invoices against purchase orders and receiving documents (the "3-way match") — a high-volume, rules-based task that's tedious for humans but well-suited to structured validation.

## Benefits

- **For the AP team:** far less time spent on manual line-by-line comparison for the majority of invoices that are already clean matches — their attention goes to the mismatches that actually need judgment.
- **For the business:** faster payment cycles (capturing early-payment discounts, avoiding late fees) and exhaustive coverage instead of a sampled audit, catching pricing or quantity discrepancies that a sample-based review would miss.
- **For suppliers:** faster, more predictable payment turnaround when their invoice matches — fewer disputes caused by processing delay rather than an actual discrepancy.

## Agentic Design

A single agent is the right shape for this use case — the task is bounded, sequential, and doesn't need separately-specialized reasoning roles.

- **Inputs read:** the incoming invoice (email, portal upload, or AP capture), the referenced purchase order, the goods-receipt record, the supplier master, and the tolerance policy table.
- **Reasoning steps:** extract structured invoice data (line items, quantities, prices, tax, terms) → retrieve the matching PO and receipt via API → compare quantities, prices, and terms within documented tolerance → check for duplicate invoice signals → classify as clean match, tolerance-bounded variance, or genuine mismatch.
- **Tools/actions available:** read APIs to the PO system, receiving system, and supplier master; a duplicate-invoice index lookup; a write action limited to submitting a match result and payment-workflow entry (never releasing payment directly unless ERP policy explicitly permits it for a bounded category).
- **Output produced:** a structured match result with line-level evidence, either a payment-workflow submission (clean match) or a routed exception with the specific discrepancy flagged (mismatch).

## Multi-Agent Design (where relevant)

Not applicable as a default — a single agent handles this well because the task is one bounded validation sequence, not several genuinely distinct reasoning problems. A multi-agent split becomes worth considering only at very high volume across many disparate ERP/supplier ecosystems, where a **per-ERP extraction agent** (handling each system's document format and quirks) feeding a **shared validation-and-routing agent** can reduce per-system maintenance overhead — but this is an implementation-scaling decision, not a requirement for the pattern to work.

## Workflow Boundary

**Trigger and inputs:** Invoice email, portal upload, or AP capture event; supplier, invoice number, line items, currency, tax, PO reference, and terms.

**Systems and evidence consulted:** AP/ERP, purchase-order system, goods-receipt record, supplier master, tolerance policy, and duplicate-invoice index.

**Outputs and allowed actions:** Structured invoice, match result, evidence links, and payment-workflow submission. Release is allowed only where ERP policy explicitly permits it.

**Human owner / approval point:** AP exception owner for mismatches, duplicates, new suppliers, and invoices above authority thresholds.

**Exception paths:** Missing PO/receipt → request evidence; mismatch → route with line-level explanation; duplicate signal → hold; tool failure → preserve in manual queue.

**Out of scope:** Creating suppliers, changing bank details, overriding tolerances, or releasing payment without evidence.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L1 (assist) | Extracts and presents the invoice, PO, and receipt side by side | AP clerk performs the actual comparison and decision | Faster data assembly only; comparison labor unchanged |
| L2 (automate, reviewed) | Extracts, retrieves, compares, and recommends a match/mismatch classification | AP clerk reviews every classification before payment submission | Time saved on comparison; coverage still bounded by review capacity |
| L3 (automate, exception-routed) | Autonomously submits clean, within-tolerance matches to payment workflow; routes only genuine mismatches | AP exception owner handles only flagged mismatches | Full population coverage at high speed; AP time reallocated to genuine exceptions |
| L4 (autonomous, monitored) | Same as L3, plus bounded auto-release of payment for very low-risk, low-value, pre-approved categories | AP owner audits a sample and monitors exception-rate drift | Cycle-time and cost-avoidance gains extend to payment release itself, with monitoring substituting for per-instance review |

- **Realistic starting level:** L2 — agent matches and validates, human reviews mismatches
- **Potential ceiling:** L3 — agent processes all within-tolerance matches autonomously, only genuine mismatches reach a human
- **Why this range:** Ground truth is unambiguous (numbers either match or they don't), making this one of the safer functions to push toward L3 — see [Finance & Accounting](../02-functions/finance-accounting.md).

## Value Signal

- **Plausible outcome definition:** An invoice matched and approved for payment without manual intervention, within policy tolerance.
- **Plausible value basis:** Time saved (AP staff hours), cost avoided (late-payment penalties from faster processing).

## KPIs Influenced

- **Leading:** Percentage of invoices auto-matched without human touch, extraction accuracy, time from invoice receipt to match result.
- **Lagging:** AP cost per invoice processed, early-payment discount capture rate, late-payment penalty incidence, exception-queue age.

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
- [Media Buy Reconciliation & Discrepancy Resolution Agent](media-buy-reconciliation-agent.md) — same structural pattern, different domain

---

**Back to:** [05-use-cases](.) · [Finance & Accounting](../02-functions/finance-accounting.md)
