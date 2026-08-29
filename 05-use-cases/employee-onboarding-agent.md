# Employee Onboarding Agent

`Home › 05-use-cases › Employee Onboarding Agent`

**Primary Function:** [HR & People](../02-functions/hr-people.md)
**Primary Domains:** Applies generically across all domains
**Also Applicable To:** All domains, with added credentialing steps in regulated domains
**Capability:** Scheduling & Constrained Optimization (secondary: Classification & Routing, for exception escalation)
**Outcome Categories:** Time Saved, Risk Reduced
**Business Outcome Category:** Efficiency

## Problem / Trigger

New-hire onboarding involves coordinating multiple systems (IT provisioning, benefits enrollment, payroll setup, facility/equipment access) that are well-defined but manually tracked, causing delays and inconsistent day-one experiences.

## Agentic Automation Opportunity

Once a hire is confirmed, an agent orchestrates the onboarding checklist across systems — submitting IT provisioning requests, sending benefits enrollment instructions and deadlines, confirming equipment orders, and tracking completion — flagging any step that stalls past its expected timeframe to the HR coordinator.

## Benefits

- **For the HR coordinator:** far less manual chasing across IT, benefits, payroll, and facilities — the coordinator's time goes to the exceptions and the new hire's actual first-day experience.
- **For the business:** a new hire fully provisioned by their start date, avoiding the productivity loss and poor first impression of day-one access gaps.
- **For the new hire:** a smoother, more consistent onboarding experience regardless of which team or manager they're joining.

## Agentic Design

- **Inputs read:** the confirmed hire record (role, start date, location), and the standard onboarding checklist per role type.
- **Reasoning steps:** once a hire is confirmed, orchestrate the onboarding checklist across systems → submit IT provisioning requests → send benefits enrollment instructions and deadlines → confirm equipment orders → track completion of every step against its expected timeframe → flag any step that stalls to the HR coordinator.
- **Tools/actions available:** write access to submit provisioning/equipment requests and enrollment communications across integrated systems; no autonomous action on anything outside the standard, pre-approved checklist.
- **Output produced:** a tracked onboarding checklist with all steps submitted and monitored, and stall alerts when a step misses its expected timeframe.

## Multi-Agent Design (where relevant)

Worth considering across large, multi-system onboarding stacks: a **per-system submission agent** for each integrated system (IT, benefits, payroll, facilities) handles that system's specific API/format quirks, while an **orchestrator agent** tracks overall checklist completion and raises the stall alert — rather than one agent needing deep integration knowledge of every HR-adjacent system at once.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Orchestrates and tracks the full checklist across systems | HR coordinator handles any exception or missing system integration | Consistent day-one provisioning for standard roles; coordinator time freed from manual chasing |
| L3 (automate, exception-routed) | Handles the full standard onboarding workflow end-to-end for roles with no special requirements | HR coordinator handles only non-standard cases | Full standard-role coverage without proportional coordinator time, non-standard roles still fully human-handled |

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
