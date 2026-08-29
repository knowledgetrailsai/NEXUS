# Use-Case Anatomy

`Home › 01-foundations › Use-Case Anatomy`

This repository is an opportunity catalog, but a useful opportunity description must be specific enough to enter discovery. A strong entry describes a bounded workflow, not a job title or a vague promise to “use AI.”

## The minimum complete description

Every candidate should answer these questions:

| Question | What to capture |
|---|---|
| Where does work begin? | Trigger, channel, frequency, and minimum required information |
| What does the agent know? | Systems of record, documents, policies, permissions, and data freshness |
| What does it produce? | Recommendation, draft, classification, transaction, or escalation |
| What can it change? | Read-only actions, reversible updates, or irreversible commitments |
| Who owns the outcome? | Named business owner, approver, and escalation queue |
| What happens when uncertain? | Confidence threshold, missing-data path, exception route, and timeout behavior |
| How is quality proven? | Offline test set, production metrics, sampling plan, and stop conditions |

## Describe the workflow as a state machine

Use a small number of explicit states rather than implying that the agent can “handle” everything:

`received → validated → enriched → recommended → approved → executed → reconciled`

At each transition, identify the actor, evidence required, allowed action, and failure path. If a transition cannot be audited after the fact, it is not ready for autonomous execution.

## Boundary rules

- Separate **understanding** (extracting, classifying, summarizing) from **decision** (choosing an outcome) and **execution** (changing a system).
- Treat permissions as part of the design. The agent must not inherit a broader authority than the human role it represents.
- Make reversibility explicit. Drafting and routing are usually reversible; payments, terminations, clinical communication, and regulatory filings may not be.
- Define an exception as a normal path, not an error. Ambiguity, policy conflict, missing data, and tool failure should all have owners.
- Keep a human decision-maker in the loop wherever policy, law, safety, or material financial exposure requires judgment.

## Evidence package for discovery

Before moving a candidate into delivery, collect a small evidence pack:

1. A process map with representative happy-path and exception cases.
2. A sample of historical inputs, labeled outcomes, and known edge cases.
3. The policy and authorization rules the workflow must honor.
4. Baseline volume, cycle time, quality, rework, and escalation measures.
5. A proposed evaluation set and a rollback/stop plan.

This turns a catalog hypothesis into a testable delivery brief without pretending that generic catalog language is already a business case.

---

**Related:** [Principles](principles.md) · [Agentic Automation Spectrum](agentic-automation-spectrum.md) · [Capabilities & Outcomes](capabilities-and-outcomes.md) · [Discovering Use Cases](discovering-use-cases.md) · [Use Case Template](../templates/use-case-template.md)

---

**Previous:** [Discovering Use Cases](discovering-use-cases.md)
**Next section:** [02-functions](../02-functions/purchasing-procurement.md)
