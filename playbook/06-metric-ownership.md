# 6. Metric ownership and change control

> Draft: sample content, to be refined.

A metric without an owner is an opinion. Owners are people in the business, not the data team.

## Roles (RACI)
| Activity | Business owner | Data team | Exec sponsor |
|---|---|---|---|
| Define the metric | A | R | I |
| Implement and test | C | A/R | I |
| Approve changes | A | R | I |
| Resolve disputes | R | C | A |
| Communicate changes | A | R | I |

## Change process
1. Change requested via pull request or ticket, with reason
2. Data team assesses impact: which dashboards, agents and reports move
3. Owner approves
4. Change shipped with a changelog entry and effective date
5. Historical restatement decided explicitly: restate or annotate

## Sample changelog
| Date | Metric | Change | Impact | Approved by |
|---|---|---|---|---|
| 2026-03-01 | Active customer | Exclude trial accounts | -4% count | CS lead |
| 2026-04-15 | ARR | Treat multi-year prepay as annualized | +1.2% ARR | Finance lead |
| 2026-05-10 | Pipeline coverage | Use weighted pipeline | Coverage 3.1x to 2.4x | RevOps lead |

## Rules
- No silent changes. Ever
- A metric changing more than 2% gets an exec heads-up before release
- Disputes go to the exec sponsor within two weeks, not into a third definition
