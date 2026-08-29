# Outage Communication & Restoration Agent

`Home › 05-use-cases › Outage Communication & Restoration Agent`

**Exclusive domain:** [Energy & Utilities](../03-domains/energy-utilities.md)
**Primary Functions:** [Customer Relations & Support](../02-functions/customer-relations-support.md), [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)
**Capability:** Synthesis & Drafting (secondary: Conversational Resolution, for status Q&A)
**Outcome Categories:** Time Saved, Coverage & Consistency Improved
**Business Outcome Category:** Customer & Employee Experience

## Problem / Trigger

An outage-management event changes frequently while customers ask for restoration timing through multiple channels. Teams manually reconcile operational updates, approved language, vulnerable-customer flags, and channel delivery.

## Agentic Automation Opportunity

The agent reads approved outage events and operator updates, groups affected service points, drafts channel-specific notices, answers status questions from the same source of truth, and escalates conflicting or stale restoration estimates.

## Benefits

- **For the customer service team:** consistent, source-grounded answers for every customer inquiry instead of manually reconciling operator updates against what's already been communicated.
- **For the utility:** fewer avoidable contacts during an outage event, since customers can get an accurate status answer without calling in.
- **For affected customers:** timely, consistent updates instead of conflicting information across channels.

## Agentic Design

- **Inputs read:** approved outage events, operator updates, and vulnerable-customer flags.
- **Reasoning steps:** read approved outage events and operator updates → group affected service points → draft channel-specific notices → answer status questions from the same source of truth → escalate conflicting or stale restoration estimates rather than presenting an unsupported one.
- **Tools/actions available:** read access to the outage-management system and approved operator updates; write access limited to publishing approved status facts in channel-specific formats — it may not infer restoration times or operate equipment.
- **Output produced:** channel-specific status notices and direct answers to status questions, all traceable to an approved operator update.

## Multi-Agent Design (where relevant)

A reasonable split at scale: a **fact-synthesis agent** consolidates operator updates into a single current-status source of truth, while a separate **channel-drafting agent** (or one per channel) turns that synthesized status into format-appropriate notices — keeping the accuracy-critical synthesis step isolated from channel-specific drafting variation.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Drafts channel-specific notices and answers from approved facts | Control room/service team reviews before publication | Faster, more consistent draft communications |
| L3 (automate, exception-routed) | Publishes approved status facts directly across channels | Control room handles conflicting/stale-estimate escalations only | Timely, consistent updates at scale, with human attention reserved for genuine data conflicts |

- **Starting / ceiling:** L2 / L3. It may draft and publish only approved status facts; it may not infer restoration times or operate equipment.
- **Outcome:** Timely, consistent updates with fewer avoidable contacts and no unsupported restoration promise.
- **Value basis:** Contact deflection, faster communications, and reduced operator rework.
- **Exceptions:** Conflicting telemetry, vulnerable-customer cases, safety reports, and stale estimates route to the control room or service team.

## Evaluation & Guardrails

Measure factual accuracy against operator updates, delivery latency, unsupported-claim rate, accessibility, and escalation recall. Retain the source event, policy version, generated message, approver, and publication time. Provide a manual broadcast fallback.

---

**Back to:** [Energy & Utilities](../03-domains/energy-utilities.md)
