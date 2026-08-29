# Tier-1 Support Resolution Agent

`Home › 05-use-cases › Tier-1 Support Resolution Agent`

**Primary Function:** [Customer Relations & Support](../02-functions/customer-relations-support.md)
**Primary Domains:** [Telecom & Media](../03-domains/telecom-media.md), [Retail & CPG](../03-domains/retail-cpg.md), [Technology & SaaS](../03-domains/technology-saas.md)
**Also Applicable To:** [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md) (with compliance overlay)
**Capability:** Classification & Routing (secondary: Conversational Resolution)
**Outcome Categories:** Cost Avoided, Time Saved, Coverage & Consistency Improved
**Business Outcome Category:** Efficiency

## Problem / Trigger

The majority of Tier-1 support tickets (billing questions, account status, order status, standard troubleshooting) follow well-documented resolution paths but still require a human to look up account data and apply the same process every time.

## Agentic Automation Opportunity

An agent classifies incoming ticket intent, retrieves account/order data via API, applies the appropriate resolution workflow (informational answer, standard action like a refund within policy, or troubleshooting steps), and closes the ticket — escalating to a human for anything outside the defined resolution set or exceeding a risk/value threshold.

This is the fully worked example in the companion [oasis-fulcrum case study](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/10-case-studies/customer-support-agent.md) — see it for a complete cost/value walkthrough of this exact pattern.

## Benefits

- **For the customer:** faster resolution of routine tickets (billing, account status, order status) without waiting in a human queue.
- **For the support team:** far less repetitive lookup-and-answer work, freeing capacity for the tickets that genuinely need judgment.
- **For the business:** lower cost per ticket resolved at high volume, and consistent application of resolution policy regardless of which agent (human or AI) originally handled a similar case.

## Agentic Design

- **Inputs read:** the incoming ticket, account/order data via API, and the documented resolution-workflow set.
- **Reasoning steps:** classify incoming ticket intent → retrieve account/order data via API → apply the appropriate resolution workflow (informational answer, standard action like a refund within policy, or troubleshooting steps) → close the ticket or escalate to a human for anything outside the defined resolution set or exceeding a risk/value threshold.
- **Tools/actions available:** read access to account/order systems; a write action limited to a pre-approved resolution action (e.g., a refund within policy) — no action outside the documented resolution set.
- **Output produced:** a resolved ticket (standard cases) or an escalation with the classification and attempted-resolution reasoning.

## Multi-Agent Design (where relevant)

Not needed as a default — classification and resolution against a documented workflow set are one coherent, bounded sequence best kept together so the resolution action always reflects the actual classified intent.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Resolves standard tickets | Human reviews low-confidence cases | Faster resolution for confidently-classified standard tickets |
| L3 (automate, exception-routed) | Handles the full standard resolution set autonomously | Human escalation only for genuine exceptions | Full standard-ticket coverage at low cost per ticket, human time concentrated on genuine exceptions |

- **Realistic starting level:** L2 — agent resolves standard tickets, human reviews low-confidence cases
- **Potential ceiling:** L3 — agent handles the full standard resolution set autonomously, escalating only genuine exceptions
- **Why this range:** High volume and well-documented resolution paths support autonomy; financial actions (refunds/credits) need an evaluation layer proportional to amount.

## Value Signal

- **Plausible outcome definition:** A ticket resolved without the customer reopening it or a related issue within 7 days — see [oasis-fulcrum's outcome definition guidance](https://github.com/knowledgetrailsai/oasis-fulcrum/blob/main/09-sector-specific-finops/customer-support-agents.md).
- **Plausible value basis:** Cost avoided (equivalent human-handled ticket cost).

## Key Risks & Guardrails

- Incorrect resolutions that satisfy the immediate ticket but recur — see [Customer Relations risks](../02-functions/customer-relations-support.md#key-cross-cutting-risks)
- Financial actions issued without proportional evaluation
- Sensitive account information handled outside approved boundaries

## Related Use Cases

- [Churn Prevention Agent](churn-prevention-agent.md)
- [IT Helpdesk Tier-1 Agent](it-helpdesk-tier1-agent.md) — closely related pattern, internal-facing

---

**Back to:** [05-use-cases](.) · [Customer Relations & Support](../02-functions/customer-relations-support.md)
