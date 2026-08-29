# Knowledge Map

`Home › 00-navigation-and-methodology › Knowledge Map`

## The Core Idea: A Grid, Not a List

Business functions — Purchasing, Sales, Customer Relations, HR, Finance, IT, Legal, Supply Chain — repeat across nearly every industry. The *pattern* of an agentic automation opportunity in Procurement is often 80% the same whether the company is a bank, a hospital, or a manufacturer. What differs is the domain-specific 20%: regulation, data sensitivity, systems of record, and risk tolerance.

This repository is organized as a **grid** to avoid re-describing the same pattern nine times:

```
FUNCTION (the common pattern) × DOMAIN (the industry-specific variant) → USE CASE
```

- **[02-functions](../02-functions/)** — one file per business function, describing the automation pattern generically and noting which domains it applies to.
- **[03-domains](../03-domains/)** — one file per industry, describing domain-specific context (regulation, systems, risk posture) and which functions matter most there.
- **[04-grid/opportunity-grid.md](../04-grid/opportunity-grid.md)** — the matrix itself, function × domain, linking to specific use cases where a domain-specific variant exists.
- **[05-use-cases](../05-use-cases/)** — the actual, concrete use case entries. A use case belongs to one primary function, and lists every domain it applies to (generically or with named variants).

## Worked Example: Tracing One Use Case

Take **"Invoice Processing & 3-Way Match Agent"**:

1. **Function:** Lives under [02-functions/finance-accounting.md](../02-functions/finance-accounting.md) as a common Finance automation pattern.
2. **Domains:** Applies broadly, but has notable variants in [Manufacturing](../03-domains/manufacturing.md) (PO/receiving-heavy) and [Retail & CPG](../03-domains/retail-cpg.md) (high volume, low unit value).
3. **Grid cell:** [04-grid/opportunity-grid.md](../04-grid/opportunity-grid.md) marks Finance × Manufacturing and Finance × Retail as "Core," linking to the use case.
4. **Use case entry:** [05-use-cases/invoice-processing-3way-match-agent.md](../05-use-cases/invoice-processing-3way-match-agent.md) has the full detail — problem, agentic pattern, maturity level, value signal, risks.

Any use case in this repository can be traced the same way — function first, domain second, grid ties them together.

## Relationship to Companion Repositories

- **[OASIS](https://github.com/knowledgetrailsai/OASIS)** — once a use case here is selected for a pilot, OASIS's six-phase lifecycle (Engage & Align → ... → Optimize & Scale) governs how it's delivered.
- **[oasis-fulcrum (AI FinOps)](https://github.com/knowledgetrailsai/oasis-fulcrum)** — once scoped, use the Outcome & Value Definition Sheet there to formalize the value case this repository only sketches (see [Value Signal](../01-foundations/principles.md#value-signal-not-a-value-case)).
- **[Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI)** — every use case's "Key Risks & Guardrails" section should be expanded using that repository's risk taxonomy and controls before a real deployment.

This repository answers *"where should we look?"* The companion repositories answer *"how do we build it responsibly and economically?"*

---

**Next:** [How to Use This Repository](how-to-use-this-repository.md)
