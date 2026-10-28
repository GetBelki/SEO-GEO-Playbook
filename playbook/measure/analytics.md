---
type: Checklist
title: Analytics
description: Where web analytics under- and over-counts — missing orders, payment redirects, double page views, session bugs, meaningless bounce, click IDs lost in redirects, Performance Max channel quirks, paused feeds, engagement benchmarks, self-reported attribution, AI-assistant referrals (referrers, UTMs, bots, server-log checks, conversion value), speculative prefetch hits and anomaly detection without LLMs.
tags: [measurement, ga4, google-ads, tracking, attribution, caveats, ai-assistants, server-logs, anomaly-detection]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays Google confirmations and third-party studies)"
  - id: siege-engagement
    resource: "https://www.siegemedia.com/research/ga4-engagement-rate-benchmarks"
    title: "Siege Media, GA4 engagement rate benchmarks (2026-08-26; 546 GA4 properties, >16B sessions)"
  - id: siege-attribution
    resource: "https://www.siegemedia.com/strategy/how-to-track-geo-attribution"
    title: "Siege Media, How to track GEO attribution (2026-10-16; single-company case)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: nz-aimeas
    resource: "https://natzir.com/en/analytics/ai-traffic-measurability/"
    title: "Natzir Turrado, The state of AI traffic measurability (2026-05-17, updated to 2026-10; server logs vs GA4 on several sites)"
  - id: dj-grounding
    resource: "https://dejan.ai/blog/grounding/"
    title: "DEJAN, How AI search grounding works: Google vs OpenAI vs Anthropic (2026-06-13; probing, 1 query)"
  - id: mt-gptbot
    resource: "https://metehan.ai/blog/i-built-a-60-000-page-ai-website-for-10-gptbot-crawled-it-30-000-times-in-12-hours/"
    title: "Metehan Yeşilyurt, A 60,000-page site crawled 30,000 times by GPTBot (2026-03-04; server logs, one site)"
  - id: bc-llm-vs-search
    resource: "https://www.bruceclay.com/blog/llms-vs-search-engines-whos-winning/"
    title: "Bruce Clay, LLMs vs search engines (2025-12-09; cites SSRN 5585812, Amsive, SALT.agency)"
  - id: ja-specevil
    resource: "https://www.jonoalderson.com/performance/speculation-rules-for-evil/"
    title: "Jono Alderson, Speculation rules for evil (2026-04-14; technical argument, no measurements)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
---

# Analytics

Which analytics numbers can't be taken at face value — orders, page views, sessions, bounce, ad attribution — and how to correct for them. Examples are from one anonymised shop.[^field-notes] Run the [comparison checklist](search-console.md#1-before-every-comparison) first.

## Rules
- **Never present analytics purchases as all orders;** reconcile against the shop or order-system total once a quarter, state the ratio, and check outlier orders and known platform-bug days before reporting a month or a small channel. *Practitioner, relayed* — [section 1](#1-analytics-doesnt-see-every-order)
- **Exclude windows with page-view or session bugs** from session, conversion-rate and item-view analyses, and drop `(not set)` landing pages and checkout restarts. *Practitioner* — [section 2](#2-page-views-sessions-and-bounce)
- **Check per template that bounce means something;** where it doesn't, use engagement time and add-to-cart rate. *Practitioner* — [section 2](#2-page-views-sessions-and-bounce)
- **Test every ad landing URL with a test click ID weekly** and re-verify ad conversions after every checkout release. *Practitioner* — [section 3](#3-ads-and-attribution)
- **Treat windows with a paused feed or a bidding-behaviour change as no baseline** for paid revenue, AOV or ROAS. *Practitioner* — [section 3](#3-ads-and-attribution), [section 4](#4-feeds)
- **Compare engagement with benchmarks only after correcting for your own tracking breaks.** *Measured* — [section 5](#5-engagement-benchmarks)
- **Ask buyers how they heard of you after purchase,** with an "AI assistant" option. *Practitioner, single case* — [section 6](#6-self-reported-attribution)
- **Bot-filter the AI channel and read AI referrals next to server logs;** most assistant clicks arrive without a referrer and some tagged visits are bots. Count AI bots only from server or CDN logs, verified against the vendors' published IP ranges — client-side trackers see none. *Measured; one site for the bot logs* — [section 7](#7-ai-assistant-referrals-referrers-utms-and-bots), [section 8](#8-ai-bots-live-in-server-logs-only)
- **Log `Sec-Purpose` and exclude speculative prefetch hits from demand counts** (site search, add-to-cart). *Practitioner, no measurements* — [section 10](#10-speculative-prefetch-hits)
- **Find anomalies with statistical models, not an LLM reading tables of numbers;** let the LLM write the code. *Practitioner, relayed* — [section 11](#11-anomaly-detection-without-llms)

## 1. Analytics doesn't see every order
- Consent decliners, blockers and tracking protection hide a share of orders. Example: GA4 captured ~83 % of real orders. Never present analytics purchases as "all orders"; compare against the shop or ERP total once a quarter and state the ratio.
- **Payment redirects** can lose revenue. Example: purchases via a card provider's redirect were tracked at 0 € for a year; year-on-year revenue stayed unusable until a full clean year had passed.
- **Orders completed on Google** (buy-now / UCP checkout, spreading through 2026) never reach the shop's analytics. Reconcile them from Merchant Center or the order system ([feeds and Merchant Center](../channels/feeds-and-merchant-center.md)).
- **Platform bugs.** A widespread GA4 bug zeroed traffic on 1 Sep 2026.[^ignite-news] Check your own data for that day before reading September trends.
- **Single faulty conversions** (one order with a wrong 5-figure value) distort a small channel's month. Check outliers before reporting.

## 2. Page views, sessions and bounce
- **Double page views.** Example: GTM page views plus enhanced-measurement history changes counted each in-shop navigation twice for years; views per session halved on the day of the fix. Sessions, users and purchases were unaffected; bounce rate moved 1–2 points.
- **Session bugs.** Example: a code bug inflated sessions by 20–37 % for a month with no extra purchases. Exclude such windows from session, conversion-rate and item-view analyses.
- **Consent banner redesigns** change how much traffic is tracked; absolute users and sessions are only partly comparable for about a year.
- **Bounce rate can be meaningless per template.** Example: product and configurator pages showed 0–2 % bounce because something marked almost every session as engaged on arrival. Use engagement time and add-to-cart rate there ([test 2](diagnostic-tests.md#2-satisfaction-per-page-type)).
- **`(not set)` landing pages** (7.5 % of organic sessions in one example) and session restarts inside checkout must be excluded from landing-page analyses.

## 3. Ads and attribution
- **Redirects that drop click IDs.** Example: some old URLs redirected without the query string, so ad clicks lost gclid and UTM and neither the ad platform nor analytics could attribute them; affected campaigns were undercounted for months. Check every ad landing URL with a test gclid weekly.
- **Performance Max in GA4** lands in "Cross-network", not "Paid Search". Compare the two only combined, or use source / medium `google / cpc`.
- **Cost by date in GA4.** Example: querying `advertiserAdCost` together with a date dimension repeated the range total on every row; query one date range per month instead. Microsoft Ads costs aren't in GA4 at all.
- **Checkout rebuilds break ad conversions.** Example: after a checkout rebuild, Google Ads and Microsoft Ads conversion tracking stayed broken for 6–8 months. Re-verify conversions after every checkout release.
- **Microsoft UET** in a tag manager setup may fire only on the first page of a visit, undercounting pages and page-based audiences.
- **Configurator and cut-to-size items** often aren't real SKUs; SKU-level analysis then hides a large share of item revenue.
- **Bidding behaviour changes.** Example: from mid-August 2026 budget-limited tROAS / tCPA campaigns spent toward their target instead of beating it; platform ROAS before and after is not comparable, and ROAS ≈ target afterwards is expected, not a decline.

## 4. Feeds
- **A paused feed** removes sale prices and products from Shopping and Performance Max; paid AOV and revenue in that window are no baseline. Feed setup in [feeds and Merchant Center](../channels/feeds-and-merchant-center.md).

## 5. Engagement benchmarks
- Median GA4 engagement rate across 546 properties: 51 %; organic 63.4 %, paid search 60.4 %, AI assistant 60.3 %, direct 45.7 %; ecommerce and retail 54.4 %; desktop 55.3 %, mobile 48.8 %.[^siege-engagement] Compare your own only after correcting for your tracking breaks.

## 6. Self-reported attribution
- In one company, analytics credited about 5 % of pipeline to AI while a "how did you hear about us" field showed far more; branded Search Console queries lagged citation gains by 30–60 days. *Single case.*[^siege-attribution]
- For shops, ask after purchase (on the confirmation page, never before checkout) with an "AI assistant" option. AI-traffic channel set-up is in [AI-visibility tracking](ai-visibility-tracking.md).

## 7. AI-assistant referrals: referrers, UTMs and bots
What server logs show that analytics misses, from logs compared with GA4 on several sites. *Measured.*[^nz-aimeas]
- **ChatGPT:** web citations carry `utm_source=chatgpt.com`, but 96–99 % arrive without a referrer; free-plan inline links and app clicks land in Direct. When OpenAI's search was probed through the API, cited links carried `utm_source=openai` — segment that source too. *Measured, probing, one query.*[^dj-grounding]
- **Claude** uses dated referral paths (`claude.ai/referral/YYYY-MM-DD`); group them under one source.
- **Gemini:** the iOS app (user agent `GeminiiOS`) lands in Direct. Google's grounding citations are wrapped in `vertexaisearch.cloud.google.com/grounding/...` links.[^dj-grounding]
- **GA4 "AI Assistant" channel** since 13 May 2026 (dated May 2026 elsewhere); channel definition in [AI-visibility tracking](ai-visibility-tracking.md#4-one-channel-definition).
- **UTM bug, 7–16 Oct 2026:** ChatGPT-attributed visits fell 68–74 % in server logs and 20–60 % in GA4. Mark the window as a gap ([AI-visibility tracking](ai-visibility-tracking.md#2-untagged-by-accident)).
- **Bots inside the AI channel:** on one site up to 35 % of visits tagged chatgpt.com were bots (data-centre IPs, outdated user agents). ChatGPT-User fetches 2–7× more pages than the visits it sends.
- **Do:** bot-filter the AI channel (data-centre IPs, outdated user agents, zero engagement) and read AI referrals together with server logs.

## 8. AI bots live in server logs only
- In one site's logs GPTBot found a new site through its XML sitemap within minutes, with no links: 29,000+ requests in 12 hours, ~470× Googlebot; in a 3-hour snapshot OAI-SearchBot made 94 requests and ChatGPT-User 1. A client-side tracker on the same site saw zero bots. *Measured, one site; author works at Peec AI.*[^mt-gptbot]
- User agents get spoofed: verify AI bots against the vendor's published IP ranges, from server or CDN logs. Log checks per page type: [test 12](diagnostic-tests.md#12-ai-bot-reliability-in-server-logs); crawler reference: [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).

> **Conflict:** whether AI crawlers fetch URLs found only in sitemaps — [details](../reference/conflicts.md#do-ai-crawlers-use-sitemaps)

## 9. Does AI-referred traffic convert?
- An SSRN paper (5585812), as relayed by Bruce Clay: 50,000+ ChatGPT-referred transactions vs 164 million from other channels across nearly 1,000 ecommerce sites; LLM traffic was "about 200x smaller than Google organic" and "under 0.2% of total traffic", and ChatGPT referrals converted worse and earned less per visit than every major channel except paid social. Amsive (same post): LLMs 0.24 % of sessions and 0.42 % of conversions vs organic 31.88 % / 33.8 %. *Measured, relayed; the post's text contradicts its charts in places — check the paper before quoting.*[^bc-llm-vs-search]
- **Do:** report AI-referred conversion rate and revenue per visit for your own site, per vertical, next to organic ([AI-visibility tracking](ai-visibility-tracking.md#5-scale-of-the-channel)).

> **Conflict:** ChatGPT referrals convert worse (SSRN, ~1,000 shops) vs far better or at parity in other samples — [details](../reference/conflicts.md#does-ai-traffic-convert-better)

## 10. Speculative prefetch hits
- Speculation rules let a page tell the browser to prefetch or prerender other URLs. A third-party page can point them at your uncached URLs (internal search such as `/search?q=*`, add-to-cart URLs such as `/cart?add-to-cart=*`), which creates real-browser load on your server. These requests carry `Sec-Purpose: prefetch` (often with no referrer), and there is no cross-site opt-out yet. *Practitioner, technical argument, no measurements.*[^ja-specevil]
- **Do:** log the `Sec-Purpose` header; serve speculative hits on search and cart URLs cheaply or rate-limit them; exclude them from demand counts such as internal-search volume and add-to-cart totals.[^ja-specevil] Your own speculation rules: [performance and caching](../technical/performance-and-caching.md).

## 11. Anomaly detection without LLMs
- LLMs hallucinate when they read tables of numbers. For Search Console and analytics anomalies, use Isolation Forest, Local Outlier Factor or forecast residuals, and have an LLM write the code rather than read the numbers. *Practitioner, relayed talk summary.*[^lr-techseo]
- **Do:** run the check on daily clicks, sessions and orders per page type, and review flagged days against the caveats list ([section 1 of Search Console](search-console.md#1-before-every-comparison)); the method is [test 25](diagnostic-tests.md#25-anomaly-detection-without-llms).

Related: [Search Console](search-console.md), [AI-visibility tracking](ai-visibility-tracking.md), [diagnostic tests](diagnostic-tests.md), [traffic drop](../situations/traffic-drop.md), [migration](../situations/migration.md).

[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: GSC impression inflation (week of 2026-04-04), GA4 AI Assistant channel (2026-05-09), GA4 bug (2026-08-29), GPT-6 referral loss with Adobe data (2026-10-10), Comscore, Seer and the field experiment on AIO clicks (2026-04-25), SparkToro zero-click; secondary reporting, primary sources not checked.
[^siege-engagement]: Siege Media, 2026-08-26: medians, 1 Jan 2024 – 1 Aug 2026.
[^siege-attribution]: Siege Media, 2026-10-16: B2B, one company; units of the survey figure unclear in the post.
[^nz-aimeas]: Natzir Turrado, 2026-05-17, updated to 2026-10: server logs vs GA4 on several sites; referrer and UTM behaviour per assistant; GA4 AI Assistant channel since 2026-05-13; UTM bug 2026-10-07 to 16 (−68 to −74 % in logs, −20 to −60 % in GA4); up to 35 % bots among chatgpt.com-tagged visits on one site; ChatGPT-User fetches 2–7× the visits it sends.
[^dj-grounding]: DEJAN, 2026-06-13: probing the grounding APIs of Google, OpenAI and Anthropic with one query; OpenAI tags cited links `utm_source=openai`; Google wraps citation links in `vertexaisearch.cloud.google.com/grounding/...`.
[^mt-gptbot]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2026-03-04: server logs of one new 60,000-page site; GPTBot 29,000+ requests in 12 h; 3-h snapshot; client-side tracker saw zero bots; advises verifying against OpenAI's published IP ranges.
[^bc-llm-vs-search]: Bruce Clay, 2025-12-09: relays SSRN paper 5585812 (50,000+ ChatGPT-referred transactions vs 164 million from other channels, nearly 1,000 ecommerce sites) and Amsive; also a SALT.agency figure (17.56 % LLM vs 24.12 % organic) whose metric is unclear in the post, so not used here; text and charts disagree in places; original paper not checked.
[^ja-specevil]: Jono Alderson, 2026-04-14: third-party speculation rules can target uncached URLs (`/search?q=*`, `/cart?add-to-cart=*`); detectable via `Sec-Purpose: prefetch`, often without referrer; no cross-site opt-out; technical argument, no measurements.
[^lr-techseo]: Lily Ray, 2025-12-05, summarising Sam Torres' Tech SEO Connect talk: LLMs hallucinate reading numeric tables; Isolation Forest, Local Outlier Factor or forecast residuals for GSC/GA4 anomalies; LLM writes the code.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
