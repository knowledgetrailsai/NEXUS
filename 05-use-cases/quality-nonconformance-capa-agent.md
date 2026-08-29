# Quality Non-Conformance & CAPA Routing Agent

`Home › 05-use-cases › Quality Non-Conformance & CAPA Routing Agent`

**Exclusive domain:** [Manufacturing & Industrial](../03-domains/manufacturing.md)
**Primary Function:** [Quality Management](../02-functions/quality-management.md)

## Problem / Trigger

Non-conformance reports from inspection, testing, or customer complaints require classification, root-cause routing, and corrective/preventive action (CAPA) tracking — a documentation-heavy process that quality teams manage manually across spreadsheets and QMS modules.

## Agentic Automation Opportunity

The agent classifies an incoming non-conformance against defect taxonomy and severity criteria, retrieves related historical NCRs and prior CAPAs for the same part/process, drafts a containment and root-cause investigation assignment, and tracks CAPA task completion against due dates — escalating recurring or safety-critical non-conformances immediately.

## Boundary, Maturity & Value

- **Starting / ceiling:** L2 / L3 for classification, routing, and tracking; root-cause determination and CAPA sign-off remain human-owned.
- **Outcome:** Non-conformances classified and routed consistently, with CAPA tasks tracked to closure without manual chasing.
- **Value basis:** Quality engineer time saved, faster containment, and reduced repeat non-conformances from better historical pattern surfacing.
- **Exceptions:** Safety-critical defects, regulatory-reportable events, and recurring non-conformances beyond a defined threshold escalate to quality leadership.

## Evaluation & Guardrails

Measure classification accuracy, routing correctness, CAPA on-time closure rate, and recurrence detection. Never let the agent close a CAPA or sign off root cause, retain full traceability from NCR to disposition, and version the defect taxonomy and severity rules it applies.

## Related Use Cases

- [Supplier Risk Monitoring Agent](supplier-risk-monitoring-agent.md)
- [Demand Forecasting & Replenishment Agent](demand-forecasting-replenishment-agent.md)

---

**Back to:** [Manufacturing & Industrial](../03-domains/manufacturing.md)
