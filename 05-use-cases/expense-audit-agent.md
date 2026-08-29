# Expense Audit Agent

`Home › 05-use-cases › Expense Audit Agent`

**Primary Function:** [Finance & Accounting](../02-functions/finance-accounting.md)
**Primary Domains:** Applies generically across all domains
**Also Applicable To:** All domains
**Capability:** Continuous Monitoring & Flagging
**Outcome Categories:** Time Saved, Risk Reduced, Coverage & Consistency Improved
**Business Outcome Category:** Efficiency

## Problem / Trigger

Expense report review — checking receipts against policy, flagging out-of-policy spend, verifying categorization — is repetitive, rules-based, and typically sampled rather than exhaustively reviewed due to volume.

## Agentic Automation Opportunity

An agent reviews every submitted expense report against documented policy (spend limits, category rules, required documentation), auto-approves fully compliant reports, and flags policy exceptions with the specific rule violated for human review — enabling exhaustive review instead of sampling.

## Benefits

- **For the finance team:** every report gets checked, not just a sample — the team's attention concentrates on genuine exceptions instead of spot-checking a fraction of the volume.
- **For the business:** policy violations get caught at effectively 100% coverage instead of a sample, directly closing the gap a sampled review structurally can't.
- **For the employee submitting an expense:** faster approval on compliant reports, since they're not waiting behind a manual review queue.

## Agentic Design

- **Inputs read:** the submitted expense report (receipts, categorization, amounts), and the documented expense policy (spend limits, category rules, required documentation).
- **Reasoning steps:** check the report against every applicable policy rule → auto-approve fully compliant reports → flag policy exceptions with the specific rule violated for human review.
- **Tools/actions available:** read access to the report and policy rules; a write action limited to approving a report and, at higher maturity, initiating payment for compliant reports under a defined threshold.
- **Output produced:** an approval (compliant reports) or a flagged exception with the specific rule cited.

## Multi-Agent Design (where relevant)

Not needed as a default — policy-rule checking against a single report is a bounded, sequential task well within a single agent's scope. A split becomes worth considering only if audit sampling (spot-checking a subset of auto-approved reports for model drift) is added as a distinct, periodic function run by a separate **audit-sampling agent** rather than the same agent marking its own homework.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Reviews all reports, auto-approves compliant ones, routes exceptions | Finance team reviews every routed exception | Full-coverage review replaces sampling; exceptions get consistent, cited flags |
| L3–L4 (exception-routed / autonomous, monitored) | Auto-approves and processes payment for compliant reports under a defined threshold, fully autonomously, with sampled audit | Finance team audits a sample and monitors drift rather than reviewing every compliant report | Near-full automation of the compliant-report population, with human attention concentrated on true exceptions and periodic quality assurance |

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
