# Expense Audit Agent

`Home › 05-use-cases › Expense Audit Agent`

**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)
**Primary Domains:** Applies generically across all domains
**Also Applicable To:** All domains

## Problem / Trigger

Expense report review — checking receipts against policy, flagging out-of-policy spend, verifying categorization — is repetitive, rules-based, and typically sampled rather than exhaustively reviewed due to volume.

## Agentic Automation Opportunity

An agent reviews every submitted expense report against documented policy (spend limits, category rules, required documentation), auto-approves fully compliant reports, and flags policy exceptions with the specific rule violated for human review — enabling exhaustive review instead of sampling.

## Automation Maturity

- **Realistic starting level:** L2 — agent reviews all reports, auto-approves compliant ones, routes exceptions
- **Potential ceiling:** L3–L4 — agent auto-approves and processes payment for compliant reports under a defined threshold, fully autonomously, with sampled audit
- **Why this range:** Policy rules are explicit and well-bounded, and per-report stakes are low, making this a strong candidate for higher automation once proven.

## Value Signal

- **Plausible outcome definition:** An expense report reviewed and correctly approved/flagged against policy without manual review, at effectively 100% coverage instead of a sample.
- **Plausible value basis:** Time saved (finance team hours), risk reduced (policy violations caught that a sampled review would have missed).

## Key Risks & Guardrails

- False negatives on policy violations that a sampled human review would have caught — track this explicitly, don't assume automation improves coverage without verifying it
- Employee-facing friction if flagging is overly aggressive or opaque about why
- See [Finance & Accounting risks](../02-functions/finance-accounting.md#key-cross-cutting-risks) — audit logging is essential given the higher autonomy ceiling here

## Related Use Cases

- [Invoice Processing & 3-Way Match Agent](invoice-processing-3way-match-agent.md)

---

**Back to:** [05-use-cases](.) · [Finance & Accounting](../02-functions/finance-accounting.md)
