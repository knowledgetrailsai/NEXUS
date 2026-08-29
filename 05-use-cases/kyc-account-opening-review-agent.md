# KYC Document Review & Account Opening Agent

`Home › 05-use-cases › KYC Document Review & Account Opening Agent`

**Exclusive domain:** [Financial Services](../03-domains/financial-services.md)
**Primary Function:** [Legal & Compliance](../02-functions/legal-compliance.md)
**Capability:** Extraction & Structured Validation (secondary: Continuous Monitoring & Flagging, for screening)
**Outcome Categories:** Time Saved, Risk Reduced, Coverage & Consistency Improved
**Business Outcome Category:** Risk & Compliance

## Problem / Trigger

Know-your-customer document review during account opening requires checking identity documents, screening against sanctions/PEP lists, and verifying completeness against regulatory requirements — a bottleneck that delays onboarding and consumes significant compliance analyst time on straightforward cases.

## Agentic Automation Opportunity

The agent extracts and validates identity document data, runs sanctions/PEP/adverse-media screening via API, checks the application against documented completeness and risk-tiering rules, and either clears the file for straightforward low-risk cases or routes it to a compliance analyst with the specific gap or hit flagged — never itself clearing a sanctions match or high-risk case.

## Benefits

- **For the compliance analyst:** low-risk, no-hit files clear automatically, leaving analyst attention for genuine screening hits and elevated-risk cases.
- **For the business:** faster onboarding for the majority of low-risk customers, and consistent, fully-documented screening on every application instead of sampled review.
- **For the customer:** faster account opening when their application is clean and complete.

## Agentic Design

- **Inputs read:** submitted identity documents, the application, and sanctions/PEP/adverse-media screening data.
- **Reasoning steps:** extract and validate identity document data → run sanctions/PEP/adverse-media screening via API → check the application against documented completeness and risk-tiering rules → clear straightforward low-risk cases or route to a compliance analyst with the specific gap or hit flagged.
- **Tools/actions available:** read access to document data and screening APIs; a write action limited to clearing a clean, no-hit, low-risk file — never clearing a screening hit or high-risk case itself.
- **Output produced:** a cleared file (clean, low-risk) or a routed exception with the specific gap or hit cited.

## Multi-Agent Design (where relevant)

Worth considering at high application volume: a **document-extraction agent** handles identity-document parsing and validation, while a separate **screening-and-risk-tiering agent** runs sanctions/PEP/adverse-media checks and applies risk-tier rules — since document extraction and screening-API integration are different technical problems that can be tuned and monitored independently.

## Autonomy → Outcome Mapping

| Level | What the agent does | Human role | Outcome realized |
|---|---|---|---|
| L2 (automate, reviewed) | Checks and flags every application; clears none autonomously | Analyst clears or escalates every application | Consistent, fully-documented screening at full coverage; clearance authority unchanged |
| L3 (automate, exception-routed) | Clears only clean, low-risk, no-hit files against documented policy | Analyst handles every screening hit, inconsistency, or elevated-risk case | Faster onboarding for the low-risk majority, analyst time concentrated on genuine risk |

- **Starting / ceiling:** L2 / L3. Agent clears only clean, low-risk, no-hit files against documented policy; any screening hit, document inconsistency, or elevated risk tier routes to an analyst.
- **Outcome:** Faster onboarding for low-risk customers and consistent, fully-documented screening on every application instead of sampled review.
- **Value basis:** Compliance analyst time saved, faster onboarding cycle time, and reduced regulatory exposure from more consistent coverage.
- **Exceptions:** Any sanctions/PEP/adverse-media hit, document inconsistency or suspected fraud, and elevated-risk jurisdictions or customer types always escalate.

## Evaluation & Guardrails

Measure screening recall (false negatives are the critical failure mode), document extraction accuracy, false-clear rate, and analyst override rate. Never let the agent clear a screening hit itself, log every decision with policy version and evidence for regulatory examination, and treat this as a permanent L2–L3 posture, not a stepping stone to full autonomy — see [Legal & Compliance risks](../02-functions/legal-compliance.md#key-cross-cutting-risks).

## Related Use Cases

- [Contract Review & Redline Agent](contract-review-redline-agent.md) — related documented-playbook review pattern

---

**Back to:** [Financial Services](../03-domains/financial-services.md)
