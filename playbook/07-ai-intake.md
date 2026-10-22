# 7. AI use-case intake and risk tiers

> Draft: sample content, to be refined. Template: [ai-use-case-intake.md](../templates/ai-use-case-intake.md).

Most AI requests are solutions looking for a problem. Intake turns "we need AI" into "this decision gets faster or better, here is how we know".

## Risk tiers
| Tier | Examples | Requirements |
|---|---|---|
| Low | Internal summaries, drafting, search over docs | Owner, basic eval, usage logging |
| Medium | Customer-adjacent drafts, sales insights, support triage | Human review, golden set eval, monthly review |
| High | Financial figures, legal, people decisions, pricing | Human approval on every output, formal eval, audit trail, exec sign-off |

## Sample intake log
| Use case | Tier | Value estimate | Decision | Reason |
|---|---|---|---|---|
| Weekly KPI summary to execs | Low | 4 h/week saved | Approve | Reads only certified metrics |
| Support ticket auto-tagging | Medium | 30% faster routing | Pilot | Needs 500-ticket golden set |
| Natural language ARR Q&A | Medium | Fewer ad hoc requests | Pilot | Only after Revenue domain is certified |
| Auto-generated performance reviews | High | Unclear | Decline | People decision, low measurable value |

## Questions that kill weak proposals fast
- What decision changes if this works?
- What happens when it is wrong, and who notices?
- What does it cost to run per month at full adoption?
