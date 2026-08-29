# Function: HR & People

`Home › 02-functions › HR & People`

## Why This Function Is a Strong Fit

Recruiting and onboarding are high-volume, document- and workflow-heavy — but HR is also one of the highest-scrutiny functions for AI, given direct impact on individuals' livelihoods. Automation depth should generally stay conservative here relative to other functions.

## Common Opportunity Patterns

| Pattern | Typical starting level | Use case |
|---|---|---|
| Candidate screening and interview scheduling | L1 → L2 | [Candidate Screening & Scheduling Agent](../05-use-cases/candidate-screening-agent.md) |
| Employee onboarding orchestration | L2 → L3 | [Employee Onboarding Agent](../05-use-cases/employee-onboarding-agent.md) |
| Policy Q&A and benefits navigation | L1 → L2 | Not yet detailed |
| Performance review drafting assistance | L1 | Not yet detailed |

## Domain Applicability

Largely domain-generic — HR patterns are similar across industries, with regulatory intensity varying:

| Domain | Notes |
|---|---|
| All domains | Core pattern applies broadly |
| [Financial Services](../03-domains/financial-services.md), [Healthcare](../03-domains/healthcare.md), [Public Sector](../03-domains/public-sector.md) | Adaptable — background-check and credentialing requirements add steps |

## Key Cross-Cutting Risks

- **Candidate screening carries the highest bias/fairness risk in this repository.** Any screening automation must be treated as high-risk under [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI)'s fairness and bias guidance, with human review of every rejection, not just a sample.
- Employment law varies materially by jurisdiction — do not assume a pattern that's compliant in one region transfers to another
- Personal and sensitive employee data handling — see [Responsible-AI privacy techniques](https://github.com/knowledgetrailsai/Responsible-AI)

---

**Previous:** [Marketing](marketing.md)
**Next:** [Finance & Accounting](finance-accounting.md)
