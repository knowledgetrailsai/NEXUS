# Domain: Capital Markets & Investment Banking

`Home › 03-domains › Capital Markets & Investment Banking`

## Domain Context

Distinct from the retail/commercial banking and insurance patterns already covered in [Financial Services](financial-services.md), this domain covers trading, investment banking, asset management, and market infrastructure — environments defined by real-time market data, strict trade-surveillance and market-conduct regulation, and a much lower tolerance for latency and unexplainable model behavior than most other domains in this repository.

**In plain terms:** this is the world of buying and selling securities, advising on deals, and managing other people's money — a fast-moving, heavily regulated environment where a huge amount of staff time goes into surveillance, research drafting, and document review that has to be both fast and defensible.

**For business readers:** the regulatory cost of getting this wrong (a missed surveillance alert, a research report that violates disclosure rules, an incomplete audit trail on a trading decision) is severe and immediate — fines, license risk, and reputational damage — which means the automation opportunity here skews toward coverage and evidence quality over raw speed, even though speed matters more here than almost anywhere else in this catalog.

**For technical readers:** integration typically means real-time or near-real-time market data and order/trade-management system feeds (read-only for surveillance use cases), research and deal-document repositories, and a documented compliance rulebook (market-abuse indicators, research-disclosure requirements, suitability rules) that the agent applies rather than infers — with every flagged instance retaining a full evidence trail for regulatory examination.

## Most Relevant Functions

| Function | Relevance | Notes |
|---|---|---|
| [Risk & Internal Audit](../02-functions/risk-internal-audit.md) | Core | Trade surveillance and market-conduct monitoring is this domain's flagship pattern |
| [Legal & Compliance](../02-functions/legal-compliance.md) | Core | Research disclosure review, deal-document review, regulatory reporting |
| [Data & Analytics](../02-functions/data-analytics.md) | Core | Market and portfolio data synthesis, first-pass research drafting support |
| [Finance & Accounting](../02-functions/finance-accounting.md) | Adaptable | Trade reconciliation and settlement support |
| [Sales](../02-functions/sales.md) | Adaptable | Suitability and disclosure rules constrain client-facing personalization materially more than in retail financial services |

## Domain-Exclusive Opportunities

- [Trade Surveillance & Market Abuse Detection Agent](../05-use-cases/trade-surveillance-market-abuse-agent.md)
- [Research Report Disclosure Compliance Agent](../05-use-cases/research-report-disclosure-compliance-agent.md)

## Regulatory Considerations

Market-abuse, best-execution, research-disclosure, and suitability regulation vary by jurisdiction and asset class, and enforcement here is generally stricter and faster-moving than in retail financial services. See the companion [Responsible-AI: Financial Services sector guidance](https://github.com/knowledgetrailsai/Responsible-AI/blob/main/11-sector-specific-ai/financial-services.md) as a starting point, but verify current market-conduct rules directly — this is one of the domains in this repository where the regulatory landscape changes fastest.

## Typical Automation Posture

L2 as the default for surveillance and monitoring (exhaustive automated flagging, human-owned investigation and disposition); L1 for anything client- or market-facing (research commentary, trade recommendations) given disclosure and suitability stakes. L3+ autonomous action is not a realistic posture anywhere in this domain given the regulatory and reputational cost of an error.

---

**Previous:** [Scientific Research & Life Sciences R&D](scientific-research.md)
**Next:** [Advertising & Media](advertising-media.md)
