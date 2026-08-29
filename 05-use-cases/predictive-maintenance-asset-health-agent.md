# Predictive Maintenance & Asset Health Agent

`Home › 05-use-cases › Predictive Maintenance & Asset Health Agent`

**Exclusive domain:** [Industrial & Heavy Operations](../03-domains/industrial-heavy-operations.md)
**Primary Function:** [Supply Chain & Operations](../02-functions/supply-chain-operations.md)

## Who This Is For

- **In plain terms:** heavy equipment — pumps, compressors, drilling rigs, conveyors — sends off warning signs before it fails, but those signs are scattered across sensor logs, inspection notes, and maintenance history that no one has time to cross-check for every asset, every day. This agent does that cross-checking continuously and tells a reliability engineer which assets need attention first, with the evidence attached.
- **For business readers:** unplanned equipment failure in this domain is expensive in a way that's easy to underestimate — it's not just repair cost, it's lost production, safety exposure, and sometimes contractual penalties for missed delivery. Shifting even a portion of maintenance from reactive (fix it when it breaks) or purely calendar-based (fix it on a schedule whether it needs it or not) to condition-based (fix it when the evidence says it needs it) is one of the more well-established ROI stories in industrial automation — the challenge is usually data quality and organizational trust in the recommendation, not the underlying technique.
- **For technical readers:** the agent reads historian/SCADA time-series data, CMMS/EAM maintenance history, and inspection records (all read-only — no write path to control systems), applies documented degradation and failure-mode indicators per asset class, and produces a ranked asset-risk list with the specific evidence behind each ranking. It does not compute a physics-based remaining-useful-life model itself unless one already exists as a validated input; it synthesizes and prioritizes signals a human would otherwise have to assemble manually.

## Problem / Trigger

Reliability and maintenance teams are responsible for far more assets than they can proactively inspect and cross-reference against operating history, so most maintenance ends up either reactive (after failure) or calendar-based (regardless of actual condition) — both of which either cost more in downtime or waste maintenance budget on assets that didn't need it yet.

## Agentic Automation Opportunity

The agent continuously ingests sensor/historian data, inspection findings, and maintenance history for the covered asset population, applies documented degradation indicators and failure-mode patterns per asset class, and generates a prioritized asset-risk list with supporting evidence — feeding directly into the maintenance planner's work-order queue for human review and scheduling, never triggering a physical maintenance action or equipment shutdown itself.

## Workflow Boundary

**Trigger and inputs:** Scheduled synthesis run (e.g., daily) or a threshold breach on a monitored asset; sensor/historian readings, inspection records, maintenance history, and asset criticality tier.

**Systems and evidence consulted:** Historian/SCADA read-only export, CMMS/EAM maintenance records, inspection database, and the documented failure-mode/degradation-indicator library per asset class.

**Outputs and allowed actions:** A ranked asset-risk report with supporting evidence and a suggested maintenance work-order draft, submitted to the planner's queue. No direct write access to control systems, and no automatic work-order creation without planner review.

**Human owner / approval point:** Maintenance planner or reliability engineer reviews and approves every suggested work order before it's scheduled.

**Exception paths:** Missing or stale sensor data → flag asset as unassessed rather than falsely clear; conflicting indicators → route to reliability engineer with both signals shown; safety-critical asset threshold breach → immediate escalation outside the normal review cycle.

**Out of scope:** Equipment control, shutdown/startup actions, safety-system overrides, and any action that isn't a maintenance-planning recommendation.

## Automation Maturity

- **Realistic starting level:** L1 — agent surfaces ranked risk and evidence, human plans and schedules all maintenance
- **Potential ceiling:** L2 — agent auto-drafts work orders for planner approval at scale once the ranking model is validated against actual failure outcomes; L3+ (autonomous scheduling) is not a realistic target given physical and safety consequences
- **Why this range:** Ground truth (did the predicted failure mode actually occur) is only knowable after the fact, and the cost of a missed prediction or a false alarm both carry real operational weight — this keeps the function at recommendation-level even at maturity.

_Indicative scale:_
`L1 (assist) ● — L2 (automate, reviewed) ○ — L3 (automate, exception-routed) — L4 (autonomous, monitored)`

## Value Signal

- **Plausible outcome definition:** An asset flagged as elevated-risk that would otherwise have failed unpredicted before its next scheduled inspection, allowing planned intervention instead of reactive repair.
- **Plausible value basis:** Cost avoided (unplanned downtime, expedited-repair premiums), risk reduced (safety exposure from unexpected failure).

## KPIs Influenced

- **Leading:** Percentage of asset population actively monitored, mean time between risk-flag and planner review, evidence-completeness rate per flag.
- **Lagging:** Unplanned-downtime hours, ratio of planned-to-reactive maintenance events, false-alarm rate against actual failure outcomes, maintenance spend per asset-class.

## Evaluation Plan

- **Offline test set:** Historical asset failure events with the sensor/inspection data available in the lead-up window, covering multiple asset classes and both true failures and false-alarm-prone conditions.
- **Quality measures:** Risk-ranking precision/recall against actual failure outcomes, lead time between flag and failure, evidence traceability completeness.
- **Launch gates:** No safety-critical asset goes unassessed silently; false-alarm rate stays within the reliability team's tolerance before scaling asset coverage.
- **Rollout path:** Shadow mode against known historical outcomes → live flagging on a limited asset subset with planner review → expand coverage as validated.

## Implementation Notes

- **Data dependencies:** Historian/SCADA time-series, CMMS/EAM maintenance history, inspection records, and a documented failure-mode library per asset class.
- **Integration dependencies:** Read-only OT/IT data bridge respecting network separation; CMMS/EAM API for work-order draft submission.
- **Permissions / audit requirements:** Strictly read-only on OT systems; every risk flag retains the source data window and indicator logic version used.
- **Likely failure modes:** Sensor drift or gaps misread as a genuine condition signal; asset-class failure-mode libraries that are incomplete or stale; alert fatigue if thresholds aren't tuned to the reliability team's actual tolerance.
- **Open discovery questions:** Which asset classes have sufficient historical failure data to validate indicators? What's the OT/IT data-access boundary at this site? Who owns threshold tuning long-term?

## Key Risks & Guardrails

- A missed failure prediction can have safety and production consequences well beyond typical business-process risk — this function needs proportionally higher validation rigor than most in this repository
- Alert fatigue from poorly-tuned thresholds erodes trust and gets the whole system ignored
- OT/IT boundary violations are a security risk in themselves, independent of the AI system's accuracy

## Related Use Cases

- [Field Work Order Dispatch Agent](field-work-order-dispatch-agent.md) — related work-order and scheduling pattern
- [Supplier Risk Monitoring Agent](supplier-risk-monitoring-agent.md) — related continuous-monitoring-and-flag pattern

---

**Back to:** [Industrial & Heavy Operations](../03-domains/industrial-heavy-operations.md)
