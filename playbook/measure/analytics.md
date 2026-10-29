---
type: Checklist
title: Analytics
description: Where web analytics under- and over-counts — missing orders, payment redirects, double page views, session bugs, meaningless bounce, click IDs lost in redirects, Performance Max channel quirks, paused feeds, engagement benchmarks, self-reported attribution, AI-assistant referrals (referrers, UTMs, bots, server-log checks, conversion value), speculative prefetch hits, anomaly detection without LLMs, friction signals, GA4 bounce and conversion benchmarks, AI shopping agents, demand by correlation, URL joins and real-user Web Vitals outside Chrome.
tags: [measurement, ga4, google-ads, tracking, attribution, caveats, ai-assistants, server-logs, anomaly-detection]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
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
  - id: am-optimized-tagging
    resource: "https://www.analyticsmania.com/post/optimized-tagging-experience-in-gtm/"
    title: "Analytics Mania, GTM Optimized Tagging Experience (2026-10-21; author's test container)"
  - id: am-utm-not-working
    resource: "https://www.analyticsmania.com/post/utm-parameters-not-working-in-google-analytics-4/"
    title: "Analytics Mania, UTM parameters not working in GA4 (updated 2026-10-12)"
  - id: am-no-data
    resource: "https://www.analyticsmania.com/post/no-data-available-in-google-analytics-4-here-are-the-solutions/"
    title: "Analytics Mania, No data available in GA4 (updated 2026-10-12)"
  - id: am-cross-domain
    resource: "https://www.analyticsmania.com/post/google-analytics-4-cross-domain-tracking-not-working/"
    title: "Analytics Mania, GA4 cross-domain tracking not working (updated 2026-10-12)"
  - id: am-content-groups
    resource: "https://www.analyticsmania.com/post/content-groups-in-google-analytics-4/"
    title: "Analytics Mania, Content Groups in GA4 (updated 2026-10-12)"
  - id: am-unassigned
    resource: "https://www.analyticsmania.com/post/unassigned-in-google-analytics-4/"
    title: "Analytics Mania, Unassigned in GA4 (updated 2026-09-18; plus reader comments)"
  - id: am-no-revenue
    resource: "https://www.analyticsmania.com/post/no-revenue-in-google-analytics-4/"
    title: "Analytics Mania, Missing revenue in GA4 (undated)"
  - id: am-events-not-showing
    resource: "https://www.analyticsmania.com/post/google-analytics-4-events-not-showing-up-in-reports/"
    title: "Analytics Mania, GA4 events not showing up (undated)"
  - id: fs-website-analytics
    resource: "https://www.fullstory.com/blog/website-analytics/"
    title: "FullStory, What are website analytics? (updated 2026-07-17; guide)"
  - id: fs-digital-friction
    resource: "https://www.fullstory.com/blog/cost-of-digital-friction"
    title: "FullStory, 65% of teams have misdiagnosed digital friction (updated 2026-08-26; Centiment survey for FullStory, n=647 US pros)"
  - id: fs-ai-personalization
    resource: "https://www.fullstory.com/blog/ai-powered-personalization"
    title: "FullStory, Nearly 3 in 4 enterprises hear customer complaints on AI personalization (updated 2026-10-26; Centiment survey for FullStory, n=573)"
  - id: fs-phygital
    resource: "https://www.fullstory.com/blog/phygital-experience/"
    title: "FullStory, Phygital experience (updated 2026-04-16; guide)"
  - id: fs-dx-analytics
    resource: "https://www.fullstory.com/blog/digital-experience-analytics/"
    title: "FullStory, What is digital experience analytics? (updated 2026-04-21; guide)"
  - id: fs-warehouse-tables
    resource: "https://www.fullstory.com/blog/your-warehouse-needs-tables-analysts-can-query/"
    title: "FullStory, Your warehouse doesn't need raw events (updated 2026-08-14; engineering opinion)"
  - id: fs-bounce-rate
    resource: "https://www.fullstory.com/blog/what-is-a-good-bounce-rate/"
    title: "FullStory, What is bounce rate? (updated 2026-09-28; guide, benchmarks unsourced)"
  - id: fs-ecom-cro
    resource: "https://www.fullstory.com/blog/ecommerce-conversion-rate-optimization/"
    title: "FullStory, How to master ecommerce CRO with behavioral data (updated 2026-06-15; guide citing third parties)"
  - id: fs-cro
    resource: "https://www.fullstory.com/blog/conversion-rate-optimization/"
    title: "FullStory, What is conversion rate optimization? (updated 2026-08-14; guide)"
  - id: fs-before-block-agent
    resource: "https://www.fullstory.com/blog/before-you-block-an-ai-agent/"
    title: "FullStory, Before you block an AI agent, find out what it came to do (updated 2026-10-21; practitioner, no data)"
  - id: fs-agent-observability
    resource: "https://www.fullstory.com/blog/ai-agent-observability-undercover-shoppers"
    title: "FullStory, Agent observability in the age of undercover AI shoppers (updated 2026-10-26; vendor observations, no sample)"
  - id: fs-agentic-commerce
    resource: "https://www.fullstory.com/blog/agentic-commerce-can-you-see-it/"
    title: "FullStory, Agentic commerce is live on your site. Can you see it? (updated 2026-10-15; vendor dashboard observations, no counts)"
  - id: sp-public-evidence
    resource: "https://sparktoro.com/blog/if-search-captures-demand-public-evidence-creates-it/"
    title: "SparkToro, If search captures demand, public evidence creates it (2026-04-01; own GA4 plus relayed data)"
  - id: sp-click-optional
    resource: "https://sparktoro.com/blog/zero-click-search-what-still-works/"
    title: "SparkToro, The click is now optional (2026-06-10; synthesis of third-party data)"
  - id: sp-zero-click-2026
    resource: "https://sparktoro.com/blog/in-2026-less-than-one-third-of-google-searches-still-send-a-click/"
    title: "SparkToro, In 2026, less than one third of Google searches still send a click (2026-06-09; Similarweb US panel Jan-Apr 2026)"
  - id: mlseo-dark-ai
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/dark-ai-traffic-hidden-in-direct/"
    title: "MLforSEO, Dark AI traffic hidden in direct (2026-08-21, updated 2026-10-24; relays Loamly vendor data)"
  - id: mlseo-content-audit
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/content-audit/content-audit-template/"
    title: "MLforSEO, Content audit template (2026-10-24; rules plus synthetic 24-URL site)"
  - id: dbb-ff-safari
    resource: "https://www.debugbear.com/blog/firefox-safari-web-vitals"
    title: "DebugBear, Firefox and Safari now support two Core Web Vitals metrics (2025-12-15, updated 2026-03-19)"
---

# Analytics

Which analytics numbers can't be taken at face value — orders, page views, sessions, bounce, ad attribution — and how to correct for them. Examples are from one anonymised shop.[^field-notes] Run the [comparison checklist](search-console.md#1-before-every-comparison) first.

## Rules
- **Never present analytics purchases as all orders;** reconcile against the shop or order-system total once a quarter, state the ratio, and check outlier orders and known platform-bug days before reporting a month or a small channel. *Practitioner, relayed* — [section 1](#1-analytics-doesnt-see-every-order)
- **Exclude windows with page-view or session bugs** from session, conversion-rate and item-view analyses, and drop `(not set)` landing pages and checkout restarts. *Practitioner* — [section 2](#2-page-views-sessions-and-bounce)
- **Check per template that bounce means something;** where it doesn't, use engagement time and add-to-cart rate, and never judge GA4 bounce against unsourced or Universal Analytics-era bands. *Practitioner* — [section 2](#2-page-views-sessions-and-bounce), [section 16](#16-bounce-rate-and-conversion-benchmarks-in-ga4)
- **Test every ad landing URL with a test click ID weekly** and re-verify ad conversions after every checkout release. *Practitioner* — [section 3](#3-ads-and-attribution)
- **Treat windows with a paused feed or a bidding-behaviour change as no baseline** for paid revenue, AOV or ROAS. *Practitioner* — [section 3](#3-ads-and-attribution), [section 4](#4-feeds)
- **Compare engagement with benchmarks only after correcting for your own tracking breaks.** *Measured* — [section 5](#5-engagement-benchmarks)
- **Ask buyers how they heard of you after purchase,** with an "AI assistant" option. *Practitioner, single case* — [section 6](#6-self-reported-attribution)
- **Bot-filter the AI channel and read AI referrals next to server logs;** most assistant clicks arrive without a referrer and some tagged visits are bots. Count AI bots only from server or CDN logs, verified against the vendors' published IP ranges — client-side trackers see none. Segment AI shopping agents out of conversion rates and tests. *Measured; one site for the bot logs; practitioner, vendor data for agents* — [section 7](#7-ai-assistant-referrals-referrers-utms-and-bots), [section 8](#8-ai-bots-live-in-server-logs-only), [section 17](#17-ai-shopping-agents-in-the-funnel)
- **Log `Sec-Purpose` and exclude speculative prefetch hits from demand counts** (site search, add-to-cart). *Practitioner, no measurements* — [section 10](#10-speculative-prefetch-hits)
- **Keep UTMs, click IDs and `_gl` alive from ad to purchase:** whitelist `utm_*` and `_gl` in routing, CDN and cache rules, never strip query strings from `page_location`, keep UTM values lowercase with source and medium both set, and test a purchase without accepting the consent banner. *Practitioner* — [section 12](#12-ga4-attribution-leaks-utms-consent-and-cross-domain), [section 13](#13-ecommerce-events-and-revenue-checks)
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
- **Redirects that drop click IDs.** Example: some old URLs redirected without the query string, so ad clicks lost gclid and UTM and neither the ad platform nor analytics could attribute them; affected campaigns were undercounted for months. Check every ad landing URL with a test gclid weekly.[^am-utm-not-working]
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

## 12. GA4 attribution leaks: UTMs, consent and cross-domain
Points from Analytics Mania (a practitioner who sells GA4/GTM courses).
- **A source without a medium is Unassigned.** Once GA4 sees any UTM it ignores the referrer, so an assistant link with `utm_source=chatgpt.com` and no `utm_medium` matches no channel rule. Check Session source / medium and build a custom channel group for AI sources ([AI-visibility tracking](ai-visibility-tracking.md#4-one-channel-definition)). *Practitioner.*[^am-unassigned]
- **Non-standard mediums** (`mail`, `em`, `pdf`) match none of GA4's 18 default channel groups and land in Unassigned. *Practitioner.*[^am-unassigned]
- **Don't judge attribution on same-day data.** Standard reports need 24–48 h and Unassigned shrinks as processing completes; Realtime should show hits within ~30 min, so an empty Realtime means a collection problem. *Practitioner.*[^am-unassigned][^am-no-data]
- **Stripped parameters.** Sites, single-page apps and CDNs that strip or 404 on unknown query parameters kill UTMs and the `_gl` linker; whitelist `utm_*` and `_gl` in routing and caching rules ([migration](../situations/migration.md#3-ads-feeds-and-ai-crawlers)). *Practitioner.*[^am-utm-not-working][^am-cross-domain]
- **A custom `page_location` that removes query strings** silently destroys campaign attribution, and the data can't be recovered. *Practitioner.*[^am-utm-not-working]
- **UTMs on internal links** mid-session don't re-attribute; find such clicks in Explore with Page location containing `utm_`. *Practitioner.*[^am-utm-not-working]
- **Consent before navigation.** If visitors move on before accepting the banner, landing-page UTMs can be lost; options are persisting UTMs, a more prominent banner or Advanced Consent Mode (with legal review). *Practitioner.*[^am-utm-not-working]
- **Auto-tagging wins.** Google Ads auto-tagging (gclid) overrides manual UTMs as `google / cpc`; the manual values remain in "Session manual source" and "Session manual campaign". UTMs are case-sensitive (enforce lowercase), and `utm_source` and `utm_medium` are both required. *Practitioner.*[^am-utm-not-working]
- **Cross-domain checkout** passes IDs via `_gl`. It fails when a domain is missing from "Configure your domains", redirects drop the query string, click handlers stop propagation, buttons or divs replace `<a>` links, forms are used (form decoration only in gtag.js), or iframes, different measurement IDs or inconsistent consent sit between the domains. Subdomains need no setup. *Practitioner.*[^am-cross-domain]
- **Measurement Protocol events** need `client_id` and `session_id` to join a session (otherwise "(not set)"); for sessions up to 72 h old also send `timestamp_micros`. *Practitioner.*[^am-unassigned]
- **Thresholding** hides small rows, mostly when demographic dimensions are in the report; the threshold is unknown (the author guesses under ~50). Remove those dimensions. *Practitioner.*[^am-events-not-showing]
- **Do:** check new campaign links with [test 28](diagnostic-tests.md#28-utm-survival-check) and consent with [test 29](diagnostic-tests.md#29-consent-signal-check-in-the-network-request).

## 13. Ecommerce events and revenue checks
- **Purchase revenue** needs a `purchase` event with `transaction_id`, `value` and an ISO currency code, plus an `items` array with `item_id`, `item_name`, `price` and `quantity` (no quantity, no item revenue); send numbers without thousands separators. *Practitioner.*[^am-no-revenue]
- **Basic Consent Mode v2:** with `analytics_storage` denied the purchase tag can be blocked entirely; test a purchase without accepting the banner in GTM Preview (Consent tab). *Practitioner.*[^am-no-revenue]
- **Denied-consent events** don't appear in DebugView or Realtime; they reach standard reports only as modelled data with Blended reporting identity. *Practitioner.*[^am-events-not-showing]
- **Event limits and lags:** event names max 40 characters; unregistered parameters are visible only for the last 30 min; custom dimensions take up to 48 h and aren't retroactive; Admin > Events lags behind reports. *Practitioner.*[^am-events-not-showing]
- **Content groups per page type:** set `content_group` with a dataLayer push (robust) or a GTM RegEx table on the path (breaks when URLs change; first match wins). The push must run before `page_view`; groups aren't retroactive and unmatched pages show "(not set)". *Practitioner.*[^am-content-groups] Use them for satisfaction per page type ([test 2](diagnostic-tests.md#2-satisfaction-per-page-type)).
- **Do:** when revenue or events go missing, run [test 27](diagnostic-tests.md#27-ga4-no-data-and-missing-revenue-triage).

## 14. GTM's optimized tagging (2026)
- GTM's Optimized Tagging Experience (October 2026) replaces the Google Tag with destination tag types (Google Analytics, Google Ads, Floodlight), moves shared settings into the container and sends data without extra Google tag libraries; Conversion Linker is marked Legacy. *Practitioner.*[^am-optimized-tagging]
- There is no page-speed promise for the optimized setup; measure on your own site. *Practitioner.*[^am-optimized-tagging]
- A container rollback restores tags but not the permissions granted during optimization (revoke them under Admin > External account links). Server-side GTM needs no change; `server_container_url` stays on the GA destination tag. *Practitioner.*[^am-optimized-tagging]
- **Do:** after migrating, check consent signals ([test 29](diagnostic-tests.md#29-consent-signal-check-in-the-network-request)) and the known migration bugs ([test 27](diagnostic-tests.md#27-ga4-no-data-and-missing-revenue-triage)).

## 15. Friction signals in behavioural data
Points from FullStory, which sells behavioural analytics and session replay; its surveys were run by Centiment for FullStory, with no fieldwork dates and no per-question bases.
- **Frustration signals,** in FullStory's definitions: rage clicks are repeated rapid clicks on one element that is expected to respond; dead clicks hit non-interactive elements; error clicks trigger an application or validation error; a thrashed cursor is rapid, erratic mouse movement. *Official; vendor data.*[^fs-website-analytics]
- **Teams learn of friction late.** Among 647 US product, engineering, data, CX and IT professionals, 52 % most often learned of friction from customer complaints or support tickets rather than from alerts or monitoring. They put its cost mainly in rising support tickets (55 %), then lower conversion (35 %) and direct revenue loss (33 %). *Measured; vendor data.*[^fs-digital-friction]
- **Personalisation errors go unseen.** 87 % of 573 enterprises hit at least one AI personalisation error in the past 12 months. Of those, 75 % learned of it through customer complaints and only 22 % caught errors in their own behavioural data; 63 % said the errors cost sales, but only about 37 % had measured the loss. *Measured; vendor data, subgroup bases not reported.*[^fs-ai-personalization]
- **Tag-based gaps.** Cookie restrictions and browser settings distort returning-visitor and session counts, and tags miss untagged edge cases and new flows; autocapture allows analysis after the fact. *Practitioner; vendor data.*[^fs-website-analytics][^fs-phygital]
- **Privacy.** Install a consent manager and pick replay tools that don't capture sensitive data by default. *Official; vendor data.*[^fs-dx-analytics]
- **Warehouse exports.** Raw events push sessionisation and transformation onto the analyst; fact and dimension tables are easier to query. *Practitioner; vendor data.*[^fs-warehouse-tables]
- **Do:** alert on rage, dead and error clicks per template, the way you alert on orders, and confirm the cause before shipping a fix ([test 30](diagnostic-tests.md#30-confirm-the-friction-cause-before-fixing)).

## 16. Bounce rate and conversion benchmarks in GA4
- **Definition.** GA4 bounce rate = 100 % − engagement rate; an engaged session lasts more than 10 s, has a key event or has more than one page view. GA4 hides bounce rate by default, and it runs lower than Universal Analytics-era benchmarks. *Official; vendor data.*[^fs-bounce-rate]
- **Don't use published bounce bands.** FullStory's bands (under 20 % suspicious, 20–40 % good, 40–55 % average, 55–70 % high, over 70 % needs attention) cite no source and mix UA and GA4 concepts. *Practitioner; vendor data, unverified.*[^fs-bounce-rate] Use your own history per template ([section 2](#2-page-views-sessions-and-bounce)).
- **Conversion benchmarks, relayed:** average ecommerce conversion ~3 %, top performers above 5 %; checkout abandonment ~70 % (Baymard); mobile said to convert at about half the desktop rate (unsourced). *Practitioner; relayed.*[^fs-ecom-cro]

> **Conflict:** "good" ecommerce conversion at 5 % or more[^fs-cro] vs ~3 % average with 5 % as top performers[^fs-ecom-cro], and 2–3 % in many industry benchmarks.

## 17. AI shopping agents in the funnel
- **Segment agents out.** AI shopping agents skew conversion rates and personalisation in retail funnels; separate agent sessions so conversion rate and experiments reflect humans, and measure agent performance on its own. *Practitioner; vendor data.*[^fs-before-block-agent][^fs-agent-observability]
- **Behavioural tells:** the pointer jumps from click to click, inactive time is high, entry is direct on deep pages, and there is no highlighting, copying or pasting; a copy/paste event marks a human taking over. *Practitioner; vendor data.*[^fs-agentic-commerce] After FullStory exposed one agent's traffic, the agent added curved mouse paths and pauses, so tells and header or IP lists decay. *Measured; vendor data, no magnitude.*[^fs-agent-observability]
- **Do:** run [test 34](diagnostic-tests.md#34-separate-ai-shopping-agents-from-humans) before reading conversion rate or an A/B test result; bot controls are in [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).

> **Conflict:** detect agents by behaviour (FullStory) vs the common practice of user-agent strings, robots.txt and verified IP ranges ([section 8](#8-ai-bots-live-in-server-logs-only)).

## 18. Demand by correlation, not last click
- **Last click hides influence.** On SparkToro's own site (SparkToro sells audience research) ~45 % of visits are direct and ~24 % come from search; GA4 shows only the last channel. *Measured; one case.*[^sp-public-evidence]
- **Read demand by correlation.** Track branded search, direct traffic, revenue, share of voice and audience growth over time as demand proxies instead of last-click channel credit. *Practitioner.*[^sp-click-optional]
- **Google's share of traffic fell 8 points** (~22 % relative) from June 2025 to May 2026 in Ahrefs' tracker of 75,000+ opted-in domains, which skews to professionally marketed sites. *Measured, relayed.*[^sp-zero-click-2026]
- **Assistant referrers** (MLforSEO, which sells courses): Perplexity passes a consistent referrer; ChatGPT desktop has appended a UTM since June 2025; ChatGPT mobile, AI Overviews and copy-paste pass nothing. *Practitioner.*[^mlseo-dark-ai] Proxy for the rest: Direct trend against branded-search trend ([AI-visibility tracking](ai-visibility-tracking.md#18-dark-ai-traffic)).

## 19. Joining crawl, Search Console and analytics per URL
- Match URLs on the path, ignoring host, query, fragment, trailing slash and case, and report join coverage; in a synthetic example 4,845 of 4,880 Search Console clicks and 8,035 of 8,075 GA4 sessions matched, and one orphan URL had clicks but wasn't crawled. *Practitioner.*[^mlseo-content-audit] Audit rules on the joined table: [ML methods for SEO](ml-methods-for-seo.md#9-content-audits-by-rules).

## 20. Real-user Web Vitals beyond Chrome
- Safari 26.2 (2025-12-12) added LCP and INP, and Firefox supports both; CLS is in neither. CrUX still covers Chrome only, so filter your real-user data to Chrome before comparing it with CrUX. Safari sometimes reports implausibly high INP. *Official, relayed; vendor data.*[^dbb-ff-safari] DebugBear sells performance monitoring. Field vs lab: [test 35](diagnostic-tests.md#35-field-crux-vs-lab-measurement).

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
[^am-optimized-tagging]: Analytics Mania, 2026-10-21: GTM Optimized Tagging Experience in the author's test container; destination tag types, Conversion Linker Legacy, no speed promise, rollback and permissions, server-side unchanged.
[^am-utm-not-working]: Analytics Mania, updated 2026-10-12: causes of lost UTMs — redirects, stripped parameters, custom page_location, internal UTMs, consent timing, auto-tagging override, case sensitivity.
[^am-no-data]: Analytics Mania, updated 2026-10-12: "no data" causes and checks; Realtime within ~30 min.
[^am-cross-domain]: Analytics Mania, updated 2026-10-12: _gl linker failure modes in cross-domain tracking.
[^am-content-groups]: Analytics Mania, updated 2026-10-12: content_group via dataLayer push or GTM RegEx table; timing before page_view; not retroactive.
[^am-unassigned]: Analytics Mania, updated 2026-09-18: Unassigned causes — UTM without medium, non-standard mediums, 18 default channel groups, processing delay 24–48 h, Measurement Protocol session joining.
[^am-no-revenue]: Analytics Mania, undated, read 2026-10-28: required purchase parameters, Basic Consent Mode blocking the purchase tag.
[^am-events-not-showing]: Analytics Mania, undated, read 2026-10-28: denied-consent events, thresholding, event-name and parameter limits, custom-dimension delay.
[^fs-website-analytics]: FullStory, updated 2026-07-17: definitions of rage, dead and error clicks and thrashed cursor; cookie and browser-setting effects on tag-based analytics; guide.
[^fs-digital-friction]: FullStory, updated 2026-08-26: Centiment survey for FullStory, n=647 US product, engineering, data, CX and IT professionals; complaints 52 %, cost attribution 55 / 35 / 33 %; per-question bases not reported.
[^fs-ai-personalization]: FullStory, updated 2026-10-26: Centiment survey for FullStory, n=573, mostly "past 12 months"; 87 % hit an error, 75 % via complaints, 22 % caught in own data, 63 % cost sales, ~37 % measured; subgroup bases not reported.
[^fs-phygital]: FullStory, updated 2026-04-16: tag-based analytics miss untagged edge cases and new flows; autocapture allows retroactive analysis; guide.
[^fs-dx-analytics]: FullStory, updated 2026-04-21: privacy laws, consent manager, replay tools that don't capture sensitive data by default; guide.
[^fs-warehouse-tables]: FullStory, updated 2026-08-14: raw events vs fact and dimension tables (hourly sync); engineering opinion, the claim about agents writing better SQL is unbenchmarked.
[^fs-bounce-rate]: FullStory, updated 2026-09-28: GA4 bounce and engaged-session definitions; bounce bands given without a source.
[^fs-ecom-cro]: FullStory, updated 2026-06-15: relays DynamicYield and Nector (~3 % average, >5 % top), Baymard (~70 % checkout abandonment); mobile half of desktop unsourced.
[^fs-cro]: FullStory, updated 2026-08-14: calls 5 % or more a good ecommerce conversion rate; guide.
[^fs-before-block-agent]: FullStory, updated 2026-10-21: segment agent sessions out of conversion and experiments; practitioner, no data.
[^fs-agent-observability]: FullStory, updated 2026-10-26: agent traffic in customer segments dropped sharply around 2026-10-16 after the dashboard exposed it, then the agent added curved mouse paths and pauses; vendor observations, no sample or magnitude.
[^fs-agentic-commerce]: FullStory, updated 2026-10-15: agent tells (pointer jumps, inactive time, deep direct entry, no copy/paste); vendor dashboard observations, no counts.
[^sp-public-evidence]: SparkToro, 2026-04-01: SparkToro's own GA4 (~45 % direct, ~24 % search); one site.
[^sp-click-optional]: SparkToro, 2026-06-10: measure demand with correlation (branded search, direct, revenue, share of voice, audience growth), not attribution; synthesis.
[^sp-zero-click-2026]: SparkToro, 2026-06-09: relays the Ahrefs traffic tracker (75,000+ opted-in domains): Google's share of traffic −8 points, June 2025 – May 2026; sample skews to professionally marketed sites.
[^mlseo-dark-ai]: MLforSEO (Beatrice Gamba), 2026-08-21, updated 2026-10-24: referrer behaviour per assistant; Direct vs branded-search proxy; relays Loamly vendor data.
[^mlseo-content-audit]: MLforSEO (Lazarina Stoy), 2026-10-24: URL join rules and coverage check on a synthetic 24-URL site.
[^dbb-ff-safari]: DebugBear, 2025-12-15, updated 2026-03-19: Safari 26.2 adds LCP and INP; Firefox supports LCP and INP; CrUX Chrome-only; the Firefox INP date in the source is likely wrong.
