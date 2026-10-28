---
type: Guide
title: Google Discover
description: Discover as a bonus channel for a shop's editorial and guide content, never a baseline — what it rewards (large images, strong headlines), its volatility and losses during core updates, the February 2026 Discover core update, why hreflang doesn't apply, and tracking it separately in Search Console.
tags: [seo, google, discover, editorial, guides, core-updates, images, headlines, international]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: gn-survival
    resource: "https://www.seoforgooglenews.com/p/ai-survival-strategies-for-publishers"
    title: "Barry Adams, AI survival strategies for publishers (2025-10-08; client experience)"
  - id: gn-loyalty
    resource: "https://www.seoforgooglenews.com/p/google-audience-loyalty-ecosystem"
    title: "Barry Adams, Google's audience loyalty ecosystem (2026-06-10; Google announcements)"
  - id: gn-article
    resource: "https://www.seoforgooglenews.com/p/perfectly-optimised-news-article-for-seo"
    title: "Barry Adams, The 'perfectly optimised' article (2025-02-10; practitioner)"
  - id: gg-may2026
    resource: "https://www.gsqi.com/marketing-blog/core-roars-back-google-may-2026-core-update-analysis/"
    title: "Glenn Gabe, May 2026 core update analysis (2026-06-10; cases)"
  - id: gg-dec2025
    resource: "https://www.gsqi.com/marketing-blog/google-december-2025-broad-core-update-analysis-findings/"
    title: "Glenn Gabe, December 2025 core update (2026-01-07; 3,000+ tracked sites, qualitative)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
---

# Google Discover

This page answers whether and how a shop should work on Google Discover, the personalised feed that shows content without a search.

**In short.** Discover sends large but volatile traffic to editorial content, and publishers rely on it more as search clicks shrink. For a shop it is a bonus for the magazine, guide and inspiration section, never a baseline to plan revenue on. Confidence labels follow the [scale](../reference/sources-and-confidence.md).

## Rules

- Treat Discover as a bonus channel for editorial and guide content, never as a baseline in forecasts or targets. *Practitioner* [why](#1-a-bonus-channel-not-a-baseline)
- Give every guide or magazine piece a large, relevant lead image, with people where relevant. *Practitioner* [why](#2-what-gets-content-picked)
- Put the weight of the on-page headline in its first 8 words and follow the H1 with a one-sentence summary. *Practitioner* [why](#2-what-gets-content-picked)
- Don't bend guide content into clickbait to chase Discover; the traffic stays volatile even when it works. *Practitioner, opinion* [why](#1-a-bonus-channel-not-a-baseline)
- Wait for a core update to finish rolling out before judging Discover losses, and check Discover separately from Search. *Practitioner, cases* [why](#3-core-updates-hit-discover-too)
- Don't rely on hreflang to steer Discover by country or language; it has no effect there. *Practitioner, relayed* [why](#4-hreflang-has-no-effect-on-discover)
- Track Discover in Search Console's Discover report, separately from Search performance. *Practitioner* [why](#5-measure-it-separately)

## 1. A bonus channel, not a baseline
- **Large, growing and volatile.** For many publishers Discover has become a "huge source of traffic" that offsets search losses, but it is volatile and tends to reward clickbait; optimise for it "to some degree", never treat it as a baseline. *Practitioner, client experience.*[^gn-survival]
- **The feed is widening.** Google is adding social content to Discover (YouTube, Instagram, X posts), rolling it out to desktop Chrome, and letting users follow sources; Search Profiles with 100K+ followers are more likely to appear. *Google announcements, relayed.*[^gn-loyalty] More formats compete for the same slots.
- **Preferred Sources.** Users can mark preferred sources; since May 2026 this also influences AI Overviews and AI Mode, mostly for timely editorial content ([Google ranking](../how-it-works/google-ranking.md#9-spam-handling-brand-size-and-preferred-sources)).
- **For a shop.** Discover traffic lands on editorial and guide pages, rarely on product or category pages (*inference* from what Discover shows). Plan revenue on search, feeds and direct; count Discover as upside ([comparison pages and guides](../page-types/comparison-and-guides.md)).

## 2. What gets content picked
- **Images.** Use large lead images and show people where relevant. *Practitioner.*[^gn-article]
- **Headlines.** In an editorial headline the first 8 words carry most weight; the on-page article headline can run up to 110 characters (this is the visible headline, not the `<title>`, which follows [titles and snippets](../technical/titles-and-snippets.md)). Put a summary sentence right after the H1, use question subheads, and link consistently to topic hubs. *Practitioner.*[^gn-article]
- **Do:** apply these to the shop's guides, buying advice and inspiration pieces, not to product pages.

## 3. Core updates hit Discover too
- **Losses come in tremors.** The May 2026 core update was visible about 48 hours in, with "tremors" during the rollout; some sites lost Discover traffic at the final tremor. The December 2025 update had a tremor on 20 December. *Practitioner, cases.*[^gg-may2026][^gg-dec2025]
- **Google says the systems barely overlap; cases say otherwise.** Google describes Discover as having "minimal overlap with Search ranking", yet many sites were hit in both Search and Discover in the same updates. *Official statement vs practitioner cases.*[^gg-may2026][^gg-dec2025]

  > **Conflict:** Google says Discover has minimal overlap with Search ranking, while case studies show sites hit in both — [details](../reference/conflicts.md#does-discover-follow-search-rankings)
- **Discover has its own core updates.** The February 2026 Discover core update (5–27 February) applied to US English only; see the [Google updates timeline](../reference/google-updates-timeline.md). Outside that market, a February 2026 Discover drop needs another explanation.
- **Do:** don't judge before the rollout ends; compare Discover and Search for the same pages; include intrusive ads and pop-ups in quality checks, since sites with aggressive ad formats (content-blocking video pop-ups) lost in these updates[^gg-may2026][^gg-dec2025] ([core-update recovery](../situations/core-update-recovery.md)).

## 4. Hreflang has no effect on Discover
- One speaker stated that hreflang has no effect on Discover; choose the domain structure for a market by what that market's results already show (one publisher launched a German ccTLD because most of the German results were already on such domains). *Practitioner, relayed (Max Prin, conference talk).*[^lr-techseo] Market setup in general: [new market](../situations/new-market.md).

  > **Conflict:** practitioners disagree on ccTLDs vs subfolders for new markets, and Google's docs are neutral — [details](../reference/conflicts.md#cctld-or-subfolder-for-a-new-market)

## 5. Measure it separately
- Search Console reports Discover in its own performance report, separate from Search. Track it there for magazine and guide content, and keep it out of organic-search trend lines so its swings don't hide or fake a search change. *Practitioner.*[^gn-survival] How to read Search Console in general: [Search Console](../measure/search-console.md).

Related: [Google ranking](../how-it-works/google-ranking.md), [comparison pages and guides](../page-types/comparison-and-guides.md), [core-update recovery](../situations/core-update-recovery.md), [Google updates timeline](../reference/google-updates-timeline.md), [Search Console](../measure/search-console.md).

[^gn-survival]: Barry Adams, 2025-10-08: publisher client experience — Discover a "huge source of traffic" for many publishers, volatile, rewards clickbait; optimise "to some degree", never a baseline; track Discover separately.
[^gn-loyalty]: Barry Adams, 2026-06-10: relays Google announcements — social content in Discover (YouTube, Instagram, X), desktop Chrome rollout, following sources, Search Profiles (100K+ followers more likely to appear), Preferred Sources.
[^gn-article]: Barry Adams, 2025-02-10: practitioner checklist for news articles — first 8 words of the headline, up to 110 characters for the article headline, summary after the H1, question subheads, topic-hub links, large images with people.
[^gg-may2026]: Glenn Gabe, 2026-06-10: May 2026 core update cases — visible ~48 h in, mid-rollout tremors, Discover losses at the final tremor, sites hit in Search and Discover; Google's "minimal overlap with Search ranking" statement quoted; aggressive ad formats among losers.
[^gg-dec2025]: Glenn Gabe, 2026-01-07: December 2025 core update, 3,000+ tracked sites, qualitative; tremor on 20 December.
[^lr-techseo]: Lily Ray, 2025-12-05, Tech SEO Connect 2025 summaries: Max Prin — hreflang has no effect on Discover; domain choice by what the market's results show (one publisher's German ccTLD, "78% of the German SERP was already .de").
