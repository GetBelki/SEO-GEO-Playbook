---
type: Playbook
title: Entering a new market
description: Launching a shop in a new country or language — hreflang and x-default, visible-language content, English fan-out vs local sources, native prompt sets, each market's marketplaces, EEA vs non-EEA surfaces, feeds and local listings, no IP auto-redirects, AI Overview launches per market, country controls in measurement, hosting location (not a geotargeting signal), machine-translated Reddit threads competing in Google AI surfaces, assistants that ignore hreflang, per-language anchor pages, and choosing ccTLD or subfolder by what the market's results show.
tags: [seo, geo, international, hreflang, markets, eea, feeds, local, measurement, ai-overviews, hosting, reddit, cctld, ai-assistants, multilingual]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: g-hreflang
    resource: "https://developers.google.com/search/docs/specialty/international/localized-versions"
    title: "Google Search Central, Tell Google about localized versions of your page (updated 2026-09-21)"
  - id: g-canonical
    resource: "https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls"
    title: "Google Search Central, How to specify a canonical URL (updated 2026-07-10)"
  - id: chatgpt-not-se
    resource: "https://think.resoneo.com/chatgpt/"
    title: "Resoneo, ChatGPT is not a search engine (Feb 2026; network traffic and decompiled frontend)"
  - id: gemini-convo
    resource: "https://think.resoneo.com/gemini-convo/"
    title: "Resoneo, How Gemini searches and cites (Oct 2026; 76,450 conversations, 222,753 searches)"
  - id: aleyda-local
    resource: "https://www.aleydasolis.com/en/ai-search/local-vs-global-ai-citations/"
    title: "Aleyda Solis, Local vs global AI citations (Oct 2026; ChatGPT, Gemini, AI Mode; US/UK/ES/BR; search extracts)"
  - id: aleyda-prompts
    resource: "https://www.aleydasolis.com/en/ai-search/ai-search-prompt-library/"
    title: "Aleyda Solis, AI search prompt library (2026; search extracts)"
  - id: aleyda-global
    resource: "https://www.aleydasolis.com/en/ai-search/global-ai-search-strategy/"
    title: "Aleyda Solis, Global AI search strategy (Mar–Apr 2026; Similarweb, 10 markets, ~87.6M AI visits; search extracts)"
  - id: aleyda-may2026
    resource: "https://www.aleydasolis.com/en/ai-search/google-may-2026-core-update-analysis-intent-market-fit-and-source-type-drove-the-biggest-visibility-shifts/"
    title: "Aleyda Solis, May 2026 core update analysis (Sistrix, US+UK; search extracts)"
  - id: ipr-precision
    resource: "https://ipullrank.com/accuracy-vs-precision"
    title: "iPullRank, Accuracy vs precision in prompt tracking (2026-09-17; cites Search Engine Land 12 prompts × 100 runs, Semrush, an SSRN study of ~38,000 responses)"
  - id: ipr-local
    resource: "https://ipullrank.com/local-ai-search-data"
    title: "iPullRank (Francine Monahan), Local AI search data (2025-12-16; Yext, 1.6M questions, 6.9M citations)"
  - id: ipr-zero-click
    resource: "https://ipullrank.com/zero-click-behavior-analysis-q3-2026"
    title: "iPullRank (Cate Dombrowski), Zero-click behavior analysis (2026-07-30; Datos, 13.1 billion searches, Oct 2024 – Dec 2025)"
  - id: gm-organic
    resource: "https://www.growth-memo.com/p/organic-traffic-is-down-but-its-not"
    title: "Growth Memo, Organic traffic is down, but it's not… (2026-10-26; Similarweb, 10,000 domains per country)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026; trial testimony, 2024 leak, author's schema compilation)"
  - id: eea
    resource: "https://searchind.com/googles-eea-search-changes-are-reshaping-product-visibility/"
    title: "Searchind, Google's EEA Search Changes are reshaping Product Visibility (Sep 2026)"
  - id: gmc-audit
    resource: "https://searchind.com/the-google-merchant-center-audit-i-run-for-every-client/"
    title: "Searchind, The Google Merchant Center Audit I run for every client (Aug 2026, updated Oct 2026)"
  - id: brodie-loyalty
    resource: "https://brodieclark.com/loyalty-program-promotion-gmc/"
    title: "Brodie Clark, Loyalty programme and promotions in Merchant Center (2025-08-13)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: ai-visible
    resource: "https://searchind.com/ecommerce-visibile-in-ai-search/"
    title: "Searchind, How to make your e-commerce visible in AI search (Sep 2025)"
  - id: ipr-openai-feed
    resource: "https://ipullrank.com/ecommerce-chatgpt-product-feeds"
    title: "iPullRank, Ecommerce ChatGPT product feeds (2025-10-20; on OpenAI's product feed spec)"
  - id: maps
    resource: "https://think.resoneo.com/google-map-dissected/"
    title: "Resoneo, Google Maps dissected (Aug 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: bp-intl
    resource: "https://botpresso.com/international-seo-guide/"
    title: "Botpresso, International SEO guide (≈2023-11)"
  - id: ah-aio-france
    resource: "https://ahrefs.com/blog/ai-overviews-france-impact/"
    title: "Ahrefs, AI Overviews launch in France (2026-09-16; 963 domains, control group)"
  - id: bc-servers
    resource: "https://www.bruceclay.com/blog/servers-and-seo-the-impact-of-servers-and-hosting-on-seo-success/"
    title: "Bruce Clay, Servers and SEO (2026-06-30; Mueller quotes, Deloitte study)"
  - id: mt-reddit-tl
    resource: "https://metehan.ai/blog/reddit-machine-translated-pages-ai-visibility/"
    title: "Metehan Yeşilyurt, Translated Reddit is winning AI citations (2026-06-22; 64.77M Reddit citations, 20 countries, 4 engines)"
  - id: gg-hreflang
    resource: "https://www.gsqi.com/marketing-blog/ai-search-hreflang-multilingual-queries/"
    title: "Glenn Gabe, AI search, hreflang and translated content (2025-12-01; informal FR/IT/ES tests, 5 assistants)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: gn-intl
    resource: "https://www.seoforgooglenews.com/p/international-seo-for-publishers"
    title: "Barry Adams, International SEO for publishers (2026-09-16; consulting projects, Google localisation docs)"
  - id: ja-multiling
    resource: "https://www.jonoalderson.com/conjecture/localisation-without-borders/"
    title: "Jono Alderson, Shaping visibility in a multilingual internet (2025-08-08; opinion)"
  - id: sp-zero-click-countries
    resource: "https://sparktoro.com/blog/zero-click-searches-highest-in-the-uk-lowest-in-germany-and-france-has-the-most-efficient-searchers/"
    title: "SparkToro with Similarweb, Zero-click searches by country (2026-06-16; Similarweb web panel, Jan–Apr 2026, 6 countries)"
  - id: srp-feb-2026-update
    resource: "https://serprecon.com/blog/feb-2026-serprecon-update"
    title: "SERPrecon, Feb 2026 SERPrecon update (2026-02-06; product method changes)"
---

# Entering a new market

Use this page when you add a country, a language version or a ccTLD, or start selling into a market where you were only visible by accident.

## Rules
- **Choose ccTLD or subfolder by what the market's results show, then give every language/region version reciprocal hreflang plus an x-default** ([section 1](#1-hreflang-and-language), [section 8](#8-cctld-or-subfolder)). *Official*; structure *Practitioner, disputed.*
- **Translate the visible content fully, with the local product terms** — Google detects language from it, not from hreflang or `lang`, and AI assistants often ignore hreflang, so test key queries per language in each assistant ([section 1](#1-hreflang-and-language), [section 2](#2-ai-assistants-english-fan-out-local-winners)). *Official*; assistants *Measured, informal tests.*
- **Never auto-redirect by IP**; suggest the local version in a banner and make the language selector crawlable `<a href>` links ([section 1](#1-hreflang-and-language)). *Practitioner, relaying Google.*
- **Keep English entity data and key pages even in a non-English market, and publish a few accurate anchor pages (About, flagship products) in each new language**, but measure local prompts natively ([section 2](#2-ai-assistants-english-fan-out-local-winners)). *Measured*; anchor pages *Opinion.*
- **Build each market's prompt set natively** rather than translating one list, and pin geography per run ([section 2](#2-ai-assistants-english-fan-out-local-winners)). *Practitioner; measured method.*
- **Map each market's leading marketplaces and local champions** as citation and corroboration channels ([section 3](#3-marketplaces-and-local-competitors)). *Measured, one month.*
- **Check which surfaces exist in the market** — EEA vs non-EEA product listings, US-first agent features, loyalty eligibility ([section 4](#4-surfaces-and-feeds-differ-by-market)). *Several sources; practitioner.*
- **Report every metric per country, with an unaffected country as control**, and set click targets from each country's own zero-click baseline ([section 5](#5-measure-per-country), [section 9](#9-zero-click-differs-by-country)). *Measured in field notes*; country rates *Measured, vendor data.*
- **Note the date AI Overviews launch in each market** — CTR falls on exposed queries while rankings hold ([section 5](#5-measure-per-country)). *Measured, vendor data.*
- **Don't move hosting into the market for SEO**; server location isn't used for geotargeting — use a CDN for speed ([section 6](#6-hosting-and-speed)). *Official statement, relayed.*
- **In non-English markets, treat machine-translated English Reddit threads as competitors** for product queries in Google's AI surfaces ([section 7](#7-translated-forum-threads)). *Measured, vendor data.*

## Steps
1. **Structure:** choose the URL pattern per market by what the market's results show ([section 8](#8-cctld-or-subfolder)); set canonicals and hreflang per [technical foundations](../technical/technical-foundations.md#10-international-and-hreflang). No IP-based redirects; a suggestion banner and a crawlable language selector instead.
2. **Content:** localise visible text, titles, H1s and the factual opening sentence; use the local-language product terms; publish About and flagship pages in the new language first.
3. **Feeds:** set up a feed for the market with local-language titles, local prices and availability ([feeds and Merchant Center](../channels/feeds-and-merchant-center.md)).
4. **Surfaces:** list which Google shopping units, AI-assistant merchant programmes and promotions exist there.
5. **Third parties:** list the market's marketplaces, comparison sites and local champions; get listed with consistent facts ([third-party presence](../channels/third-party-presence.md)).
6. **Local presence:** business profile and local inventory where you have stores ([local](../channels/local.md)). Keep hosting where it is; add a CDN if the new market is far from the server ([section 6](#6-hosting-and-speed)).
7. **Measurement:** country splits in Search Console and analytics, a native prompt set per market that checks which language version each assistant links ([test 9](../measure/diagnostic-tests.md#9-prompt-tracking-per-engine)), a control country ([test 6](../measure/diagnostic-tests.md#6-country-or-segment-control)); note whether and when AI Overviews launched in the market.

## 1. Hreflang and language
- HTML link elements, HTTP headers or the sitemap: "The three methods are equivalent".[^g-hreflang]
- Each version lists "itself as well as all other language versions"; "If two pages don't both point to each other, the tags will be ignored." Use fully qualified URLs, ISO 639-1 language and ISO 3166-1 Alpha 2 region codes; "You can't specify the country code by itself."[^g-hreflang]
- `x-default` "is used when no other language/region matches the user's browser setting".[^g-hreflang]
- "Google doesn't use hreflang or the HTML lang attribute to detect the language of a page" — the visible content decides.[^g-hreflang] A half-translated template reads as the wrong language. Google's localisation docs, as relayed by a practitioner, treat pages as duplicates only if the main content stays untranslated: translate the full main content, not only the template.[^gn-intl]
- Canonicals that carry `hreflang` attributes "are not used for canonicalization"; use HTTPS URLs in hreflang.[^g-canonical]
- **No IP auto-redirects.** Googlebot crawls mainly from the US and must be able to reach every locale; redirecting by IP hides the other versions from it. Suggest the local version in a banner instead, and make the language selector plain crawlable `<a href>` links. *Practitioner, relaying Mueller.*[^bp-intl] (Google's hreflang page says nothing explicit on IP redirects.)[^g-hreflang]

## 2. AI assistants: English fan-out, local winners
- **English fan-out.** More than half of ChatGPT's sub-queries are English;[^chatgpt-not-se] Gemini sends an English query for 55 % of non-English questions.[^gemini-convo] Keep an English version of key pages and English entity data.
- **Local sources still win a large minority.** Local ccTLDs took about 41 % of citations in Brazil, 38 % in the UK and 24 % in Spain; Gemini's local share ranged from 51.7 % (Brazil) to 16.6 % (Spain), AI Mode's stayed at 22.6–27.5 %; Home/DIY had among the highest local shares. *Measured; search extracts.*[^aleyda-local]
- **Native prompt sets.** Start with 30–50 tagged core prompts per market (market and language among the tags) and build each country's set natively. *Practitioner.*[^aleyda-prompts] Pin geography for every run. *Measured method.*[^ipr-precision]
- **Local answers cite websites first;** listings act as verification. *Measured, vendor data.*[^ipr-local] Keep the same facts on the site and in every listing.
- **Assistants often ignore hreflang.** In informal tests with French, Italian and Spanish queries, ChatGPT, Perplexity and Claude mostly returned the US-English URL despite hreflang; Copilot was correct 3 of 3; Gemini only once links were requested; AI Overviews were less consistent than AI Mode and the blue links. *Measured, informal tests, 5 assistants.*[^gg-hreflang] **Do:** test key queries per language in each assistant, and put the local terms in each version's visible content so the right version matches on its own.
- **Anchor pages per language.** With no local-language footprint, models borrow facts from other languages or from similar companies. *Opinion, no data.*[^ja-multiling] **Do:** publish a few accurate anchor pages per language — About and flagship products — and clean up mistranslated mentions ([homepage and brand](../page-types/homepage-and-brand.md)).

## 3. Marketplaces and local competitors
- Across ~87.6M AI visits in 10 markets (March 2026), amazon.com took 28.0 % of US AI ecommerce clicks; Amazon.it took 46.2 % in Italy; local champions led elsewhere (bol.com in the Netherlands, Mercado Livre in Brazil). *Measured, one month.*[^aleyda-global]
- In the May 2026 core update, local marketplaces in the UK gained about 21–23 % while their US .com versions fell about 54 %: the source that fits the market won. *Measured visibility.*[^aleyda-may2026]
- Find competitors per market and intent; the US leader isn't necessarily the local one.

## 4. Surfaces and feeds differ by market
- **EEA vs non-EEA.** Free product listings and "Popular products" disappeared in the EEA around mid-Sep 2026; a "comparison sites" unit appeared. Paid Shopping, CSS and feeds are unchanged.[^eea] Outside the EEA, free listings still send clicks.
- **Feed titles per market.** Use the local-language term in titles; change titles in the feed, not the shop backend. *Practitioner.*[^gmc-audit]
- **Programme eligibility varies.** Merchant Center loyalty was eligible in the US, UK, Germany, France and Australia (before the EEA change).[^brodie-loyalty] Perplexity's merchant programme was US/CA-only in 2026.[^ai-visible] OpenAI's feed supports regional pricing.[^ipr-openai-feed]
- **Local stores.** A "Stores" tab in Shopping shows local-inventory results, supplied by local inventory feeds and the business profile.[^brodie-notes] For Maps, correct primary category and clean identity data first. *From code.*[^maps]

## 5. Measure per country
- NavBoost's click memory is described per country and device.[^navboost] Zero-click rates differ by device and country (US mobile 66 %),[^ipr-zero-click] and organic declines too (US −13.2 %, France −24.4 %, Aug 2024 – Aug 2026).[^gm-organic] Never blend markets in one CTR or traffic trend.
- **Country control.** After the EEA removal, Germany lost 67 % of merchant-listing clicks while Switzerland held — a clean confirmation without platform reports.[^field-notes]
- **AI Overview launches arrive market by market.** When AI Overviews launched in France (2026-07-22), domains with high exposure (> 20 % of their queries showing an AI Overview) saw median CTR fall from 2.29 % to 1.76 % (−23.1 % raw, −24.8 % against a control group with < 2 % AI Overview rate); across all 963 domains, median CTR fell 5.7 % and clicks 8.8 %, about −0.9 CTR points per point of exposure. *Measured, vendor data, 28 days before vs 9 after.*[^ah-aio-france] **Do:** record the launch date per market, compute your AI Overview exposure rate, and read a CTR fall with stable impressions and positions against it ([traffic drop](traffic-drop.md#3-segment-then-name-the-surface), [Google AI features](../how-it-works/google-ai-features.md)).

## 6. Hosting and speed
- Google's John Mueller: "with regards to SEO, the server's location is not used for geotargeting". *Official statement, relayed by an agency blog.*[^bc-servers] Geotargeting comes from hreflang, URL structure and content ([section 1](#1-hreflang-and-language)).
- Speed still matters to buyers: a Deloitte study found a 0.1 s mobile speed gain went with about 10 % more retail spend. *Measured, relayed.*[^bc-servers] **Do:** don't move servers for SEO; serve the new market through a CDN ([Core Web Vitals](../technical/technical-foundations.md#9-core-web-vitals)).

## 7. Translated forum threads
- Across 64.77M Reddit citations in 20 countries and 4 engines (1 Mar – 10 Jun 2026), machine-translated Reddit URLs (`?tl=`) took 5.71 % of Reddit's AI citations — but 52 % of Google AI Overviews' Reddit citations in Germany and 72 % of AI Mode's in Spain. ChatGPT dropped them from 6.14 % (April) to 0.30 % (1–10 June); Perplexity cited none. In Germany they clustered in commercial categories (bags and fashion 13.0 %, tech hardware 12.7 %, audio and smart home 11.6 %). *Measured, vendor data (author works at an AI-visibility vendor).*[^mt-reddit-tl]
- **Do:** in a non-English market, check which translated English threads Google's AI surfaces cite for your product queries, and treat them as competitors: answer the same questions in the local language on your pages and in local communities ([third-party presence](../channels/third-party-presence.md#7-forums-and-discussions)).

## 8. ccTLD or subfolder
- Sources disagree: one news consultant prefers separate ccTLDs beyond a few countries, calling hreflang "hints, not directives" that are often invalid and slow to be accepted;[^gn-intl] another practitioner says to follow what the market's results already show — one publisher launched a .de because "78% of the German SERP was already .de" — and notes hreflang has no effect on Discover;[^lr-techseo] Google's docs are neutral. *Practitioner, publisher context; conference talk, relayed.*
- **Do:** look at the top results for your main category queries in the new market; if local ccTLDs dominate, weigh a ccTLD, otherwise a subfolder keeps one domain's strength. Either way, hreflang and fully translated main content still apply ([section 1](#1-hreflang-and-language), [technical foundations](../technical/technical-foundations.md#10-international-and-hreflang)).

> **Conflict:** ccTLDs beyond a few countries vs follow the market's results vs Google's neutral docs — [details](../reference/conflicts.md#cctld-or-subfolder-for-a-new-market)

## 9. Zero-click differs by country
SparkToro sells audience research; Similarweb co-authored the study.
- **Rates by country.** Share of Google searches ending without a click: Germany 62.1 %, Italy 63.4 %, Canada 63.8 %, France 65.3 %, US 68.0 %, UK 69.5 %. Web browsers only, Google app excluded; the period is labelled Jan–Apr 2026 for the US, so the non-US period is ambiguous. *Measured, vendor data.*[^sp-zero-click-countries]
- **Where the clicks go.** Clicks to Alphabet-owned sites were 7.3 % (UK) to 9.4 % (Canada) of clicks; clicks to the open web per 1,000 Google searches were 287 in Germany, 280 Italy, 271 France, 268 Canada, 232 UK and 231 US. *Measured, vendor data.*[^sp-zero-click-countries]
- **Tools by language.** One content-scoring vendor states its lexical and semantic metrics are fully supported for English, Spanish, French, German, Italian and Portuguese, but less accurate for Russian, Japanese, Korean and Chinese because of tokenisation. *Practitioner, vendor data.*[^srp-feb-2026-update] Check language support before comparing tool scores across markets.
- **Do:** set click targets per market from that market's own baseline, not from US figures; a UK launch can expect fewer clicks per search than a German one ([section 5](#5-measure-per-country), [traffic drop](traffic-drop.md#3-segment-then-name-the-surface)).

Related: [migration](migration.md), [AI assistants](../how-it-works/ai-assistants.md), [shopping surfaces](../how-it-works/shopping-surfaces.md), [AI visibility tracking](../measure/ai-visibility-tracking.md).

[^g-hreflang]: Google, localized versions, read 2026-10-27; nothing explicit on IP-based redirects in the extracted text.
[^g-canonical]: Google, canonical URLs, read 2026-10-27.
[^chatgpt-not-se]: Resoneo, "ChatGPT is not a search engine" (data Jan 2026): >50 % English fan-outs.
[^gemini-convo]: Resoneo, Gemini conversations, read 2026-10-27: cited-passage positions and lengths; 55 % English queries for non-English questions.
[^aleyda-local]: Aleyda Solis, Oct 2026, via search extracts: 10 topics, US/UK/ES/BR, ChatGPT, Gemini, AI Mode.
[^aleyda-prompts]: Aleyda Solis, 2026, via search extracts (direct fetch blocked): library sizes, tagging, 3–5 runs in 24–72 h.
[^ipr-precision]: iPullRank, 2026-09-17: Search Engine Land (Sonders) 12 prompts × 100 runs, logged-out ChatGPT; binomial margins; Semrush Instant vs Thinking; SSRN study on prompt wording.
[^ipr-local]: iPullRank, 2025-12-16: Yext study; Google doesn't cite Business Profiles.
[^aleyda-global]: Aleyda Solis, Mar–Apr 2026, via search extracts: Similarweb, 10 markets, 39.3M of the AI visits ecommerce.
[^aleyda-may2026]: Aleyda Solis, May 2026 core update, Sistrix 26 May – 2 Jun 2026, via search extracts.
[^eea]: Searchind, EEA changes, read 2026-10-27: redesign, comparison-sites unit, paid Shopping unchanged.
[^gmc-audit]: Searchind, Merchant Center audit, read 2026-10-27: title test design, feed-only changes, material most missing, specific categories, auto-created data sources, disapproval CSV, warehouse transfer.
[^brodie-loyalty]: Brodie Clark, 2025-08-13: promotions add-on, 6-month maximum, promotions rejection rate, loyalty markets, Merchant Center over structured data, no organic loyalty reporting.
[^ai-visible]: Searchind, AI visibility, read 2026-10-27: OpenAI and Perplexity merchant programmes.
[^ipr-openai-feed]: iPullRank, 2025-10-20: OpenAI feed spec fields (enable_search, enable_checkout, relationships, q_and_a, model_3d_link), 15-minute updates.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^maps]: Resoneo, Google Maps dissected, Aug 2026: 72 RankSignal values, primary category, identity.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: click-signal families, 13-month history per query and page by country and device, Glue for SERP blocks, compare short visits per page type. No measured ranking effects shown.
[^ipr-zero-click]: iPullRank (Dombrowski), 2026-07-30: Datos clickstream; ad clicks unchanged.
[^gm-organic]: Growth Memo, 2026-10-26: Similarweb modelled visits; AI referrals 2.85 % of SEO traffic in the US.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^bp-intl]: Botpresso, international SEO guide, ≈2023-11 (no publish date shown): relays Mueller on IP redirects and US-based crawling; banner and crawlable language links.
[^ah-aio-france]: Ahrefs, 2026-09-16: France AI Overviews launch 2026-07-22; 963 top-click French domains; 28 days before vs 9 after; control group of domains with < 2 % AI Overview rate; vendor data, short post-window.
[^bc-servers]: Bruce Clay, 2026-06-30: relays Mueller on server location and geotargeting, and Deloitte "Milliseconds Make Millions" (0.1 s mobile speed gain ≈ 10 % more retail spend); agency blog.
[^mt-reddit-tl]: Metehan Yeşilyurt, 2026-06-22: 64.77M Reddit citations, 20 countries, ChatGPT, Perplexity, Google AI Overviews and AI Mode, 1 Mar – 10 Jun 2026; ChatGPT DE share 18.06 % → 1.54 %. Author works at Peec AI.
[^gg-hreflang]: Glenn Gabe, 2025-12-01: informal tests with French, Italian and Spanish queries in 5 assistants; ChatGPT, Perplexity, Claude mostly returned the US-English URL; Copilot 3/3; Gemini only when links requested; AIO less consistent than AI Mode and blue links.
[^lr-techseo]: Lily Ray, Tech SEO Connect 2025 recap, 2025-12-05: Max Prin — hreflang has no effect on Discover; choose domain structure by what the market's SERP shows ("78% of the German SERP was already .de"). Her summary of the talk.
[^gn-intl]: Barry Adams, 2026-09-16: consulting projects; hreflang "hints, not directives"; prefers ccTLDs beyond a few countries (one consultant's news-publisher view); relays Google's localisation docs (duplicates only if main content stays untranslated).
[^ja-multiling]: Jono Alderson, 2025-08-08: opinion, no data; models borrow from other languages or similar companies; anchor pages per language; clean mistranslated mentions.
[^sp-zero-click-countries]: SparkToro with Similarweb, 2026-06-16: desktop+mobile web panel, Jan–Apr 2026 (period label for non-US countries ambiguous), Google app excluded; zero-click share, clicks to Alphabet properties and open-web clicks per 1,000 searches for DE, IT, CA, FR, US, UK.
[^srp-feb-2026-update]: SERPrecon, 2026-02-06: product notes; lexical and semantic metrics fully supported for EN, ES, FR, DE, IT, PT; BM25 and bigram NPMI less accurate for RU, JA, KO, ZH. Vendor data.
