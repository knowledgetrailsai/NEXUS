# Field Work Order Dispatch Agent

`Home › 05-use-cases › Field Work Order Dispatch Agent`

**Exclusive domain:** [Energy & Utilities](../03-domains/energy-utilities.md)
**Primary Function:** [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)
**Capability:** Scheduling & Constrained Optimization
**Outcome Categories:** Time Saved, Coverage & Consistency Improved
**Business Outcome Category:** Efficiency

## Problem / Trigger

Dispatchers balance technician skills, geography, safety certifications, priority, outage impact, parts availability, and appointment windows across changing work orders.

## Agentic Automation Opportunity

The agent proposes a ranked schedule from the work-management system, checks qualifications and travel constraints, explains trade-offs, and updates customers after dispatcher approval. It re-plans when a technician, part, or outage priority changes.

## Benefits

- **For the dispatcher:** starts from a ranked, constraint-checked schedule proposal instead of building one manually against every technician's skills, certifications, and location.
- **For the business:** more work orders completed within window from systematically evaluating trade-offs across the full technician pool, not just the ones a dispatcher happens to think of first.
- **For the customer:** more reliable appointment windows and faster updates when a technician, part, or priority changes.

## Agentic Design

- **Inputs read:** the work-management system's open work orders, technician skills/certifications/location, parts availability, and outage priority data.
- **Reasoning steps:** propose a ranked schedule → check qualifications and travel constraints → explain trade-offs in the proposal → update customers once the dispatcher approves → re-plan when a technician, part, or priority changes.
- **Tools/actions available:** read access to the work-management and technician-qualification systems; write access limited to a proposed schedule and (post-approval) customer update messages — no autonomous assignment outside routine, low-risk, explicitly-bounded work.
- **Output produced:** a ranked, explained schedule proposal for dispatcher approval, and post-approval customer updates.

## Multi-Agent Design (where relevant)

Not needed as a default — schedule proposal generation is one coherent constraint-satisfaction task. Consider a separate **customer-communication agent** downstream of the approved schedule if update volume and channel variety (SMS, app, email) grow large enough to warrant decoupling that from the scheduling logic itself.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Proposes a ranked schedule with explained trade-offs | Dispatcher reviews and approves every assignment | Faster, more systematically evaluated scheduling; assignment authority stays fully human |
| L3 (automate, exception-routed) | Same, plus bounded auto-assignment for routine, low-risk work with explicit constraints | Dispatcher reviews only flagged/complex assignments | More work orders completed within window at scale, dispatcher time concentrated on genuine judgment calls |

- **Starting / ceiling:** L2 / L3. Recommendations first; bounded auto-assignment only for routine, low-risk work with explicit constraints.
- **Outcome:** More work orders completed within window without violating qualification, rest, or safety constraints.
- **Value basis:** Travel time avoided, utilization, response time, and backlog reduction.
- **Exceptions:** Safety-critical work, emergency priority conflicts, missing certification, and infeasible schedules escalate to a dispatcher.

## Evaluation & Guardrails

Test constraint satisfaction, schedule quality versus dispatcher baselines, missed-window rate, fairness of workload distribution, and unsafe-assignment rate. Use read-only shadow mode before any write access; preserve dispatcher override and an immutable assignment history.

---

**Back to:** [Energy & Utilities](../03-domains/energy-utilities.md)
