# 10. Build vs buy

> Draft: sample content, to be refined.

Small teams should buy almost everything except the definitions that make the business unique.

## Decision matrix
| Factor | Lean build | Lean buy |
|---|---|---|
| Differentiation | Core to how you compete | Commodity capability |
| Team capacity | Spare, skilled, stable | Stretched |
| Time to value | Can wait months | Need it this quarter |
| Lock-in risk | Vendor would own your definitions | Easy to export and leave |
| Total cost (3 years) | Lower including people | Lower including people |

## Sample decisions
| Capability | Decision | Why |
|---|---|---|
| Ingestion connectors | Buy | Commodity, maintenance heavy |
| Warehouse | Buy | Nobody should run their own |
| Transformation and semantic layer | Build on open tooling | This is where your definitions live |
| BI tool | Buy | Commodity, user familiarity matters |
| AI agent over metrics | Build thin layer on a vendor model | Definitions stay yours, model is swappable |
| Data catalog | Defer | Low adoption until semantic layer exists |

## Rule of thumb
Count people cost honestly. One engineer maintaining a custom tool for a year usually costs more than the license you avoided.
