# [Use Case Name]

`Home › 05-use-cases › [Use Case Name]`

**Primary Function:** [link to 02-functions file]
**Primary Domains:** [links to 03-domains files where this is Core]
**Also Applicable To:** [domains where this is Adaptable/Applies generically]
**Capability:** [primary capability from the Capability Taxonomy — Extraction & Structured Validation / Classification & Routing / Synthesis & Drafting / Forecasting & Pattern Detection / Continuous Monitoring & Flagging / Scheduling & Constrained Optimization / Conversational Resolution / Visual Perception & Inspection] (+ secondary capability if genuinely present)
**Outcome Categories:** [2-3 from: Cost Avoided / Revenue Influenced / Time Saved / Risk Reduced / Coverage & Consistency Improved — see [Capabilities & Outcomes](../01-foundations/capabilities-and-outcomes.md)]
**Business Outcome Category:** [primary from: Efficiency / Productivity / Revenue Growth / Risk & Compliance / Customer & Employee Experience — see [Business Outcome Categories](../01-foundations/capabilities-and-outcomes.md#business-outcome-categories)]

## Who This Is For

_Three short lenses on the same use case — write each for a reader who has 60 seconds and only wants their angle._

- **In plain terms:** _What is this, described without jargon, as you'd explain it to someone outside the company?_
- **For business readers:** _What changes operationally, what it costs to get wrong, and why a business leader should care._
- **For technical readers:** _What systems, data, and integration points this actually touches — the shape of the build, not the code._

## Problem / Trigger

_What business situation creates this opportunity? What happens today without automation?_

## Benefits

_Concrete, stakeholder-specific benefits — distinct from the Outcome Categories above. Name what actually changes for each stakeholder, not a restated outcome label._

- **For the person doing the work today:** _e.g., less time on repetitive assembly/checking, more time on the judgment calls that need them_
- **For the business:** _e.g., faster cycle time, more consistent policy application, earlier risk detection_
- **For the end customer/requester (if applicable):** _e.g., faster response, more consistent treatment_

## Agentic Design

_The single-agent architecture. Describe the reasoning loop concretely — not "the agent handles X" but what it actually reads, in what order, what it checks, and what it produces._

- **Inputs read:** _systems, documents, data sources_
- **Reasoning steps:** _the actual sequence — e.g., classify → retrieve → validate → draft → route_
- **Tools/actions available:** _what it can call — read APIs, write APIs (if any), search, calculation_
- **Output produced:** _draft, classification, flag, recommendation, or bounded transaction_

## Multi-Agent Design (where relevant)

_Only include this section if the task's scale, latency, or role-separation genuinely benefits from decomposing into multiple cooperating agents — don't force a single bounded task into an artificial multi-agent shape. State clearly if a single agent is actually the right design and this section doesn't apply._

- **Why multiple agents (if applicable):** _e.g., a retrieval/evidence-gathering agent feeding a separate drafting agent, or a specialist agent per data source with an orchestrator reconciling outputs_
- **Role decomposition:** _name each agent's distinct responsibility and handoff point_
- **Coordination/failure handling:** _what happens when one agent's output conflicts with another's, or one fails_

## Workflow Boundary

**Trigger and inputs:**

**Systems and evidence consulted:**

**Outputs and allowed actions:**

**Human owner / approval point:**

**Exception paths:** _missing data, ambiguity, policy conflict, tool failure, and timeout_

**Out of scope:**

## Autonomy → Outcome Mapping

_What outcome is realistically achievable at each level — not just a starting point and ceiling. Mark the realistic starting point and potential ceiling._

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L1 (assist) | | | |
| L2 (automate, reviewed) | | | |
| L3 (automate, exception-routed) | | | |
| L4 (autonomous, monitored) | | | |

- **Realistic starting level:**
- **Potential ceiling:**
- **Why this range:** _brief justification_

## Value Signal

_Not a value case — see [Principles](../01-foundations/principles.md#value-signal-not-a-value-case). Name the plausible outcome definition and value basis only._

- **Plausible outcome definition:**
- **Plausible value basis:** (cost avoided / revenue influenced / time saved / risk reduced / coverage improved)

## KPIs Influenced

_Name the metrics a sponsor would actually track — leading indicators (process-level, visible early) and lagging indicators (outcome-level, visible later). Don't attach numbers; that belongs in an oasis-fulcrum value case, not here._

- **Leading:** _e.g., cycle time, first-pass resolution rate, coverage (% of volume touched)_
- **Lagging:** _e.g., cost per transaction, revenue retained/influenced, error/exception rate, satisfaction score_

## Evaluation Plan

- **Offline test set:** _source, size, labels, and edge-case coverage_
- **Quality measures:** _task, policy, operational, human, and business measures_
- **Launch gates:** _thresholds and stop conditions_
- **Rollout path:** _shadow → assist → bounded execution → scale_

## Implementation Notes

- **Data dependencies:**
- **Integration dependencies:**
- **Permissions / audit requirements:**
- **Likely failure modes:**
- **Open discovery questions:**

## Key Risks & Guardrails

_Name the risk in plain terms — full control design belongs in Responsible-AI._

-
-

## Related Use Cases

-

---

**Back to:** [05-use-cases](../05-use-cases/) · [Primary function](../02-functions/)
