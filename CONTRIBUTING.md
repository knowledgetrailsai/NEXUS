# Contributing to OASIS Agentic Grid

This is a living catalog, released under MIT, mapping agentic AI automation opportunities across business functions and industry domains.

## What's Most Valuable

- **New use cases** — filled examples using [templates/use-case-template.md](templates/use-case-template.md), added to `05-use-cases/`.
- **Domain-specific variants** — a use case that applies differently in a specific industry (regulatory constraints, workflow differences) is worth its own entry, cross-linked from both the function and domain file.
- **Grid corrections** — if `04-grid/opportunity-grid.md` marks a function/domain intersection incorrectly (too optimistic or too conservative), open an issue.
- **Real maturity signals** — if you've deployed one of these patterns, note which [automation maturity level](01-foundations/agentic-automation-spectrum.md) you actually reached and why.

## How to Contribute

1. Fork the repository.
2. New use case: copy [templates/use-case-template.md](templates/use-case-template.md) into `05-use-cases/`, fill it in — including its Capability tag from [Capabilities & Outcomes](01-foundations/capabilities-and-outcomes.md), Benefits, Agentic Design, and Autonomy → Outcome Mapping — and link it from the relevant function file (`02-functions/`), domain file(s) (`03-domains/`), and the grid (`04-grid/opportunity-grid.md`).
3. **Don't add a "pattern" row without a use case.** A function file's "Use Cases in This Function" table lists only real, linked use cases. If a pattern is worth naming but not yet written up, put it in that section's trailing prose ("Other credible patterns... aren't yet written up"), not as a table row with "Not yet detailed" — patterns are use cases, not a separate, thinner abstraction.
4. Changes to core structure (`01-foundations/`, `04-grid/`) — open an issue first.
5. Update `INDEX.md` if you add or rename a file.

## Code of Conduct

Be concrete. A use case entry should be specific enough that someone could scope a pilot from it — vague "AI could help with X" entries add noise, not value.
