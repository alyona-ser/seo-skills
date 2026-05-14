# 01 — Backlinks summary (DATA_getBacklinksSummary)

> Source: `DATA_getBacklinksSummary(target="stripe.com", mode="domain")` — pending SE Ranking auth.

## Expected payload schema

```jsonc
{
  "target": "stripe.com",
  "mode": "domain",
  "totals": {
    "backlinks": <int>,
    "ref_domains": <int>,
    "ref_subdomains": <int>,
    "ref_ips": <int>,
    "ref_subnets": <int>,
    "dofollow_links_pct": <float>,
    "nofollow_links_pct": <float>
  },
  "link_types": {
    "text": <int>,
    "image": <int>,
    "form": <int>,
    "frame": <int>,
    "redirect": <int>
  },
  "growth": {
    "new_backlinks_30d": <int>,
    "lost_backlinks_30d": <int>,
    "new_ref_domains_30d": <int>,
    "lost_ref_domains_30d": <int>,
    "net_30d_pct_change": <float>
  }
}
```

## Why this step matters

The summary is the entry point: it confirms whether the profile is in the expected order of magnitude (hundreds of millions of backlinks for a brand the size of Stripe). A sharp drop in any total can signal:

- Crawl issue on SE Ranking's side.
- Penalty / de-indexation on Stripe's side (very unlikely at this scale).
- Mass-disavow at the apex of the link graph (very unlikely).

For an established brand like Stripe, the summary should be remarkably stable month-over-month. Any > 5% MoM swing in `ref_domains` is worth investigating.
