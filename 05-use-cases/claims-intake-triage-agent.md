# Claims Intake & Triage Agent

`Home › 05-use-cases › Claims Intake & Triage Agent`

**Exclusive domain:** [Insurance](../03-domains/insurance.md)
**Primary Functions:** [Claims Management](../02-functions/claims-management.md), [Customer Relations & Support](../02-functions/customer-relations-support.md)
**Capability:** Classification & Routing
**Outcome Categories:** Time Saved, Risk Reduced, Coverage & Consistency Improved
**Business Outcome Category:** Customer & Employee Experience

## Problem / Trigger

First notice of loss arrives through many channels in inconsistent formats, and manual intake delays routing to the right adjuster while increasing the risk of missed fraud indicators or coverage red flags.

## Agentic Automation Opportunity

The agent captures claim details from the reporting channel, verifies policy coverage and status, checks for known fraud indicators against documented rules, assigns severity and routes to the correct adjuster queue, and sends the claimant an acknowledgment with next steps — never itself approving, denying, or valuing a claim.

## Benefits

- **For the claimant:** faster acknowledgment and a clear next step immediately after reporting a loss, instead of waiting for manual triage.
- **For the adjuster:** cases arrive pre-verified and pre-severity-scored, so time goes to investigation and decision rather than data assembly.
- **For the insurer:** fraud indicators get checked on every claim at intake, not just the ones an adjuster happens to notice.

## Agentic Design

- **Inputs read:** the claim report (whatever channel it arrives through), the policy administration system, and documented fraud-indicator rules.
- **Reasoning steps:** capture claim details from the reporting channel → verify policy coverage and status → check for known fraud indicators against documented rules → assign severity → route to the correct adjuster queue → send the claimant an acknowledgment with next steps.
- **Tools/actions available:** read access to the policy administration system; write access limited to case creation, routing, and a templated acknowledgment message — never a coverage or valuation determination.
- **Output produced:** a routed, severity-scored claim case with a claimant acknowledgment.

## Multi-Agent Design (where relevant)

Not needed as a default — intake, verification, and routing are one bounded, sequential flow. Fraud-indicator checking could run as a separate specialized model feeding into this agent's routing decision if the fraud-detection logic grows complex enough to warrant independent tuning and evaluation.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Intake, verification, fraud-flagging, and routing for every claim | Adjuster handles disposition and settlement | Faster, consistent intake at full coverage; coverage/settlement decisions unchanged |
| L3 (automate, exception-routed) | Same, at full coverage with only genuine exceptions surfaced | Adjuster handles only flagged exceptions and all disposition decisions | Full intake/triage automation with adjuster time concentrated on investigation and decisions |

- **Starting / ceiling:** L2 / L3 for intake and routing; coverage and settlement decisions remain L1 (human-owned) indefinitely.
- **Outcome:** Claims routed to the correct queue with complete intake on first contact, fewer misroutes and reopens.
- **Value basis:** Adjuster time saved, faster time-to-first-contact, and improved fraud-flag catch rate at intake.
- **Exceptions:** Suspected fraud, coverage disputes, catastrophic or high-severity losses, and claimant vulnerability signals escalate immediately.

## Evaluation & Guardrails

Measure routing accuracy, intake completeness, fraud-flag precision/recall, and time-to-first-contact. Never let the agent communicate a coverage determination, retain the policy version and evidence behind every triage decision, and preserve an audit trail from first notice to adjuster handoff.

## Related Use Cases

- [Tier-1 Support Resolution Agent](tier1-support-resolution-agent.md) — related intake-and-route pattern
- [Hotel Service Recovery Agent](hotel-service-recovery-agent.md) — related bounded-remedy pattern

---

**Back to:** [Insurance](../03-domains/insurance.md)
