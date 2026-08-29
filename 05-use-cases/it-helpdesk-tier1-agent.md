# IT Helpdesk Tier-1 Agent

`Home › 05-use-cases › IT Helpdesk Tier-1 Agent`

**Primary Function:** [IT & Security](../02-functions/it-security.md)
**Primary Domains:** Applies generically across all domains
**Also Applicable To:** All domains, with tighter scoping in higher-security-posture domains

## Problem / Trigger

The majority of internal IT tickets (password resets, access requests, common software issues, standard hardware requests) follow known runbooks but still require a human agent to execute the same steps repeatedly.

## Agentic Automation Opportunity

An agent classifies incoming IT tickets, executes standard, pre-approved remediation runbooks (password reset, standard software install request, common troubleshooting steps) via API to IT systems, and escalates anything outside the defined runbook set — with all actions logged for audit.

## Automation Maturity

- **Realistic starting level:** L2 — agent executes standard runbooks, human reviews low-confidence classifications
- **Potential ceiling:** L3 — agent handles the full standard runbook set autonomously, escalating genuine exceptions
- **Why this range:** Very similar risk/reward profile to [Tier-1 Support Resolution](tier1-support-resolution-agent.md), but internal-facing, which somewhat lowers external reputational risk while system-access actions still warrant care.

## Value Signal

- **Plausible outcome definition:** A ticket resolved via a standard runbook without human execution, and without a repeat ticket on the same issue within a defined window.
- **Plausible value basis:** Cost avoided (IT support hours), time saved (employee wait time for resolution).

## Key Risks & Guardrails

- **Any action not trivially reversible should stay at L2 with human confirmation** — see [IT & Security risks](../02-functions/it-security.md#key-cross-cutting-risks)
- Agent access to IT systems is itself a privileged-access surface requiring the same governance as any privileged account
- Runbook actions must be scoped narrowly — this is not a general system-administration agent

## Related Use Cases

- [Tier-1 Support Resolution Agent](tier1-support-resolution-agent.md) — closely related pattern, external-facing
- [Employee Onboarding Agent](employee-onboarding-agent.md) — shares the IT provisioning touchpoint

---

**Back to:** [05-use-cases](.) · [IT & Security](../02-functions/it-security.md)
