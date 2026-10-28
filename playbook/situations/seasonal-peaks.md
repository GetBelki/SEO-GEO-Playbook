---
type: Playbook
title: Seasonal peaks
description: Preparing for Black Friday, Christmas and other peaks — evergreen URLs with the year in title and H1, pages kept between seasons, publishing ~6 months ahead, branded promo intents, Merchant Center promotions, measurement around peaks, update rollouts that land in peak season, and real dated refreshes for AI rerankers that favour recent pages.
tags: [seo, seasonal, black-friday, christmas, merchant-center, promotions, measurement, core-update, freshness, chatgpt]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: seasonal
    resource: "https://searchind.com/the-complete-guide-to-seasonal-e-commerce-seo/"
    title: "Searchind, The Complete Guide to Seasonal E-commerce SEO (Mar 2026)"
  - id: d2c
    resource: "https://searchind.com/the-complete-d2c-ecommerce-seo-guide-strategies-for-sustainable-growth/"
    title: "Searchind, The Complete D2C Ecommerce SEO Guide (Dec 2025)"
  - id: g-crawl-budget
    resource: "https://developers.google.com/search/docs/crawling-indexing/large-site-managing-crawl-budget"
    title: "Google Search Central, Large site owner's guide to managing crawl budget"
  - id: g-site-move
    resource: "https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes"
    title: "Google Search Central, Site moves with URL changes (updated 2026-08-20)"
  - id: brodie-loyalty
    resource: "https://brodieclark.com/loyalty-program-promotion-gmc/"
    title: "Brodie Clark, Loyalty programme and promotions in Merchant Center (2025-08-13)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: gm-intents
    resource: "https://www.growth-memo.com/p/traditional-intents-can-no-longer"
    title: "Growth Memo, Traditional intents can no longer… (2026-06-01; ~846,000 US sessions; recommendations partly paywalled)"
  - id: status
    resource: "https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history"
    title: "Google Search Status Dashboard, Ranking history (42 entries since Nov 2021) and the per-incident pages, read 2026-10-27"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: mt-config
    resource: "https://metehan.ai/blog/chatgpt-5-search-configuration/"
    title: "Metehan Yeşilyurt, ChatGPT GPT-5 search configuration files (2025-08-20; page source of one Plus session)"
  - id: mt-recency
    resource: "https://metehan.ai/blog/i-found-it-in-the-code-science-proved-it-in-the-lab-the-recency-bias-thats-reshaping-ai-search/"
    title: "Metehan Yeşilyurt, Recency bias in AI search (2025-10-03; config + Fang et al. arXiv:2509.11353, 7 LLMs)"
---

# Seasonal peaks

Use this page when planning a recurring peak — Black Friday or Black Week, Christmas, back-to-school, a sale event — and when reading its numbers afterwards.

## Rules
- **Give every seasonal page one evergreen URL with no year in the slug**; the year goes in title and H1 ([section 1](#1-one-url-that-lives-all-year)). *Practitioner.*
- **Keep seasonal pages live between seasons and update them each year** — never delete them after the campaign ([section 1](#1-one-url-that-lives-all-year)). *Practitioner; official on 404s.*
- **Publish or refresh about six months before the peak**, and plan from at least 16 months of data ([section 1](#1-one-url-that-lives-all-year)). *Practitioner.*
- **Give branded promo questions their own answer pages** — discount codes, student discounts, sale dates ([section 2](#2-branded-promo-intents-and-merchant-center)). *Practitioner.*
- **Run long-lived promotions through Merchant Center**, not only on the site ([section 2](#2-branded-promo-intents-and-merchant-center)). *Practitioner how-to.*
- **Compare peaks with the same weeks of last year, aligned by week**, after listing breaks like a paused feed ([section 3](#3-measuring-around-a-peak)). *Practitioner; field notes.*
- **Check the update calendar before reading a peak:** core updates have landed in November and December ([section 4](#4-updates-that-hit-peak-season)). *Official dates.*
- **Refresh seasonal guides with real changes and a visible updated date before the peak; never fake a date** ([section 5](#5-fresh-dates-for-ai-answers)). *From code; Measured, peer study.*

## Steps
1. **~6 months ahead:** review the last 16+ months of Search Console for seasonal queries and pages; list which seasonal pages exist, which 404 and which carry a year in the slug.
2. **Fix URLs:** move dated pages to one evergreen path with single-hop 301s; restore deleted pages that still earn impressions ([migration](migration.md)).
3. **Refresh content:** update title, H1 (with the year), dates, the factual opening and the offer; keep internal links from navigation and category pages ([category pages](../page-types/category-pages.md)). Show a visible updated date that matches the real edit ([section 5](#5-fresh-dates-for-ai-answers)).
4. **Brand intents:** check where "[brand] discount code", "[brand] Black Friday" and similar queries land; build a policy page if they land on a form ([homepage and brand](../page-types/homepage-and-brand.md)).
5. **Feeds:** set up Merchant Center promotions and sale prices; check feed links and that no feed pause is planned ([feeds and Merchant Center](../channels/feeds-and-merchant-center.md)).
6. **Before the peak:** write down every planned tracking, checkout or feed change and check the [update timeline](../reference/google-updates-timeline.md#updates).
7. **After the peak:** compare the same weeks year on year; keep the page live and note what to change next year.

## 1. One URL that lives all year
- **Evergreen slugs** (`/black-friday/`, not `/black-friday-2024/`). Keep the page between seasons and update content and metadata each year; the year goes in title and H1, where searchers use it. Publish ~6 months before the peak; analyse ≥ 16 months of data. *Practitioner.*[^seasonal]
- **Don't delete after the campaign.** In one shop a Black Week page with ~15,000 impressions in 16 months had been deleted after the campaign and returned 404.[^field-notes] A 404 is "a strong signal not to crawl that URL again".[^g-crawl-budget] Whatever history the URL had is gone next season.
- **Years in slugs force a migration every year.** The same shop had moved its dated Christmas hubs to one evergreen path with single-hop 301s, but its biggest seasonal page still carried the year in the new slug, so each year needed another URL and redirect.[^field-notes] Moves follow the official rules: map old to new, permanent redirects kept "generally at least 1 year".[^g-site-move]

## 2. Branded promo intents and Merchant Center
- **Branded intent pages.** Cover discount codes, prices and reviews with dedicated pages; a "[brand] discount code" page stating the voucher policy captures searches even for small brands. *Practitioner.*[^d2c]
- **Example.** "[brand] discount code" searches (~3,000 impressions a year, position 1–2) landed on the newsletter sign-up page; "[brand] student discount" landed on a store page.[^field-notes] The searcher wanted a policy and got a form.
- **Brand queries aren't a sure click.** With an AI Overview, 45.8 % of navigational searchers were still on the results page after 21 s (12 % without).[^gm-intents] Merchant knowledge panels show deals and loyalty benefits from Merchant Center and the business profile.[^brodie-notes]
- **Promotions in Merchant Center** can show on free listings and in the merchant knowledge panel; long-running promotions (maximum 6 months) help the store-quality promotions metric; Merchant Center data "takes precedence over structured data". *Practitioner how-to.*[^brodie-loyalty]
- **Price history.** Product results can show a typical / low / high price insight "based on the last 90 days";[^brodie-notes] a long-inflated "was" price before a sale can surface as "high".

## 3. Measuring around a peak
- **Same weeks, aligned.** Where seasonality is strong, compare with the same weeks of the previous year and keep week boundaries aligned.[^status]
- **List the breaks first.** A paused feed removes sale prices and products from Shopping and Performance Max; paid AOV and revenue in that window are no baseline.[^field-notes] See [analytics](../measure/analytics.md) and [Search Console](../measure/search-console.md) for the other breaks.
- If the peak underperforms, work through [traffic drop](traffic-drop.md) before changing the page.

## 4. Updates that hit peak season
From the dashboard's ranking history:[^status]
- **November / December:** core updates ran 2–28 Nov 2023, 11 Nov – 5 Dec 2024, 12–18 Dec 2024 (followed by a spam update 19–26 Dec 2024) and 11–29 Dec 2025; a reviews update ran 8 Nov – 7 Dec 2023.
- **March:** there has been a core update in March every year from 2023 to 2026 — relevant to spring and Easter peaks.
- Core rollouts take about 12–19 days. A peak that falls inside one can't be compared cleanly; mark the rollout on the chart and read [core update recovery](core-update-recovery.md) if the season went badly.

## 5. Fresh dates for AI answers
- ChatGPT's search config (Aug 2025) sets `use_freshness_scoring_profile: true`. *From code.*[^mt-config] In a peer study, LLM rerankers shifted their top 10 toward newer dates by +0.82 to +4.78 years from injected dates alone, with up to 95-rank jumps and 8.25–25.23 % preference reversals. *Measured, 7 LLMs.*[^mt-recency]
- **Do:** before each peak, refresh gift guides and seasonal hubs with real changes (this year's range, prices, dates) and show the updated date visibly; never change a date without changing the content ([comparison pages and guides](../page-types/comparison-and-guides.md#4-one-topic-in-depth-dated-honestly)). How assistants weigh freshness: [AI assistants](../how-it-works/ai-assistants.md#8-assistants-cite-fresher-content-than-search).

Related: [page types: comparison and guides](../page-types/comparison-and-guides.md), [Google updates timeline](../reference/google-updates-timeline.md).

[^seasonal]: Searchind, seasonal SEO, read 2026-10-27: evergreen URLs, keep pages between seasons, ~6 months ahead, ≥ 16 months of data.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^g-crawl-budget]: Google, crawl budget guide, read 2026-10-27.
[^g-site-move]: Google, site moves with URL changes, read 2026-10-27.
[^d2c]: Searchind, D2C guide, read 2026-10-27: branded intent pages incl. discount codes; brand / non-brand split.
[^gm-intents]: Growth Memo, 2026-06-01: share still active at 21 s by intent with and without AIO; schema recommendations are opinion, no test shown.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^brodie-loyalty]: Brodie Clark, 2025-08-13: promotions add-on, 6-month maximum, promotions rejection rate, loyalty markets, Merchant Center over structured data, no organic loyalty reporting.
[^status]: Google Search Status Dashboard, Ranking history and incident pages (`https://status.search.google.com/incidents/<id>`), read 2026-10-27. Durations are rounded to whole days except under one day. End of the Oct 2023 spam update is logged 19 Oct 22:15 PT; its note says complete as of 20 Oct.
[^mt-config]: Metehan Yeşilyurt, 2025-08-20: ChatGPT search configuration from the page source of one Plus session; may be stale. Author works at Peec AI.
[^mt-recency]: Metehan Yeşilyurt, 2025-10-03, citing Fang et al. (arXiv:2509.11353): 7 LLM rerankers, injected dates shift top-10 by +0.82 to +4.78 years, up to 95-rank jumps, 8.25–25.23 % preference reversals.
