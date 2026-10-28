---
type: Timeline
title: Google ranking updates, 2023 – 2026
description: Every core, spam, helpful-content and reviews update and ranking incident on Google's Search Status Dashboard since January 2023, with start, end and duration, plus rollout patterns and how to use the dates in analyses.
tags: [seo, google, core-update, spam-update, timeline, measurement]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T02:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-01-31T00:00:00Z
sources:
  - id: status
    resource: "https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history"
    title: "Google Search Status Dashboard, Ranking history (42 entries since Nov 2021) and the per-incident pages, read 2026-10-27"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays Google confirmations and third-party studies)"
---

# Google ranking updates, 2023 – 2026

All dates and times are US/Pacific, as the dashboard shows them. The history page gives start and duration only, so each end date comes from that incident's own page.[^status] Use this list with the [Search Console pitfalls](../measure/search-console.md): a change that starts *before* an update's start date wasn't caused by it.

## Updates

| Update | Type | Start | End | Days |
|---|---|---|---|---|
| February 2023 product reviews update | reviews | 2023-02-21 | 2023-03-07 | 14 |
| March 2023 core update | core | 2023-03-15 | 2023-03-28 | 13 |
| April 2023 reviews update | reviews | 2023-04-12 | 2023-04-25 | 13 |
| August 2023 core update | core | 2023-08-22 | 2023-09-07 | 16 |
| September 2023 helpful content update | helpful content | 2023-09-14 | 2023-09-28 | 13 |
| October 2023 spam update | spam | 2023-10-04 | 2023-10-19 | 15 |
| October 2023 core update | core | 2023-10-05 | 2023-10-19 | 14 |
| Discover issue during the Oct 2023 core update | incident | 2023-10-05 | 2023-10-31 | 26 |
| November 2023 core update | core | 2023-11-02 | 2023-11-28 | 26 |
| November 2023 reviews update | reviews | 2023-11-08 | 2023-12-07 | 29 |
| March 2024 core update | core | 2024-03-05 | 2024-04-19 | 45 |
| March 2024 spam update | spam | 2024-03-05 | 2024-03-20 | 15 |
| June 2024 spam update | spam | 2024-06-20 | 2024-06-27 | 7 |
| August 2024 core update | core | 2024-08-15 | 2024-09-03 | 19 |
| Ranking issue, "unrelated to the ongoing core update" | incident | 2024-08-15 | 2024-08-20 | 4 |
| November 2024 core update | core | 2024-11-11 | 2024-12-05 | 24 |
| December 2024 core update | core | 2024-12-12 | 2024-12-18 | 6 |
| December 2024 spam update | spam | 2024-12-19 | 2024-12-26 | 7 |
| March 2025 core update | core | 2025-03-13 | 2025-03-27 | 14 |
| June 2025 core update | core | 2025-06-30 | 2025-07-17 | 17 |
| August 2025 spam update | spam | 2025-08-26 | 2025-09-22 | 27 |
| December 2025 core update | core | 2025-12-11 | 2025-12-29 | 18 |
| February 2026 Discover update (US English only) | Discover core | 2026-02-05 | 2026-02-27 | 22 |
| March 2026 spam update | spam | 2026-03-24 | 2026-03-25 | 0.8 |
| March 2026 core update | core | 2026-03-27 | 2026-04-08 | 12 |
| May 2026 core update | core | 2026-05-21 | 2026-06-02 | 12 |
| June 2026 spam update | spam | 2026-06-24 | 2026-06-26 | 2 |
| August 2026 spam update | spam | 2026-08-18 | 2026-08-21 | 3 |
| September 2026 spam update | spam | 2026-09-24 | 2026-10-08 | 14 |

As of 2026-10-27 no ranking incident is open.[^status]

**Unannounced changes that also break comparisons** (not on the dashboard):
- **From 27 May 2025:** indexed page counts fell on many sites as Google dropped low-engagement pages ([how Google ranks](../how-it-works/google-ranking.md)).
- **From ~10 Sep 2025:** the `&num=100` change cut Search Console impressions and improved average position ([measurement pitfalls](../measure/search-console.md)).
- **From 13 May 2025:** Search Console impressions inflated, clicks unaffected, as Google confirmed according to secondary reporting ([measurement pitfalls](../measure/search-console.md)).[^ignite-news]
- **2026-05-07:** FAQ rich results reported dropped.[^ignite-news]
- **Mid-Sep 2026:** free product listings removed in the EEA ([feeds](../how-it-works/shopping-surfaces.md)).

## Patterns
- **Core updates come 3–4 times a year:** 4 in 2023, 4 in 2024, 3 in 2025 and 2 in 2026 so far. There has been one in March every year.
- **Core rollouts take about 12–19 days** (median ~16). The outliers are March 2024 at 45 days and December 2024 at 6. Google usually announces "up to 2 weeks", and rollouts often run one to two weeks past that.
- **Spam updates are getting shorter and more frequent.** Before 2026 they took 7–27 days. In 2026 there have been four: three finished within 3 days, and September took 14. Since December 2024 every spam update "applies globally and to all languages".
- **Ecommerce was hit hard by the August 2026 spam update.** SE Ranking reported 85.34 % of tracked ecommerce and retail rankings affected and 16.7 % of top-ranking URLs leaving the top 100 during the rollout, vs 9.2 % in a typical period (sample not stated).[^ignite-news] How the 2026 core updates shifted visibility is in [how Google ranks](../how-it-works/google-ranking.md).
- **Updates overlap:**
  - Oct 2023: spam, core and a Discover bug at once.
  - Nov 2023: core and reviews.
  - Mar 2024: core and spam started one minute apart.
  - Aug 2024: core and an unrelated ranking bug.
  - Dec 2024 core → spam, and Mar 2026 spam → core, ran back to back.

  A loss inside these windows can't be pinned on one update from dates alone.
- **Reviews and helpful content updates are no longer posted.** Since November 2023 the reviews system "is now improved at a regular, ongoing pace" and isn't announced; the last helpful content entry is September 2023.
- **Announcements can be backdated.** The March 2023 core update was posted on 22 March with a start date of 15 March, and the February 2023 reviews update was posted after it had finished.
- **The dashboard doesn't say what an update targets.** It gives the name and expected length, plus language or country scope for some.

## How to use the dates
- **Before / after windows:** compare full weeks before the start with full weeks after the end. Leave out the rollout itself; rankings move throughout it.
- **Check when the change started.** If a slide began weeks before an update, look for site-side causes first ([diagnostic tests](../measure/diagnostic-tests.md#3-loss-by-directory)).
- **Overlapping updates:** name both in the analysis and don't attribute the change to one.
- **Weekday and seasonal effects:** keep week boundaries aligned, and compare with the same weeks of the previous year where seasonality is strong.
- Keep this table current: check the dashboard monthly and set `stale_after` again.

Related: [how Google ranking works](../how-it-works/google-ranking.md), [core-update recovery](../situations/core-update-recovery.md), [traffic drop](../situations/traffic-drop.md).

[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: GSC impression inflation (week of 2026-04-04), FAQ rich results (2026-05-07), SE Ranking on the August 2026 spam update (week of 2026-08-29); secondary reporting, primary sources not checked.
[^status]: Google Search Status Dashboard, Ranking history and incident pages (`https://status.search.google.com/incidents/<id>`), read 2026-10-27. Durations are rounded to whole days except under one day. End of the Oct 2023 spam update is logged 19 Oct 22:15 PT; its note says complete as of 20 Oct.
