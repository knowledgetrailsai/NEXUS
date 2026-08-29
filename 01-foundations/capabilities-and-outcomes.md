# Capabilities & Outcomes

`Home › 01-foundations › Capabilities & Outcomes`

Function and domain answer "whose problem is this" and "in which industry." **Capability** answers a third question: "what is the agent actually doing, mechanically, regardless of function or domain?" This is the dimension that makes cross-domain reuse visible — a Trade Surveillance Agent (Capital Markets) and a Supplier Risk Monitoring Agent (Manufacturing) look unrelated by function and domain, but they're the same capability: **Continuous Monitoring & Flagging**.

This repository's breakdown is four-dimensional, not three:

```
DOMAIN (industry context) × FUNCTION (business owner) × CAPABILITY (mechanical pattern) → USE CASE → OUTCOME
```

A use case is where all three meet a real workflow. There is no separate "pattern" layer above the use case — **a pattern that isn't attached to a concrete use case is just a capability description, not a catalog entry.** Where a function file used to list a pattern as "not yet detailed," that pattern should either become a real use case or not be listed as a row at all — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## The Capability Taxonomy

Every use case in [05-use-cases](../05-use-cases/) is tagged with one primary capability from this list:

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
**Next:** [Use-Case Anatomy](use-case-anatomy.md)
