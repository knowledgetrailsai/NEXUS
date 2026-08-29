# Claims Intake & Triage Agent

`Home › 05-use-cases › Claims Intake & Triage Agent`

**Exclusive domain:** [Insurance](../03-domains/insurance.md)
**Primary Functions:** [Claims Management](../02-functions/claims-management.md), [Customer Relations & Support](../02-functions/customer-relations-support.md)

## Problem / Trigger

First notice of loss arrives through many channels in inconsistent formats, and manual intake delays routing to the right adjuster while increasing the risk of missed fraud indicators or coverage red flags.

## Agentic Automation Opportunity

The agent captures claim details from the reporting channel, verifies policy coverage and status, checks for known fraud indicators against documented rules, assigns severity and routes to the correct adjuster queue, and sends the claimant an acknowledgment with next steps — never itself approving, denying, or valuing a claim.

## Boundary, Maturity & Value

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
