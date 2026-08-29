# Media Buy Reconciliation & Discrepancy Resolution Agent

`Home › 05-use-cases › Media Buy Reconciliation & Discrepancy Resolution Agent`

**Exclusive domain:** [Advertising & Media](../03-domains/advertising-media.md)
**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)

## Who This Is For

- **In plain terms:** when an agency buys ad space across many platforms for a client, three different numbers exist for every line item — what was booked, what the platform says actually ran, and what got billed — and they don't always match. Someone has to chase down every mismatch by hand. This agent checks all three numbers automatically and only bothers a human when something genuinely doesn't reconcile.
- **For business readers:** reconciliation discrepancies that go unresolved either erode margin (the agency eats the difference) or erode client trust (the client gets billed for something that didn't run as planned) — and both outcomes are common in an industry running campaigns across dozens of platforms with different reporting cadences. Automating the matching itself, at full coverage instead of a sample, catches more of these before they reach the client invoice.
- **For technical readers:** this is a three-way-match variant — reading media-plan/booking data, platform-reported delivery data (via each platform's reporting API), and billing/invoice data, then matching line items within a documented tolerance and routing genuine mismatches (not just timing-lag noise) to a media operations analyst.

## Problem / Trigger

Campaigns run across many ad platforms with different reporting formats, definitions, and latency, so reconciling booked spend against actual delivery and final billing requires manually cross-referencing multiple systems per campaign — a slow process, typically done on a sample or only when a client questions an invoice, rather than exhaustively.

## Agentic Automation Opportunity

The agent retrieves booked media-plan line items, platform-reported delivery data, and billing records for a campaign, matches them within documented tolerance (accounting for known reporting-lag and definitional differences across platforms), and either clears fully-reconciled line items or flags genuine discrepancies with the specific mismatch and its evidence for a media operations analyst — never issuing a credit, adjusting an invoice, or resolving a discrepancy with the platform or client itself.

## Workflow Boundary

**Trigger and inputs:** Campaign reconciliation cycle (e.g., monthly billing close) or an ad-hoc reconciliation request; campaign ID, flight dates, and the platforms involved.

**Systems and evidence consulted:** Media-plan/booking system, each involved platform's reporting API, and the billing/invoicing system.

**Outputs and allowed actions:** A reconciliation report listing matched and flagged line items with evidence, submitted to the media operations queue. No invoice adjustment, credit issuance, or platform/client communication is generated autonomously.

**Human owner / approval point:** Media operations analyst reviews every flagged discrepancy and decides on resolution (dispute with platform, credit to client, or accepted variance).

**Exception paths:** A platform reporting API outage or delay → hold the affected line items as unreconciled rather than assuming a match; a discrepancy exceeding a defined materiality threshold → escalate immediately rather than waiting for the standard cycle.

**Out of scope:** Invoice adjustment, credit issuance, client communication, and dispute resolution with ad platforms.

## Automation Maturity

- **Realistic starting level:** L2 — agent reconciles exhaustively and flags every genuine discrepancy, analyst resolves all flagged items
- **Potential ceiling:** L3 — agent auto-clears fully-matched line items at full coverage with only genuine discrepancies reaching an analyst, once tolerance rules are validated against real reporting-lag patterns per platform
- **Why this range:** Ground truth (do the three numbers match within documented tolerance) is largely unambiguous once platform-specific reporting quirks are encoded, making this a strong candidate for higher automation similar to other three-way-match patterns in this repository.

_Indicative scale:_
`L1 (assist) — L2 (automate, reviewed) ● — L3 (automate, exception-routed) ○ — L4 (autonomous, monitored)`

## Value Signal

- **Plausible outcome definition:** A campaign's media spend reconciled across booking, delivery, and billing at full line-item coverage without manual cross-referencing, with genuine discrepancies caught before the client invoice is finalized.
- **Plausible value basis:** Time saved (media operations analyst hours), cost avoided (margin erosion from unresolved discrepancies, billing errors reaching clients).

## KPIs Influenced

- **Leading:** Percentage of campaign line items reconciled without manual intervention, reconciliation cycle time, discrepancy-flag precision (real mismatches vs. reporting-lag noise).
- **Lagging:** Billing accuracy rate on client invoices, margin leakage from unresolved discrepancies, client billing-dispute volume.

## Evaluation Plan

- **Offline test set:** Historical campaigns with known reconciliation outcomes across multiple platforms, covering clean matches, known reporting-lag patterns, and genuine discrepancies.
- **Quality measures:** Match accuracy, false-discrepancy rate (flagging noise as a real issue), false-clear rate (missing a genuine discrepancy — the more costly failure mode), reconciliation cycle time.
- **Launch gates:** False-clear rate at or below the finance team's tolerance; reconciliation cycle time meaningfully reduced from the manual baseline before scaling to L3.
- **Rollout path:** Shadow reconciliation alongside the manual process → assist with analyst review of every line item → bounded auto-clear for bounded platforms once tolerance rules are validated → scale across platforms.

## Implementation Notes

- **Data dependencies:** Media-plan/booking data, per-platform reporting API access, and billing/invoice records.
- **Integration dependencies:** API access to each ad platform's reporting endpoint (varies by platform), booking system, and billing system.
- **Permissions / audit requirements:** Read-only across booking, platform, and billing systems; every reconciliation decision retains the source data and tolerance rule applied.
- **Likely failure modes:** Platform-specific reporting definitions misapplied as if universal; reporting-lag mistaken for a genuine discrepancy; a platform API change silently breaking the data feed.
- **Open discovery questions:** Which platforms are in scope, and what are their known reporting-lag and definitional quirks? What materiality threshold triggers immediate escalation versus standard-cycle review? Who owns tolerance-rule maintenance as platforms change their reporting?

## Key Risks & Guardrails

- A false-clear (missing a genuine discrepancy) is the more costly failure mode than a false-flag, and tolerance rules should be tuned accordingly
- Platform reporting APIs change without notice; a silent data-feed break should fail loudly, not produce a false reconciliation
- Never let the agent issue a credit, adjust an invoice, or communicate with a client or platform — resolution authority stays with the media operations analyst

## Related Use Cases

- [Invoice Processing & 3-Way Match Agent](invoice-processing-3way-match-agent.md) — same structural pattern, different domain
- [Expense Audit Agent](expense-audit-agent.md) — related exhaustive-review-against-policy pattern

---

**Back to:** [Advertising & Media](../03-domains/advertising-media.md)
