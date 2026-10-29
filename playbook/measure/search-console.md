---
type: Checklist
title: Search Console
description: How to read Search Console without being fooled — the comparison checklist, num=100, filtered and inflated impressions, the Generative AI report and AI Mode clicks, where AI Overviews show, text ads, zero-click and organic-decline benchmarks, whole-site CTR benchmarks, brand-verification queries, bot-like LLM query bursts and AI Mode follow-ups, how much volume a title test needs, same-language hreflang click attribution, the URL Inspection API quota, Insights query groups, the zero-click series by country, and decay and striking-distance definitions.
tags: [measurement, search-console, ai-overviews, ctr, zero-click, caveats, branded-search, hreflang, ai-mode]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T09:15:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T09:22:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: chuleta-timelines
    resource: "https://newsletter.chuletaseo.com/p/google-admite-que-el-seo-se-nota"
    title: "Chuleta SEO (Emilio Rodríguez García), Google admite que el SEO se nota (2026-10-22; Spanish newsletter relaying Gary Illyes at Search Central Live Barcelona)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays Google confirmations and third-party studies)"
  - id: aleyda-ads
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/serp-shifts-ads-remonetized/"
    title: "Aleyda Solis, SERP shifts: search is being re-monetised (~Feb 2026; 4 US verticals, Jan 2025 vs Jan 2026; search extracts)"
  - id: thrive-traffic
    resource: "https://thriveagency.com/news/notice-your-website-traffic-is-declining-lately/"
    title: "Thrive, Website traffic declining (2025-09-08; relays Authoritas, Dec 2024, 10,000 US keywords)"
  - id: ipr-zero-click
    resource: "https://ipullrank.com/zero-click-behavior-analysis-q3-2026"
    title: "iPullRank (Cate Dombrowski), Zero-click behavior analysis (2026-07-30; Datos, 13.1 billion searches, Oct 2024 – Dec 2025)"
  - id: brodie-num100
    resource: "https://brodieclark.com/the-great-decoupling-num100/"
    title: "Brodie Clark, The Great Decoupling and num=100 (updated 2025-09-26; cites LOCOMOTIVE, ThotSEO, JetOctopus samples)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings, Jun 2025 – Oct 2026; month anchors)"
  - id: mh-gsc-ai
    resource: "https://www.mariehaynes.com/new-aio-and-aimode-info-in-gsc/"
    title: "Marie Haynes, New AIO and AI Mode info in Search Console (2026-06-03)"
  - id: bing-ai-perf
    resource: "https://blogs.bing.com/webmaster/February-2026/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview"
    title: "Bing Webmaster Blog, AI Performance in Bing Webmaster Tools (public preview, 2026-02-10)"
  - id: gm-organic
    resource: "https://www.growth-memo.com/p/organic-traffic-is-down-but-its-not"
    title: "Growth Memo, Organic traffic is down, but it's not… (2026-10-26; Similarweb, 10,000 domains per country)"
  - id: gm-gsc75
    resource: "https://www.growth-memo.com/p/gsc-data-is-75-incomplete"
    title: "Growth Memo, GSC data is 75 % incomplete (2026-02-02; 450M impressions; method paywalled)"
  - id: eea
    resource: "https://searchind.com/googles-eea-search-changes-are-reshaping-product-visibility/"
    title: "Searchind, Google's EEA Search Changes (Sep 2026)"
  - id: ah-ctr-bench
    resource: "https://ahrefs.com/blog/what-is-a-good-ctr/"
    title: "Ahrefs, What is a good CTR (2026-06-22; 422,421 GSC sites, updated monthly)"
  - id: bp-brand-verify
    resource: "https://botpresso.com/how-do-users-verify-a-brand/"
    title: "Botpresso, How users verify a brand (≈2026-10)"
  - id: nz-aimeas
    resource: "https://natzir.com/en/analytics/ai-traffic-measurability/"
    title: "Natzir Turrado, The state of AI traffic measurability (2026-05-17, updated to 2026-10; server logs vs GA4 on several sites)"
  - id: mt-gscprompts
    resource: "https://metehan.ai/blog/stop-guessing-which-prompts-to-track/"
    title: "Metehan Yeşilyurt, Choosing prompts to track from Search Console (2025-12-12; method)"
  - id: sbs-clicks
    resource: "https://www.seobythesea.com/2015/07/google-click-through-feedback-search-results/"
    title: "SEO by the Sea, Click-through user feedback on search results (2015-07-31; patent US 9,092,510)"
  - id: gg-canonical
    resource: "https://www.gsqi.com/marketing-blog/rel-canonical-hint-cascade-chatgpt/"
    title: "Glenn Gabe, Rel canonical is just a hint — cascade to ChatGPT (2026-02-17; 3 client cases)"
  - id: gg-pdf
    resource: "https://www.gsqi.com/marketing-blog/how-to-find-all-pdfs-deindexed-url-inspection-api/"
    title: "Glenn Gabe, Finding deindexed PDFs with the URL Inspection API (2026-09-16; method + client observations)"
  - id: gg-aimode
    resource: "https://www.gsqi.com/marketing-blog/how-to-find-ai-mode-queries-gsc/"
    title: "Glenn Gabe, Finding AI Mode queries in GSC (2026-08-13; one 50K+ query export)"
  - id: ls-semkw
    resource: "https://lazarinastoy.com/semantic-keyword-research-ai-era/"
    title: "Lazarina Stoy, AI-powered semantic keyword research (2026-10-25; talk, framework)"
  - id: seer-zero-click-paid
    resource: "https://www.seerinteractive.com/insights/zero-click-search-paid-strategy"
    title: "Seer Interactive, The case of the missing click (2026-07-14; client portfolio, 6 verticals, Dec 2025 – May 2026)"
  - id: gn-zero
    resource: "https://www.seoforgooglenews.com/p/google-zero-is-a-lie"
    title: "Barry Adams, SEO for Google News: Google Zero is a lie (2026-03-02; relays Similarweb/Graphite, Chartbeat)"
  - id: gn-aiyear
    resource: "https://www.seoforgooglenews.com/p/googles-ai-adventure-year-one"
    title: "Barry Adams, Google's AI adventure — one year on (2025-05-08; relays Sistrix, Datos/SparkToro)"
  - id: sp-zero-click-2026
    resource: "https://sparktoro.com/blog/in-2026-less-than-one-third-of-google-searches-still-send-a-click/"
    title: "SparkToro, In 2026, less than one third of Google searches still send a click (2026-06-09; Similarweb US panel Jan-Apr 2026)"
  - id: sp-zero-click-countries
    resource: "https://sparktoro.com/blog/zero-click-searches-highest-in-the-uk-lowest-in-germany-and-france-has-the-most-efficient-searchers/"
    title: "SparkToro with Similarweb, Zero-click searches by country (2026-06-16; Similarweb panel, Jan-Apr 2026, 6 countries)"
  - id: mlseo-content-audit
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/content-audit/content-audit-template/"
    title: "MLforSEO, Content audit template (2026-10-24; rules plus synthetic 24-URL site)"
  - id: mlseo-internal-linking
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/internal-link-analysis/automate-internal-linking-ai/"
    title: "MLforSEO, 10 ways to automate internal linking with AI (2026-10-22; one blog, synthetic DiD demo)"
---

# Search Console

What Search Console numbers can and can't tell you, and which outside breaks to account for before comparing any two periods.

## Rules
- **Before any comparison, list the breaks between the two periods** and say so next to every number that crosses one. *Practitioner* — [section 1](#1-before-every-comparison)
- **Start impression and position baselines on 13 Sept 2025, split by device,** and don't read earlier impression growth as evidence about AI Overviews. *Official, samples measured* — [section 2](#2-num100-from-10-sept-2025)
- **Trust clicks over impressions,** compare impressions only within the same period type, and treat zero-click bursts of long natural-language queries and AI Mode follow-ups ("yes", "tell me more") as machine or AI Mode traffic. *Measured, relayed; practitioner* — [section 3](#3-impressions-are-filtered-and-were-inflated), [section 12](#12-bot-like-llm-query-bursts)
- **Use the Generative AI report for exposure only** and join its pages to organic clicks to see which AI-visible pages still earn clicks. *Official, relayed* — [section 4](#4-ai-reports-search-console-and-bing)
- **Segment CTR losses by query type, brand / non-brand, device and country** before attributing them to an update or to AI Overviews; where two markets share a language, read each by country filter, not only its directory property. *Measured, relayed; practitioner* — [section 5](#5-where-ai-overviews-show), [section 7](#7-zero-click-is-the-baseline), [section 14](#14-same-language-hreflang-clicks-go-to-the-canonical)
- **Track the organic / paid / zero-click split per query set** and annotate ad and UI changes on traffic charts before reading a trend. *Measured* — [section 6](#6-ads-and-ui-inside-the-results)
- **Benchmark organic decline against comparable sites,** not country averages or industry headlines driven by a few large domains. *Measured (modelled), relayed* — [section 8](#8-organic-decline-benchmarks)
- **Use an unaffected country as control** when a change applies only to some markets. *Measured* — [section 9](#9-country-breaks-eea-free-listings)
- **Judge site CTR against your own history;** outside CTR benchmarks are a sanity range only. *Measured, vendor data* — [section 10](#10-whole-site-ctr-benchmarks)
- **Once a quarter, pull the queries people use to check you out** (reviews, scam, returns, delivery…) and fix the pages they land on. *Practitioner* — [section 11](#11-brand-verification-queries)

## 1. Before every comparison
This list applies to all measurement — Search Console, [analytics](analytics.md), [AI-visibility tracking](ai-visibility-tracking.md) and [rank tracking](rank-tracking.md).
1. **List the breaks** that fall between the two periods (your own tracking changes plus the outside ones below). Write them in a dated caveats list; it pays back every month.
2. **If a period crosses a break, say so next to the number**, or pick windows that don't cross it.
3. **Prefer a control:** another country, an untouched page set, or a metric the break doesn't touch.
4. **Search Console is the source of truth for organic search;** analytics is the source for what visitors did after landing; ad platforms for spend. Don't mix them in one ratio without saying so.

- **Core and spam updates.** Use the dated list in the [Google updates timeline](../reference/google-updates-timeline.md), with rollout start and end. A slide that starts *before* an update began isn't caused by it, and overlapping updates can't be told apart by dates alone.

## 2. num=100 (from ~10 Sept 2025)
- Google stopped supporting the `&num=100` results parameter ("not something that we formally support"). Impressions fell from about 10 September, mostly on desktop, and average position "improved" without any real ranking change, especially beyond position 20; rank trackers cut their depth to about the top 30 ([rank tracking](rank-tracking.md#3-tracker-depth-after-num100)).[^brodie-num100]
- **Third-party samples:** 87.7 % of 319 properties saw a drop; median impression loss ~15 % across 1,334 sites; aggregate −25 % across 1,000 sites.[^brodie-num100]
- **Use baselines from 13 Sept 2025 on,** split by device, and don't use pre-September impression growth as evidence that AI Overviews cut CTR — part of it was bot impressions (*inference*).[^brodie-num100]

> **Conflict:** the start date is given as 10 Sept and as "around September 11" — [details](../reference/conflicts.md#when-did-num100-hit)

## 3. Impressions are filtered and were inflated
- **Search Console filters most impressions.** An analysis of 450M impressions claims about three quarters are filtered out, and bots and AI Overviews distort the rest. *Headline only; method paywalled.*[^gm-gsc75]
- **Search Console impressions inflated from 13 May 2025 to April 2026** (clicks unaffected), a bug Google acknowledged.[^ignite-news][^nz-aimeas] Until 2026-10-28 this page gave only the start date; the end (April 2026) comes from a later source. Annotate the whole period on impression charts, and compare impressions only within the same period type.

## 4. AI reports: Search Console and Bing
- **Search Console's "Generative AI" report** (rolling out from mid-2026, first mainly in the UK) shows impressions from AI Overviews, AI Mode and Discover AI features by page, country, device and date — impressions only, no clicks, positions or CTR.[^mh-gsc-ai] It has been available globally since 31 Aug 2026; AI Overviews and AI Mode are combined in one figure, and there are no queries. *Official, relayed.*[^nz-aimeas] Join its pages to organic clicks to see which AI-visible pages still earn clicks.
- **AI Mode clicks sit inside "Web".** Since 17 June 2025 clicks from AI Mode are counted in the normal "Web" search type and can't be separated there. *Official, relayed.*[^nz-aimeas]
- **Bing's coverage limits** (how much of the citation data maps to queries and pages): [AI-visibility tracking](ai-visibility-tracking.md#9-bing-ai-performance-what-it-covers).
- **Bing's AI Performance report** gives page-level citations for Copilot; setup and use in [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).[^bing-ai-perf]

## 5. Where AI Overviews show
- In a December 2024 sample of 10,000 US keywords, AIOs appeared on 29.9 % of keywords but 11.5 % of search volume: problem-solving queries 74 %, explicit questions 69 %, non-brand 33 % vs brand 19.6 %, navigational almost never.[^thrive-traffic]
- Later figures are higher (Comscore: 39.4 % of US desktop searches in June 2026, up from 25.8 %; Seer: 95.4 % for comparison and 83.4 % for price/buy queries), and a randomised field experiment found 38 % fewer organic clicks to external sites when an AIO appeared.[^ignite-news]
- A larger vendor sample from September 2025 found much lower trigger rates for commercial, transactional and Shopping queries, while branded queries caught up with non-branded ones by September 2026: see [Google AI features](../how-it-works/google-ai-features.md#7-when-ai-overviews-show). The estimated CTR loss with an AIO is largest at position 1 and shrinks down the page: [Google AI features](../how-it-works/google-ai-features.md#8-what-an-ai-overview-costs-in-clicks).
- Segment CTR losses by query type and brand / non-brand before attributing them to an update.

> **Conflict:** AI Overview trigger rates for commercial queries range from a few percent to most queries depending on the study — [details](../reference/conflicts.md#how-often-do-ai-overviews-show)

> **Conflict:** AI Overviews vs text ads as the main cause of falling organic CTR — [details](../reference/conflicts.md#why-is-organic-ctr-falling)

## 6. Ads and UI inside the results
- **Text ads take organic clicks too.** US, January 2025 vs January 2026: for headphones, text ads went from 3 % to 16 % of clicks and all paid from 16 % to 36 %, with zero-click stable at 63 %; for jeans, organic fell from 73 % to 56 % while text ads rose from 7 % to 16 %. In this data text ads were the largest measurable driver of the organic decline, ahead of AI Overviews. *Measured, method partly visible; search extracts.*[^aleyda-ads] Track the organic / paid / zero-click split per query set before blaming AI Overviews.
- **Ads and UI inside organic units.** Ads were added to formerly organic-only product grids (2026), and AI-surface citation layouts change every few weeks.[^brodie-notes] Annotate these on traffic charts before reading a trend.

## 7. Zero-click is the baseline
- Across 13.1 billion searches (Oct 2024 – Dec 2025, 94.5 % desktop), 46.96 % ended without a click, up about 2.6 points over the period, almost all from organic; US mobile reached 66 %.[^ipr-zero-click] Segment by device and country before comparing CTRs.
- SparkToro's figure for early 2026 is 68.01 %;[^ignite-news] the gap is method (desktop-heavy clickstream vs a mobile-inclusive panel), not a contradiction — quote zero-click rates with their source and device mix.
- **Paid CTR falls too.** In one agency's client portfolio (6 verticals, mostly B2B / lead-gen), nonbrand paid CTR fell from 16.39 % to 14.13 % while impressions rose 28 % (Dec 2025 → May 2026); organic sessions fell 32.3 % and direct rose 53.6 %, direct overtook organic in Nov 2025, and organic conversion rate rose 133 %. Informational queries had the lowest paid CTR in all 6 verticals. *Measured, agency portfolio, mostly B2B.*[^seer-zero-click-paid]
- **Do:** use branded impressions plus direct traffic as a zero-click health check, and geo holdouts when testing a change.[^seer-zero-click-paid]

> **Conflict:** 46.96 % vs 68.01 % zero-click depending on panel and device mix — [details](../reference/conflicts.md#how-high-is-zero-click)

## 8. Organic decline benchmarks
- **Organic traffic is falling broadly, unevenly.** Modelled US organic visits fell 13.2 % from Aug 2024 to Aug 2026 (France −24.4 %); about 1 % of domains account for 40.2 % (US) and 48.5 % (France) of the loss; without publishers the US decline is 7.8 %. Paid search grew 21 % in the US. *Similarweb models, not causal.*[^gm-organic]
- **Industry headlines are skewed by a few domains and one-off events.** Similarweb/Graphite data put the decline of Google traffic to top global sites at "two and a half percent", with Google still "nearly 20%" of all web visits; Chartbeat's "33%" decline is an aggregate skewed by a few big sites and by a year-over-year comparison against the 2024 US election (Jan–Nov YTD about −15 %). *Measured, relayed; publisher view.*[^gn-zero]
- **Queries grew; clicks didn't.** Google queries rose "21%" in 2024 vs 2023 (Datos via SparkToro), but total clicks are not expected to grow much ("Peak Search"), so organic is close to zero-sum. *Measured, relayed; the zero-sum reading is opinion.*[^gn-aiyear] Read your clicks as a share of the clicks in your query set, against competitors, not only as an absolute trend.
- Benchmark against comparable sites, not country averages, check whether a few large domains or one-off events drive an industry figure before quoting it, and check ad load and updates before blaming AI.

## 9. Country breaks: EEA free listings
- **EEA free product listings removed (mid-Sept 2026).** Organic Shopping ("Merchant listings") clicks fall in EEA countries; use a non-EEA country as control.[^eea] Background in [shopping surfaces](../how-it-works/shopping-surfaces.md); method in [diagnostic test 6](diagnostic-tests.md#6-country-or-segment-control).

## 10. Whole-site CTR benchmarks
- Across 422,421 Search Console sites (June 2026), the median whole-site CTR was 1–2 %; Shopping sites had a median of 1.33 % (n=2,245; mean 2.51 %); median CTR rose with Domain Rating from 0.39 % to 2.91 %. The article's text and tables disagree in places. *Measured, vendor data, updated monthly.*[^ah-ctr-bench]
- **Do:** compare CTR with your own history, segmented as in [section 5](#5-where-ai-overviews-show); use outside benchmarks only as a sanity range.

## 11. Brand-verification queries
- Before buying from an unfamiliar shop, people search to check it. Filter Search Console queries with a regex such as `review|reviews|legit|scam|fake|return|returns|refund|refunds|delivery|trustpilot|reddit|amazon|worth it|real or fake`, then open each landing page that matches and list its queries. *Practitioner.*[^bp-brand-verify]
- **Do:** run it quarterly; build or extend the returns, delivery and reviews pages those queries land on, and check what third-party pages rank for them ([homepage and brand](../page-types/homepage-and-brand.md), [third-party presence](../channels/third-party-presence.md)).

## 12. Bot-like LLM query bursts
- Search Console can show bursts of long, conversational queries with many impressions and no clicks — about 125,000 impressions and no clicks on one post in one practitioner's data — which look like LLM-driven machine traffic rather than people. *Practitioner, one case.*[^mt-gscprompts]
- **Do:** flag zero-click bursts of long natural-language queries as probable machine traffic and exclude them before reading impression or CTR trends. The same Search Console queries (≥ 1,000 impressions, rewritten conversationally) are a good seed for a prompt-tracking set ([test 9](diagnostic-tests.md#9-prompt-tracking-per-engine)).[^mt-gscprompts]
- **AI Mode queries are mixed in.** Search Console has no filter for AI Mode queries. In one 50K+ query export, follow-ups such as "yes", "no" and "tell me more" showed impressions and no clicks, and some queries came from AI-visibility trackers. *Practitioner, one export.*[^gg-aimode]
- **Do:** add single-word and conversational follow-ups to the same bot / AI Mode query filter before reading impression or CTR trends.[^gg-aimode]

## 13. Title and snippet tests need volume
- A Google patent applies implicit click feedback only after a selection threshold (e.g. ~100 clicks), within a time window, and compares it with background click trends; trial evidence supports a rolling click window. *Patent; use in production unknown.*[^sbs-clicks]
- **Do:** judge title and snippet tests on long-tail pages only after they have had enough impressions and clicks, and compare with an unchanged control set over the same window (*inference*). Feed title tests: [test 5](diagnostic-tests.md#5-feed-attribute-coverage-and-title-tests); titles: [titles and snippets](../technical/titles-and-snippets.md).

## 14. Same-language hreflang: clicks go to the canonical
- Where two countries share a language and their versions are linked with hreflang, Google may pick the other country's URL as canonical while still showing the right country's URL in results. In one case, relayed with Google's confirmation, millions of URLs were canonicalised to the other country's version. Search Console credits clicks to the canonical, so one country's directory property showed a loss that wasn't real. *Practitioner, relayed Google confirmation.*[^gg-canonical]
- **Do:** read each market with the country filter on the domain property, not only its directory property, and check Google-selected canonicals per country and page type ([test 24](diagnostic-tests.md#24-google-selected-canonicals-per-page-type), [new market](../situations/new-market.md)).

## 15. URL Inspection API quota
- The URL Inspection API allows 2,000 URLs per property per day, counted separately for each property, so verified directory properties multiply the daily quota. *Practitioner observation.*[^gg-pdf]
- The same method found PDFs that Google deindexed at scale from about 25 August 2026 ("Crawled – currently not indexed"); some were later reindexed. *Practitioner, client observations.*[^gg-pdf]
- **Do:** verify directory properties for large page types before relying on daily per-URL checks ([test 17](diagnostic-tests.md#17-daily-index-status-per-url)), and convert PDFs that drive traffic to HTML pages.

## 16. Insights query groups
- Search Console Insights added AI-driven query groups in late October 2025. Fan-out queries have no search volume, so these groups are one of the few first-party views of how Google clusters your queries. *Practitioner.*[^ls-semkw]
- **Do:** use the query groups as a cross-check for your own keyword clusters ([keyword research](../channels/keyword-research.md)).

## 17. Zero-click series and country split
SparkToro (which sells audience research) with Similarweb panel data.
- **The series crosses panels.** Zero-click searches: ~45 % (~2016, Jumpshot), 49 % (2019, Jumpshot), 60.45 % (2024, Datos US), 68.01 % (US, Jan–Apr 2026, Similarweb desktop and mobile web panel, Google app excluded, so the true rate is likely higher). The author calls the cross-panel comparison "apples and oranges". *Measured; different panels.*[^sp-zero-click-2026]
- **What changed, 2024 → 2026:** searches with at least one click fell 9.51 points (−22.9 % relative) and "performed another search" rose 7.2 points; any click counts (organic, paid, Maps, YouTube) except a new search. The 2026 paid/organic split is an estimate, because mobile paid clicks were modelled with an external ratio. *Measured.*[^sp-zero-click-2026]
- **By country (Jan–Apr 2026, web browsers only):** zero-click Germany 62.1 %, Italy 63.4 %, Canada 63.8 %, France 65.3 %, US 68.0 %, UK 69.5 %; searches with a click: Germany 37.9 %, UK 30.5 %. The non-US period label is ambiguous. *Measured; vendor data.*[^sp-zero-click-countries]
- **Do:** compare zero-click figures only within one panel and country; for a German-market site use the German figure, not the US one.

## 18. Decay and striking distance from two periods
From MLforSEO (which sells courses).
- **Definitions used:** decay = clicks down 30 % or more between two consecutive 3-month periods, for pages with at least 20 clicks in the earlier one; striking distance = average position 4–20 with at least 200 impressions. Two-period comparisons can't detect slow declines or separate seasonality. *Practitioner.*[^mlseo-content-audit]
- **Internal-link targets from striking distance:** pages at average position 4–20 with at least 50 impressions for 2–7-word queries, linked from pages that mention the query, after a cannibalisation check; on one blog 242 such queries gave 110 suggestions. It misses the long tail, because Search Console omits rare queries. *Practitioner.*[^mlseo-internal-linking] Method: [ML methods for SEO](ml-methods-for-seo.md#3-internal-link-suggestions).
- **Do:** compare against the same period last year as well before calling a page decayed ([section 1](#1-before-every-comparison)).

## 19. How long changes take to show
- **Google's typical times,** as relayed from a Search Central Live talk: a new page is discovered in about 20 hours, an existing page is re-crawled about every 30 days, link signals are processed within minutes to 3 weeks, and title changes show in 1–2 days. A site migration settles in 1–3 months, and recovery from a core update takes 3–6 months, sometimes up to a year. *Official statement, relayed and paraphrased (no direct quote or recording).*[^chuleta-timelines]
- **The steps add up.** Discovery, crawling, indexing and serving happen one after another, so a page change can take one to three weeks to show. *Practitioner.*[^chuleta-timelines]
- **Do:** before concluding a change failed, check the page's last crawl date in URL Inspection, and compare absolute numbers, not only shares. See [diagnostic tests](diagnostic-tests.md).

Related: [analytics](analytics.md), [AI-visibility tracking](ai-visibility-tracking.md), [rank tracking](rank-tracking.md), [diagnostic tests](diagnostic-tests.md), [traffic drop](../situations/traffic-drop.md), [Google AI features](../how-it-works/google-ai-features.md).

[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: GSC impression inflation (week of 2026-04-04), GA4 AI Assistant channel (2026-05-09), GA4 bug (2026-08-29), GPT-6 referral loss with Adobe data (2026-10-10), Comscore, Seer and the field experiment on AIO clicks (2026-04-25), SparkToro zero-click; secondary reporting, primary sources not checked.
[^aleyda-ads]: Aleyda Solis, ~Feb 2026, via search extracts: four US verticals (headphones, jeans, greeting cards, online games), top queries, Jan 2025 vs Jan 2026; AIO figures there measure presence, not clicks.
[^thrive-traffic]: Thrive, 2025-09-08, relaying Authoritas (Dec 2024, 10,000 US keywords, 7 industries); dated.
[^ipr-zero-click]: iPullRank (Dombrowski), 2026-07-30: Datos clickstream; ad clicks unchanged.
[^brodie-num100]: Brodie Clark, updated 2025-09-26, and notes #sep-2025: impressions down from 10 Sep, desktop-heavy; Google quote; third-party samples (LOCOMOTIVE 319 sites, ThotSEO 1,334, JetOctopus 1,000); bot-impression reading is his inference. Marie Haynes dates the change "around September 11".
[^brodie-notes]: Brodie Clark notes, Apr – Sep 2026: ads in product grids, citation-UI changes.
[^mh-gsc-ai]: Marie Haynes, 2026-06-03: Generative AI performance section, impressions only; grounding opt-out toggle.
[^bing-ai-perf]: Bing Webmaster Blog, 2026-02-10: page-level citations, grounding-query sample.
[^gm-gsc75]: Growth Memo, 2026-02-02: headline claim; not verified.
[^gm-organic]: Growth Memo, 2026-10-26: Similarweb modelled visits; AI referrals 2.85 % of SEO traffic in the US.
[^eea]: Searchind, EEA changes, read 2026-10-27.
[^ah-ctr-bench]: Ahrefs, 2026-06-22: 422,421 GSC sites connected to Ahrefs, June 2026; median 1–2 %; Shopping median 1.33 % (n=2,245, mean 2.51 %); median by DR 0.39 % → 2.91 %; text and tables inconsistent in places.
[^bp-brand-verify]: Botpresso, ≈2026-10 (no publish date shown): query patterns for reviews, legitimacy, returns, refunds, delivery, Trustpilot, Reddit, Amazon, "worth it", "real or fake"; the regex above is assembled from that list.
[^nz-aimeas]: Natzir Turrado, 2026-05-17, updated to 2026-10: summarises Google's documentation — Generative AI performance report since June 2026, global since 2026-08-31, impressions only by page, country and device, AI Overviews and AI Mode combined, no queries or clicks; AI Mode clicks inside "Web" since 2025-06-17; impressions May 2025 – April 2026 inflated by a bug Google acknowledged.
[^mt-gscprompts]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2025-12-12: method for seeding prompts from Search Console queries with ≥ 1,000 impressions; ~125k impressions, no clicks, on one post; practitioner observation.
[^sbs-clicks]: SEO by the Sea (Bill Slawski), 2015-07-31: patent US 9,092,510; selection threshold (e.g. ~100 clicks), time window, comparison with background click trends; antitrust-trial testimony supports a rolling click window, not this patent's exact use.
[^gg-canonical]: Glenn Gabe (GSQi), 2026-02-17: 3 client cases; same-language hreflang across two countries, millions of URLs canonicalised to the other country's version while the right URL was shown; clicks credited to the canonical; Google's confirmation relayed by the author.
[^gg-pdf]: Glenn Gabe (GSQi), 2026-09-16: URL Inspection API quota 2,000 URLs per property per day, separate per property; PDFs deindexed at scale from ~2026-08-25, some reindexed; method plus client observations.
[^gg-aimode]: Glenn Gabe (GSQi), 2026-08-13: one 50K+ query export; AI Mode queries mixed in with no surface filter; follow-ups "yes", "no", "tell me more" without clicks; some queries from AI-visibility trackers.
[^ls-semkw]: Lazarina Stoy, 2026-10-25 (republished talk): fan-out queries have no volume; Search Console Insights added AI-driven query groups in late October 2025.
[^seer-zero-click-paid]: Seer Interactive, 2026-07-14: client portfolio, 6 verticals, mostly B2B / lead-gen, Dec 2025 – May 2026; nonbrand paid CTR 16.39 % → 14.13 %, impressions +28 %; organic sessions −32.3 %, direct +53.6 %, direct above organic from Nov 2025; organic conversion rate +133 %.
[^gn-zero]: Barry Adams, SEO for Google News, 2026-03-02: relays Similarweb/Graphite ("two and a half percent" decline to top global sites; Google "nearly 20%" of web visits) and Chartbeat ("33%", skewed by a few large sites and the 2024 US election comparison; Jan–Nov YTD ~−15 %); publisher-focused; primaries not checked.
[^gn-aiyear]: Barry Adams, SEO for Google News, 2025-05-08: relays Datos via SparkToro, Google queries +"21%" in 2024 vs 2023; "Peak Search" is his reading.
[^sp-zero-click-2026]: SparkToro (Rand Fishkin), 2026-06-09: Similarweb US desktop and mobile web panel, Jan–Apr 2026 (device mix assumed 2/3 mobile), vs Datos 2024 and Jumpshot 2016/2019; Google app excluded; mobile paid clicks modelled with a 3.12–3.81 % ratio from an external panel.
[^sp-zero-click-countries]: SparkToro with Similarweb, 2026-06-16: desktop and mobile web panel, Jan–Apr 2026, 6 countries; Google app excluded; period label says "(US)".
[^mlseo-content-audit]: MLforSEO (Lazarina Stoy), 2026-10-24: decay, striking-distance and thin-content rules on a synthetic 24-URL site.
[^mlseo-internal-linking]: MLforSEO (Lazarina Stoy), 2026-10-22: Search Console striking-distance linking on one 68–79-post blog; 242 queries → 110 suggestions.
[^chuleta-timelines]: Chuleta SEO, 2026-10-22, Spanish, read in full; claims translated. Paraphrases Gary Illyes at Search Central Live Barcelona (no direct quote or recording given): new page discovered in ~20 hours, existing page re-crawled ~30 days, link signals processed in minutes to 3 weeks, title updates 1–2 days, site migration 1–3 months, core-update recovery 3–6 months (up to a year); the author notes the steps add up. Also relays a Cloudflare–OpenAI discovery pilot ("hundreds of millions" of pages, no method) and Bing's Topics Portfolio beta.
