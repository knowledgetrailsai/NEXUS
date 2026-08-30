# Capabilities & Outcomes

`Home › 01-foundations › Capabilities & Outcomes`

Function and domain answer "whose problem is this" and "in which industry." **Capability** answers a third question: "what is the agent actually doing, mechanically, regardless of function or domain?" This is the dimension that makes cross-domain reuse visible — a Trade Surveillance Agent (Capital Markets) and a Supplier Risk Monitoring Agent (Manufacturing) look unrelated by function and domain, but they're the same capability: **Continuous Monitoring & Flagging**.

This repository's breakdown is four-dimensional, not three:

```
DOMAIN (industry context) × FUNCTION (business owner) × CAPABILITY (mechanical pattern) → USE CASE → OUTCOME
```

A use case is where all three meet a real workflow. There is no separate "pattern" layer above the use case — **a pattern that isn't attached to a concrete use case is just a capability description, not a catalog entry.** Where a function file used to list a pattern as "not yet detailed," that pattern should either become a real use case or not be listed as a row at all — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## The Capability Taxonomy

Every use case in [05-use-cases](../05-use-cases/benefits-eligibility-document-verification-agent.md) is tagged with one primary capability from this list:

| Capability | What it mechanically does | Representative use cases |
|---|---|---|
| **Extraction & Structured Validation** | Pulls structured data from documents/systems and checks it against a rule set (does A match B within tolerance) | [Invoice Processing & 3-Way Match](../05-use-cases/invoice-processing-3way-match-agent.md), [KYC Document Review](../05-use-cases/kyc-account-opening-review-agent.md) |
| **Classification & Routing** | Triages an incoming item to the correct category, queue, or owner | [Tier-1 Support Resolution](../05-use-cases/tier1-support-resolution-agent.md), [Claims Intake & Triage](../05-use-cases/claims-intake-triage-agent.md) |
| **Synthesis & Drafting** | Produces a written artifact (summary, draft, report) from source material | [Literature Review & Research Synthesis](../05-use-cases/literature-review-research-synthesis-agent.md), [Contract Review & Redline](../05-use-cases/contract-review-redline-agent.md) |
| **Forecasting & Pattern Detection** | Projects a future state or detects an anomaly from historical/streaming data | [Demand Forecasting & Replenishment](../05-use-cases/demand-forecasting-replenishment-agent.md), [Predictive Maintenance & Asset Health](../05-use-cases/predictive-maintenance-asset-health-agent.md) |
| **Continuous Monitoring & Flagging** | Applies a documented rule exhaustively across a full population, on an ongoing basis, rather than a sample | [Continuous Controls Testing](../05-use-cases/continuous-controls-testing-agent.md), [Trade Surveillance & Market Abuse Detection](../05-use-cases/trade-surveillance-market-abuse-agent.md) |
| **Scheduling & Constrained Optimization** | Allocates a limited resource against many competing hard/soft constraints | [Course Scheduling Conflict](../05-use-cases/course-scheduling-conflict-agent.md), [Field Work Order Dispatch](../05-use-cases/field-work-order-dispatch-agent.md) |
| **Conversational Resolution** | Resolves an end-to-end request through interactive dialogue with the requester | [IT Helpdesk Tier-1](../05-use-cases/it-helpdesk-tier1-agent.md), [Constituent Service Request Routing](../05-use-cases/constituent-service-request-agent.md) |
| **Visual Perception & Inspection** | Detects a condition, defect, or hazard from image/video data | [Visual Safety & Asset Inspection](../05-use-cases/visual-safety-asset-inspection-agent.md) |

A use case can have a secondary capability (e.g., Trade Surveillance is primarily Continuous Monitoring & Flagging, secondarily Synthesis & Drafting for the case file itself) — name the primary one first.

## The Outcome Taxonomy

Every use case names which outcome categories it plausibly targets — this is the same [Value Signal](principles.md#value-signal-not-a-value-case) discipline, organized so it's comparable across the catalog:

| Outcome category | What "success" looks like | Typical proof point |
|---|---|---|
| **Cost Avoided** | A cost that would otherwise have been incurred didn't happen | Fraud caught, downtime avoided, penalty avoided |
| **Revenue Influenced** | Revenue that wouldn't have happened, happened (or was protected) | Renewal saved, upsell surfaced, faster quote-to-close |
| **Time Saved** | The same outcome achieved with less human labor | Hours reallocated per case, cycle-time reduction |
| **Risk Reduced** | A negative event became less likely or was caught earlier | Compliance gap caught pre-launch, safety hazard flagged early |
| **Coverage / Consistency Improved** | The same standard applied to more of the population, more uniformly | Sampled review → exhaustive review, consistent policy application |

Most use cases target 2–3 of these; naming all of them dilutes the signal — see [Principles](principles.md).

## Business Outcome Categories

The Outcome Taxonomy above is precise but not how most business stakeholders talk. When you're reconciling a discovery finding against an executive priority (see [Discovering Use Cases](discovering-use-cases.md)), it's more natural to classify a use case under one of these business-facing categories — each maps onto one or more of the technical outcome categories above:

| Business category | What it means to a stakeholder | Maps to (Outcome Taxonomy) | Example use cases |
|---|---|---|---|
| **Efficiency** | The same output for less cost or time — doing the existing work more cheaply | Cost Avoided, Time Saved | [Invoice Processing & 3-Way Match](../05-use-cases/invoice-processing-3way-match-agent.md), [Expense Audit Agent](../05-use-cases/expense-audit-agent.md) |
| **Productivity** | More output from the same people — not cheaper, but more throughput per person | Time Saved (reallocated, not eliminated), Coverage & Consistency Improved | [Self-Service Analytics & Insight Drafting](../05-use-cases/self-service-analytics-insight-agent.md), [Literature Review & Research Synthesis](../05-use-cases/literature-review-research-synthesis-agent.md) |
| **Revenue Growth** | Top-line impact — new revenue, retained revenue, or faster revenue realization | Revenue Influenced | [Subscription Renewal & Usage Review](../05-use-cases/subscription-renewal-usage-review-agent.md), [Proposal & Quote Generation](../05-use-cases/proposal-quote-generation-agent.md) |
| **Risk & Compliance** | Reduced exposure to a regulatory, financial, safety, or reputational bad outcome | Risk Reduced, Coverage & Consistency Improved | [Trade Surveillance & Market Abuse Detection](../05-use-cases/trade-surveillance-market-abuse-agent.md), [Visual Safety & Asset Inspection](../05-use-cases/visual-safety-asset-inspection-agent.md), [KYC Document Review](../05-use-cases/kyc-account-opening-review-agent.md) |
| **Customer/Employee Experience** | Faster, more consistent, or less frustrating interactions for the person on the receiving end | Time Saved, Coverage & Consistency Improved | [Tier-1 Support Resolution](../05-use-cases/tier1-support-resolution-agent.md), [Hotel Service Recovery](../05-use-cases/hotel-service-recovery-agent.md) |

**Efficiency vs. Productivity, precisely:** these two get conflated often enough to be worth separating explicitly. Efficiency means the *same* work costs less (headcount or hours genuinely reduced). Productivity means the *same* people produce *more* (hours are reallocated to higher-value work, not cut). A use case's Autonomy → Outcome Mapping table usually reveals which one it actually is: if the human role at the target autonomy level disappears, that's efficiency; if it shifts to reviewing exceptions or doing higher-judgment work, that's productivity. Don't claim both without being specific about which resource is actually freed and what happens to it.

A use case can span more than one business category (Trade Surveillance is both Risk & Compliance and, secondarily, Productivity for the analyst) — but pick a primary one for classification, the same discipline as the Capability tag.

## Classifying the Catalog by Business Category

This cross-cutting index is populated as use cases are tagged with their Outcome Categories — see each use case's header. As of this writing, tagging is complete for a representative subset (the use cases named in the table above); extending it across the full catalog in [05-use-cases](../05-use-cases/benefits-eligibility-document-verification-agent.md) is ongoing — see [CONTRIBUTING.md](../CONTRIBUTING.md) if a use case you're using isn't yet classified.

## Capability × Outcome Is Not a Fixed Mapping

A capability doesn't guarantee an outcome — the same capability can target different outcomes depending on what's automated. Continuous Monitoring & Flagging can target **Risk Reduced** (Trade Surveillance) or **Cost Avoided** (Predictive Maintenance) depending on what's being monitored and why. This is why each use case states its own outcome mapping explicitly (see the Autonomy → Outcome table in the [use case template](../templates/use-case-template.md)) rather than inheriting one from its capability alone.

## How This Changes a Use Case Page

Each use case now states, in addition to Function and Domain:
- **Capability:** primary (and optionally secondary) capability from the taxonomy above
- **Benefits:** concrete, stakeholder-specific benefits — distinct from the Value Signal's outcome categories, this is "what changes for the person doing the work" and "what changes for the business," stated plainly
- **Agentic Design:** the single-agent architecture — what it reads, how it reasons step by step, what it produces
- **Multi-Agent Design (where relevant):** how the workflow could decompose into multiple cooperating agents with distinct roles, if the task's complexity or scale genuinely warrants it — not every use case needs this section; a simple bounded task run by one agent shouldn't be artificially split
- **Autonomy → Outcome Mapping:** a table showing what outcome is realistically achievable at each automation level, not just a starting point and ceiling — see the template

---

**Previous:** [The Agentic Automation Spectrum](agentic-automation-spectrum.md)
**Next:** [Discovering Use Cases](discovering-use-cases.md)
