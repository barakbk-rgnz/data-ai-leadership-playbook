# ADR-0001: Governed semantic layer before AI agents

**Status:** Accepted
**Context type:** Pattern, generalized from B2B SaaS analytics work

## Context
Leadership wants AI agents that answer business questions in natural language. The warehouse has dozens of tables, several definitions of the same metric (for example "ARR" or "active customer"), and dashboards that disagree with each other.

An agent pointed at that estate will answer confidently and inconsistently. Users will not distinguish a wrong agent from a wrong team.

## Decision
Build a governed semantic layer first. Agents query only through it.

- One definition per metric, owned by a named person, with grain and filters documented
- Business-friendly views and semantic models sit on top of curated tables, never raw ones
- Agents and dashboards share the same layer, so a disagreement is a bug in one place
- Agent access to raw tables is disabled by default

## Options considered
| Option | Upside | Downside |
|---|---|---|
| Agent over raw warehouse | Fastest demo | Inconsistent answers, no audit trail, trust collapses after the first visible error |
| Agent plus prompt-level metric definitions | Cheap | Definitions drift from the warehouse, nobody owns them |
| **Semantic layer first, agent on top** | One source of truth, testable, reusable by BI | 6 to 10 weeks before the first agent demo |
| Buy an end-to-end AI analytics tool | Speed | Definitions live in a vendor, lock-in, weak governance |

## Consequences
**Good**
- Agent accuracy becomes measurable against golden questions
- Metric disputes move from meetings to pull requests
- BI and AI reuse the same investment

**Bad**
- Slower first demo, which needs active stakeholder management
- Requires someone to own metric definitions, which is a people problem before it is a tech problem
- Coverage starts narrow. Questions outside the layer get "I can't answer that", by design

## Guardrails
- Start with 1 domain and 10 to 15 metrics, not the whole business
- Ship an eval set (golden questions with expected answers) with the first agent release
- Track "refused" and "wrong" separately. Refusal is acceptable, wrong is not

## Revisit when
- Over 30% of real user questions fall outside the layer
- Maintaining the layer costs more than the trust it buys
