# 9. Evaluating agents over governed data

> Draft: sample content, to be refined.

If you cannot measure an agent, you cannot ship it to an exec. Evals are the unit tests of AI.

## Build a golden set
- 50 to 100 real questions collected from Slack, tickets and meetings
- Each has an expected answer, computed from the semantic layer
- Include questions the agent should refuse (out of scope, ambiguous, restricted)

## Score four outcomes separately
| Outcome | Meaning | Acceptable? |
|---|---|---|
| Correct | Right answer, right metric | Yes |
| Refused | Said "I can't answer that" | Yes, if out of scope |
| Wrong | Confident and incorrect | No. This is the number that matters |
| Partial | Right metric, wrong filter or period | Counts as wrong for Tier 1 metrics |

## Sample eval run
| Release | Questions | Correct | Refused | Wrong | Partial | Ship? |
|---|---|---|---|---|---|---|
| v0.1 | 60 | 38 (63%) | 8 | 10 | 4 | No |
| v0.2 | 60 | 47 (78%) | 9 | 3 | 1 | Pilot only |
| v0.3 | 80 | 68 (85%) | 11 | 1 | 0 | Yes |

## Release gate (sample)
- Wrong rate under 2% on Tier 1 metrics
- Every refusal has a clear message pointing to a human
- Eval re-runs automatically on every metric or prompt change
