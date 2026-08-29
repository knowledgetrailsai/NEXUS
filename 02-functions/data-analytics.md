# Function: Data & Analytics

`Home › 02-functions › Data & Analytics`

## Why This Function Is a Strong Fit

Analysts spend a disproportionate share of their time on repeatable groundwork — pulling data, checking it against known quality issues, and drafting the first-pass narrative around a chart — before they ever get to the judgment calls that actually require an analyst. That groundwork is exactly what agentic automation is good at.

**In plain terms:** think of this as a research assistant for anyone who works with data — it pulls the numbers, checks them, drafts a chart and a plain-language explanation, and hands it to a human to sanity-check and add the judgment a spreadsheet can't provide.

**For business readers:** the value here isn't replacing analysts — it's giving every team a faster first draft, so a business question raised on Monday doesn't wait until Thursday for someone with SQL access to get to it. The risk to manage is the opposite of the value: a wrong number delivered confidently is worse than no number at all, so verification discipline matters more here than speed.

**For technical readers:** this typically means an agent with read access to a data warehouse or BI semantic layer (never write access to source systems), a defined set of vetted metrics and their known caveats, and a drafting layer that produces a chart plus narrative — with every number traceable back to the query that produced it.

## Common Opportunity Patterns

| Pattern | Typical starting level | Use case |
|---|---|---|
| Self-service query drafting and insight narrative generation | L1 → L2 | [Self-Service Analytics & Insight Drafting Agent](../05-use-cases/self-service-analytics-insight-agent.md) |
| Data quality anomaly detection and flagging | L1 → L2 | Not yet detailed |
| Recurring report generation and distribution | L2 → L3 | Not yet detailed |
| Dashboard narrative summarization ("what changed and why") | L1 → L2 | Not yet detailed |

## Domain Applicability

| Domain | Notes |
|---|---|
| [Technology & SaaS](../03-domains/technology-saas.md), [Retail & CPG](../03-domains/retail-cpg.md) | Core — high data volume, mature warehouse/BI tooling |
| [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md) | Core, with materially higher requirements around numerical accuracy and auditability |
| [Scientific Research](../03-domains/scientific-research.md) | Adaptable — experimental data has stricter provenance requirements than business analytics |
| All other domains | Applies generically wherever a data warehouse or BI layer exists |

## Key Cross-Cutting Risks

- A confidently wrong number is the central failure mode of this function — every output needs a traceable path back to its source query
- Metric definitions drift across teams; an agent trained on one team's definition can silently misapply it elsewhere
- Narrative generation can imply causation from correlation if not explicitly constrained

---

**Previous:** [Marketing](marketing.md)
**Next:** [HR & People](hr-people.md)
