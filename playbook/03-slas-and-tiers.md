# 3. SLAs and service tiers

> Draft: sample content, to be refined.

Not every dashboard deserves the same care. Tiers make that explicit so you can say no to on-call for a vanity chart.

## Tier definitions
| Tier | What it is | Owner | Freshness | Incident response | Tests |
|---|---|---|---|---|---|
| 1 Certified | Board, finance, exec metrics | Named person | Daily by 08:00 | 4 business hours | Required, blocking |
| 2 Supported | Team dashboards, shared datasets | Team lead | Daily | 2 business days | Recommended |
| 3 Self-serve | Sandbox, exploration | Creator | Best effort | None | Optional |

## Promotion path
Tier 3 to Tier 2: has an owner, used by more than 5 people for 30 days.
Tier 2 to Tier 1: metric contract signed, tests pass, used in a recurring exec decision.

## Sample SLA dashboard
| Asset | Tier | SLA met (last 30d) | Incidents | Owner |
|---|---|---|---|---|
| ARR and NRR | 1 | 97% | 1 | Finance lead |
| Pipeline coverage | 1 | 100% | 0 | RevOps lead |
| Support ticket trends | 2 | 92% | 2 | CS lead |
| Feature usage explorer | 3 | n/a | n/a | Product analyst |

## Rules
- Tier 1 assets get a visible badge. Anything without it is "use with care"
- Demote assets unused for 90 days
- Breaking a Tier 1 SLA triggers a short written postmortem
