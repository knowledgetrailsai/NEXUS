# Prioritization Framework

`Home › 04-grid › Prioritization Framework`

Once you've identified candidate use cases from the [grid](opportunity-grid.md), use this framework to sequence them. This is a lightweight first-pass filter — the rigorous version happens inside [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum)'s [Phase 1](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/06-lifecycle/phase-1-define-baseline.md) once a candidate is selected.

## Four Screening Questions

1. **Value signal strength** — does the use case name a clear, plausible outcome and value basis (see [Principles: Value Signal](../01-foundations/principles.md#value-signal-not-a-value-case))? Vague value signals are a yellow flag, not a disqualifier — but they mean more discovery work before Phase 1.
2. **Realistic starting maturity** — per the [Agentic Automation Spectrum](../01-foundations/agentic-automation-spectrum.md), can this start at L1–L2 and prove itself, or does it require L3+ from day one? Prefer candidates that can start low and earn autonomy.
3. **Risk profile** — per the use case's "Key Risks & Guardrails" section, is this a function/domain combination with elevated risk (see [HR & People](../02-functions/hr-people.md), [Legal & Compliance](../02-functions/legal-compliance.md), or any [Healthcare](../03-domains/healthcare.md)/[Financial Services](../03-domains/financial-services.md) intersection)? Higher risk doesn't disqualify — it raises the bar on evaluation design per [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI).
4. **Grid maturity** — is this a "Core" cell (well-evidenced) or an "Adaptable"/"Limited" cell (less proven)? Prefer Core cells for a first pilot; save Adaptable/Limited cells for once the organization has delivery muscle.

## A Simple 2×2

Plot candidates on: **Value Signal Strength** (weak → strong) × **Automation Ceiling Reachable Safely** (low → high, per the spectrum). Favor the top-right quadrant (strong value, safely high ceiling) for first pilots — not necessarily the single highest-value idea, if its risk profile demands a slower on-ramp.

## Handoff to Delivery

## A Repeatable Screening Score

Score each candidate from 1 (weak) to 5 (strong), and record the evidence behind every score.

| Dimension | Weight | 1 means | 5 means |
|---|---:|---|---|
| Outcome clarity | 25% | No measurable owner or outcome | Baseline and target are measurable |
| Workflow readiness | 20% | Variable, undocumented process | Stable states and known exceptions |
| Data / integration readiness | 20% | Missing or inaccessible data | Trusted data and supported interfaces |
| Safe autonomy | 20% | Irreversible, high-impact action | Reversible, bounded action |
| Adoption leverage | 15% | No clear user or owner | Strong owner and change pathway |

**Weighted score =** `(outcome × .25) + (workflow × .20) + (data × .20) + (autonomy × .20) + (adoption × .15)`.

Use the score to sequence discovery, not to approve a project. Scores of 4.0–5.0 are candidates for a shadow or assist pilot; 3.0–3.9 require resolving the weakest dependency; below 3.0 should remain catalog hypotheses.

## Discovery Packet

Before a go/no-go decision, attach the score, process map, representative cases, data owner, business owner, risk tier, baseline measures, rollout stage, and explicit stop conditions. This keeps the grid from becoming a list of uncosted aspirations.

Once a use case is selected:

1. Move it into [OASIS](https://github.com/knowledgetrailsai/OASIS) Phase 1 — Engage & Align
2. Complete [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum)'s Outcome & Value Definition Sheet, replacing this repository's Value Signal with a sourced, sign-off-backed value case
3. Apply [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI)'s risk assessment proportional to the use case's flagged risks

---

**Previous:** [The Opportunity Grid](opportunity-grid.md)
**Next section:** [05-use-cases](../05-use-cases/)
