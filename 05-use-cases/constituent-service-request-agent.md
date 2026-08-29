# Constituent Service Request Routing Agent

`Home › 05-use-cases › Constituent Service Request Routing Agent`

**Exclusive domain:** [Public Sector & Government](../03-domains/public-sector.md)
**Primary Function:** [Customer Relations & Support](../02-functions/customer-relations-support.md)
**Capability:** Classification & Routing
**Outcome Categories:** Time Saved, Coverage & Consistency Improved
**Business Outcome Category:** Customer & Employee Experience

## Problem / Trigger

Constituent requests (permits, benefits status, non-emergency service issues, records requests) arrive through many channels and departments, and manual triage causes delays, misroutes, and inconsistent handling of time-sensitive or vulnerable-constituent cases.

## Agentic Automation Opportunity

The agent classifies the request type and urgency, retrieves the constituent's case status from the relevant system, answers informational questions from approved public guidance, and creates or routes a case to the correct department — never itself approving a benefit, permit, or exception to policy.

## Benefits

- **For caseworkers:** requests arrive pre-classified and pre-routed, reducing time spent on triage that isn't actually the caseworker's specialty.
- **For the department:** more consistent handling of routine requests, and faster acknowledgment on time-sensitive ones.
- **For constituents:** faster response and fewer instances of a request bouncing between departments before reaching the right one.

## Agentic Design

- **Inputs read:** the constituent's request (any channel), the constituent's case status where relevant, and approved public guidance documents.
- **Reasoning steps:** classify the request type and urgency → retrieve the constituent's case status from the relevant system → answer informational questions from approved public guidance → create or route a case to the correct department.
- **Tools/actions available:** read access to case-status systems and approved guidance; write access limited to case creation/routing and informational responses — never a benefit, permit, or policy-exception decision.
- **Output produced:** a routed case and, where applicable, a grounded informational answer.

## Multi-Agent Design (where relevant)

Not needed as a default — classification, informational lookup, and routing form one bounded, sequential flow appropriate for a single agent given this domain's conservative automation posture.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Routes and answers informational questions from approved guidance | Caseworker handles anything requiring an eligibility/benefit decision | Faster routing and informational response; decision authority unchanged |
| L3 (automate, exception-routed) | Same, at full routing coverage for administrative requests | Caseworker handles only escalations and all substantive decisions | Full administrative-routing coverage with caseworker time concentrated on substantive cases |

- **Starting / ceiling:** L2 / L3 for routing and informational response; eligibility and benefit decisions stay L1, human-owned.
- **Outcome:** Requests routed correctly on first contact with fewer handoffs and faster acknowledgment.
- **Value basis:** Staff triage time saved, faster response time, and reduced repeat-contact volume.
- **Exceptions:** Safety or welfare concerns, legal/records requests, appeals, and identity-verification failures escalate to a caseworker immediately.

## Evaluation & Guardrails

Measure routing accuracy, response groundedness against approved guidance, missed-urgency rate, and accessibility compliance. Disclose automation to constituents, minimize retained personal data, enforce role-based access to case systems, and preserve a human appeal path for every automated response.

## Related Use Cases

- [Student Services Case Routing Agent](student-services-case-routing-agent.md) — closely related pattern
- [Tier-1 Support Resolution Agent](tier1-support-resolution-agent.md)

---

**Back to:** [Public Sector & Government](../03-domains/public-sector.md)
