# 02 — Per-subdomain overview (structure ready, metrics pending auth)

> Source: would come from `DATA_getDomainOverviewWorldwide` per subdomain. SE Ranking auth unavailable in this worktree.

## Schema (what a full run captures per subdomain)

```jsonc
{
  "subdomain": "developers.notion.com",
  "organic_keywords": 12345,
  "organic_traffic_estimate": 67890,
  "organic_traffic_cost_usd": 12345.67,
  "paid_keywords": 0,
  "domain_authority": 78,
  "top_regions": ["us", "uk", "de", "fr"]
}
```

## Subdomains in scope for this run

1. `www.notion.com` (post-migration apex — gets the bulk of marketing traffic)
2. `www.notion.so` (legacy apex — declining; serves redirects + user-workspace pages)
3. `developers.notion.com` (API/SDK docs)
4. `sitemaps.notion.com` (operational; no SEO traffic)
5. `app.notion.com` (operational; not a marketing surface)

## What we'd expect (qualitative, pending real numbers)

- `www.notion.com` should dominate by 1–2 orders of magnitude on every metric (keywords, traffic, DA).
- `www.notion.so` is in active decline — its 301 to `www.notion.com` means Google is consolidating signals; expect dropping keywords month-over-month, eventually approaching zero except for user-workspace URLs that haven't been migrated.
- `developers.notion.com` will be in the low thousands of keywords (API/SDK queries) with very high DA (developer docs accumulate strong technical backlinks).
- `sitemaps.notion.com` and `app.notion.com` should have ≈ 0 SEO traffic — they're operational endpoints, typically noindex or behind auth.

## Pending

A full run would emit a table like:

| Subdomain | Org. KWs | Traffic est. | DA | Top regions |
|---|---|---|---|---|
| www.notion.com | (n) | (n)/mo | (DA) | us, uk, de, jp, kr |
| www.notion.so | (n, decreasing) | (n)/mo | (DA) | us |
| developers.notion.com | (n) | (n)/mo | (DA) | us |
| sitemaps.notion.com | 0 | 0 | n/a | n/a |
| app.notion.com | ≈ 0 | ≈ 0 | n/a | n/a |
