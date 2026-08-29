# Discovering Use Cases

`Home › 01-foundations › Discovering Use Cases`

Everything else in this repository assumes you already have a candidate — a named workflow to look up by function or domain. This page answers the question that comes *before* that: **how do you find the candidates in the first place?** This is the work that happens before you ever open [the grid](../04-grid/opportunity-grid.md), and it's also the substance of [OASIS](https://github.com/knowledgetrailsai/OASIS) Phase 1 — Engage & Align.

## Two Directions of Discovery

Discovery runs in two directions, and a good program does both rather than picking one:

- **Bottom-up** — start with how work actually happens today (processes, tickets, workshops, direct observation) and surface repeatable, bounded patterns worth automating. Finds real pain, sized by real volume.
- **Top-down** — start with what leadership is trying to achieve (cost reduction, revenue growth, risk posture, a strategic initiative) and work backward to the functions and domains most likely to move that needle. Finds strategic relevance, but can miss operational reality if it stops at the whiteboard.

Bottom-up without top-down tends to produce a long list of locally-obvious automations with no shared priority. Top-down without bottom-up tends to produce ambitious mandates nobody can actually scope. Run both and reconcile them into one backlog.

## Discovery Methods

| Method | What it is | What it surfaces well | What it takes to run | Typical output |
|---|---|---|---|---|
| **Process analysis / process mining** | Reconstructing the actual workflow from system logs, ticket timestamps, and case data — not the documented SOP, but what really happens, including rework and exceptions | High-volume, well-instrumented digital workflows; where time and cost actually go, including hidden rework loops | Access to system/log data (ticketing, ERP, CRM event logs) and someone who can query it; days to weeks depending on data access | A process map with cycle-time and volume by step, and a ranked list of the most time/cost-heavy steps |
| **Stakeholder & user workshops** | Structured facilitated sessions with the people who do the work (and their managers) to surface pain points, walk through a real case end-to-end, and pressure-test whether a workflow is as bounded as it looks on paper | Tacit knowledge that never made it into a system log — exceptions, workarounds, "the real reason this takes so long" | 60–90 minutes with 4–8 participants per session, a facilitator, and a structured agenda (see below) | A list of pain points ranked by the room, a walked-through example case, and a first-pass list of exception types |
| **Shadowing / time-and-motion observation** | Directly observing someone doing the work, in real time, without interrupting — noting what they check, where they hesitate, what they work around | The gap between the documented process and the actual one; UI/tool friction that workshops under-report because people forget to mention what's become automatic to them | A few hours per role observed; requires the observed person's comfort with being watched | An annotated task walkthrough with actual time spent per step and undocumented workarounds |
| **Pain-point surveys / intake forms** | A lightweight, broad-reach form asking "what's a repetitive task you wish you didn't have to do" across a wide population | Volume of candidate ideas across many teams cheaply; useful for surfacing something no one thought to escalate | Low effort to run, but produces noisy, uneven-quality submissions that need triage | A long list of unranked candidate ideas, useful as raw material for the methods above, not a substitute for them |
| **Data-driven discovery** | Mining operational data directly for volume, cost, and cycle-time signals — ticket categories by volume, error/rework rates, SLA breach patterns — without first talking to anyone | Where the real *volume* is, independent of who's loudest about their pain point; good for challenging assumptions about what "everyone knows" is the bottleneck | Requires access to operational reporting/BI and a defined metric set; can run in parallel with other methods | A ranked list of workflows by volume, cost, and current cycle time/error rate |
| **Document & policy audit** | Inventorying the documented rules a workflow already runs on — policies, approval matrices, defect taxonomies, tolerance tables | Whether a workflow has clear enough documented rules to be a safe automation candidate at all — a prerequisite this repository assumes (see [Use-Case Anatomy](use-case-anatomy.md)) | Access to policy documentation and the process owner who can confirm it's current | The rule set a candidate agent would need to apply, and a flag on any rule that's "tribal knowledge" rather than documented |
| **Executive / strategy alignment sessions** | Working sessions with leadership to translate strategic priorities (cost program, growth target, risk posture, a board-level initiative) into candidate functions and domains | Strategic relevance and executive sponsorship — critical for a candidate to survive prioritization and get resourced later | A senior stakeholder's time and a structured translation exercise (priority → function/domain → candidate workflows) | A short list of functions/domains to focus bottom-up discovery on, and the business outcome category (see below) each priority maps to |

## Running a Good Workshop

Since this is often the highest-leverage method and the easiest to run badly:

- **Bring the right people.** The person who actually does the work, not just their manager — managers describe the process as designed, doers describe it as lived.
- **Walk one real case end-to-end**, not an abstract description of the process. Ask "tell me about the last time this got complicated" before "tell me how this normally works" — the complications are where the exception paths in [Use-Case Anatomy](use-case-anatomy.md) come from.
- **Capture volume and frequency**, not just pain intensity. A once-a-quarter headache and a daily annoyance need different treatment even if the room is equally vocal about both.
- **Ask what they'd never want automated.** This surfaces judgment-heavy steps early, so the eventual use case's human-owner and approval points aren't an afterthought.
- **Write it up within a day**, while the specifics are still fresh, into the same shape [Use-Case Anatomy](use-case-anatomy.md) asks for — trigger, systems touched, output, exception paths.

## From Discovery to This Repository

Once a method above has produced a real candidate:

1. Check whether it already resembles an entry in [05-use-cases](../05-use-cases/) — discovery often confirms a known pattern rather than finding something novel, which is fine and faster to scope.
2. If it's genuinely new, use [Use-Case Anatomy](use-case-anatomy.md) to turn the discovery notes into a bounded workflow description.
3. Tag it with a [Capability](capabilities-and-outcomes.md) and [Outcome Category](capabilities-and-outcomes.md#business-outcome-categories) — this is also where you reconcile a bottom-up finding against a top-down priority: does this candidate's outcome category match what leadership said mattered?
4. Run it through the [Prioritization Framework](../04-grid/prioritization-framework.md)'s screening score.
5. Assemble the Discovery Packet and move it into [OASIS](https://github.com/knowledgetrailsai/OASIS) Phase 1 — Engage & Align, where the organization's own stakeholders take over from this repository's generic guidance.

## OASIS Alignment

This page and [Use-Case Anatomy](use-case-anatomy.md) together are the pre-work for **OASIS Phase 1 (Engage & Align)** — they produce the raw material (a scored, documented candidate) that Phase 1 formalizes with named sponsors, committed resourcing, and a chartered scope. This repository doesn't replace Phase 1's stakeholder alignment work; it makes sure you arrive at it with evidence rather than an opinion.

---

**Previous:** [Capabilities & Outcomes](capabilities-and-outcomes.md)
**Next:** [Use-Case Anatomy](use-case-anatomy.md)
