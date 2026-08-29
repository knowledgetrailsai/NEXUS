# Experiment Data Quality & Reproducibility Check Agent

`Home › 05-use-cases › Experiment Data Quality & Reproducibility Check Agent`

**Exclusive domain:** [Scientific Research & Life Sciences R&D](../03-domains/scientific-research.md)
**Primary Function:** [Data & Analytics](../02-functions/data-analytics.md)

## Who This Is For

- **In plain terms:** before results from an experiment get written up or acted on, someone should check the underlying data for the kind of problems that quietly undermine a result — missing values, outliers, inconsistent units, a protocol deviation that wasn't flagged. This agent runs that check systematically instead of relying on a researcher noticing by eye.
- **For business readers:** a result built on a data-quality issue that surfaces late (after publication, after a go/no-go decision) is far more expensive to fix than one caught before anyone relies on it — systematic checking at the point of data collection is cheap insurance against that.
- **For technical readers:** this means integration with ELN/LIMS data exports, applying documented data-quality rules (range checks, unit consistency, missingness patterns, protocol-deviation flags) and comparing against prior runs of the same protocol for anomalies — the agent flags issues for researcher review, it never adjusts, excludes, or reinterprets data itself.

## Problem / Trigger

Experimental data quality issues (missing values, unit inconsistencies, unflagged protocol deviations, statistical outliers) are typically caught only when a researcher happens to notice them during analysis — often well after data collection, when correcting the issue is harder or impossible.

## Agentic Automation Opportunity

As experimental data is recorded, the agent checks it against documented data-quality rules and prior-run patterns for the same protocol, flagging anomalies, missingness, and potential protocol deviations for the researcher's review — the researcher decides whether a flagged issue affects the result's validity; the agent never excludes data or adjusts an analysis itself.

## Boundary, Maturity & Value

- **Starting / ceiling:** L1 / L2. Agent flags for every case; researcher reviews and decides how to handle every flagged issue. This stays at L1–L2 as a permanent posture, matching this domain's general posture on anything touching result validity.
- **Outcome:** Data-quality issues caught at or near the point of collection rather than during downstream analysis or after publication.
- **Value basis:** Time saved (researcher time not spent discovering data issues late), risk reduced (fewer results built on an unnoticed data-quality problem).
- **Exceptions:** Any flagged issue that could affect a result already used in a decision, submission, or publication routes to the researcher and study lead immediately, not the standard review queue.

_Indicative scale:_
`L1 (assist) ●○ — L2 (automate, reviewed) — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## KPIs Influenced

- **Leading:** Time between data collection and quality-flag review, flag-confirmation rate (real issues vs. false positives), percentage of experimental runs checked.
- **Lagging:** Rate of data-quality issues discovered post-analysis (should decline as this catches them earlier), rework time from issues caught late.

## Key Risks & Guardrails

- The agent must never exclude, adjust, or reinterpret data — flagging is its entire role, and the decision about what a flag means for the result stays with the researcher
- A data-quality rule library that's miscalibrated for a specific protocol can generate noise that gets ignored — validate rules against real protocol variation before relying on them
- This is not a substitute for statistical or experimental-design review — it catches data mechanics issues, not whether the experiment itself was well-designed

## Related Use Cases

- [Literature Review & Research Synthesis Agent](literature-review-research-synthesis-agent.md) — related research-integrity-focused pattern, different stage of the research process
- [Self-Service Analytics & Insight Drafting Agent](self-service-analytics-insight-agent.md) — related data-quality pattern, different domain

---

**Back to:** [Scientific Research & Life Sciences R&D](../03-domains/scientific-research.md)
