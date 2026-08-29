# Evaluation & Rollout

`Home › 01-foundations › Evaluation & Rollout`

Agent quality is not one accuracy percentage. A production-ready evaluation tests the whole workflow: correct interpretation, policy compliance, tool use, human handoff, and measurable business outcomes.

## Evaluation layers

| Layer | Core question | Example measures |
|---|---|---|
| Task quality | Did the agent understand and produce the right result? | extraction accuracy, groundedness, classification precision/recall |
| Policy quality | Did it respect rules and authority? | unauthorized-action rate, policy violation rate, approval-chain accuracy |
| Operational quality | Did the workflow behave reliably? | completion rate, latency, tool failure rate, duplicate actions |
| Human quality | Did people receive useful, appropriately timed work? | acceptance rate, override rate, escalation quality, reviewer time |
| Business quality | Did the intended outcome improve? | cycle time, first-contact resolution, leakage avoided, forecast error |

## Minimum test design

Build a stratified evaluation set containing normal cases, boundary values, ambiguous inputs, missing fields, adversarial instructions, policy conflicts, and tool/API failures. Keep a holdout set that is not used for prompt or workflow tuning. For high-impact workflows, require review by the accountable business and risk owners before live testing.

## Rollout ladder

1. **Shadow:** observe real inputs and generate proposed outputs without affecting the system of record.
2. **Assist:** expose the recommendation or draft to a human who makes the final decision.
3. **Bounded execution:** permit narrow, reversible actions with explicit thresholds and immediate escalation outside them.
4. **Scale:** expand volume, domains, or autonomy only after the previous stage meets its quality and safety gates.

## Release gates

Define thresholds before launch. A gate should include a quality target, a maximum tolerated harmful-error rate, an owner, and a response when it fails. Monitor by segment, not only in aggregate: business unit, geography, language, supplier/customer type, and risk tier can hide materially different behavior.

## Stop conditions

Pause execution when there is a material policy breach, unexplained drift, repeated duplicate or irreversible actions, loss of audit evidence, or a tool integration behaving outside its contract. A rollback should restore the previous human-controlled path; it should not depend on the agent being available.

---

**Related:** [Use-Case Anatomy](use-case-anatomy.md) · [Prioritization Framework](../04-grid/prioritization-framework.md) · [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI)
