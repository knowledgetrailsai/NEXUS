# Travel Disruption Rebooking Agent

`Home › 05-use-cases › Travel Disruption Rebooking Agent`

**Exclusive domain:** [Travel & Hospitality](../03-domains/travel-hospitality.md)
**Primary Functions:** [Customer Relations & Support](../02-functions/customer-relations-support.md), [Sales](../02-functions/sales.md)
**Capability:** Scheduling & Constrained Optimization (secondary: Conversational Resolution)
**Outcome Categories:** Time Saved, Revenue Influenced (retention)
**Business Outcome Category:** Customer & Employee Experience

## Problem / Trigger

Cancellation, delay, weather, or missed connection creates a time-sensitive need to find compliant alternatives across inventory, fare rules, passenger needs, and partner systems.

## Agentic Automation Opportunity

The agent detects disruption, retrieves the booking and applicable policy, ranks viable alternatives, presents trade-offs, and books only within a customer-approved and policy-bounded envelope.

## Benefits

- **For the service team:** ranked, policy-checked alternatives arrive ready to present, instead of staff manually searching inventory and checking fare rules under time pressure.
- **For the business:** faster reaccommodation reduces missed connections and the downstream cost of a stranded traveler, and consistent policy-bounded booking reduces both overcommitment and inconsistent compensation.
- **For the traveler:** a faster path to a valid alternative or a clear escalation, before their next decision deadline rather than after it's passed.

## Agentic Design

- **Inputs read:** the disruption event, the booking record, applicable fare/compensation policy, and available inventory across partner systems.
- **Reasoning steps:** detect the disruption → retrieve the booking and applicable policy → rank viable alternatives → present trade-offs to the customer → book only within a customer-approved and policy-bounded envelope.
- **Tools/actions available:** read access to booking, policy, and inventory systems; a write (booking) action limited to a customer-approved, policy-bounded alternative — idempotent to prevent duplicate bookings.
- **Output produced:** a set of ranked, explained alternatives, and (on customer approval) a confirmed rebooking within policy.

## Multi-Agent Design (where relevant)

Worth considering where partner/inventory systems are numerous: an **inventory-search agent** per carrier/partner system retrieves options in that system's native format, feeding a **ranking-and-presentation agent** that normalizes and ranks across all sources before presenting trade-offs — rather than one agent needing native fluency in every partner's booking API.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Assists with ranked options and trade-offs | Customer/agent chooses and confirms every rebooking | Faster option discovery; booking decision stays fully human/customer-driven |
| L3 (automate, exception-routed) | Bounded rebooking for standard itineraries with explicit customer consent | Human handles only exceptions (unaccompanied minors, accessibility, group bookings, etc.) | Faster reaccommodation at scale for standard itineraries, human attention reserved for genuinely complex cases |

- **Starting / ceiling:** L2 / L3. Assist with options first; bounded rebooking for standard itineraries and explicit customer consent.
- **Outcome:** Affected travelers receive a valid alternative or clear escalation before the next decision deadline.
- **Value basis:** Handle time, reaccommodation cost, customer retention, and missed-connection reduction.
- **Exceptions:** Unaccompanied minors, accessibility needs, border/visa uncertainty, group bookings, and out-of-policy compensation escalate.

## Evaluation & Guardrails

Test policy compliance, inventory freshness, booking idempotency, customer acceptance, and incorrect-rebooking rate. Require a final itinerary summary and consent, prevent duplicate bookings, and preserve a human service-recovery route.

---

**Back to:** [Travel & Hospitality](../03-domains/travel-hospitality.md)
