# Contributing to OASIS Agentic Grid

This is a living catalog, released under MIT, mapping agentic AI automation opportunities across business functions and industry domains.

## What's Most Valuable

- **New use cases** — filled examples using [templates/use-case-template.md](templates/use-case-template.md), added to `05-use-cases/`.
- **Domain-specific variants** — a use case that applies differently in a specific industry (regulatory constraints, workflow differences) is worth its own entry, cross-linked from both the function and domain file.
- **Grid corrections** — if `04-grid/opportunity-grid.md` marks a function/domain intersection incorrectly (too optimistic or too conservative), open an issue.
- **Real maturity signals** — if you've deployed one of these patterns, note which [automation maturity level](01-foundations/agentic-automation-spectrum.md) you actually reached and why.

## How to Contribute

1. Fork the repository.
2. New use case: copy [templates/use-case-template.md](templates/use-case-template.md) into `05-use-cases/`, fill it in, and link it from the relevant function file (`02-functions/`), domain file(s) (`03-domains/`), and the grid (`04-grid/opportunity-grid.md`).
3. Changes to core structure (`01-foundations/`, `04-grid/`) — open an issue first.
4. Update `INDEX.md` if you add or rename a file.

## Code of Conduct

Be concrete. A use case entry should be specific enough that someone could scope a pilot from it — vague "AI could help with X" entries add noise, not value.
