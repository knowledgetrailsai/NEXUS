# Outage Communication & Restoration Agent

`Home › 05-use-cases › Outage Communication & Restoration Agent`

**Exclusive domain:** [Energy & Utilities](../03-domains/energy-utilities.md)
**Primary Functions:** [Customer Relations & Support](../02-functions/customer-relations-support.md), [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)

## Problem / Trigger

An outage-management event changes frequently while customers ask for restoration timing through multiple channels. Teams manually reconcile operational updates, approved language, vulnerable-customer flags, and channel delivery.

## Agentic Automation Opportunity

The agent reads approved outage events and operator updates, groups affected service points, drafts channel-specific notices, answers status questions from the same source of truth, and escalates conflicting or stale restoration estimates.

## Boundary, Maturity & Value

- **Starting / ceiling:** L2 / L3. It may draft and publish only approved status facts; it may not infer restoration times or operate equipment.
- **Outcome:** Timely, consistent updates with fewer avoidable contacts and no unsupported restoration promise.
- **Value basis:** Contact deflection, faster communications, and reduced operator rework.
- **Exceptions:** Conflicting telemetry, vulnerable-customer cases, safety reports, and stale estimates route to the control room or service team.

## Evaluation & Guardrails

Measure factual accuracy against operator updates, delivery latency, unsupported-claim rate, accessibility, and escalation recall. Retain the source event, policy version, generated message, approver, and publication time. Provide a manual broadcast fallback.

---

**Back to:** [Energy & Utilities](../03-domains/energy-utilities.md)
