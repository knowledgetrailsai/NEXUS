# Field Work Order Dispatch Agent

`Home › 05-use-cases › Field Work Order Dispatch Agent`

**Exclusive domain:** [Energy & Utilities](../03-domains/energy-utilities.md)
**Primary Function:** [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)

## Problem / Trigger

Dispatchers balance technician skills, geography, safety certifications, priority, outage impact, parts availability, and appointment windows across changing work orders.

## Agentic Automation Opportunity

The agent proposes a ranked schedule from the work-management system, checks qualifications and travel constraints, explains trade-offs, and updates customers after dispatcher approval. It re-plans when a technician, part, or outage priority changes.

## Boundary, Maturity & Value

- **Starting / ceiling:** L2 / L3. Recommendations first; bounded auto-assignment only for routine, low-risk work with explicit constraints.
- **Outcome:** More work orders completed within window without violating qualification, rest, or safety constraints.
- **Value basis:** Travel time avoided, utilization, response time, and backlog reduction.
- **Exceptions:** Safety-critical work, emergency priority conflicts, missing certification, and infeasible schedules escalate to a dispatcher.

## Evaluation & Guardrails

Test constraint satisfaction, schedule quality versus dispatcher baselines, missed-window rate, fairness of workload distribution, and unsafe-assignment rate. Use read-only shadow mode before any write access; preserve dispatcher override and an immutable assignment history.

---

**Back to:** [Energy & Utilities](../03-domains/energy-utilities.md)
