# Function: Risk & Internal Audit

`Home › 02-functions › Risk & Internal Audit`

## Why This Function Is a Strong Fit

Internal audit and controls testing today are largely sample-based, because exhaustive manual review of every transaction or control instance doesn't scale. An agent that can apply the same test consistently across 100% of a population — rather than a 5% sample — is a structurally different (and better) coverage model, not just a faster version of the old one.

**In plain terms:** this is the function that checks whether the rules the company set for itself are actually being followed — an agent can check every transaction against the rule instead of just a sample, catching things a spot-check would miss, while a human auditor still decides what any finding actually means.

**For business readers:** the value case here is coverage, not just speed — moving from sampled to exhaustive controls testing surfaces issues earlier and more reliably, which matters directly for regulatory exposure and financial-statement risk. The corresponding discipline required is equally exhaustive audit logging, since this function's entire credibility rests on defensible evidence.

**For technical readers:** this typically means read-only access to transaction systems and the documented control library, a rules engine that encodes each control test precisely (not an inferred approximation of it), and an evidence trail that links every pass/fail result back to the specific transaction and control version tested.

## Use Cases in This Function

| Use case | Capability | Typical starting level |
|---|---|---|
| [Continuous Controls Testing Agent](../05-use-cases/continuous-controls-testing-agent.md) | Continuous Monitoring & Flagging | L2 → L3 |
| [Trade Surveillance & Market Abuse Detection Agent](../05-use-cases/trade-surveillance-market-abuse-agent.md) | Continuous Monitoring & Flagging | L2 |
| [Visual Safety & Asset Inspection Agent](../05-use-cases/visual-safety-asset-inspection-agent.md) | Visual Perception & Inspection | L1 → L2 |

Other credible patterns (risk register monitoring, audit workpaper drafting, regulatory change impact assessment) aren't yet written up as full use cases — see [CONTRIBUTING.md](../CONTRIBUTING.md).

## Domain Applicability

| Domain | Notes |
|---|---|
| [Financial Services](../03-domains/financial-services.md), [Insurance](../03-domains/insurance.md) | Core — high regulatory intensity, well-documented control libraries |
| [Technology & SaaS](../03-domains/technology-saas.md) | Core — SOC 2/compliance-driven control environments are a strong fit |
| [Manufacturing](../03-domains/manufacturing.md), [Industrial & Heavy Operations](../03-domains/industrial-heavy-operations.md) | Adaptable — safety-incident and near-miss pattern monitoring extends the same model |
| All other domains | Applies generically wherever a documented internal control library exists |

## Key Cross-Cutting Risks

- A control test that's subtly miscoded produces confident, wrong results at scale — validate every automated test against manual results before trusting it as the system of record
- This function's value depends entirely on defensible evidence; audit logging and control-version tracking are not optional add-ons
- Findings and risk judgments remain human-owned — the agent's role is coverage and evidence, not the audit opinion itself

---

**Previous:** [Legal & Compliance](legal-compliance.md)
**Next:** [Supply Chain & Operations](supply-chain-operations.md)
