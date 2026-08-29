# KYC Document Review & Account Opening Agent

`Home › 05-use-cases › KYC Document Review & Account Opening Agent`

**Exclusive domain:** [Financial Services](../03-domains/financial-services.md)
**Primary Function:** [Legal & Compliance](../02-functions/legal-compliance.md)

## Problem / Trigger

Know-your-customer document review during account opening requires checking identity documents, screening against sanctions/PEP lists, and verifying completeness against regulatory requirements — a bottleneck that delays onboarding and consumes significant compliance analyst time on straightforward cases.

## Agentic Automation Opportunity

The agent extracts and validates identity document data, runs sanctions/PEP/adverse-media screening via API, checks the application against documented completeness and risk-tiering rules, and either clears the file for straightforward low-risk cases or routes it to a compliance analyst with the specific gap or hit flagged — never itself clearing a sanctions match or high-risk case.

## Boundary, Maturity & Value

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
