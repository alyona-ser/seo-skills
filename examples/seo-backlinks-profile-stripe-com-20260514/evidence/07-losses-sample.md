# 07 — Recent lost backlinks (sample)

> Source: `DATA_listNewLostBacklinks(target="stripe.com", limit=100)` + `DATA_listNewLostReferringDomains` — pending SE Ranking auth.

## Why we sample lost links

A profile audit isn't just about the new-link surface — losses tell a story too:

- **High-authority losses** are immediate red flags. Did a major partner stop linking? Did a press piece de-index? Did a popular GitHub repo migrate to a competitor?
- **Many low-authority losses** are usually noise (small blogs going stale, sites going dark) — track in aggregate, don't act on individuals.
- **Patterns in losses** matter: 50 losses from the same subnet on the same day is interesting (could be a hosting provider migration, could be a removed PBN).

## Schema

```jsonc
{
  "domain": "example-partner.com",
  "authority": 65,
  "last_seen": "2026-04-12",
  "first_seen": "2018-09-03",
  "lost_link": "https://example-partner.com/integrations/stripe",
  "anchor": "Stripe payments",
  "rel": "dofollow"
}
```

## What to do with this list

1. **Sort by authority descending.** Top 10–20 losses are the actionable ones.
2. **Email outreach** to high-authority losses to ask why the link was removed. Most of the time it's a site redesign, partner deprecation, or content refresh — and they're often willing to re-add the link.
3. **Cross-reference with `seo-drift`** to confirm whether the loss correlates with any ranking impact.

## Pending

Real loss data on next run.
