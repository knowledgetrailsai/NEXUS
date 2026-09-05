# Nexus:OASIS Agentic Grid

A catalog of agentic AI automation opportunities, organized as a **grid**: business functions (which repeat across industries) crossed with domains (which give each function its industry-specific shape). Built to answer, concretely: *where in our business is agentic AI actually a good fit, and how far can automation realistically go there?*

```
FUNCTION (the common pattern) × DOMAIN (the industry-specific variant) → USE CASE
```

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Status](https://img.shields.io/badge/status-draft%20v1.0-orange)

See [00-navigation-and-methodology/knowledge-map.md](00-navigation-and-methodology/knowledge-map.md) for the full grid model and a worked example.

## Start Here

New to this repository? Read [00-navigation-and-methodology/how-to-use-this-repository.md](00-navigation-and-methodology/how-to-use-this-repository.md), which routes you by function-first, domain-first, or "show me everything."

## Repository Structure

### 00 · Navigation and Methodology
- [Knowledge Map](00-navigation-and-methodology/knowledge-map.md)
- [How to Use This Repository](00-navigation-and-methodology/how-to-use-this-repository.md)

### 01 · Foundations
- [What Is This Repository](01-foundations/what-is-this-repository.md)
- [Principles](01-foundations/principles.md)
- [The Agentic Automation Spectrum (L1–L4)](01-foundations/agentic-automation-spectrum.md)
- [Capabilities & Outcomes](01-foundations/capabilities-and-outcomes.md): the capability taxonomy and outcome categories every use case is tagged against
- [Discovering Use Cases](01-foundations/discovering-use-cases.md) — process analysis, workshops, shadowing, and other discovery methods, aligned to OASIS Phase 1
- [Use-Case Anatomy](01-foundations/use-case-anatomy.md), covering how to turn an idea into a bounded workflow
- [Evaluation & Rollout](01-foundations/evaluation-and-rollout.md) — test layers, launch gates, and autonomy progression

### 02 · Functions (the common patterns)
- [Purchasing & Procurement](02-functions/purchasing-procurement.md)
- [Sales](02-functions/sales.md)
- [Customer Relations & Support](02-functions/customer-relations-support.md)
- [Marketing](02-functions/marketing.md)
- [Data & Analytics](02-functions/data-analytics.md)
- [HR & People](02-functions/hr-people.md)
- [Finance & Accounting](02-functions/finance-accounting.md)
- [IT & Security](02-functions/it-security.md)
- [Legal & Compliance](02-functions/legal-compliance.md)
- [Risk & Internal Audit](02-functions/risk-internal-audit.md)
- [Supply Chain & Operations](02-functions/supply-chain-operations.md)
- [Quality Management](02-functions/quality-management.md)
- [Operations & Resource Scheduling](02-functions/operations-resource-scheduling.md)
- [Claims Management](02-functions/claims-management.md)
- [Research & Development](02-functions/research-development.md)

### 03 · Domains (the industry-specific variants)
- [Financial Services](03-domains/financial-services.md)
- [Healthcare & Life Sciences](03-domains/healthcare.md)
- [Retail & CPG](03-domains/retail-cpg.md)
- [Manufacturing & Industrial](03-domains/manufacturing.md)
- [Insurance](03-domains/insurance.md)
- [Telecom & Media](03-domains/telecom-media.md)
- [Public Sector & Government](03-domains/public-sector.md)
- [Technology & SaaS](03-domains/technology-saas.md)
- [Energy & Utilities](03-domains/energy-utilities.md)
- [Education & Higher Education](03-domains/education-higher-education.md)
- [Travel & Hospitality](03-domains/travel-hospitality.md)
- [Industrial & Heavy Operations](03-domains/industrial-heavy-operations.md)
- [Scientific Research & Life Sciences R&D](03-domains/scientific-research.md)
- [Capital Markets & Investment Banking](03-domains/capital-markets-investment-banking.md)
- [Advertising & Media](03-domains/advertising-media.md)

### 04 · Grid
- [The Opportunity Grid](04-grid/opportunity-grid.md) — the full function × domain matrix
- [Prioritization Framework](04-grid/prioritization-framework.md)

### 05 · Use Cases
46 detailed entries spanning the common function patterns plus domain-exclusive workflows. See [05-use-cases/](05-use-cases/benefits-eligibility-document-verification-agent.md) for the full list. Domain-exclusive entries are intentionally not forced into the general grid. Newer entries also carry a "Who This Is For" section (plain-language / business / technical summaries) and a KPIs Influenced section — see the [use case template](templates/use-case-template.md).

### Glossary & Templates
- [Glossary](glossary/glossary.md)
- [Use Case Template](templates/use-case-template.md)

Not sure where to look? See [INDEX.md](INDEX.md) for every file, or [00-navigation-and-methodology/how-to-use-this-repository.md](00-navigation-and-methodology/how-to-use-this-repository.md).

## Quick Start

1. Read [Principles](01-foundations/principles.md) and the [Agentic Automation Spectrum](01-foundations/agentic-automation-spectrum.md).
2. Scan the [Opportunity Grid](04-grid/opportunity-grid.md) for your domain, or browse a [function](02-functions/claims-management.md) that interests you.
3. Read the full [use case](05-use-cases/benefits-eligibility-document-verification-agent.md) entries for your top candidates, checking the workflow boundary and exception paths.
4. Use the [Prioritization Framework](04-grid/prioritization-framework.md) to sequence candidates.
5. Apply [Use-Case Anatomy](01-foundations/use-case-anatomy.md) and [Evaluation & Rollout](01-foundations/evaluation-and-rollout.md) to prepare a discovery brief.
6. Move your top candidate into [OASIS](https://github.com/knowledgetrailsai/OASIS) Phase 1, formalize its value case with [oasis-fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum), and assess its risk with [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI).

## Relationship to companion repositories

Nexus is the cross-cutting opportunity catalog feeding [OASIS](https://github.com/knowledgetrailsai/OASIS) Chapter 5 (Opportunity Portfolio and Transformation Horizons). It is not itself a Part III chapter companion, the way [Axiom](https://github.com/knowledgetrailsai/Axiom) is a background reference rather than a chapter companion. See the [Companion Repository Index](https://github.com/knowledgetrailsai/OASIS/blob/main/References/companion-repository-index.md) for the full map of which repository backs which chapter.

**Nexus answers "where should we look?"** Once a use case is selected here, it moves into the chapter-specific companions that answer "how do we build, evaluate, secure, cost, and govern it":

- **[Ageis](https://github.com/knowledgetrailsai/Ageis)** (Chapter 14): agentic coding delivery, once the use case reaches implementation.
- **[Forge](https://github.com/knowledgetrailsai/Forge)** (Chapter 15): data and knowledge engineering, where a use case's data dependencies are scoped.
- **[Loom](https://github.com/knowledgetrailsai/Loom)** (Chapter 16): human-AI workflow, where a use case's human-in-the-loop shape is decided.
- **[Helm](https://github.com/knowledgetrailsai/HELM)** (Chapters 17/18/19/21/26): deployment, operations, and AgentOps once the use case ships.
- **[Verity](https://github.com/knowledgetrailsai/Verity)** (Chapter 18) — the deep evaluation and reliability methodology.
- **[Compass](https://github.com/knowledgetrailsai/responsible-ai)** (Chapters 19–20): responsible AI, security, and regulatory compliance.
- **[Fulcrum](https://github.com/knowledgetrailsai/oasis-fulcrum)** (Chapter 22) — cost and value tracking once the use case is in production.

## Contributing

This is a living catalog — see [CONTRIBUTING.md](CONTRIBUTING.md). New use cases, domain-specific variants, and grid corrections are especially welcome.

## Disclaimer

Every use case's Value Signal is a plausible hypothesis, not a committed business case (see [Principles](01-foundations/principles.md#value-signal-not-a-value-case)). Every use case's Key Risks section is a starting flag, not a complete risk assessment — see [Responsible-AI](https://github.com/knowledgetrailsai/Responsible-AI) for full treatment before deployment.

## License

Licensed under [CC BY-SA 4.0](https://github.com/knowledgetrailsai/OASIS/blob/main/LICENSE.md). Reuse and adaptation are welcome with credit to KnowledgeTrails-OASIS, a link to the license, an indication of changes, and release of adaptations under the same license.

## About Us

**Shripadraj Mujumdar** is an Agentic AI & Automation Strategist, Advisor, and Responsible AI Expert with 28+ years of experience in enterprise architecture and AI-driven transformation, including deep hands-on work in Agentic AI, Generative AI, and enterprise data and knowledge platforms. His practice spans designing multi-agent systems, knowledge-graph and RAG architectures, accelerated delivery capabilities, and Responsible AI governance frameworks aligned to global regulatory standards. This methodology ecosystem distills that practitioner experience — architecture, delivery, evaluation, governance, and economics — into a single, reusable body of work.

**Ankit Mirajkar** is a Data & AI Architect and technology consultant specializing in modern data platforms, enterprise data architecture, and Agentic AI. His expertise spans scalable data engineering, AI-ready data platforms, Generative AI, and cloud technologies, with a strong focus on turning complex data challenges into practical, production-ready solutions. He also works at the intersection of architecture, technology strategy, and innovation to help organizations build intelligent, scalable data ecosystems.
