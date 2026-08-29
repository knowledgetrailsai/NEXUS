# Domain: Healthcare & Life Sciences

`Home › 03-domains › Healthcare`

## Domain Context

Highest-stakes domain in this grid for anything touching clinical decisions or patient-facing communication. Administrative and operational functions (scheduling, claims, supply chain) are strong agentic fits; clinical judgment is explicitly out of scope for this repository.

## Most Relevant Functions

| Function | Relevance | Notes |
|---|---|---|
| [Purchasing & Procurement](../02-functions/purchasing-procurement.md) | Adaptable | Regulated/clinical procurement categories add complexity |
| [Customer Relations & Support](../02-functions/customer-relations-support.md) | Adaptable | Keep clinical questions strictly out of agent scope; administrative-only |
| [Operations & Resource Scheduling](../02-functions/operations-resource-scheduling.md) | Adaptable | Appointment scheduling and referral coordination |
| [HR & People](../02-functions/hr-people.md) | Adaptable | Credentialing and licensure verification adds steps |
| [Finance & Accounting](../02-functions/finance-accounting.md) | Applies generically | Often with grant/fund accounting overlay |

## Domain-Exclusive Opportunities

- [Prior Authorization Request Agent](../05-use-cases/prior-authorization-request-agent.md)
- [Patient Appointment Scheduling & Referral Coordination Agent](../05-use-cases/patient-scheduling-referral-coordination-agent.md)

## Regulatory Considerations

Patient data handling, clinical communication boundaries, and credentialing requirements are all materially higher-stakes here than in most domains. See [Responsible-AI: Healthcare sector guidance](https://github.com/knowledgetrailsai/Responsible-AI/blob/main/11-sector-specific-ai/healthcare.md).

## Typical Automation Posture

Administrative/operational workflows can reach L2–L3. Anything adjacent to clinical judgment or patient-facing medical communication should stay at L1 (assist only) pending explicit clinical and regulatory review — this repository does not evaluate that boundary for you.

---

**Previous:** [Financial Services](financial-services.md)
**Next:** [Retail & CPG](retail-cpg.md)
