# Hotel Service Recovery Agent

`Home › 05-use-cases › Hotel Service Recovery Agent`

**Exclusive domain:** [Travel & Hospitality](../03-domains/travel-hospitality.md)
**Primary Functions:** [Customer Relations & Support](../02-functions/customer-relations-support.md), [Finance & Accounting](../02-functions/finance-accounting.md)
**Capability:** Conversational Resolution
**Outcome Categories:** Time Saved, Revenue Influenced (retention)
**Business Outcome Category:** Customer & Employee Experience

## Problem / Trigger

Guests report room, housekeeping, amenity, or billing failures while staff coordinate across property systems and compensation policies.

## Agentic Automation Opportunity

The agent identifies the reservation, verifies the issue, checks property policy and guest history, proposes a remedy, creates the operational task, and issues only pre-authorized low-value credits.

## Benefits

- **For hotel staff:** the agent handles reservation lookup, policy checking, and low-value credit issuance, freeing staff to focus on the guest interaction itself and on cases that need real judgment.
- **For the property:** consistent compensation decisions across similar incidents, instead of ad hoc amounts varying by which staff member handled it.
- **For the guest:** faster acknowledgment and resolution of a service failure, with a task actually created and tracked rather than a verbal promise that may not get followed up.

## Agentic Design

- **Inputs read:** the reservation record, property service-recovery policy, and guest history.
- **Reasoning steps:** identify the reservation → verify the reported issue → check property policy and guest history → propose a remedy → create the operational task → issue only pre-authorized low-value credits.
- **Tools/actions available:** read access to reservation and policy systems; a write action limited to creating an operational task and issuing a credit within a pre-authorized cap — no autonomous authority above that cap.
- **Output produced:** a proposed remedy, a created operational task, and (within cap) an issued credit.

## Multi-Agent Design (where relevant)

Not needed as a default — this is a single, sequential guest-recovery workflow. Not worth splitting into multiple agents given the bounded scope and the explicit low-value credit cap that already limits blast radius.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Recommends a remedy and drafts the operational task | Staff approves every recommendation and credit before issuance | Faster, more consistent proposed remedies; issuance authority stays fully human |
| L3 (automate, exception-routed) | Same, plus bounded service recovery (task creation and low-value credit) for standard incidents | Staff handles only escalations above the exception thresholds | Faster resolution for the majority of standard incidents, staff time concentrated on genuine escalations |

- **Starting / ceiling:** L2 / L3. Human-approved recommendations first; bounded service recovery for standard incidents.
- **Outcome:** Issue acknowledged, owned, and resolved within the service promise with consistent compensation.
- **Value basis:** Resolution time, repeat-contact reduction, staff coordination, and retention.
- **Exceptions:** Safety, discrimination, injury, privacy, suspected fraud, and compensation above threshold escalate to management.

## Evaluation & Guardrails

Measure correct reservation matching, task completion, resolution time, compensation accuracy, guest satisfaction, and escalation recall. Enforce least privilege, cap credits, log policy versions and approvals, and never expose another guest's information.

---

**Back to:** [Travel & Hospitality](../03-domains/travel-hospitality.md)
