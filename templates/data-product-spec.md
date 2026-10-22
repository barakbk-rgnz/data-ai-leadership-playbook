# Data product spec: <name>

> Sample filled in below. Copy and replace.

| Field | Value |
|---|---|
| Name | Customer health dataset |
| Purpose (decision it supports) | Which accounts CS should contact this week |
| Business owner | CS lead |
| Technical owner | Analytics engineer |
| Consumers | CS team, churn agent, exec dashboard |
| Tier | 2 (Supported) |
| Grain | One row per account per day |
| Key fields | account_id, health_score, usage_trend_30d, open_tickets, renewal_date |
| Sources | Product usage events, support tickets, CRM |
| Freshness SLA | Daily by 07:00 |
| Quality tests | Unique account per day, score between 0 and 100, no null renewal dates for active accounts |
| Access / sensitivity | Internal, no PII beyond account name |
| Success metric | 80% of CS team uses it weekly within 60 days |
| Deprecation plan | Replace legacy health spreadsheet by end of quarter |
