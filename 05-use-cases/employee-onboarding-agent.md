# Employee Onboarding Agent

`Home › 05-use-cases › Employee Onboarding Agent`

**Primary Function:** [HR & People](../02-functions/hr-people.md)
**Primary Domains:** Applies generically across all domains
**Also Applicable To:** All domains, with added credentialing steps in regulated domains

## Problem / Trigger

New-hire onboarding involves coordinating multiple systems (IT provisioning, benefits enrollment, payroll setup, facility/equipment access) that are well-defined but manually tracked, causing delays and inconsistent day-one experiences.

## Agentic Automation Opportunity

Once a hire is confirmed, an agent orchestrates the onboarding checklist across systems — submitting IT provisioning requests, sending benefits enrollment instructions and deadlines, confirming equipment orders, and tracking completion — flagging any step that stalls past its expected timeframe to the HR coordinator.

## Automation Maturity

- **Realistic starting level:** L2 — agent orchestrates and tracks, human handles any exception or missing system integration
- **Potential ceiling:** L3 — agent handles the full standard onboarding workflow end-to-end for roles with no special requirements, escalating only non-standard cases
- **Why this range:** This is workflow orchestration against well-defined steps, not judgment-heavy decision-making — a good fit for higher automation than most HR use cases.

## Value Signal

- **Plausible outcome definition:** A new hire fully provisioned (IT access, benefits enrolled, equipment received) by their start date without manual chasing.
- **Plausible value basis:** Time saved (HR coordinator hours), risk reduced (fewer day-one access/equipment gaps).

## Key Risks & Guardrails

- Personal and sensitive employee data handled across multiple systems — see [HR & People risks](../02-functions/hr-people.md#key-cross-cutting-risks)
- Credentialing/background-check requirements in regulated domains must gate system access appropriately
- System integration failures should fail loudly to a human, not silently drop a step

## Related Use Cases

- [Candidate Screening & Scheduling Agent](candidate-screening-agent.md)
- [IT Helpdesk Tier-1 Agent](it-helpdesk-tier1-agent.md) — shares the IT provisioning touchpoint

---

**Back to:** [05-use-cases](.) · [HR & People](../02-functions/hr-people.md)
