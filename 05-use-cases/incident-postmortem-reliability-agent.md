# Incident Postmortem & Reliability Reporting Agent

`Home › 05-use-cases › Incident Postmortem & Reliability Reporting Agent`

**Exclusive domain:** [Technology & SaaS](../03-domains/technology-saas.md)
**Primary Function:** [IT & Security](../02-functions/it-security.md)

## Who This Is For

- **In plain terms:** after a system outage or incident, someone has to write up what happened, pulling together timelines, logs, and Slack threads into a coherent postmortem — a task that's important but often gets rushed or delayed because everyone wants to move on to fixing the actual problem. This agent drafts the first version from the available evidence, so the engineering team edits and adds judgment instead of starting from a blank page.
- **For business readers:** postmortem quality directly affects whether the same incident happens again — a rushed or incomplete writeup means the real root cause and follow-up actions get lost. Making the drafting step faster increases the chance a thorough postmortem actually gets written.
- **For technical readers:** this means integration with incident-management tooling, logging/observability platforms, and chat history for the incident channel — assembling a timeline and draft root-cause narrative from available evidence, with the engineering team verifying and completing the analysis.

## Problem / Trigger

Writing a thorough incident postmortem requires reconstructing a timeline from multiple systems (monitoring, logs, chat, ticketing) and drafting a root-cause narrative — valuable but time-consuming work that competes with the pressure to move on once an incident is resolved, often resulting in a thin or delayed writeup.

## Agentic Automation Opportunity

Following an incident's resolution, the agent assembles a timeline from monitoring, logging, and incident-channel data, drafts a first-pass narrative of what happened and a candidate root-cause hypothesis, and structures it into the team's postmortem template — the engineering team verifies, corrects, and completes the root-cause analysis and action items.

## Boundary, Maturity & Value

- **Starting / ceiling:** L1 / L2. Agent drafts and structures from available evidence; the engineering team verifies and owns the final root-cause determination and action items.
- **Outcome:** A complete, evidence-backed postmortem draft available immediately after incident resolution rather than days later (or not at all).
- **Value basis:** Time saved (engineer postmortem-writing hours), risk reduced (fewer incidents without a completed postmortem, meaning fewer repeat failures from an unaddressed root cause).
- **Exceptions:** Any incident involving a security breach, data loss, or customer-data exposure routes through the security incident-response process rather than the standard postmortem flow.

_Indicative scale:_
`L1 (assist) ●○ — L2 (automate, reviewed) — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## KPIs Influenced

- **Leading:** Time from incident resolution to postmortem draft, percentage of incidents with a completed postmortem, draft-to-final edit distance (how much the team had to change).
- **Lagging:** Repeat-incident rate for the same root cause, mean time to resolution trend, engineering time spent on postmortems.

## Key Risks & Guardrails

- A confidently wrong root-cause hypothesis in a draft can anchor the team's thinking — the draft must be clearly labeled as a starting hypothesis, not a conclusion
- Security-relevant incidents need a materially different process (and different data handling) than standard reliability postmortems
- Blameless-postmortem culture depends on how incidents are described — the agent's narrative must describe events and systems, not attribute fault to individuals

## Related Use Cases

- [Self-Service Analytics & Insight Drafting Agent](self-service-analytics-insight-agent.md) — related evidence-synthesis-and-draft pattern
- [Continuous Controls Testing Agent](continuous-controls-testing-agent.md) — related exhaustive-evidence pattern, different function

---

**Back to:** [Technology & SaaS](../03-domains/technology-saas.md)
