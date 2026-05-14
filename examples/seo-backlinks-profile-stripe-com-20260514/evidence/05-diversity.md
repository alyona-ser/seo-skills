# 05 — IP and subnet diversity

> Source: `DATA_getReferringIps`, `DATA_getReferringIpsCount`, `DATA_getReferringSubnetsCount` — pending SE Ranking auth.

## Expected ratios for Stripe

| Metric | Expected value | Healthy range |
|---|---|---|
| Unique referring IPs | hundreds of thousands | — |
| Unique /24 subnets | tens of thousands | — |
| Ref-domain : unique-subnet ratio | 3–10 | 3–10 (healthy); >15 = concentrated PBN risk |
| Most-referred subnet | < 0.5% of total ref domains | < 1% (any single subnet contributing >5% = strong PBN signal) |

## Why diversity matters

A natural backlink profile has links from many hosting providers (AWS, GCP, DigitalOcean, OVH, Hetzner, regional providers, university networks). A manipulative profile shows clustering — many "different" domains hosted in the same datacenter rack, often shared registrant, often near-identical templates.

For Stripe, the legitimate breadth of customers (every customer's website is in scope as a potential linker) makes the profile *very* diverse. Concentration ratios should be well within healthy bands.

## What would be alarming

- A new subnet appearing this month with 500+ referring domains: investigate immediately (PBN spin-up signal).
- The domain:subnet ratio jumping from 6 to 20 month-over-month: investigate.
- Country distribution showing a sudden surge from a single country with no business justification (e.g. 10x increase in `.tk` domains): investigate.

## Pending

Live counts on next run.
