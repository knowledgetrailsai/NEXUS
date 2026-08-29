# Function: Supply Chain & Operations

`Home › 02-functions › Supply Chain & Operations`

## Why This Function Is a Strong Fit

Forecasting, replenishment, and logistics coordination are data-rich, pattern-based, and directly tied to measurable outcomes (stockouts avoided, inventory cost reduced) — making this function especially well-suited to the [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum) value-density model.

**Scope note:** this function covers the physical flow of goods and materials — forecasting, replenishment, logistics, and warehouse/distribution coordination. Field service dispatch and asset maintenance scheduling belong to [Operations & Resource Scheduling](operations-resource-scheduling.md); product/process quality issues belong to [Quality Management](quality-management.md); insurance claims belong to [Claims Management](claims-management.md) — each is a distinct business function with its own systems, professionals, and stakes, not a variant of supply chain.

## Common Opportunity Patterns

| Pattern | Typical starting level | Use case |
|---|---|---|
| Demand forecasting and replenishment recommendations | L2 → L3 | [Demand Forecasting & Replenishment Agent](../05-use-cases/demand-forecasting-replenishment-agent.md) |
| Logistics exception monitoring and rerouting suggestions | L1 → L2 | Not yet detailed |
| Supplier delivery performance tracking | L1 → L2 | Closely related to [Purchasing & Procurement: Supplier Risk Monitoring](purchasing-procurement.md) |
| Warehouse and distribution exception handling | L2 → L3 | Not yet detailed |

## Domain Applicability

| Domain | Notes |
|---|---|
| [Retail & CPG](../03-domains/retail-cpg.md), [Manufacturing](../03-domains/manufacturing.md) | Core — this is often the highest-value function in these domains |
| [Telecom & Media](../03-domains/telecom-media.md) | Adaptable — network/field logistics coordination (distinct from the field dispatch pattern itself, see [Operations & Resource Scheduling](operations-resource-scheduling.md)) |
| [Insurance](../03-domains/insurance.md) | Limited direct fit — claims processing is a distinct function; see [Claims Management](claims-management.md) for this domain's flagship opportunity instead |
| [Financial Services](../03-domains/financial-services.md), [Technology & SaaS](../03-domains/technology-saas.md), [Public Sector](../03-domains/public-sector.md), [Healthcare](../03-domains/healthcare.md) | Limited direct fit, though healthcare supply chain (medical inventory) is a notable adjacent case |

## Key Cross-Cutting Risks

- Forecasting errors compound across a supply chain — validate against a human-reviewed baseline before scaling to L3
- Autonomous reordering (L4) directly commits real money — start with recommendation-only (L2) and earn autonomy incrementally
- Data quality from upstream systems (POS, IoT sensors) directly bounds achievable accuracy

---

**Previous:** [Risk & Internal Audit](risk-internal-audit.md)
**Next:** [Quality Management](quality-management.md)
