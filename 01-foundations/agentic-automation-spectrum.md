# The Agentic Automation Spectrum

`Home › 01-foundations › Agentic Automation Spectrum`

Every use case in [05-use-cases](../05-use-cases/benefits-eligibility-document-verification-agent.md) is rated against this four-level spectrum — both its **realistic starting level** and its **potential ceiling**. Skipping levels (going straight to autonomous) is usually a mistake; see [04-grid/prioritization-framework.md](../04-grid/prioritization-framework.md).

## L1 — Assist (Co-Pilot)

The human does the work; AI suggests, drafts, or surfaces information. The human reviews everything before it's used. Lowest risk, fastest to deploy, and often the right permanent home for judgment-heavy or high-stakes decisions.

*Example: an AI drafts a contract redline; a lawyer reviews and edits every clause before it goes out.*

## L2 — Automate (Single-Step, Reviewed)

AI executes one discrete, well-bounded task end-to-end (classification, extraction, routing), typically with human review on a sample or on exceptions rather than every instance.

*Example: an AI auto-classifies and routes support tickets; a human reviews only the low-confidence ones.*

## L3 — Agentic (Multi-Step, Exception-Escalated)

AI plans and executes a multi-step workflow — reasoning, calling tools, checking its own work — escalating to a human only for exceptions or high-risk branches, per a defined threshold.

*Example: an AI processes a standard invoice end-to-end (match PO → validate → approve), escalating only mismatches above a dollar threshold.*

## L4 — Autonomous (Bounded, Monitored)

AI operates within pre-approved policy bounds without per-task human approval, monitored continuously with the ability to intervene or roll back. Reserved for high-volume, low-stakes, well-understood workflows with strong observability.

*Example: an AI automatically approves and processes routine expense reports under a defined dollar and category threshold, with all approvals logged and sampled for audit.*

## Using This Scale

- Every [use case entry](../05-use-cases/benefits-eligibility-document-verification-agent.md) states a **realistic starting level** (usually L1 or L2) and a **potential ceiling** (often L3, occasionally L4).
- Moving up a level should follow the same lifecycle discipline as [OASIS](https://github.com/knowledgetrailsai/OASIS) — piloted, calibrated, and governed before scaling — not assumed at design time.
- Higher levels demand proportionally more of the [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI) evaluation and guardrail treatment, and more rigorous [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum) cost/value tracking — the "Shadow Tax of Evaluation" grows with autonomy.

---

**Previous:** [Principles](principles.md)
**Next:** [Capabilities & Outcomes](capabilities-and-outcomes.md)
