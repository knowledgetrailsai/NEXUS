# Function: HR & People

`Home › 02-functions › HR & People`

## Why This Function Is a Strong Fit

Recruiting and onboarding are high-volume, document- and workflow-heavy — but HR is also one of the highest-scrutiny functions for AI, given direct impact on individuals' livelihoods. Automation depth should generally stay conservative here relative to other functions.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Candidate Screening & Scheduling Agent](../05-use-cases/candidate-screening-agent.md) | Classification & Routing | L1 → L2 |
| [Employee Onboarding Agent](../05-use-cases/employee-onboarding-agent.md) | Scheduling & Constrained Optimization | L2 → L3 |

Other credible patterns (benefits Q&A, performance-review drafting) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md).

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

**Previous:** [Data & Analytics](data-analytics.md)
**Next:** [Finance & Accounting](finance-accounting.md)
