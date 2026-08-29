# Underwriting Risk Data Assembly Agent

`Home › 05-use-cases › Underwriting Risk Data Assembly Agent`

**Exclusive domain:** [Insurance](../03-domains/insurance.md)
**Primary Function:** [Data & Analytics](../02-functions/data-analytics.md)

## Who This Is For

- **In plain terms:** before an underwriter decides whether and how to price a policy, they need a full picture — application details, prior claims history, and relevant external risk data (property records, driving history, industry risk factors). Pulling that together today is manual; this agent assembles the full risk file so the underwriter starts from a complete picture instead of building one first.
- **For business readers:** underwriter time spent assembling data instead of judging risk is pure overhead — compressing that step lets underwriters handle more submissions at the same quality, without changing who actually prices the risk.
- **For technical readers:** this means integration with the policy administration system, claims history database, and authorized external data sources (property/vehicle records, industry risk databases), assembled into a structured underwriting file — the agent never computes or recommends a price or risk tier itself.

## Problem / Trigger

Underwriters spend a meaningful share of their time pulling application data, claims history, and external risk records together into a usable file before they can begin the actual risk assessment — a repeatable assembly task, not a judgment task, that nonetheless consumes senior underwriting time.

## Agentic Automation Opportunity

Given a new submission, the agent retrieves application data, prior claims history, and relevant external risk records, and assembles them into a structured underwriting file with source citations — flagging any missing or inconsistent data rather than presenting an incomplete picture as complete. The underwriter makes every pricing and risk-tier decision from the assembled file.

## Boundary, Maturity & Value

- **Starting / ceiling:** L1 / L2. Agent assembles and structures data; underwriter makes every risk and pricing judgment. Ceiling stays at L2 (reviewed assembly) — pricing/risk-tier decisions are not a target for automation in this use case.
- **Outcome:** A complete, sourced underwriting file available at submission intake instead of after manual assembly, shortening time-to-quote.
- **Value basis:** Time saved (underwriter assembly hours), cycle-time reduction (faster time-to-quote), risk reduced (fewer submissions underwritten on an incomplete picture).
- **Exceptions:** Missing or conflicting external data, submissions in lines of business without a documented data-source mapping, and any request to interpret risk significance escalate to the underwriter.

_Indicative scale:_
`L1 (assist) ●○ — L2 (automate, reviewed) — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## KPIs Influenced

- **Leading:** Time-to-complete-file at submission, data-source coverage rate, flagged-gap rate.
- **Lagging:** Time-to-quote, underwriter submissions handled per period, rate of post-bind claims linked to a risk factor that was in available data but missed pre-bind.

## Key Risks & Guardrails

- The agent must never imply a risk judgment through how it presents data (ordering, emphasis) — assembly and interpretation are different tasks, and only the underwriter does the latter
- External data source staleness (a lapsed record check) can create a false sense of completeness
- Data source access must respect the same regulatory and consent boundaries as manual underwriting research

## Related Use Cases

- [Claims Intake & Triage Agent](claims-intake-triage-agent.md) — related structured-intake pattern, different stage of the policy lifecycle
- [KYC Document Review & Account Opening Agent](kyc-account-opening-review-agent.md) — related document-assembly-for-decision pattern, different domain

---

**Back to:** [Insurance](../03-domains/insurance.md)
