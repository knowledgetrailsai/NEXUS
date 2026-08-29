# Course Scheduling Conflict Agent

`Home › 05-use-cases › Course Scheduling Conflict Agent`

**Exclusive domain:** [Education & Higher Education](../03-domains/education-higher-education.md)
**Primary Function:** [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md)

## Problem / Trigger

Registrar teams resolve clashes among rooms, instructors, cohorts, accessibility needs, prerequisites, and exam windows through spreadsheets and repeated negotiation.

## Agentic Automation Opportunity

The agent detects hard and soft conflicts, explains affected constraints, proposes alternate sections or rooms, and prepares a change set for registrar approval. It never silently changes a published timetable.

## Boundary, Maturity & Value

- **Starting / ceiling:** L2 / L3. Recommendation and simulation first; bounded updates only after registrar approval.
- **Outcome:** Fewer conflicts and faster schedule publication without violating hard constraints.
- **Value basis:** Registrar time, room utilization, student disruption, and schedule-cycle time.
- **Exceptions:** Accessibility conflicts, accreditation constraints, and instructor disputes require human resolution.

## Evaluation & Guardrails

Validate hard-constraint satisfaction, proposal acceptance, downstream timetable errors, and impact by student group. Version every schedule, show the rationale for each proposed change, and preserve rollback to the last approved publication.

---

**Back to:** [Education & Higher Education](../03-domains/education-higher-education.md)
