---
type: Playbook
title: Diagnostic tests
description: Repeatable checks, with a symptom-to-test table — exact-term gap, satisfaction per page type, loss by directory, fetching a page as an AI assistant does, feed attribute coverage, country controls, prompt tracking, AI-bot logs, raw vs rendered internal links, daily index status per URL, passage tests with open rerankers, order-swapped LLM comparisons, ChatGPT site: fan-outs, Gemini's indexed view of a page, brand-canon accuracy, AI-invented URLs, Google-selected canonicals, anomaly detection without LLMs and support-type queries.
tags: [seo, geo, method, search-console, ga4, feeds, testing, internal-links, indexing, passages, canonicals, anomaly-detection]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: aleyda-prompts
    resource: "https://www.aleydasolis.com/en/ai-search/ai-search-prompt-library/"
    title: "Aleyda Solis, AI search prompt library (2026; search extracts)"
  - id: aleyda-checklist
    resource: "https://www.aleydasolis.com/en/ai-search/ai-search-optimization-checklist/"
    title: "Aleyda Solis, AI search optimization checklist, 12 steps (updated Sep 2026; search extracts)"
  - id: aleyda-third-party
    resource: "https://www.aleydasolis.com/en/ai-search/third-party-citation-optimization-ai-search/"
    title: "Aleyda Solis, Third-party citation optimization worksheet (2026; search extracts)"
  - id: siege-leader
    resource: "https://www.siegemedia.com/strategy/category-leader-trap"
    title: "Siege Media, The category leader trap (2026-09-25)"
  - id: bing-ai-perf
    resource: "https://blogs.bing.com/webmaster/February-2026/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview"
    title: "Bing Webmaster Blog, AI Performance in Bing Webmaster Tools (public preview, 2026-02-10)"
  - id: ipr-precision
    resource: "https://ipullrank.com/accuracy-vs-precision"
    title: "iPullRank, Accuracy vs precision in prompt tracking (2026-09-17; cites Search Engine Land 12 prompts × 100 runs, Semrush, an SSRN study of ~38,000 responses)"
  - id: ipr-pagespeed
    resource: "https://ipullrank.com/page-speed-impacts"
    title: "iPullRank, Page speed impacts on AI citation (2026-05-08)"
  - id: ipr-fanout
    resource: "https://ipullrank.com/how-ai-mode-works"
    title: "iPullRank, How AI Mode works (2025-05-27) and the free Qforia fan-out tool"
  - id: ipr-agentic-rag
    resource: "https://ipullrank.com/agentic-rag"
    title: "iPullRank, Agentic RAG (2026-05-20; Observable Agentic RAG Audit)"
  - id: ipr-metrics
    resource: "https://ipullrank.com/metrics-for-ai-search"
    title: "iPullRank (Francine Monahan), Metrics for AI search (2025-11-23)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05)"
  - id: mh-spam
    resource: "https://www.mariehaynes.com/august-2025-spam-update/"
    title: "Marie Haynes, August 2025 spam update (2025-10-20)"
  - id: gm-direct
    resource: "https://www.growth-memo.com/p/does-ai-drive-more-direct-traffic"
    title: "Growth Memo, Does AI drive more direct traffic (2026-10-19)"
  - id: gm-plan
    resource: "https://www.growth-memo.com/p/how-to-plan-2027-when-traffic-is"
    title: "Growth Memo, How to plan 2027 when traffic is… (2026-10-05)"
  - id: gm-reasoning
    resource: "https://www.growth-memo.com/p/reasoning-lift-what-happens-to-ai"
    title: "Growth Memo, Reasoning lift (2026-05-18)"
  - id: gm-owners
    resource: "https://www.growth-memo.com/p/does-topical-authority-matter-in"
    title: "Growth Memo, Does topical authority matter in ChatGPT (2026-07-20)"
  - id: qus
    resource: "https://www.resoneo.com/qus-query-expansion-google-and-mysterious-scoring/"
    title: "Resoneo, QUS query expansion and term scoring (Jul 2025)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026)"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6 (Oct 2024)"
  - id: llm-crawler
    resource: "https://think.resoneo.com/sentinel/geo-llm-crawler-report.html"
    title: "Resoneo, LLM crawler test (Jan 2026)"
  - id: gmc-audit
    resource: "https://searchind.com/the-google-merchant-center-audit-i-run-for-every-client/"
    title: "Searchind, The Google Merchant Center Audit I run for every client (Aug 2026)"
  - id: organic-analysis
    resource: "https://searchind.com/organic-seo-analysis-for-ecommerce/"
    title: "Searchind, The complete guide for Search/SEO analysis for eCommerce (Jun 2025, updated Apr 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2026"
  - id: bp-rendered-links
    resource: "https://botpresso.com/python-script-to-find-inlinks-missing-from-rendered-html/"
    title: "Botpresso, Inlinks missing from rendered HTML (≈2023)"
  - id: bp-77k
    resource: "https://botpresso.com/how-did-we-catch-a-77k-url-redirect-on-day-1-with-indexvigil/"
    title: "Botpresso, How we caught a 77K-URL redirect on day 1 (≈2026-10; one enterprise ecommerce case; promotes IndexVigil)"
  - id: mt-rerank
    resource: "https://metehan.ai/blog/rerankers-for-geo-aeo-how-ai-search-chooses-passages-and-sources/"
    title: "Metehan Yeşilyurt, Rerankers for GEO (2026-08-06; 12 open rerankers × 2 passages × 1 query)"
  - id: dj-ablation
    resource: "https://dejan.ai/blog/ablation/"
    title: "DEJAN, Grounding snippet ablation (2026-10-20; tool, 1 query, 1 page, n=188 rankings)"
  - id: dj-embmap
    resource: "https://dejan.ai/blog/gemma-gemini-embeddings/"
    title: "DEJAN, A 300M model predicts Gemini's embeddings at 0.83 cosine (2026-08-14; 199,998 Wikidata labels)"
  - id: dj-firstread
    resource: "https://dejan.ai/blog/rank-signal-recipe/"
    title: "DEJAN, Gemini picks whichever page it reads first 92 % of the time (2026-07-26; 24,445 + 5,200 pairwise votes, synthetic pages)"
  - id: mt-sitequeries
    resource: "https://metehan.ai/blog/reddit-lost-most-its-visibility-chatgpt-site-filled-gap/"
    title: "Metehan Yeşilyurt, Reddit lost its ChatGPT visibility and the site parameter filled the gap (2026-08-21; Peec logs, 14.9M queries/week)"
  - id: mt-sitehack
    resource: "https://metehan.ai/blog/want-real-short-term-ai-visibility-hack-bad-actors-hands/"
    title: "Metehan Yeşilyurt, Hallucinated hostnames in ChatGPT site: fan-outs (2026-08-28; Peec logs, >2M site: queries, 134,922 hostnames, DNS/WHOIS)"
  - id: dj-sitefanout
    resource: "https://dejan.ai/blog/site-fanouts/"
    title: "DEJAN, OpenAI fan-out data shows no rise in site: use (2026-08-25; 551,695 fan-outs, 196,692 OpenAI, via API)"
  - id: dj-notlive
    resource: "https://dejan.ai/blog/googles-still-doesnt-see-your-live-page/"
    title: "DEJAN, Google still doesn't see your live page (2026-05-07; probing, 2 URLs)"
  - id: nz-render
    resource: "https://natzir.com/en/seo/googlebot-full-fetch-render-search-console/"
    title: "Natzir Turrado, Googlebot's full fetch and render in Search Console (2026-09-30; tool/method)"
  - id: mt-gptbot
    resource: "https://metehan.ai/blog/i-built-a-60-000-page-ai-website-for-10-gptbot-crawled-it-30-000-times-in-12-hours/"
    title: "Metehan Yeşilyurt, A 60,000-page site crawled 30,000 times by GPTBot (2026-03-04; server logs, one site)"
  - id: gg-js
    resource: "https://www.gsqi.com/marketing-blog/can-ai-search-platforms-render-javascript/"
    title: "Glenn Gabe (GSQi), Are AI search platforms still unable to render JavaScript? (2026-10-19; 3 test page types × 5 assistants)"
  - id: seer-brand-accuracy
    resource: "https://www.seerinteractive.com/insights/ai-brand-accuracy-study"
    title: "Seer Interactive, AI declined to answer prompts about our brand 31 % of the time (2026-08-27; 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, May 1 – Jun 9 2026, own brand)"
  - id: lr-gullible
    resource: "https://lilyray.nyc/which-ai-search-tools-llms-are-the-most-gullible/"
    title: "Lily Ray, Which AI search tools are the most gullible? (2025-06-17; one planted page, 5 questions, 6 engines, one run)"
  - id: cc-kpis
    resource: "https://www.wix.com/studio/ai-search-lab/ai-search-visibility-kpis"
    title: "Crystal Carter, AI search visibility KPIs (2025-07-29, updated 2025-08-03; Wix AI Search Lab; framework)"
  - id: gg-canonical
    resource: "https://www.gsqi.com/marketing-blog/rel-canonical-hint-cascade-chatgpt/"
    title: "Glenn Gabe, Rel canonical is just a hint — cascade to ChatGPT (2026-02-17; 3 client cases)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: ja-bugreport
    resource: "https://www.jonoalderson.com/conjecture/search-volume-bug-report/"
    title: "Jono Alderson, Sometimes search volume is a bug report (2026-10-17; argument)"
---

# Diagnostic tests

Each test turns a claim from the principles pages ([Google ranking](../how-it-works/google-ranking.md), [AI assistants](../how-it-works/ai-assistants.md)) into a check on your own data. Run the [comparison checklist](search-console.md#1-before-every-comparison) first: pick windows that don't cross a break.

## Which test when

| Symptom or question | Test |
|---|---|
| Specific queries lost clicks or positions | [1](#1-exact-term-gap-on-lost-queries), [2](#2-satisfaction-per-page-type) |
| Pages lost rankings; are visitors disappointed? | [2](#2-satisfaction-per-page-type) |
| Traffic fell during a core or spam update | [3](#3-loss-by-directory), [8](#8-indexed-pages-by-page-type) |
| Indexed page count is falling | [8](#8-indexed-pages-by-page-type) |
| Assistants don't cite or describe a page correctly | [4](#4-fetch-a-page-the-way-an-ai-assistant-does), [12](#12-ai-bot-reliability-in-server-logs), [13](#13-fan-out-coverage) |
| Shopping or product-card visibility is weak | [5](#5-feed-attribute-coverage-and-title-tests) |
| A drop might be a market-specific change | [6](#6-country-or-segment-control) |
| Where to compete; who the competitors are | [7](#7-market-and-competitor-read) |
| How visible are we in AI assistants? | [9](#9-prompt-tracking-per-engine), [14](#14-third-party-citation-audit) |
| Direct traffic jumped | [10](#10-is-a-direct-spike-real) |
| Monthly reporting of SEO and GEO together | [11](#11-monthly-read-exposure-behaviour-outcomes) |
| AI bots fail or time out on pages | [12](#12-ai-bot-reliability-in-server-logs) |
| Which content to write for AI Mode | [13](#13-fan-out-coverage) |
| Full AI-search audit | [15](#15-full-ai-search-audit-skeleton) |
| Links or navigation may exist only after JavaScript runs | [16](#16-raw-vs-rendered-internal-links), [4](#4-fetch-a-page-the-way-an-ai-assistant-does) |
| Migration, redirect or template release coming up or just shipped | [17](#17-daily-index-status-per-url), [16](#16-raw-vs-rendered-internal-links) |
| One URL pattern lost clicks suddenly | [17](#17-daily-index-status-per-url), [3](#3-loss-by-directory) |
| Does a draft section answer the query before it goes live? | [18](#18-passage-test-before-publishing), [13](#13-fan-out-coverage) |
| Comparing two page versions with an LLM as judge | [19](#19-order-swapped-llm-page-comparisons) |
| Which hostnames does ChatGPT search inside for our prompts? | [20](#20-which-sites-does-chatgpt-search-inside), [9](#9-prompt-tracking-per-engine) |
| Page changes don't show up in Gemini or AI Mode | [21](#21-is-the-page-in-geminis-view), [17](#17-daily-index-status-per-url) |
| Assistants state wrong facts about us, or decline to answer | [22](#22-brand-canon-accuracy), [14](#14-third-party-citation-audit) |
| AI user agents or AI referrals land on 404s | [23](#23-ai-invented-urls-on-your-domain), [12](#12-ai-bot-reliability-in-server-logs) |
| Google picks other canonicals, or one country's property loses clicks | [24](#24-google-selected-canonicals-per-page-type), [17](#17-daily-index-status-per-url) |
| Flag unusual days in Search Console or analytics automatically | [25](#25-anomaly-detection-without-llms) |
| Queries about returns, delivery, contact or cancellation rise or fall | [26](#26-support-type-queries) |

## 1. Exact-term gap on lost queries
**Claim tested:** terms missing from title, H1 or slug cost rankings.[^qus]
1. Search Console, query × page, same weeks this year vs last year (both after Sept 2025). Keep non-brand queries with ≥ 15 clicks last year that lost clicks.
2. For each, take the ranking URL and fetch its live title, H1 and slug. Match words case-insensitively; normalise umlauts/ß and hyphens.
3. Add a monthly position series per query to see *when* it slid.
4. Include one control query that didn't drop.

**Reading:** exact phrase present + steady slide → competitor or quality shift, not lexical. Phrase missing + sharp drop → cheap test: add the word to title and H1. **Example:** 6 of 7 lost queries already had their phrase; the one without it was the sharpest drop.[^field-notes] Check archived snapshots for on-page changes in the drop window.

## 2. Satisfaction per page type
**Claim tested:** Google remembers short visits per query and page (NavBoost).[^navboost]
1. Analytics, sessions from organic Google, by landing page (and by device): sessions, engaged sessions, engagement time, add-to-carts, purchases.
2. Classify each URL by path into page types (home, category, product, configurator/tool, editorial, promo, utility). Drop utility pages, `(not set)` and checkout restarts.
3. Compare each page with the **median of its own type** (pages with ≥ 50 sessions), on desktop and mobile separately.
4. Check per template that bounce means something ([analytics](analytics.md#2-page-views-sessions-and-bounce)); if not, use engagement time and add-to-cart rate.

**Reading:** a page far below its type on mobile is a likely "short click" source. A page that lost rankings but satisfies better than its type has a different problem.

## 3. Loss by directory
**Claim tested:** quality is scored per section; sections move together.[^leak-6]
1. Search Console clicks and impressions by first path segment (and second, for big sections), weekly, across the update window.
2. Index each directory to its pre-update average.

For update analysis, compare clicks only, in equal windows on either side of the rollout ([timeline](../reference/google-updates-timeline.md)), sort pages by loss and look for shared directories.[^mh-spam]

**Reading:** directories moving as blocks support a section-level cause (thin URL sets, off-topic sections); scattered single-page losses point to page or query causes.

## 4. Fetch a page the way an AI assistant does
**Claim tested:** assistants read static HTML only, from the top.[^llm-crawler] Gemini is disputed (see the conflict below).
```bash
curl -sL -A "Mozilla/5.0 AppleWebKit/537.36 (KHTML, like Gecko); compatible; ChatGPT-User/1.0; +https://openai.com/bot" https://example.com/category/ -o page.html
```
Check in `page.html`:
- HTTP 200, no bot challenge page.
- H1 present; the first ~200 characters after it state facts (what, attributes, price from, availability).
- Price and key specs present as text, not only in JSON-LD or script.
- robots.txt: which AI user agents are disallowed, and whether a CDN injected rules.

Then ask each assistant (ChatGPT, Claude, Perplexity, Gemini, Copilot) for the first and last paragraph of the page's main content, and compare with the page. In a retest with 3 test page types (main content rendered by JavaScript; static shell with JavaScript main content; parallax/WebGL), ChatGPT, Claude and Perplexity failed all three, Gemini read the content in all three, and Copilot passed the two JavaScript tests but failed WebGL. *Practitioner test, 3 page types × 5 assistants.*[^gg-js] Gemini probably reads Google's rendered index ([test 21](#21-is-the-page-in-geminis-view)), so a pass there says nothing about the other assistants.

> **Conflict:** Gemini listed as static-only in one one-page test vs reading JavaScript content in 3 of 3 page types — [details](../reference/conflicts.md#do-ai-assistants-render-javascript)

Repeat for the top landing pages per template; one bad template affects thousands of URLs.

## 5. Feed attribute coverage and title tests
**Claim tested:** attribute gaps and weak titles cost Shopping and AI visibility.[^gmc-audit]
1. Export the feed; per product category, count items with material, colour, size, specific Google category, and title length.
2. For gaps, check whether the data exists in the shop (feed fix) or not at all (product-data gap).
3. **Title test:** 20–30 products get the new pattern via a feed rule; 20–30 comparable products stay unchanged. Compare impressions and CTR per item in the ad platform's shopping report for 4+ weeks.

## 6. Country or segment control
When an outside change might apply only to some markets (EEA rules, a regional rollout), split the metric by country and use an unaffected country as the control. **Example:** after the EEA free-listings removal, Germany lost 67 % of merchant-listing clicks while Switzerland held — a clean confirmation without access to the platform's own reports.[^field-notes]

## 7. Market and competitor read
Find competitors per intent manually first, then with tools; separate search competitors from commercial ones; compare catalogue depth per category; estimate organic share per category from keyword exports split brand / non-brand. Pick battlefields where competitors are weak. *Practitioner.*[^organic-analysis]

## 8. Indexed pages by page type
**Claim tested:** Google drops pages users don't engage with from the index (seen from 27 May 2025).[^mh-deindex]
1. Search Console page indexing report, exported monthly; classify URLs by page type as in test 2.
2. Track indexed and "Crawled – currently not indexed" counts per type over time. Ignore feed and pagination URLs.
3. For dropped pages: those with backlinks get a 301 to the closest live page; the rest are improved or consolidated.
4. Rule out technical causes first: inspect a sample with "Test live URL"; check that robots.txt doesn't block CSS or JS.

## 9. Prompt tracking per engine
**Claim tested:** visibility differs by engine, mode and between citations and mentions.[^gm-reasoning][^gm-owners]
1. Fix a prompt set per category (20–50 buyer prompts, incl. comparison prompts), and fix engine, model and reasoning mode.
2. Run it on a schedule, logged out; record **citations** (your URL as a source) and **mentions** (your brand recommended) separately, per engine.
3. Note model releases and UI changes next to the series; a jump on a release date is the model, not you.
4. **Repeat each prompt enough times.** Each answer is one sample: across 100 runs of 12 prompts, ChatGPT named about 44 brands per prompt but about 10 per answer, and only ~11 % of brands appeared in 80 % or more of runs.[^ipr-precision] Margin of error on a 50 % appearance rate:

   | Runs per prompt | 5 | 10 | 20 | 50 | 100 |
   |---|---|---|---|---|---|
   | ± points | 44 | 31 | 22 | 14 | 10 |

   Run enough that the interval is narrower than the smallest change you'd act on; report rate ± range. Pin geography, store raw answers, and don't treat API results as the consumer app or logged-in runs as clean (memory). Rewording a prompt can halve visibility (SSRN study, ~38,000 responses).[^ipr-precision]
5. **Size the library.** 30–60 prompts for a single product line, 100–250+ for a multi-product brand; start with 30–50 tagged core prompts per market (ID, group, journey stage, market, language, platform, date, run number), keep experimental prompts apart, build each country's set natively rather than translating one list. Weight non-brand prompts for discovery; use brand prompts to check how accurately you're described.[^aleyda-prompts]

   > **Conflict:** 3–5 runs per core prompt[^aleyda-prompts] vs ±44 points of error at 5 runs[^ipr-precision] — [details](../reference/conflicts.md#how-many-prompt-runs)

## 10. Is a Direct spike real?
Segment Direct by landing page, country, browser, OS and screen size; bots cluster on one landing page, odd screen sizes or one country, with near-zero engagement. Exclude login and pricing pages. Only then look for AI influence — in one study none could be found.[^gm-direct] A self-reported "how did you hear about us" field adds signal no analytics tool can.

## 11. Monthly read: exposure, behaviour, outcomes
Report three layers together and diagnose from how they move relative to each other: **exposure** (AI citations and mentions, Search Console impressions), **behaviour** (branded search, Direct after bot filtering), **outcomes** (orders, revenue). Exposure up with branded search flat suggests a distribution problem; branded search up with outcomes flat points at the site. *Practitioner framework.*[^gm-plan] iPullRank's version splits the same way: inputs (passage relevance, fan-out coverage, bot crawl), channel (share of voice, citation rate and sentiment, mentions), performance (AI-referred sessions and revenue); it adds Bing Webmaster Tools' AI performance report as a citation source.[^ipr-metrics]

## 12. AI-bot reliability in server logs
**Claim tested:** pages AI crawlers time out on don't get cited.[^ipr-pagespeed]
1. Filter server or CDN logs to AI user agents (GPTBot, OAI-SearchBot, ChatGPT-User, ClaudeBot, Claude-User, PerplexityBot, Google-Extended…).
2. Per page type: share of 4xx/5xx and 499 (client closed), response time, cache status (HIT / MISS / BYPASS).
3. Align CDN, load-balancer and origin timeouts; edge-cache HTML for these bots where safe (never cart, checkout, account).
4. Check whether sitemap-only URLs ever get fetched ([why](../how-it-works/ai-assistants.md)). In one new site's logs GPTBot found pages through the XML sitemap alone within minutes.[^mt-gptbot] Verify bots against the vendors' published IP ranges, since user agents get spoofed ([analytics](analytics.md#8-ai-bots-live-in-server-logs-only)).

   > **Conflict:** whether AI crawlers fetch sitemap-only URLs — [details](../reference/conflicts.md#do-ai-crawlers-use-sitemaps)

## 13. Fan-out coverage
**Claim tested:** AI Mode cites the passage that best answers a sub-query, not the top-ranked page.[^ipr-fanout]
1. Generate sub-queries for 5–10 high-value queries with a fan-out simulator (iPullRank's free Qforia) or by logging the queries a deep-research mode runs.[^ipr-agentic-rag]
2. For each sub-query, note which of your pages has a self-contained passage that answers it.
3. Gaps with commercial value are content briefs; gaps you'd answer better with a tool (calculator, configurator, API) are tool briefs.

## 14. Third-party citation audit
**Claim tested:** most AI citations come from third parties, and stale listings undercut your own claims.[^aleyda-third-party][^siege-leader]
1. From the prompt runs (test 9) and Bing Webmaster Tools' AI Performance report (page-level citations for Copilot),[^bing-ai-perf] list every third-party domain cited for your category prompts: marketplaces, review sites, affiliates, roundups, forums, video.
2. For each, check whether you're listed and whether the facts match your site and feed (price range, assortment, returns, delivery, location).
3. Fix or refresh the listings you control; before cutting an affiliate or roundup listing, check whether it is cited.

## 15. Full AI-search audit skeleton
Aleyda Solis' 12-step checklist works as the outline: steps 1–2 measure presence (tests 9 and 14), steps 3–10 diagnose readiness — owned content, extractability (direct answer first, clear headings, self-contained sections), entities, third-party corroboration, commercial data (price, stock, feeds, schema and policies kept consistent), localisation — and steps 11–12 report business impact and validate the result (test 11).[^aleyda-checklist] Each readiness step maps to a page here: [AI assistants](../how-it-works/ai-assistants.md), [product pages](../page-types/product-pages.md), [category pages](../page-types/category-pages.md), [third-party presence](../channels/third-party-presence.md), [feeds and Merchant Center](../channels/feeds-and-merchant-center.md), [technical foundations](../technical/technical-foundations.md).

## 16. Raw vs rendered internal links
**Claim tested:** links that exist only in the rendered HTML are invisible to AI bots and to some crawlers.[^bp-rendered-links] AI assistants read static HTML only.[^llm-crawler]
1. Per template, pick a few URLs (category with subcategories, product, editorial).
2. Collect internal links from the raw HTML (view-source, or a plain fetch as in [test 4](#4-fetch-a-page-the-way-an-ai-assistant-does)).
3. Collect internal links from the rendered HTML (Search Console URL Inspection → rendered HTML, or the Rich Results Test).
4. Diff the two sets per URL: list links present only after rendering, and note which part of the page holds them (navigation, subcategory block, related products, pagination).

**Reading:** links only in the rendered set are missed by AI crawlers and by crawlers that don't render. If they carry subcategories, pagination or related products, move them into the server-rendered HTML ([internal linking](../technical/internal-linking.md), [JavaScript](../technical/technical-foundations.md#7-javascript)). *Practitioner method.*[^bp-rendered-links]

## 17. Daily index status per URL
**Claim tested:** Search Console's aggregate reports show a decline but not which URLs changed state, or when; a daily per-URL check does.[^bp-77k]
1. Before a migration, redirect batch or template change, export every indexed URL pattern that earns clicks — legacy patterns included — and pick the URLs to watch (all of them for small sets, a sample per pattern for large ones).
2. Query the Search Console URL Inspection API daily for each: coverage state ("Indexed", "Page with redirect", …), the reason, and the last crawl date.
3. Store each day's result and alert on the same day when URLs of one pattern change state.
4. Join with clicks per URL from the Search Analytics export to size the impact.

**Reading:** a block of URLs moving from "Indexed" to "Page with redirect" on dated crawls points to a redirect rule, not a quality or update effect. **Example:** a developer's bulk redirect hit a legacy template of 77,493 URLs that had earned 8.23K clicks and 196K impressions in the prior 3 months; Search Console showed only the decline, the daily per-URL check showed each URL's change of state on a dated crawl. *Practitioner, one case, vendor promoting its tool.*[^bp-77k] See [migration](../situations/migration.md#5-monitoring-after-launch).

## 18. Passage test before publishing
**Claim tested:** rerankers and grounding pick the passage that answers the query directly, and one specific sentence carries most of the effect.[^mt-rerank][^dj-ablation]
1. Pick the target query and 2–4 of its sub-queries ([test 13](#13-fan-out-coverage)); take the draft section and a rival version (e.g. descriptive vs direct-answer first sentence).
2. Score each passage against each query with 2–3 open rerankers (e.g. a MiniLM cross-encoder and Qwen3-Reranker-0.6B). In one small test the direct-answer passage beat the descriptive one by MiniLM-L6 0.0019 % vs > 99.9 % and Qwen3-Reranker-0.6B 0.27 % vs > 99.9 %; missing query concepts hurt more than word order. Classic BERT rerankers see only 512 tokens. *Measured, small controlled test, reproducible with open models; no evidence that ChatGPT uses these models.*[^mt-rerank]
3. **Ablation:** remove one sentence at a time and re-score to find the sentence that carries the answer. In one tool run (1 query, 1 page, n=188) one specific factual sentence was worth +4.10 ± 0.10 of 5 rank places, 20 % of the text held 80 % of the gain, repeating the brand name 4× added +0.10 ± 0.10 (≈ 0) and a tangential sentence cost −0.20. *Measured, one query, paid tool.*[^dj-ablation]

**Reading:** keep and sharpen the answering sentence (entity named, decision criteria covered, answer first); cut off-topic promo lines; don't repeat the brand for effect. Scores are relative, between versions of your own passage — not a prediction of any engine's ranking. **Don't** use proxy embeddings to predict Gemini's order: a linear map from a 300M open model to Gemini's embeddings reached 0.831 cosine but recovered only 39 % of the true top-10 neighbours, so rank order doesn't transfer; use them only for coarse topical checks. *Measured.*[^dj-embmap] Why passages matter: [AI assistants](../how-it-works/ai-assistants.md).

## 19. Order-swapped LLM page comparisons
**Claim tested:** an LLM judging two pages favours the one it reads first.[^dj-firstread]
1. When you ask an LLM which of two pages (yours vs a competitor's, or two drafts) better answers a query, run it twice: A then B, and B then A.
2. Repeat each order several times; record the model and whether thinking was on.
3. Count a win only if it survives both orders.

**Reading:** with synthetic ~500-word pages, Gemini as grounding judge picked the page read first 92.4 % of the time, and 215 of 260 pairs flipped winner when the order was reversed; pages rewritten to 31 factors won 15.2 % of second-slot cases (396/2,600) vs 0/2,600 unguided (50.7 % with thinking on). *Measured, synthetic pages, one model.*[^dj-firstread] Retrieval order dominates and content breaks ties: a single-order test mostly measures position, and in production, ranking in the retrieved set comes first.

## 20. Which sites does ChatGPT search inside?
**Claim tested:** ChatGPT runs `site:` searches inside official brand sites, docs, help centres and review platforms, so facts missing from your own pages can't be found there.[^mt-sitequeries]
1. Run your category and brand prompts in the consumer app, with realistic long prompts as well as short ones, and capture the fan-out queries (browser developer tools on the app, or a tracker that logs fan-outs; API results differ) (*inference*).
2. List every `site:` query and its hostname: is your own domain among them, and which review platforms or competitors are?
3. For each `site:` query on your domain, check that the answer (specs, delivery, returns, prices) exists as text on a crawlable page.
4. List hostnames that look like your brand but aren't yours (hyphenated or other-TLD variants). ChatGPT sometimes invents such hostnames for `site:` searches; citations still pointed at the real domain, but 4 unregistered domains appeared 100+ times and ~104 appeared 10–99 times in one vendor's logs. *Measured, vendor data, case-level.*[^mt-sitehack] Register and redirect obvious variants of your own brand — never other brands'.

**Reading:** in consumer-app logs `site:` fan-outs rose from < 0.11 % to 26.2 % of weekly queries in August 2026, mostly aimed at official brand sites, docs, help centres and review platforms, < 1 % at reddit.com (*measured, vendor data, not reproducible outside the vendor*);[^mt-sitequeries] API data shows 0.15–6 % depending on model, and long ad-hoc prompts produce 7–91× more `site:` queries than short tracking prompts.[^dj-sitefanout] Date-stamp results with the model version ([AI-visibility tracking](ai-visibility-tracking.md#11-re-baseline-at-every-model-change)).

> **Conflict:** 26.2 % (consumer app) vs 0.15–6 % (API) `site:` fan-outs — [details](../reference/conflicts.md#how-often-does-chatgpt-search-inside-sites)

## 21. Is the page in Gemini's view?
**Claim tested:** Gemini and AI Mode read Google's indexed copy of a page, not the live page.[^dj-notlive]
1. Search Console URL Inspection: is the URL indexed, and when was it last crawled? A change made after the last crawl isn't in Gemini's view yet.
2. Open the indexed page's rendered HTML (not only the live test) and check that below-the-fold product grids, internal links and lazy-loaded images exist there. Limits seen in the tool: live-test screenshots cut at ~1,750 px; stored rendered HTML keeps the first 100,000 nodes; Googlebot doesn't scroll, so images lazy-loaded below the viewport or by script fail; Shadow DOM is flattened. *Tool observation.*[^nz-render]
3. Optionally ask Gemini about the URL through its URL access: for unindexed pages it returned `URL_FETCH_STATUS_NOT_IN_SEARCH_INDEX` or `URL_FETCH_STATUS_EMPTY_CONTENTS_IN_INDEX`. *Measured, probing, 2 URLs.*[^dj-notlive]

**Reading:** if the URL isn't indexed, or the content sits beyond the stored rendered HTML, Gemini can't use it — fix indexing and rendering first ([test 16](#16-raw-vs-rendered-internal-links), [test 17](#17-daily-index-status-per-url), [JavaScript](../technical/technical-foundations.md#7-javascript)). Live-test tools don't show what Gemini sees; expect changes in Gemini and AI Mode only after a recrawl.

## 22. Brand canon accuracy
**Claim tested:** assistants more often decline to answer brand questions than get them wrong; wrong answers come from stale profiles; and made-up claims on poorly covered questions get repeated.[^seer-brand-accuracy][^lr-gullible]
1. Write the brand canon: 20–50 checkable facts, with the correct answer and the page that states it — locations and pickup, delivery countries and times, returns, payment options, services offered and not offered, assortment boundaries — plus a few obscure attributes few pages cover (e.g. a minimum order or a service you don't offer) (*inference for the shop list*).
2. Turn each fact into a direct prompt and a comparative one ("does X or Y offer…"); run them monthly per engine, several runs each, from a clean account ([AI-visibility tracking](ai-visibility-tracking.md#10-what-prompt-trackers-dont-tell-you)).
3. Score every answer accurate / wrong / no answer; for wrong answers, record the cited source.
4. Fix your own pages first, then the profiles the wrong answers cite; re-run after the next crawl.

**Reading:** in one B2B brand's own study (28,123 responses, 6 AI surfaces), answers were accurate 95.9 % of the time when given, but 31.2 % of prompts got no answer and 2.8 % were wrong; comparative prompts were only 18.8 % accurate because 80.3 % went unanswered, and wrong answers traced back to stale profiles. *Measured, one brand.*[^seer-brand-accuracy] A high no-answer rate means missing facts, not bad ones. In a one-run test, a page with made-up claims on questions nobody else covered was indexed "within 12 hours" and repeated "within 24 hours"; AI Mode used it for 4 of 5 questions, AI Overviews, Gemini, ChatGPT and Perplexity for 2 each (Perplexity once without a caveat), Claude for none; engines that sought agreement across sources resisted more. *Measured, one run.*[^lr-gullible] So publish correct facts early, on your own pages, for brand and product questions nobody covers, and keep the obscure attributes in the monthly check. Tracking series: [AI-visibility tracking](ai-visibility-tracking.md#13-brand-canon-accurate-wrong-no-answer).

## 23. AI-invented URLs on your domain
**Claim tested:** AI bots and assistants send traffic to URL paths on your own domain that never existed.[^cc-kpis]
1. Monthly, filter server or CDN logs for AI user agents (ChatGPT-User, OAI-SearchBot, PerplexityBot, Perplexity-User, Claude-User…) and AI referrers (chatgpt.com, perplexity.ai, gemini.google.com, claude.ai, copilot.microsoft.com) on 404 responses.
2. Group by path and count; keep paths that recur across days or sources.
3. 301 recurring invented paths to the closest real page (same product, category or policy); leave one-offs as 404.

**Reading:** recurring invented paths show what assistants expect your URLs to be — often a product or policy page they describe but can't find. *Practitioner.*[^cc-kpis] Invented hostnames in ChatGPT's `site:` searches are a separate check ([test 20](#20-which-sites-does-chatgpt-search-inside)); bot reliability on real URLs is [test 12](#12-ai-bot-reliability-in-server-logs).

## 24. Google-selected canonicals per page type
**Claim tested:** `rel=canonical` is a hint; Google's chosen canonicals may differ from yours, and the choice carries over into AI citations.[^gg-canonical]
1. Per page type (and per country version where markets share a language), sample URLs and read the user-declared and Google-selected canonical through the URL Inspection API (quota in [Search Console](search-console.md#15-url-inspection-api-quota)).
2. Count mismatches per page type and per country; note whether Google's choice is a weaker page (filter, sort, print or secondary version) or another country's URL.
3. Make sure every subdomain is a verified property, so pages on forgotten subdomains are visible too.
4. Where Google picks pages meant only for on-site users, test `noindex` on those pages rather than relying on the canonical alone.

**Reading:** in one case Google chose weaker secondary pages as canonical on "tens of thousands" of URLs; the canonical tag alone didn't fix it, `noindex` on the pages meant only for on-site users did. Google's chosen canonicals carried over into ChatGPT's citations (*inference*). *Practitioner, 3 cases.*[^gg-canonical] With same-language hreflang, Google may canonicalise to the other country while showing the right URL, and Search Console then credits clicks to the canonical — a false loss in one country's directory property ([Search Console](search-console.md#14-same-language-hreflang-clicks-go-to-the-canonical)).

## 25. Anomaly detection without LLMs
**Claim tested:** LLMs hallucinate when they read tables of numbers; statistical models flag anomalies reliably.[^lr-techseo]
1. Export daily series: Search Console clicks and impressions per page type or directory; analytics sessions, add-to-carts and orders per channel.
2. Flag outliers with Isolation Forest or Local Outlier Factor (features: value, day of week, change vs the previous 7 days), or forecast each series and flag large residuals.
3. Let an LLM write and explain the code; don't paste the tables into an LLM to "spot" anomalies.
4. Review each flagged day against your caveats list and the [Google updates timeline](../reference/google-updates-timeline.md) before acting.

**Reading:** a flag is a prompt to look, not a finding; rule out tracking breaks and bot days first ([analytics](analytics.md#11-anomaly-detection-without-llms)). *Practitioner, relayed talk summary.*[^lr-techseo]

## 26. Support-type queries
**Claim tested:** some search volume is caused by the business — hidden contact details, cancellation, pricing, compatibility — and works as a bug report.[^ja-bugreport]
1. Tag query clusters in Search Console that signal a problem, not demand: returns, delivery, order tracking, contact, cancellation, compatibility (shop clusters are *inference*).
2. Ask of each: "would we be happy if this volume doubled?" If not, it's support-type.
3. Route each cluster to its owner (customer service, product, checkout) with the landing pages it hits.
4. Report these clusters apart from SEO demand; a decline after a fix is a success, not an SEO loss.

**Reading:** fixing the cause can lower traffic. *Practitioner, argument.*[^ja-bugreport] Related but different: queries people use to check out an unfamiliar shop ([Search Console](search-console.md#11-brand-verification-queries)).

Related: [Search Console](search-console.md), [analytics](analytics.md), [AI-visibility tracking](ai-visibility-tracking.md), [rank tracking](rank-tracking.md), [sources and confidence](../reference/sources-and-confidence.md), [traffic drop](../situations/traffic-drop.md), [core-update recovery](../situations/core-update-recovery.md).

[^qus]: Resoneo, QUS, 2025-07-22: per-term scoring, title weight.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: compare short visits per page type; memory per device.
[^leak-6]: Resoneo, leak part 6, 2024-10-31: section-level scores, new pages inherit the section average.
[^llm-crawler]: Resoneo, LLM crawler report, Jan 2026: static HTML only for ChatGPT-User, Claude-User, Gemini, Perplexity-User.
[^gmc-audit]: Searchind, Merchant Center audit: title test on 20–30 products, feed-only changes.
[^organic-analysis]: Searchind, organic analysis guide: manual competitor discovery per intent, catalogue depth, organic share per category.
[^aleyda-prompts]: Aleyda Solis, 2026, via search extracts (direct fetch blocked): library sizes, tagging, 3–5 runs in 24–72 h.
[^aleyda-checklist]: Aleyda Solis, checklist updated Sep 2026 and 3-layer framework, via search extracts.
[^aleyda-third-party]: Aleyda Solis, third-party citation worksheet and AI search citations study (2026-08-02), via search extracts.
[^siege-leader]: Siege Media, 2026-09-25: affiliate and sponsorship sites among the most-cited domains.
[^bing-ai-perf]: Bing Webmaster Blog, 2026-02-10: page-level citations, grounding-query sample.
[^ipr-precision]: iPullRank, 2026-09-17: Search Engine Land (Sonders) 12 prompts × 100 runs, logged-out ChatGPT; binomial margins; Semrush Instant vs Thinking; SSRN study on prompt wording.
[^ipr-pagespeed]: iPullRank, 2026-05-08: Profound 700K pages; log segmentation and caching advice.
[^ipr-fanout]: iPullRank, 2025-05-27: fan-out patents, passage selection; Qforia tool.
[^ipr-agentic-rag]: iPullRank, 2026-05-20: Observable Agentic RAG Audit (5 queries through deep-research modes, log sub-queries).
[^ipr-metrics]: iPullRank (Monahan), 2025-11-23, and Google AI search guidance post (2026-05-18): three-tier metrics, custom GA4 channel group, log analysis, Bing AI performance.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites.
[^mh-spam]: Marie Haynes, 2025-10-20: click-only comparison, pages sorted by loss, shared directories.
[^gm-direct]: Growth Memo, 2026-10-19: bot segmentation, placebo-tested correlations, self-reported attribution.
[^gm-plan]: Growth Memo, 2026-10-05: exposure / behaviour / outcome framework (opinion); zero-click 60.45 % (2024) → 68.01 % (early 2026) per SparkToro/Similarweb.
[^gm-reasoning]: Growth Memo, 2026-05-18: sources and fan-out change with reasoning mode.
[^gm-owners]: Growth Memo, 2026-07-20: citations and mentions barely correlate.
[^field-notes]: Anonymised shop, Oct 2026: exact-term test on 7 lost queries; EEA country split.
[^bp-rendered-links]: Botpresso, ≈2023 (no publish date shown): Python script diffing inlinks in raw vs rendered HTML; practitioner method.
[^bp-77k]: Botpresso, ≈2026-10: one enterprise Magento migration; daily URL Inspection API checks; the agency promotes its own monitoring tool.
[^mt-rerank]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2026-08-06: 12 open rerankers × 2 passages × 1 query; direct-answer vs descriptive passage; small controlled test, reproducible with open models; no evidence ChatGPT uses these rerankers.
[^dj-ablation]: DEJAN, 2026-10-20: grounding-snippet ablation tool, 1 query, 1 page, n=188 rankings; paid tool.
[^dj-embmap]: DEJAN, 2026-08-14: linear map EmbeddingGemma-300m → gemini-embedding-001 on 199,998 Wikidata labels, 50k held out; 0.831 cosine, 39 % of true top-10 neighbours recovered, cosine band 0.08 wide.
[^dj-firstread]: DEJAN, 2026-07-26: 24,445 + 5,200 pairwise votes on synthetic ~500-word pages, Gemini as grounding judge; 92.4 % first-read wins; 215/260 pairs flipped; 31-factor rewrites 396/2,600 vs 0/2,600; one model.
[^mt-sitequeries]: Metehan Yeşilyurt (works at Peec AI), 2026-08-21: Peec consumer-app logs, 14.9M queries a week; `site:` share < 0.11 % (mid-May – late Jul 2026) → 26.2 % (week of Aug 10), daily peak ~29.2 %; targets mostly official brand sites, docs, help centres, review platforms; < 1 % reddit.com; not reproducible outside Peec.
[^mt-sitehack]: Metehan Yeşilyurt (works at Peec AI), 2026-08-28: Peec logs, > 2M `site:` queries, 134,922 hostnames, DNS/WHOIS checks; case-level.
[^dj-sitefanout]: DEJAN, 2026-08-25: 196,692 OpenAI fan-outs via the API; `site:` share 5–6 % on gpt-5.2 / 5.4, 0.15 % on gpt-5.5; long ad-hoc prompts 7–91× more `site:` queries than short tracking prompts; consumer app not tested.
[^dj-notlive]: DEJAN, 2026-05-07: probing Gemini's URL access with 2 URLs; fetch statuses for unindexed pages.
[^nz-render]: Natzir Turrado, 2026-09-30: tool/method for Search Console's fetch and render; screenshot cut ~1,750 px, 100,000-node limit, no scrolling, Shadow DOM flattened.
[^mt-gptbot]: Metehan Yeşilyurt (works at Peec AI), 2026-03-04: server logs of one new site; GPTBot found it through the XML sitemap with no links.
[^gg-js]: Glenn Gabe (GSQi), 2026-10-19: 3 test page types (JS main content; static shell + JS main; parallax/WebGL) × 5 assistants; ChatGPT, Claude, Perplexity failed all three; Gemini passed all three; Copilot passed the two JS tests, failed WebGL; the first-and-last-paragraph prompt is this playbook's way of repeating the check.
[^seer-brand-accuracy]: Seer Interactive, 2026-08-27: own (B2B) brand; 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, 2026-05-01 – 2026-06-09; accurate 95.9 % when answered, no answer 31.2 %, wrong 2.8 %; comparative prompts 18.8 % accurate, 80.3 % unanswered; wrong answers from stale profiles.
[^lr-gullible]: Lily Ray, 2025-06-17: one planted page, 5 questions, 6 engines, one run; indexed within 12 h, repeated within 24 h; AI Mode 4/5, AI Overviews 2, Gemini 2, ChatGPT 2, Perplexity 2 (once without caveat), Claude 0.
[^cc-kpis]: Crystal Carter, Wix AI Search Lab, 2025-07-29 (updated 2025-08-03): AI bots and assistants hitting invented URL paths; monthly log filter and 301s for recurring paths; framework, no measurements.
[^gg-canonical]: Glenn Gabe (GSQi), 2026-02-17: 3 client cases; Google chose weaker secondary pages on "tens of thousands" of URLs; noindex on on-site-only pages fixed it, canonical alone didn't; carry-over to ChatGPT citations is his inference; same-language hreflang case with relayed Google confirmation.
[^lr-techseo]: Lily Ray, 2025-12-05, summarising Sam Torres' Tech SEO Connect talk: LLMs hallucinate reading numeric tables; Isolation Forest, Local Outlier Factor or forecast residuals for GSC/GA4 anomalies; LLM writes the code.
[^ja-bugreport]: Jono Alderson, 2026-10-17: argument; support-type query volume (hidden contact, cancellation, pricing, compatibility); "double the volume" test; fixing it can lower traffic.
