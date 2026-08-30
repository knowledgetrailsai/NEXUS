# Knowledge Map

`Home › 00-navigation-and-methodology › Knowledge Map`

## The Core Idea: Four Dimensions, Not a List

This repository breaks agentic opportunity down along four dimensions, not one:

```
DOMAIN (industry context) × FUNCTION (business owner) × CAPABILITY (mechanical pattern) → USE CASE → OUTCOME
```

- **Domain** — the industry context: regulation, systems of record, risk tolerance, terminology. See [03-domains](../03-domains/advertising-media.md).
- **Function** — who owns the problem inside the business: Purchasing, Sales, Finance, Claims Management, and so on. The same function's problem shape recurs across industries. See [02-functions](../02-functions/claims-management.md).
- **Capability** — what the agent mechanically does, independent of function or domain: extraction and validation, classification and routing, forecasting, continuous monitoring, scheduling, synthesis, conversation, visual perception. See [Capabilities & Outcomes](../01-foundations/capabilities-and-outcomes.md).
- **Use Case** — where a domain, a function, and a capability meet a real, bounded workflow. See [05-use-cases](../05-use-cases/benefits-eligibility-document-verification-agent.md).

**A pattern is a use case, not a separate abstraction.** Earlier versions of this repository listed generic "opportunity patterns" inside function files, some linked to a detailed use case and some marked "not yet detailed." That's been retired: if a pattern is worth naming, it gets written up as a real use case with its own page; if it isn't yet, it isn't listed as a phantom row. Function files now link directly to the use cases that live under them.

- **[04-grid/opportunity-grid.md](../04-grid/opportunity-grid.md)** — the function × domain matrix, for scanning fit at a glance before going to individual use cases.

## What Changed in a Use Case Page

Every use case entry now states, beyond the original problem/opportunity/risk description:

| Section | What it answers |
|---|---|
| Capability tag | Which mechanical pattern from the [Capability Taxonomy](../01-foundations/capabilities-and-outcomes.md) this is |
| Benefits | Concrete, stakeholder-specific benefits — what changes for the person doing the work and for the business, stated plainly, separate from the outcome-category Value Signal |
| Agentic Design | The single-agent architecture: what it reads, how it reasons step by step, what it produces |
| Multi-Agent Design | Where the task's scale or complexity genuinely warrants decomposing into multiple cooperating agents with distinct roles — not forced onto every use case |
| Autonomy → Outcome Mapping | What outcome is realistically achievable at each automation level (L1–L4), not just a single starting point and ceiling |

See the [use case template](../templates/use-case-template.md) for the full current structure.

## Worked Example: Tracing One Use Case

Take **"Invoice Processing & 3-Way Match Agent"**:

1. **Function:** [Finance & Accounting](../02-functions/finance-accounting.md).
2. **Domain:** Core in [Manufacturing](../03-domains/manufacturing.md) and [Retail & CPG](../03-domains/retail-cpg.md); applies generically wherever PO-based purchasing exists.
3. **Capability:** Extraction & Structured Validation — see [Capabilities & Outcomes](../01-foundations/capabilities-and-outcomes.md).
4. **Grid cell:** [04-grid/opportunity-grid.md](../04-grid/opportunity-grid.md) marks Finance × Manufacturing and Finance × Retail as "Core," linking to the use case.
5. **Use case entry:** [05-use-cases/invoice-processing-3way-match-agent.md](../05-use-cases/invoice-processing-3way-match-agent.md) has the full detail — problem, agentic and multi-agent design, autonomy-to-outcome mapping, benefits, risks.

Any use case in this repository can be traced the same way.

## Relationship to Companion Repositories

- **[OASIS](https://github.com/knowledgetrailsai/OASIS)** — once a use case here is selected for a pilot, OASIS's six-phase lifecycle (Engage & Align → ... → Optimize & Scale) governs how it's delivered.
- **[oasis-fulcrum (AI FinOps)](https://github.com/knowledgetrailsai/oasis-fulcrum)** — once scoped, use the Outcome & Value Definition Sheet there to formalize the value case this repository only sketches (see [Value Signal](../01-foundations/principles.md#value-signal-not-a-value-case)).
- **[Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI)** — every use case's "Key Risks & Guardrails" section should be expanded using that repository's risk taxonomy and controls before a real deployment.

This repository answers *"where should we look, and how would it actually work?"* The companion repositories answer *"how do we build it responsibly and economically?"*

---

**Next:** [How to Use This Repository](how-to-use-this-repository.md)
