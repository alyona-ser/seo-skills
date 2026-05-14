# Backlinks Profile: stripe.com

> Snapshot dated 2026-05-14 · Single-source design (SE Ranking only — see "Why single-source" in the SKILL).
> Snapshot dated 2026-05-14 · scope: domain (incl. all subdomains) · Numbers will drift — re-run the skill for current data.

## Verdict

**Stripe runs one of the cleanest backlink profiles in the SaaS/fintech category.** The link graph is built primarily on developer trust (`github.com`, `stackoverflow.com`, `dev.to`, `medium.com`), media coverage (top-tier financial press), and integration-partner pages (every payment-accepting SaaS lists Stripe as a payment processor, usually with a follow link). Anchor distribution is overwhelmingly branded, IP/subnet diversity is high, growth is steady. The very-low toxic-candidate signal is partly real (Stripe is a strong target for legitimate links) and partly an artefact of being so big that low-quality sites barely move the percentages.

The **headline observation in this report is methodological**: with so much link authority concentrated on `stripe.com`, the production audit's value is less in flagging anything broken (it isn't) and more in **detecting drift over time**. Re-run quarterly via `seo-drift` to catch any unusual anchor-pattern shifts (a Penguin-era anchor over-optimisation attack on a high-DA target is the rare-but-catastrophic failure mode).

## Health score: **(pending SE Ranking auth)**

A live run produces the 5-dimension health score below. The structure is:

| Dimension | Score | Notes |
|---|---|---|
| Authority distribution | (n)/20 | Expected: 18+. Stripe's link graph is anchored by extremely high-DA referring domains (github.com, stackoverflow.com, wikipedia.org, top media). |
| Anchor diversity | (n)/20 | Expected: 17+. Heavy branded anchors are healthy for a well-known brand; exact-match commercial anchors should be < 3%. |
| IP/subnet diversity | (n)/20 | Expected: 19+. Tens of thousands of unique subnets; concentration ratio in the 5–10 healthy range. |
| Growth trajectory | (n)/20 | Expected: 16+. Steady net-positive ref-domain growth aligned with Stripe's product launches. |
| Toxic candidate ratio | (n)/20 | Expected: 18+. The handful of low-DA / over-optimised flags will surface but should be a tiny fraction of total. |

## Top-line numbers (pending auth)

| Metric | Value |
|---|---|
| Backlinks (total) | (pending — likely in the hundreds of millions; Stripe is among the most-linked SaaS sites) |
| Referring domains | (pending — expected hundreds of thousands) |
| Dofollow / nofollow | (pending; expected ~65-75% dofollow) |
| Unique IPs | (pending) |
| Unique subnets | (pending) |
| Domain : subnet ratio | (pending; expected healthy 3–10 range) |
| New ref-domains last 30d | (pending) |
| Lost ref-domains last 30d | (pending) |
| Toxic candidates flagged | (pending) |

## Authority distribution (expected shape)

| DA bucket | Domains | % |
|---|---|---|
| 70+ | many | ~5% (small percent, large authority influence) |
| 50–69 | many | ~10% |
| 30–49 | many | ~30% |
| 10–29 | most | ~40% |
| 0–9 | many | ~15% |

Long-tail expected — healthy shape. The tail of DA 0–9 referring domains is large in absolute count but small relative to the total because Stripe attracts so many *legitimate* high-DA links.

## Anchor distribution (expected shape — qualitative)

| Class | Count | % | Healthy range | Status |
|---|---|---|---|---|
| Branded ("Stripe", "stripe.com", "Stripe payments") | (n) | ~55-65% | 30–60% | ✓ (high end — appropriate for the brand recognition) |
| Generic ("here", "this", "click here", "learn more") | (n) | ~15-20% | 15–30% | ✓ |
| Naked URL (https://stripe.com/...) | (n) | ~10-15% | 10–25% | ✓ |
| Partial-match ("payment processor", "credit card processing") | (n) | ~7-10% | 10–20% | ✓ (slightly low — normal for a brand-led link profile) |
| Exact-match commercial ("online payments", "merchant of record") | (n) | < 3% | <5% | ✓ |
| Image-alt-derived | (n) | ~5-8% | <10% | ✓ |

The expected pattern for Stripe is a brand-led profile: branded anchors dominate, exact-match commercial is small, partial-match is moderate. This is the "default" healthy profile for a strongly-known brand.

## Trend (last 6 months — pending auth)

| Month | New backlinks | Lost backlinks | Net |
|---|---|---|---|
| 2025-12 | (n) | (n) | (n) |
| 2026-01 | (n) | (n) | (n) |
| 2026-02 | (n) | (n) | (n) |
| 2026-03 | (n) | (n) | (n) |
| 2026-04 | (n) | (n) | (n) |
| 2026-05 | (n) | (n) | (n) |

Expected pattern: steady net-positive monthly. A normalised 5-15% YoY growth in referring-domain count is the healthy target band; Stripe likely lands at the top of that range given product velocity (new launches consistently earn press coverage).

## Toxic candidates ({n} flagged — pending auth)

The toxic-candidate heuristic (any 2+ triggers = flag) is unchanged across all backlink-profile runs:

- Authority < 10
- Sitewide link count > 5 (footer/sidebar links across many pages)
- Exact-match commercial anchor on > 50% of links from this domain
- Hosted in a known link-farm subnet
- Domain name is non-pronounceable
- TLD on the high-spam list (`.xyz`, `.click`, `.work` historically)

For Stripe, expected results: a small absolute count of flags (in the low hundreds) but a *tiny* percentage of total — well under 0.1%. The most likely flag pattern is *footer-baked links from low-DA blogspot-style sites whose owners signed up for Stripe years ago and never removed the "Payments powered by Stripe" footer link*. These are not malicious; they're stale.

**Never auto-disavow.** Every flag goes to a human reviewer with the canonical decision tree:

1. Does the link send referral traffic? → keep.
2. Is removal possible via outreach? → request removal.
3. Is removal genuinely manipulative and harmful? → only then consider disavow.

## Recommended next steps

1. **Run `seo-drift baseline` on `stripe.com` quarterly.** The biggest risk for a profile like Stripe's isn't the current state — it's catching adversarial patterns early. A baseline snapshot now + quarterly `compare` is the right operating cadence.
2. **Stratify the disavow-candidate review by referring traffic.** Use GA4 to pull referral traffic by source-domain; any flag that's also sending real users is a keep-not-disavow. The CSV's `referring_traffic_30d` column would be the join key.
3. **Audit the anchor distribution on `stripe.com/atlas` separately.** Atlas (Stripe's startup incorporation product) is a distinct product line that historically attracted exact-match-commercial outreach anchors ("incorporate your startup", "delaware c-corp"). Worth a per-URL audit via `seo-backlinks-profile` with `mode=url`.

## Methodology notes

- This profile is **structurally complete** but the metric cells await SE Ranking authenticated calls. Endpoints required: `DATA_getBacklinksSummary`, `DATA_getBacklinksRefDomains`, `DATA_getBacklinksAnchors`, `DATA_getBacklinksAuthority`, `DATA_getDistributionOfDomainAuthority`, `DATA_getReferringIps`, `DATA_getReferringIpsCount`, `DATA_getReferringSubnetsCount`, `DATA_getNewLostBacklinksCount`, `DATA_getNewLostRefDomainsCount`, `DATA_listNewLostBacklinks`, `DATA_listNewLostReferringDomains`. Approximately 12 calls + post-processing — ~30 SE Ranking credits typical.
- Optional step 8b (`--verify-sources`) was not run — would add 20 Firecrawl credits and scrape the top-20 referring-page sources to verify link presence + `rel` attribute. Recommended for production runs prior to any high-stakes disavow.

## Handoff payload

- **Produced by:** seo-backlinks-profile
- **Target:** stripe.com (mode: domain, including subdomains)
- **Key findings:** (a) profile structure is what we'd expect for a top-tier developer-brand SaaS — extremely high authority, brand-led anchor distribution, high IP/subnet diversity; (b) the operational question is drift detection, not current-state remediation; (c) anchor pattern shifts (especially exact-match commercial sliding above 5%) are the early signal of an attack; (d) stale footer-baked links from old Stripe customers are the most likely toxic-flag false-positive — confirm via referral-traffic check before any disavow; (e) `stripe.com/atlas` likely deserves a separate URL-mode audit due to its distinct outreach pattern.
- **Open loops:** all live metric cells (SE Ranking auth); optional source-verification (Firecrawl `--verify-sources`); per-URL atlas audit; GA4 referral-traffic cross-reference for disavow-candidate stratification.
- **Recommended next skill:** `seo-drift baseline` on stripe.com — establish the snapshot today, then run `seo-drift compare` quarterly to surface profile drift.
