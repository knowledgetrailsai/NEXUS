# Course Scheduling Conflict Agent

`Home › 05-use-cases › Course Scheduling Conflict Agent`

**Exclusive domain:** [Education & Higher Education](../03-domains/education-higher-education.md)
**Primary Function:** [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)
**Capability:** Scheduling & Constrained Optimization
**Outcome Categories:** Time Saved, Coverage & Consistency Improved
**Business Outcome Category:** Efficiency

## Problem / Trigger

Registrar teams resolve clashes among rooms, instructors, cohorts, accessibility needs, prerequisites, and exam windows through spreadsheets and repeated negotiation.

## Agentic Automation Opportunity

The agent detects hard and soft conflicts, explains affected constraints, proposes alternate sections or rooms, and prepares a change set for registrar approval. It never silently changes a published timetable.

## Benefits

- **For the registrar team:** conflicts get surfaced with the specific constraints they violate, instead of being found by trial and error across spreadsheets.
- **For the institution:** faster schedule publication and better room/instructor utilization from systematically evaluating trade-offs across the full timetable.
- **For students:** fewer schedule changes after the fact, and clearer visibility into why a change was needed when one is.

## Agentic Design

- **Inputs read:** the current course catalog, room inventory, instructor availability and constraints, cohort enrollment data, and accessibility/prerequisite requirements.
- **Reasoning steps:** detect hard conflicts (double-booked room, instructor conflict) and soft conflicts (suboptimal but technically feasible) → explain which constraints are affected → propose alternate sections or rooms → prepare a change set for registrar approval.
- **Tools/actions available:** read access to the scheduling system and constraint data; write access limited to a proposed change set — it never silently changes a published timetable.
- **Output produced:** a conflict report with explained trade-offs and a proposed, registrar-approvable change set.

## Multi-Agent Design (where relevant)

Not needed as a default — conflict detection and proposal generation are one coherent constraint-satisfaction task better handled by a single agent with the full constraint picture than split across agents that would need to negotiate with each other over the same room/instructor pool.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Detects conflicts, explains them, and simulates proposed changes | Registrar approves every change before publication | Faster conflict detection and resolution proposal; publication authority stays fully human |
| L3 (automate, exception-routed) | Same, plus bounded auto-updates for narrowly-scoped, non-controversial changes | Registrar reviews only flagged/complex changes | Faster schedule cycles at scale, reserving registrar time for genuine judgment calls |

- **Starting / ceiling:** L2 / L3. Recommendation and simulation first; bounded updates only after registrar approval.
- **Outcome:** Fewer conflicts and faster schedule publication without violating hard constraints.
- **Value basis:** Registrar time, room utilization, student disruption, and schedule-cycle time.
- **Exceptions:** Accessibility conflicts, accreditation constraints, and instructor disputes require human resolution.

## Evaluation & Guardrails

Validate hard-constraint satisfaction, proposal acceptance, downstream timetable errors, and impact by student group. Version every schedule, show the rationale for each proposed change, and preserve rollback to the last approved publication.

---

**Back to:** [Education & Higher Education](../03-domains/education-higher-education.md)
