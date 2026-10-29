---
type: Playbook
title: Organic traffic drop
description: A decision flow for a fall in organic or AI-referred traffic — rule out measurement breaks, date it against Google updates, split by device, country, brand and query type, then test directories, lost queries, satisfaction, indexing, AI Overview launches per market, AI referral shifts by page type, platform-side citation shifts such as ChatGPT dropping Reddit, structural surface changes, branded CTR lost to a missing favicon, country-section losses from cross-country canonicalisation, paid CTR falling too, skewed industry decline figures, mid-rollout tremors and security tools serving 4xx to bots — and don't disavow tool-flagged links.
tags: [seo, traffic-drop, diagnosis, search-console, ga4, core-update, measurement, ai-overviews, links, chatgpt, reddit, favicon, hreflang, canonicals, paid-search, server-logs]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: brodie-num100
    resource: "https://brodieclark.com/the-great-decoupling-num100/"
    title: "Brodie Clark, The Great Decoupling and num=100 (updated 2025-09-26; cites LOCOMOTIVE, ThotSEO, JetOctopus samples)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings, Jun 2025 – Oct 2026; month anchors)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays Google confirmations and third-party studies)"
  - id: gm-direct
    resource: "https://www.growth-memo.com/p/does-ai-drive-more-direct-traffic"
    title: "Growth Memo, Does AI drive more direct traffic (2026-10-19; 12 GA4 properties)"
  - id: gm-organic
    resource: "https://www.growth-memo.com/p/organic-traffic-is-down-but-its-not"
    title: "Growth Memo, Organic traffic is down, but it's not… (2026-10-26; Similarweb, 10,000 domains per country)"
  - id: aleyda-ads
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/serp-shifts-ads-remonetized/"
    title: "Aleyda Solis, SERP shifts: search is being re-monetised (~Feb 2026; 4 US verticals, Jan 2025 vs Jan 2026; search extracts)"
  - id: thrive-traffic
    resource: "https://thriveagency.com/news/notice-your-website-traffic-is-declining-lately/"
    title: "Thrive, Website traffic declining (2025-09-08; relays Authoritas, Dec 2024, 10,000 US keywords)"
  - id: ipr-zero-click
    resource: "https://ipullrank.com/zero-click-behavior-analysis-q3-2026"
    title: "iPullRank (Cate Dombrowski), Zero-click behavior analysis (2026-07-30; Datos, 13.1 billion searches, Oct 2024 – Dec 2025)"
  - id: ipr-generative
    resource: "https://ipullrank.com/generative-serps"
    title: "iPullRank, Generative SERPs (2026-10-15; Nozzle, 27.5M results, 2026-08-20 – 2026-10-09)"
  - id: eea
    resource: "https://searchind.com/googles-eea-search-changes-are-reshaping-product-visibility/"
    title: "Searchind, Google's EEA Search Changes (Sep 2026)"
  - id: status
    resource: "https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history"
    title: "Google Search Status Dashboard, Ranking history (42 entries since Nov 2021) and the per-incident pages, read 2026-10-27"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6: how Google Search works (Oct 2024)"
  - id: qus
    resource: "https://www.resoneo.com/qus-query-expansion-google-and-mysterious-scoring/"
    title: "Resoneo, QUS query expansion and term scoring (Jul 2025; few US examples)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026; trial testimony, 2024 leak, author's schema compilation)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: mh-cni
    resource: "https://www.mariehaynes.com/crawled-currently-not-indexed/"
    title: "Marie Haynes, Crawled – currently not indexed (2026-07-16) and migration issues may be site quality (2026-10-13)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: ah-aio-france
    resource: "https://ahrefs.com/blog/ai-overviews-france-impact/"
    title: "Ahrefs, AI Overviews launch in France (2026-09-16; 963 domains, control group)"
  - id: ah-toxic
    resource: "https://ahrefs.com/blog/toxic-backlinks/"
    title: "Ahrefs, Toxic backlinks (2024-02-28; Google statements, poll, anecdotes)"
  - id: bp-chatgpt-links
    resource: "https://botpresso.com/chatgpt-may-links-update-traffic-impact-study/"
    title: "Botpresso, ChatGPT May links update traffic study (≈2026-07; 52 client sites, GA4)"
  - id: nz-aimeas
    resource: "https://natzir.com/en/analytics/ai-traffic-measurability/"
    title: "Natzir Turrado, The state of AI traffic measurability (2026-05-17, updated to 2026-10; server logs vs GA4 on several sites)"
  - id: mt-sitequeries
    resource: "https://metehan.ai/blog/reddit-lost-most-its-visibility-chatgpt-site-filled-gap/"
    title: "Metehan Yeşilyurt, Reddit lost its ChatGPT visibility and the site parameter filled the gap (2026-08-21; Peec logs, 14.9M queries/week)"
  - id: brief-distinct
    resource: "https://seobrief.substack.com/p/when-the-logo-comes-off-is-it-still"
    title: "Jes Scholz, SEO Brief: distinctiveness (2026-06-18; essay + one client case)"
  - id: gg-canonical
    resource: "https://www.gsqi.com/marketing-blog/rel-canonical-hint-cascade-chatgpt/"
    title: "Glenn Gabe, Rel canonical is just a hint — cascade to ChatGPT (2026-02-17; 3 client cases)"
  - id: seer-zero-click-paid
    resource: "https://www.seerinteractive.com/insights/zero-click-search-paid-strategy"
    title: "Seer Interactive, The case of the missing click (2026-07-14; client portfolio, 6 verticals, Dec 2025 – May 2026)"
  - id: gn-zero
    resource: "https://www.seoforgooglenews.com/p/google-zero-is-a-lie"
    title: "Barry Adams, SEO for Google News: Google Zero is a lie (2026-03-02; relays Similarweb/Graphite, Chartbeat)"
  - id: gg-may2026
    resource: "https://www.gsqi.com/marketing-blog/core-roars-back-google-may-2026-core-update-analysis/"
    title: "Glenn Gabe, May 2026 core update analysis (2026-06-10; cases)"
  - id: gg-dec2025
    resource: "https://www.gsqi.com/marketing-blog/google-december-2025-broad-core-update-analysis-findings/"
    title: "Glenn Gabe, December 2025 core update (2026-01-07; 3,000+ tracked sites, qualitative)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: sp-zero-click-2026
    resource: "https://sparktoro.com/blog/in-2026-less-than-one-third-of-google-searches-still-send-a-click/"
    title: "SparkToro, In 2026, less than one third of Google searches still send a click (2026-06-09; Similarweb US web panel, Jan–Apr 2026)"
  - id: mlseo-content-audit
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/content-audit/content-audit-template/"
    title: "ML for SEO, Content audit template (2026-10-24; rules plus synthetic 24-URL site)"
---

# Organic traffic drop

Use this page when organic clicks, organic sessions or AI-referred sessions fall and someone asks why. Work the steps in order: most "drops" we investigated were measurement breaks, and the cheap checks rule out the expensive theories.[^field-notes]

## Rules
- **Rule out measurement breaks before anything else** — including a country section whose clicks Google credits to another country's canonical; a drop that crosses a known break isn't a drop until it survives a control ([step 1](#1-is-it-a-measurement-break)). *Practitioner, confirmed in field notes; canonical cases relayed.*
- **Use Search Console clicks, not impressions or average position,** for anything that crosses 10 Sep 2025 ([step 1](#1-is-it-a-measurement-break)). *Measured, third-party samples.*
- **Don't blame an update for a slide that began before its start date, and don't judge one before its rollout ends** — mid-rollout tremors still move rankings; overlapping updates can't be separated by dates alone ([step 2](#2-did-it-start-before-or-after-an-update)). *Official dates; reading is practitioner.*
- **Split by device, country and brand / non-brand before naming a cause**; zero-click, AI Overviews and outside changes all hit segments unevenly. If branded CTR falls while impressions and position hold, check favicon and site-name display first ([step 3](#3-segment-then-name-the-surface)). *Measured*; favicon *one case.*
- **Split the click loss by query type before blaming AI Overviews**; text ads were the larger driver in one four-vertical study. Check whether paid CTR fell too, and whether an industry decline figure is skewed by a few big sites ([step 3](#3-segment-then-name-the-surface)). *Measured, method partly visible; agency portfolio; relayed.*
- **Look for whole directories moving together** — that points at section-level quality, not single pages ([step 4](#4-site-side-causes)). *From the leak.*
- **Test lost queries for the exact term before renaming anything** ([step 4](#4-site-side-causes)). *Observed output, few examples; field notes.*
- **If clicks fall in one market while impressions and positions hold, check whether AI Overviews just launched there** and compute your exposure rate ([step 3](#3-segment-then-name-the-surface)). *Measured, vendor data.*
- **Split AI referrals by landing-page type** before calling a page type's loss a drop; ChatGPT shifted referrals toward homepages from 7 May 2026 ([step 3](#3-segment-then-name-the-surface)). *Measured, observational.*
- **Don't disavow links an SEO tool calls "toxic"**; look at anchor patterns only when there is a manual action ([step 4](#4-site-side-causes)). *Official statements, relayed.*
- **Check platform-side citation shifts before blaming the site for an AI-referral drop** — ChatGPT's Reddit citations fell about 95 % in August 2026 — and check server logs for 4xx your own security tools serve to Googlebot and AI bots ([step 3](#3-segment-then-name-the-surface), [step 4](#4-site-side-causes)). *Measured, vendor log data; practitioner talk, relayed.*

## Steps
1. **Measurement break?** List every break between the two periods: own tracking bugs, Search Console num=100 and impression inflation, untagged AI referrals, bots in Direct, platform bugs, paused feeds, redirects that drop click IDs, clicks credited to another country's canonical. Check [Search Console](../measure/search-console.md), [analytics](../measure/analytics.md) and [rank tracking](../measure/rank-tracking.md) pitfalls; for Direct, run [test 10](../measure/diagnostic-tests.md#10-is-a-direct-spike-real).
2. **Before or after an update?** Plot weekly clicks against the [update dates](../reference/google-updates-timeline.md#updates); compare full weeks before the start with full weeks after the end ([how to use the dates](../reference/google-updates-timeline.md#how-to-use-the-dates)). If it overlaps another update, name both. If the rollout hasn't ended, wait. If it began earlier, go to step 4 first.
3. **Segment:** device, country ([test 6](../measure/diagnostic-tests.md#6-country-or-segment-control)), brand / non-brand; for AI referrals, landing-page type (homepage, category, product, editorial).
4. **Query type:** informational vs commercial vs navigational; check whether AI Overviews, text ads or product-grid ads appeared on the lost queries, and whether AI Overviews launched in that market during the window.
   > **Conflict:** AI Overviews vs text ads as the main cause of falling organic CTR — [details](../reference/conflicts.md#why-is-organic-ctr-falling)
5. **Directories or single pages?** Run [test 3](../measure/diagnostic-tests.md#3-loss-by-directory).
6. **Lost queries:** run the [exact-term gap test](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries); if the phrase is present, look for a competitor gain or a results-page change.
7. **Satisfaction per page type:** run [test 2](../measure/diagnostic-tests.md#2-satisfaction-per-page-type).
8. **Indexing:** run [test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type); if one URL pattern fell out after a release, run [test 17](../measure/diagnostic-tests.md#17-daily-index-status-per-url). Check status codes per bot in server logs ([step 4](#4-site-side-causes)).
9. **Structural surface changes:** EEA free listings, ads in formerly organic units, new AI-surface layouts ([feeds and Merchant Center](../channels/feeds-and-merchant-center.md)).

| Symptom | Likely cause | Test / page |
|---|---|---|
| Impressions fell from ~10 Sep 2025, clicks flat, position "improved" | num=100 change | [Search Console](../measure/search-console.md) |
| Direct up, organic or AI referral down, near-zero engagement | Bots, or untagged AI links after a model release | [test 10](../measure/diagnostic-tests.md#10-is-a-direct-spike-real), [analytics](../measure/analytics.md) |
| Sessions or views jump on one day, purchases flat | Tracking bug or fix | [analytics](../measure/analytics.md) |
| Rank tracker drops, Search Console holds | Degraded tracker captures | [rank tracking](../measure/rank-tracking.md) |
| Slide starts inside a rollout | Core or spam update | [core update recovery](core-update-recovery.md) |
| Whole directory down | Section-level quality | [test 3](../measure/diagnostic-tests.md#3-loss-by-directory) |
| A few queries lost, phrase missing on page | Lexical gap | [test 1](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries) |
| Indexed count of one page type falling | Indexing as quality | [test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type) |
| Merchant-listing clicks down in EEA only | EEA free-listings removal | [test 6](../measure/diagnostic-tests.md#6-country-or-segment-control) |
| CTR down on question queries | AI Overviews or zero-click | [Google AI features](../how-it-works/google-ai-features.md) |
| Clicks and CTR down in one market, impressions and positions flat | AI Overviews launched in that market | [step 3](#3-segment-then-name-the-surface), [new market](new-market.md#5-measure-per-country) |
| ChatGPT referrals to product or blog pages down, homepage up (from 7 May 2026) | ChatGPT link change, not a site problem | [step 3](#3-segment-then-name-the-surface), [AI visibility tracking](../measure/ai-visibility-tracking.md) |
| One URL pattern lost clicks right after a release | Bulk redirect or template change; check per-URL index status | [test 17](../measure/diagnostic-tests.md#17-daily-index-status-per-url), [migration](migration.md#5-monitoring-after-launch) |
| A tool flags "toxic" backlinks after the drop | Not a cause without a manual action | [step 4](#4-site-side-causes), [links and digital PR](../channels/links-and-digital-pr.md) |
| Impressions high from May 2025, step down around April 2026, clicks flat | End of the Search Console impression-inflation bug | [step 1](#1-is-it-a-measurement-break), [Search Console](../measure/search-console.md) |
| ChatGPT referrals down 7–16 Oct 2026, Direct up | ChatGPT UTM bug, not lost visibility | [step 1](#1-is-it-a-measurement-break), [AI visibility tracking](../measure/ai-visibility-tracking.md) |
| ChatGPT visibility via Reddit or forum threads gone from August 2026 | ChatGPT cut Reddit citations; Google AI surfaces not affected the same way | [step 3](#3-segment-then-name-the-surface), [third-party presence](../channels/third-party-presence.md#7-forums-and-discussions) |
| Branded clicks and CTR down, branded impressions and position flat | Favicon or site name missing or wrong in results | [step 3](#3-segment-then-name-the-surface), [homepage and brand](../page-types/homepage-and-brand.md) |
| One country's directory property loses clicks, another country's gains; same language in both | Google canonicalised to the other country's URL; clicks credited there | [step 1](#1-is-it-a-measurement-break), [new market](new-market.md) |
| Organic and paid nonbrand CTR both falling, impressions up, Direct up | Zero-click across the results page, not an SEO problem alone | [step 3](#3-segment-then-name-the-surface) |
| An industry report shows a large search-traffic decline | Aggregate skewed by a few big sites or a one-off comparison year | [step 3](#3-segment-then-name-the-surface) |
| Rankings swing mid-rollout, then again near its end | Update tremors; wait for the rollout to end | [step 2](#2-did-it-start-before-or-after-an-update), [core update recovery](core-update-recovery.md) |
| Googlebot and AI-bot fetches fall, Search Console Crawl Stats look normal | Security tool or WAF serving 4xx to bots | [step 4](#4-site-side-causes), [AI crawlers and controls](../technical/ai-crawlers-and-controls.md) |

## 1. Is it a measurement break?
- **num=100.** Search Console impressions fell from about 10 Sep 2025, mostly on desktop, and average position improved without a real ranking change; 87.7 % of 319 properties saw a drop.[^brodie-num100] Use 13 Sep 2025 as the first clean day.
- **Impression inflation** from 13 May 2025 until April 2026, from a bug Google acknowledged; clicks unaffected.[^ignite-news][^nz-aimeas] Annotate the whole period; impressions across its end aren't comparable.
- **Untagged AI.** After the GPT-6 rollout (from ~9 Oct 2026) reported ChatGPT traffic fell 22–57 % across datasets while Direct rose; a fix began on 15 Oct. A GA4 bug zeroed traffic on 1 Sep 2026.[^ignite-news] Server logs date the ChatGPT UTM bug 7–16 Oct 2026: ChatGPT-attributed visits fell 68–74 % in logs and 20–60 % in GA4. Even outside such bugs, 96–99 % of ChatGPT citation clicks arrive without a referrer and rely on `utm_source=chatgpt.com`. *Measured, server logs vs GA4, several sites.*[^nz-aimeas] Read AI referrals with logs ([analytics](../measure/analytics.md), [AI visibility tracking](../measure/ai-visibility-tracking.md)).
- **Bots in Direct.** One site had 409,000 Direct sessions with 198 engaged; AI-traced sessions were 0.003 % of Direct.[^gm-direct]
- **Own breaks.** A session bug inflated sessions by 20–37 % for a month; a paused feed made paid revenue in that window no baseline.[^field-notes]
- **Trackers.** One vendor's anomalous captures rose from 0.17 % to 8.0 % of results pages after 13 Sep 2026.[^ipr-generative]
- **Clicks credited to another country.** With same-language hreflang across two countries, Google canonicalised millions of URLs to the other country's version while still showing the right country's URL; Search Console credits clicks to the canonical, so one country's directory property showed a loss that wasn't real. *Practitioner case; Google confirmation relayed.*[^gg-canonical] **Do:** filter Search Console by country, not only by directory property ([Search Console](../measure/search-console.md), [new market](new-market.md)).

## 2. Did it start before or after an update?
Core rollouts take about 12–19 days; several overlapped (March 2024 core and spam started one minute apart).[^status] A change that starts before an update's start date wasn't caused by it. For update losses, see [core update recovery](core-update-recovery.md).

**Don't judge mid-rollout.** The May 2026 core update was visible about 48 hours in, with "tremors" during the rollout, and some sites lost Discover only at the final tremor; the December 2025 update had a tremor on 20 December. *Practitioner, cases.*[^gg-may2026][^gg-dec2025] Read the result only after the rollout has ended.

## 3. Segment, then name the surface
- **Device.** 46.96 % of searches ended without a click (desktop-heavy); US mobile reached 66 %.[^ipr-zero-click]
- **Query type and brand.** In 10,000 US keywords (Dec 2024), AI Overviews showed on 74 % of problem-solving queries, 69 % of explicit questions, 33 % non-brand vs 19.6 % brand.[^thrive-traffic]
- **Ads.** For headphones, text ads went from 3 % to 16 % of clicks between January 2025 and January 2026; text ads were the largest measurable driver of the organic decline in that data.[^aleyda-ads] Ads also moved into formerly organic product grids.[^brodie-notes]
- **Benchmark.** Modelled US organic visits fell 13.2 % from Aug 2024 to Aug 2026, unevenly; compare with comparable sites, not country averages.[^gm-organic] SparkToro (which sells audience research) put US zero-click at 68.01 % of Google web searches in Jan–Apr 2026 (Similarweb panel, Google app excluded, so likely higher) and relays an Ahrefs tracker in which Google's share of site traffic fell 8 points (~22 % relative) from June 2025 to May 2026, on a sample skewed to professionally marketed sites. *Measured, vendor data; relayed.*[^sp-zero-click-2026] Rates by country: [new market](new-market.md#9-zero-click-differs-by-country).
- **Read industry decline figures critically.** Similarweb/Graphite data put the decline in Google traffic to top global sites at "two and a half percent", with Google still "nearly 20%" of all web visits; Chartbeat's "33%" decline was an aggregate skewed by a few big sites and by a year-over-year comparison against the 2024 US election (Jan–Nov year to date about −15 %). *Relayed, publisher context.*[^gn-zero] **Do:** before quoting an industry figure as context for your drop, check whether a few large domains or a one-off event drive it.
- **Branded CTR.** When branded clicks fall while branded impressions and position stay flat, check the favicon and site-name display first: in one case a developer had removed the favicon by accident, and the fix took minutes. *One case.*[^brief-distinct] Display checklist: [homepage and brand](../page-types/homepage-and-brand.md).
- **Paid CTR falls too.** Across one agency's client portfolio (6 verticals, mostly B2B/lead-gen), nonbrand paid CTR fell from 16.39 % to 14.13 % while impressions rose 28 % (Dec 2025 → May 2026); organic sessions fell 32.3 %, Direct rose 53.6 % and overtook organic in Nov 2025, and organic conversion rate rose 133 %; informational queries had the lowest paid CTR in all 6 verticals. *Measured, agency portfolio, mostly B2B.*[^seer-zero-click-paid] **Do:** if paid CTR is falling on the same queries, the click loss is page-wide; track branded impressions plus Direct as a zero-click health check, and use geo holdouts to test changes.
- **EEA.** Free product listings disappeared mid-Sep 2026; one shop lost 67 % of merchant-listing clicks in Germany while Switzerland held.[^eea][^field-notes]
- **AI Overview launch in a market.** After AI Overviews launched in France (2026-07-22), highly exposed domains (> 20 % AI Overview rate) saw median CTR fall from 2.29 % to 1.76 % (−23.1 % raw, −24.8 % control-adjusted); the whole panel of 963 domains lost 5.7 % median CTR and 8.8 % clicks, about −0.9 CTR points per point of exposure. *Measured, vendor data.*[^ah-aio-france] **Do:** when clicks fall but impressions and positions hold, check whether AI Overviews launched in that market and compute the share of your queries that show one.
- **AI referrals by page type.** From 7 May 2026 ChatGPT changed how it links (unannounced): across 52 sites, ChatGPT sessions rose from 183,497 to 363,089 (+97.9 %, median site +54 %), but the gain was concentrated (top site 64 % of net gain, top 5 91 %, the other 47 sites +10 % combined). Homepages rose 1,316 % (7,990 → 113,183; share 4.4 % → 31.2 %); landing pages +60 % but share 71 % → 57 %; blogs −28 %; 16 of the 17 sites that lost product-page traffic gained homepage traffic. *Measured, observational, GA4.*[^bp-chatgpt-links] A product-page "drop" in AI referrals across that date may be a shift to the homepage; split by page type before diagnosing, and keep bestsellers and category entry points above the fold on the homepage ([homepage and brand](../page-types/homepage-and-brand.md)).
- **Platform-side citation shifts.** Reddit's share of ChatGPT citations fell from ~4.6 % to 0.23 % between early August and 21 Aug 2026 (−95 %), in steps on 8 and 14 August, while Google's AI surfaces were not affected the same way. *Measured, vendor log data (author works at an AI-visibility vendor), not reproducible outside it.*[^mt-sitequeries] If your AI visibility leaned on forum threads, a drop from that date is the platform, not your site; shift ChatGPT-facing work toward review platforms and your own pages, and recheck monthly ([third-party presence](../channels/third-party-presence.md)).

## 4. Site-side causes
- **Directories.** The leak names section-level quality scores; new pages inherit the section's average.[^leak-6] Blocks moving together fit that; scattered losses point at pages or queries.
- **Exact terms.** A term in the title adds ~3.5 to its score on average; numbers score 0.[^qus] In one shop, 6 of 7 lost queries already had their phrase; the one without it dropped hardest.[^field-notes]
- **Satisfaction.** NavBoost remembers short visits per query and page, by device; compare within page type.[^navboost] One category set that lost clicks bounced less than its type (12.5 % vs 20.8 %) — the loss wasn't dissatisfaction.[^field-notes]
- **Indexing.** From 27 May 2025 Google dropped low-engagement pages from the index on ~40 reviewed sites; clicks mostly didn't fall.[^mh-deindex] "Crawled – currently not indexed" usually means quality; rule out blocked CSS/JS first.[^mh-cni]
- **Decay or drop?** A practitioner audit rule calls a page decaying when its clicks fall 30 % or more between two consecutive 3-month periods (pages with at least 20 clicks before); a two-period comparison can't see slow declines or separate seasonality. *Practitioner.*[^mlseo-content-audit] (ML for SEO sells courses.) Pages that decay one by one point at content; whole directories at the section ([scaling content and templates](scaling-content-and-templates.md#11-content-audit-rules)).
- **Bots blocked by your own security tools.** A first-party log dashboard found a security tool returning HTTP 406 to Googlebot and every AI bot; Search Console Crawl Stats didn't show it (unreliable for large domains). *Practitioner talk (Rachel Anderson), relayed.*[^lr-techseo] **Do:** report status codes per bot from server logs and alert on any 4xx served to verified bots ([AI crawlers and controls](../technical/ai-crawlers-and-controls.md), [diagnostic tests](../measure/diagnostic-tests.md)).
- **Links: don't disavow by tool score.** Google has "no notion" of toxic links (Mueller); disavow only with "a considerable number of spammy, artificial, or low-quality links" that caused or will likely cause a manual action. Illyes found no case where negative SEO really caused a drop. In a poll 38 % of SEOs still disavow; anecdotes include one site −60 % after a tool-driven disavow and a test disavow whose dip reversed. *Google statements relayed by a vendor; poll and anecdotes.*[^ah-toxic] **Do:** check Search Console's Manual actions report; only if there is one, look for exact-match anchor patterns ([links and digital PR](../channels/links-and-digital-pr.md), [spam policies](../technical/technical-foundations.md#11-links-and-spam-policies)).

Related: [core update recovery](core-update-recovery.md), [Google ranking](../how-it-works/google-ranking.md), [diagnostic tests](../measure/diagnostic-tests.md), [conflicts](../reference/conflicts.md).

[^brodie-num100]: Brodie Clark, updated 2025-09-26, and notes #sep-2025: impressions down from 10 Sep, desktop-heavy; Google quote; third-party samples (LOCOMOTIVE 319 sites, ThotSEO 1,334, JetOctopus 1,000); bot-impression reading is his inference. Marie Haynes dates the change "around September 11".
[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: GSC impression inflation (week of 2026-04-04), GA4 AI Assistant channel (2026-05-09), GA4 bug (2026-08-29), GPT-6 referral loss with Adobe data (2026-10-10), Comscore, Seer and the field experiment on AIO clicks (2026-04-25), SparkToro zero-click; secondary reporting, primary sources not checked.
[^gm-direct]: Growth Memo, 2026-10-19: 12 GA4 properties (B2B-skewed), 4 brands, 632 correlation tests.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^ipr-generative]: iPullRank, 2026-10-15: Nozzle measurement; "poisoned" is the vendor's term; scraper degradation is King's inference.
[^status]: Google Search Status Dashboard, Ranking history and incident pages (`https://status.search.google.com/incidents/<id>`), read 2026-10-27. Durations are rounded to whole days except under one day. End of the Oct 2023 spam update is logged 19 Oct 22:15 PT; its note says complete as of 20 Oct.
[^ipr-zero-click]: iPullRank (Dombrowski), 2026-07-30: Datos clickstream; ad clicks unchanged.
[^thrive-traffic]: Thrive, 2025-09-08, relaying Authoritas (Dec 2024, 10,000 US keywords, 7 industries); dated.
[^aleyda-ads]: Aleyda Solis, ~Feb 2026, via search extracts: four US verticals (headphones, jeans, greeting cards, online games), top queries, Jan 2025 vs Jan 2026; AIO figures there measure presence, not clicks.
[^brodie-notes]: Brodie Clark notes, Apr – Sep 2026: ads in product grids, citation-UI changes.
[^gm-organic]: Growth Memo, 2026-10-26: Similarweb modelled visits; AI referrals 2.85 % of SEO traffic in the US.
[^eea]: Searchind, EEA changes, read 2026-10-27.
[^leak-6]: Resoneo, leak part 6, 2024-10-31: index tiers, crawl skipping, siteFocusScore/siteRadius, new pages inherit the sitechunk average.
[^qus]: Resoneo, QUS, 2025-07-22: per-term scores 0–~10, title +3.5, numbers 0, exact vs derived match.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: click-signal families, 13-month history per query and page by country and device, Glue for SERP blocks, compare short visits per page type. No measured ranking effects shown.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^mh-cni]: Marie Haynes, 2026-07-16 and 2026-10-13: Search Central Toronto quote, Search Console help text, robots.txt CSS/JS case, one migration case.
[^ah-aio-france]: Ahrefs, 2026-09-16: France AI Overviews launch 2026-07-22; 963 top-click French domains; 28 days before vs 9 after; control group of domains with < 2 % AI Overview rate; vendor data, short post-window.
[^ah-toxic]: Ahrefs, toxic backlinks, 2024-02-28: relays Mueller and Illyes statements and Google's disavow criterion; a poll of SEOs; anecdotes; vendor content.
[^bp-chatgpt-links]: Botpresso, ≈2026-07: 52 client sites (43 B2C, 9 B2B), GA4 ChatGPT referrals 26 Mar – 6 May vs 7 May – 17 Jun 2026; observational; OpenAI didn't announce the change; ecommerce: 12 of 17 stores grew.
[^nz-aimeas]: Natzir Turrado, 2026-05-17, updated to 2026-10: Search Console impressions inflated May 2025 – April 2026 by a bug Google acknowledged; ChatGPT UTM bug 7–16 Oct 2026 (−68 to −74 % in logs, −20 to −60 % in GA4); 96–99 % of ChatGPT citation clicks without referrer; server logs vs GA4 on several sites.
[^mt-sitequeries]: Metehan Yeşilyurt, 2026-08-21: Peec logs, 14.9M queries per week; Reddit share of ChatGPT citations ~4.6 % → 0.23 %; author works at Peec AI.
[^brief-distinct]: Jes Scholz, 2026-06-18: one client case — branded clicks fell sharply, impressions and position flat; favicon removed by accident, fixed in minutes.
[^gg-canonical]: Glenn Gabe, 2026-02-17: same-language hreflang across two countries; Google canonicalised millions of URLs to the other country's version but showed the right URL; GSC credits clicks to the canonical; Google confirmation relayed; client case.
[^seer-zero-click-paid]: Seer Interactive, 2026-07-14: client portfolio, 6 verticals, mostly B2B/lead-gen, Dec 2025 – May 2026; nonbrand paid CTR 16.39 % → 14.13 %, impressions +28 %, organic sessions −32.3 %, Direct +53.6 %, organic conversion rate +133 %.
[^gn-zero]: Barry Adams, 2026-03-02: relays Similarweb/Graphite ("two and a half percent" decline to top global sites; Google "nearly 20%" of web visits) and Chartbeat ("33%", skewed; Jan–Nov YTD ~−15 %); publisher context.
[^gg-may2026]: Glenn Gabe, 2026-06-10: May 2026 core update visible ~48 h in, mid-rollout tremors, Discover losses at the final tremor; cases.
[^gg-dec2025]: Glenn Gabe, 2026-01-07: December 2025 core update, tremor on 20 December; 3,000+ tracked sites, qualitative.
[^lr-techseo]: Lily Ray, Tech SEO Connect 2025 recap, 2025-12-05: Rachel Anderson's log dashboard (security tool returning 406 to Googlebot and AI bots; GSC Crawl Stats didn't show it); her summary of the talk.
[^sp-zero-click-2026]: SparkToro, 2026-06-09: Similarweb US desktop+mobile web panel, Jan–Apr 2026, 68.01 % zero-click, Google app excluded; relays Ahrefs tracker (75,000+ opted-in domains): Google's share of traffic −8 points Jun 2025–May 2026.
[^mlseo-content-audit]: ML for SEO, 2026-10-24: rule order, first match wins; decay = clicks −30 % or more between two consecutive 3-month Search Console periods (≥20 clicks earlier); striking distance = position 4–20 with ≥200 impressions; thin = <300 words with demand; prune if <10 clicks, <200 impressions, <20 sessions and no key events. Demonstrated on a synthetic 24-URL site.
