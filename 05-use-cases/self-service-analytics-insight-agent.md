# Self-Service Analytics & Insight Drafting Agent

`Home › 05-use-cases › Self-Service Analytics & Insight Drafting Agent`

**Primary Function:** [Data & Analytics](../02-functions/data-analytics.md)
**Primary Domains:** [Technology & SaaS](../03-domains/technology-saas.md), [Retail & CPG](../03-domains/retail-cpg.md), [Financial Services](../03-domains/financial-services.md)
**Also Applicable To:** Any domain with a warehouse or BI semantic layer in place

## Who This Is For

- **In plain terms:** anyone who has a business question that needs a number — "how did signups change last month," "which region is underperforming" — normally has to wait for someone on the data team to pull it. This agent answers the question directly from the company's approved data, shows the chart, and explains it in plain language, with the underlying query visible so the number can be checked.
- **For business readers:** the value is speed and reach — a question that used to sit in an analyst's queue for days gets a first-draft answer immediately, freeing analysts for the harder questions that actually need their judgment. The corresponding discipline is that "fast" must not mean "unverified" — a wrong number stated confidently is more damaging to decision-making than a slow right one.
- **For technical readers:** this means an agent with read-only access to a data warehouse or BI semantic layer (never to raw production systems), a vetted metric library with documented definitions and known caveats, and a drafting layer that produces a chart plus narrative — with the generated query attached so any number is independently checkable.

## Problem / Trigger

Business teams routinely need answers to data questions that require SQL or BI-tool fluency they don't have, creating a queue on the analytics team for work that's often more about translation (business question → query) than genuine analytical judgment.

## Agentic Automation Opportunity

Given a natural-language business question, the agent translates it into a query against the vetted metric library and semantic layer, generates a chart, and drafts a plain-language narrative explaining what the data shows — attaching the underlying query and flagging any known caveats on the metrics used, rather than presenting the number without context. Novel or ambiguous questions that fall outside the vetted metric library route to a human analyst.

## Automation Maturity

- **Realistic starting level:** L1 — agent drafts query, chart, and narrative; analyst spot-checks before wider distribution
- **Potential ceiling:** L2 — agent answers vetted, well-defined metric questions directly for broad self-service use, with analysts reviewing only novel or high-stakes requests
- **Why this range:** Vetted metrics with documented definitions are safe to automate at scale; anything requiring new metric definition or judgment about what to measure stays analyst-led.

_Indicative scale:_
`L1 (assist) ● — L2 (automate, reviewed) ○ — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## Value Signal

- **Plausible outcome definition:** A business question answered accurately from the vetted metric library without analyst involvement, freeing analyst time for questions that genuinely require judgment.
- **Plausible value basis:** Time saved (analyst hours, requester wait time), faster decision cycles from immediate self-service answers.

## KPIs Influenced

- **Leading:** Percentage of data requests self-served without analyst involvement, time-to-answer for business questions, query-accuracy spot-check pass rate.
- **Lagging:** Analyst time reallocated to higher-judgment work, decision cycle time for data-informed business decisions, rate of decisions made on stale or manually-pulled (and therefore potentially outdated) data.

## Key Risks & Guardrails

- A confidently wrong number is the central failure mode — every output needs a visible, checkable query behind it, not just a polished narrative
- Metric definitions can drift or be misapplied across teams; the agent must use the vetted library's definition, not infer its own
- Narrative drafting can imply causation from correlation if not explicitly constrained to describe what the data shows, not why

## Related Use Cases

- [Expense Audit Agent](expense-audit-agent.md) — related structured-data-review pattern, different function

---

**Back to:** [05-use-cases](.) · [Data & Analytics](../02-functions/data-analytics.md)
