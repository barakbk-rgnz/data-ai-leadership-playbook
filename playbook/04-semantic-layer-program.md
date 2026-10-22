# 4. Governed semantic layer program

> Draft: sample content, to be refined. See also [ADR-0001](../adr/0001-semantic-layer-before-ai-agents.md).

The semantic layer is where business definitions become code. It is a program, not a project: it needs owners, a backlog and change control.

## Phases
| Phase | Weeks | Scope | Exit criteria |
|---|---|---|---|
| 0. Discover | 1 to 2 | Find the 10 to 15 metrics people argue about | Ranked list with current definitions |
| 1. Pilot domain | 3 to 8 | One domain, for example Revenue | Metric contracts signed, tests green, 1 dashboard migrated |
| 2. Expand | 9 to 20 | 2 to 3 more domains | 50% of Tier 1 dashboards on the layer |
| 3. AI on top | 16+ | Agent queries only the layer | Eval pass rate above threshold |

## Sample pilot metrics (Revenue domain)
| Metric | Grain | Owner | Status |
|---|---|---|---|
| ARR | Account, month | Finance lead | Certified |
| New ARR | Account, month | Finance lead | Certified |
| Net revenue retention | Cohort, month | Finance lead | In review |
| Active customer | Account, day | CS lead | Disputed |
| Pipeline coverage | Segment, quarter | RevOps lead | Draft |

## Design principles
- Curated tables in, business-friendly models out. Never expose raw tables
- One definition per metric. Variants get their own name ("ARR excl. one-offs")
- Every metric has a [metric contract](../templates/metric-contract.md)
- BI and AI read the same layer

## Common failure modes
- Starting with the whole business instead of one domain
- No business owner, so engineers decide definitions by default
- Migrating dashboards without retiring the old ones
