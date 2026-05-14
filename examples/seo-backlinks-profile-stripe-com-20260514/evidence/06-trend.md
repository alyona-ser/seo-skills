# 06 — Trend (last 6 months)

> Source: `DATA_getNewLostBacklinksCount` + `DATA_getNewLostRefDomainsCount` — pending SE Ranking auth.

## Expected pattern

For Stripe, the 6-month trend should show:

- Steady positive net growth in referring domains (5–15% YoY).
- Spikes aligned with major launches / fundraises / press events.
- Modest dips around large platform deprecations (Stripe occasionally retires APIs and customer integrations remove links).

## Pattern types to flag

| Pattern | Signal | Action |
|---|---|---|
| Steady +0–2% MoM net growth | Healthy baseline | Continue |
| Sudden +50% spike | Press event or paid-link campaign | Investigate source; if paid, monitor for Google's algorithmic response |
| Sudden -10% MoM drop | De-indexation / partner removal / algo update | Investigate immediately |
| Steady -3% MoM decline | Profile drift; possibly an outdated brand-mention base aging out | Address with renewed press cadence |

## What real Stripe data would likely show (qualitative)

Stripe's launch cadence is steady (one major product launch per quarter, ~weekly minor updates). Expect:

- Q1: spike around early-year roadmap announcements
- Q2: spike around Sessions (Stripe's user conference)
- Q3: steady baseline
- Q4: spike around year-end product launches and financial press recaps

Off-cadence spikes outside this rhythm are the interesting ones.

## Pending

Real time-series data on next run.
