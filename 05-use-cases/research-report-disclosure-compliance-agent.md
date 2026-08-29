# Research Report Disclosure Compliance Agent

`Home › 05-use-cases › Research Report Disclosure Compliance Agent`

**Exclusive domain:** [Capital Markets & Investment Banking](../03-domains/capital-markets-investment-banking.md)
**Primary Function:** [Legal & Compliance](../02-functions/legal-compliance.md)

## Who This Is For

- **In plain terms:** when an analyst publishes research on a company or security, strict rules govern what disclosures must be included (conflicts of interest, ratings history, required disclaimers) — a compliance reviewer checks every report against those rules before publication. This agent does the first pass, checking the report against the documented disclosure requirements and flagging anything missing before it reaches the compliance reviewer.
- **For business readers:** a missed disclosure isn't a minor error — it's a regulatory violation with direct enforcement exposure. Catching gaps before compliance review, at full coverage instead of relying on the reviewer alone, adds a real layer of protection without slowing down publication for the majority of reports that are already compliant.
- **For technical readers:** this means checking a research report's text against the documented disclosure-requirement library (analyst holdings, banking relationships, rating-history rules, required disclaimers by jurisdiction and security type) — flagging gaps for the compliance reviewer, never approving a report for publication itself.

## Problem / Trigger

Research reports must include specific, often jurisdiction- and security-type-dependent disclosures before publication, and checking every report against the full disclosure requirement set is a manual, checklist-heavy task that competes with publication-speed pressure.

## Agentic Automation Opportunity

Before a research report goes to compliance review, the agent checks it against the documented disclosure-requirement library for the relevant jurisdiction and security type, flags any missing or incomplete disclosure with the specific requirement cited, and passes a structured checklist to the compliance reviewer alongside the report — the reviewer makes the final publication decision.

## Boundary, Maturity & Value

- **Starting / ceiling:** L1 / L2. Agent checks and flags for every report; compliance reviewer approves every publication. This function should stay at L1–L2 as a permanent posture given publication-decision stakes.
- **Outcome:** Disclosure gaps caught before compliance review on every report, not just the ones a reviewer happens to catch under time pressure.
- **Value basis:** Risk reduced (regulatory exposure from a missed disclosure caught before publication), time saved (compliance reviewer time reallocated from manual checklist review to substantive review).
- **Exceptions:** Any report on a novel security type, cross-jurisdiction publication, or a disclosure requirement not covered in the documented library escalates to compliance immediately.

_Indicative scale:_
`L1 (assist) ●○ — L2 (automate, reviewed) — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## KPIs Influenced

- **Leading:** Disclosure-gap catch rate before compliance review, time added to publication cycle, checklist-coverage completeness per report.
- **Lagging:** Post-publication disclosure violations found by compliance audit or regulator, compliance reviewer time per report, publication cycle time.

## Key Risks & Guardrails

- A stale or incomplete disclosure-requirement library produces confidently wrong "all clear" results — this library needs active, documented maintenance as rules change across jurisdictions
- Publication approval is a compliance judgment that must remain human-owned regardless of how mature the checking becomes
- A missed disclosure requirement not yet in the documented library is a gap in the tool, not a false negative to tolerate — track and close these gaps deliberately

## Related Use Cases

- [Trade Surveillance & Market Abuse Detection Agent](trade-surveillance-market-abuse-agent.md) — related compliance-evidence pattern, different stage of the research-to-trading lifecycle
- [Contract Review & Redline Agent](contract-review-redline-agent.md) — related documented-checklist review pattern

---

**Back to:** [Capital Markets & Investment Banking](../03-domains/capital-markets-investment-banking.md)
