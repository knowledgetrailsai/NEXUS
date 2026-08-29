# Domain: Advertising & Media

`Home › 03-domains › Advertising & Media`

## Domain Context

Distinct from [Telecom & Media](telecom-media.md) (content distribution and networks) and from the [Marketing](../02-functions/marketing.md) function (an advertiser's own in-house marketing team), this domain covers the advertising supply chain itself: agencies, ad tech platforms, and media buying/planning operations that plan, execute, and reconcile advertising campaigns across many publishers and platforms on behalf of clients.

**In plain terms:** this is the business of buying ad space for clients across dozens of platforms at once, then proving afterward that the money was spent where it was supposed to be — a process with a lot of moving numbers across systems that don't always agree with each other.

**For business readers:** discrepancies between what was booked, what actually ran, and what was billed are endemic to this industry because campaigns span many platforms with different reporting formats and timing — reconciling them manually is slow and error-prone, and the errors go directly to client trust and margin. This is a domain where "boring" automation (matching numbers across systems) has an outsized impact on client relationships.

**For technical readers:** integration typically means read access to multiple ad-platform reporting APIs, the campaign/media-plan system of record, and invoicing/billing systems — reconciling three or more independently-reported numbers per campaign line item, each with its own definitions and latency, which makes this a variant of the three-way-match pattern seen elsewhere in this repository rather than a novel problem.

## Most Relevant Functions

| Function | Relevance | Notes |
|---|---|---|
| [Finance & Accounting](../02-functions/finance-accounting.md) | Core | Media spend reconciliation across platforms, client invoicing, discrepancy resolution |
| [Data & Analytics](../02-functions/data-analytics.md) | Core | Cross-platform performance reporting and campaign insight drafting |
| [Marketing](../02-functions/marketing.md) | Adaptable | Campaign content variant generation, applied at agency scale across many clients |
| [Sales](../02-functions/sales.md) | Applies generically | New-business proposal and media-plan drafting |

## Domain-Exclusive Opportunities

- [Media Buy Reconciliation & Discrepancy Resolution Agent](../05-use-cases/media-buy-reconciliation-agent.md)

## Regulatory Considerations

Advertising-standards, data-privacy (audience targeting and tracking), and disclosure regulation (sponsored content, political advertising) vary significantly by jurisdiction and platform. Consumer-protection and privacy rules apply broadly to any targeting or personalization use case in this domain — see the [Marketing function's](../02-functions/marketing.md) risk notes for the underlying pattern.

## Typical Automation Posture

Strong candidate for L2–L3 in reconciliation and reporting workflows, where ground truth (do the numbers match) is largely unambiguous — a good structural fit for the same automation depth as [Finance & Accounting's invoice-matching pattern](../02-functions/finance-accounting.md). Client-facing strategic recommendations and creative decisions stay L1, human-led.

---

**Previous:** [Capital Markets & Investment Banking](capital-markets-investment-banking.md)
**Next:** [Financial Services](financial-services.md)
