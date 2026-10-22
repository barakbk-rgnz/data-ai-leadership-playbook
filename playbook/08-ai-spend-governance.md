# 8. AI spend and seat governance

> Draft: sample content, to be refined.

AI spend grows quietly: seats bought by every team, API keys on personal cards, agents nobody switched off. Make it visible before you try to control it.

## Three cost buckets
| Bucket | Examples | Who owns budget |
|---|---|---|
| Seats | Chat assistants, coding assistants, copilots | Team using them |
| Usage | API tokens, agent runs | Product or data team running them |
| Platform | Vector stores, eval tooling, compute | Data & AI team |

## Sample monthly view
| Item | Bucket | Monthly cost | Active users / runs | Cost per active | Action |
|---|---|---|---|---|---|
| Chat assistant seats (80) | Seats | 2,400 | 52 active | 46 | Reclaim 20 idle seats |
| Coding assistant (15) | Seats | 450 | 15 active | 30 | Keep |
| KPI summary agent | Usage | 120 | 4,000 runs | 0.03 per run | Keep |
| Experimental RAG bot | Usage | 900 | 40 runs | 22.50 per run | Shut down or redesign |

## Policies
- One company account per tool. No personal cards
- Seats idle for 30 days get reclaimed
- Every agent in production has an owner, a budget and a kill switch
- Report AI spend next to the value it claims, monthly
