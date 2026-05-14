# 04 — Authority distribution

> Source: `DATA_getBacklinksAuthority(target="stripe.com")` + `DATA_getDistributionOfDomainAuthority(target="stripe.com")` — pending SE Ranking auth.

## Expected histogram shape

For a brand at Stripe's scale, the DA-of-referring-domains histogram looks like:

```
DA 80–100 │ ████  ~3%   (top media, GitHub, Wikipedia, Stack Overflow, top SaaS)
DA 60–79  │ ███████  ~7%   (substantial press, mid-tier SaaS competitors-and-partners)
DA 40–59  │ ████████████████  ~18%  (industry blogs, fintech ecosystem)
DA 20–39  │ ███████████████████████████  ~32%  (smaller tech blogs, dev tutorials)
DA 10–19  │ ████████████████████████  ~25%  (very long tail of small blogs, partner sites)
DA 0–9    │ ███████████  ~15%  (noise floor — personal blogs, low-quality outlets)
```

## Why this shape is healthy

The "fat middle" (DA 20–59) is where most legitimate small/medium-business links sit. A profile that's too top-heavy (DA 60+ > 30%) often signals press-bot/PR pickup linking without organic developer adoption; a profile that's too bottom-heavy (DA 0–19 > 70%) is the classic link-network / PBN signal.

Stripe's expected shape — fat middle + small (5–10%) head + long but bounded (< 20%) low-DA tail — is the textbook healthy distribution.

## Anomaly thresholds

- DA 0–9 > 25%: investigate (link-farm risk).
- DA 80+ < 1%: investigate (loss of high-trust signal — unusual for a top brand).
- DA distribution shape changes by > 5 percentage points in any bucket month-over-month: investigate.

## Pending

Live counts on next run with auth.
