---
type: Checklist
title: AI-visibility tracking
description: How to count AI-assistant traffic and visibility — untagged clicks by design and by accident, Direct spikes that are bots, GA4's AI Assistant channel, one hostname-anchored channel group, the real size of the channel, per-engine reporting, mentions without links, the May 2026 ChatGPT link change, what Bing's AI Performance covers, prompt-tracker pitfalls (personalisation, clean accounts), re-baselining at model changes and fan-out volatility, entity tracking with search on and off, brand-canon accuracy, share of voice beyond presence, building the prompt set, runs and margin of error, AI as a brand channel, dark AI traffic and AI Overview citation tracking.
tags: [measurement, geo, ga4, chatgpt, ai-assistants, attribution, caveats, prompt-tracking, share-of-voice, brand-accuracy]
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
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026; 1,249 answers, 88k results, server logs of 325k URLs)"
  - id: gm-direct
    resource: "https://www.growth-memo.com/p/does-ai-drive-more-direct-traffic"
    title: "Growth Memo, Does AI drive more direct traffic (2026-10-19; 12 GA4 properties, 632 correlation tests)"
  - id: ipr-brand
    resource: "https://ipullrank.com/ai-search-is-a-branding-channel"
    title: "iPullRank, AI search is a branding channel (2026-10-22; cites BrightEdge, Pew, Growth Memo)"
  - id: mh-geo
    resource: "https://www.mariehaynes.com/geo-is-a-distraction/"
    title: "Marie Haynes, GEO is a distraction (2026-10-21; 100 GA4 properties, 12 months, >145M sessions)"
  - id: siege-conversion
    resource: "https://www.siegemedia.com/research/ai-traffic-conversion-rates"
    title: "Siege Media, AI traffic conversion rates (2026-06-30; 78 GA4 properties, Jan–May 2026)"
  - id: aleyda-traffic
    resource: "https://www.aleydasolis.com/en/ai-search/ai-traffic-citations-research/"
    title: "Aleyda Solis, AI traffic vs citations research (~Apr–May 2026; 40 US sites, Semrush + Similarweb; search extracts)"
  - id: ipr-aimode-referrals
    resource: "https://ipullrank.com/early-referral-data-ai-mode"
    title: "iPullRank (Garrett Sussman), Early referral data from AI Mode (2025-09-26; SimilarWeb panel, 100K+ users)"
  - id: gm-consensus
    resource: "https://www.growth-memo.com/p/the-consensus-gap"
    title: "Growth Memo, The consensus gap (2026-05-11; 3.7M citations, 20,000-prompt sample, Omnia data)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: bp-chatgpt-links
    resource: "https://botpresso.com/chatgpt-may-links-update-traffic-impact-study/"
    title: "Botpresso, ChatGPT May links update traffic study (≈2026-07; 52 client sites, GA4)"
  - id: bp-ga4-ai
    resource: "https://botpresso.com/how-to-create-ai-traffic-dashboard-in-ga4/"
    title: "Botpresso, AI traffic dashboard in GA4 (≈2025-09)"
  - id: ah-mentions-links
    resource: "https://ahrefs.com/blog/ai-citations-vs-impressions-study/"
    title: "Ahrefs, AI citations vs impressions (2025-11-26; one brand, 31,000+ mentions)"
  - id: ah-aio-change
    resource: "https://ahrefs.com/blog/ai-overview-change/"
    title: "Ahrefs, How often AI Overviews change (2025-11-11; 43,000+ keywords)"
  - id: nz-aimeas
    resource: "https://natzir.com/en/analytics/ai-traffic-measurability/"
    title: "Natzir Turrado, The state of AI traffic measurability (2026-05-17, updated to 2026-10; server logs vs GA4 on several sites)"
  - id: nz-bingai
    resource: "https://natzir.com/en/seo/bing-ai-performance-query-page-mapping/"
    title: "Natzir Turrado, Exporting Bing AI Performance query–page mapping (2026-05-18; 6 sites)"
  - id: nz-trackers
    resource: "https://natzir.com/en/seo/ai-visibility-tools-prompt-trackers/"
    title: "Natzir Turrado, What prompt trackers don't tell you (2026-01-29; literature/vendor-study review + own Bing data, 6 sites)"
  - id: nz-model
    resource: "https://natzir.com/en/seo/model-change-most-mentioned-brand-ai/"
    title: "Natzir Turrado, How a model change can make your brand one of the most mentioned by AI (2026-10-21; 4 Gemini models, 7–20 runs per model per prompt, ablations, 5 categories)"
  - id: mt-memory
    resource: "https://metehan.ai/blog/chatgpts-personal-memory-affects-everything-in-responses-openai-is-using-google-analytics/"
    title: "Metehan Yeşilyurt, ChatGPT's memory affects responses (2025-12-20; hidden metadata, one account)"
  - id: dj-prompt
    resource: "https://dejan.ai/blog/prompt-tracking/"
    title: "DEJAN, Why we don't do prompt tracking (2026-10-04; practitioner method)"
  - id: dj-sitefanout
    resource: "https://dejan.ai/blog/site-fanouts/"
    title: "DEJAN, OpenAI fan-out data shows no rise in site: use (2026-08-25; 551,695 fan-outs, 196,692 OpenAI, via API)"
  - id: mt-sitequeries
    resource: "https://metehan.ai/blog/reddit-lost-most-its-visibility-chatgpt-site-filled-gap/"
    title: "Metehan Yeşilyurt, Reddit lost its ChatGPT visibility and the site parameter filled the gap (2026-08-21; Peec logs, 14.9M queries/week)"
  - id: ls-context
    resource: "https://lazarinastoy.com/context-not-content-is-king-ai-search/"
    title: "Lazarina Stoy, Context (not content) is king in AI search (2026-10-25; review of patents and third-party studies)"
  - id: seer-brand-accuracy
    resource: "https://www.seerinteractive.com/insights/ai-brand-accuracy-study"
    title: "Seer Interactive, AI declined to answer prompts about our brand 31 % of the time (2026-08-27; 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, May 1 – Jun 9 2026, own brand)"
  - id: seer-luna
    resource: "https://www.seerinteractive.com/insights/gpt-5.5-vs-gpt-5.6-luna"
    title: "Seer Interactive, ChatGPT-5.6 Luna runs more targeted searches (2026-09-24; 346 matched prompts, 6 industries)"
  - id: seer-chatgpt-structure
    resource: "https://www.seerinteractive.com/insights/chatgpt-data-structure"
    title: "Seer Interactive, Same prompt, different data structure (2026-10-22; 1 prompt captured 3 times + 6-prompt suite, signed-in network payloads)"
  - id: seer-visibility-lying
    resource: "https://www.seerinteractive.com/insights/ai-visibility-is-lying-to-you"
    title: "Seer Interactive, AI visibility is lying to you (2026-08-31; 2 client cases + hypotheticals)"
  - id: brief-topical
    resource: "https://seobrief.substack.com/p/topical-authority"
    title: "Jes Scholz, SEO Brief: topical authority (2026-04-08; essay, relays an Ehrenberg-Bass salience paper)"
  - id: brief-availability
    resource: "https://seobrief.substack.com/p/the-brief-about-digital-availability"
    title: "Jes Scholz, SEO Brief: digital availability (2026-07-08; essay + methods)"
  - id: cc-rapp
    resource: "https://www.crystalcarter.ai/post/value-of-visibility-the-rapp-audit-for-llm-mentions-citations"
    title: "Crystal Carter, The RAPP audit for LLM mentions and citations (≈2026-03; practitioner framework)"
  - id: cc-kpis
    resource: "https://www.wix.com/studio/ai-search-lab/ai-search-visibility-kpis"
    title: "Crystal Carter, AI search visibility KPIs (2025-07-29, updated 2025-08-03; Wix AI Search Lab; framework)"
  - id: ja-clicks
    resource: "https://www.jonoalderson.com/conjecture/clicks-dont-count/"
    title: "Jono Alderson, Clicks don't count (2026-03-12; argument)"
  - id: gg-gsclinks
    resource: "https://www.gsqi.com/marketing-blog/chatgpt-links-in-google-search-console/"
    title: "Glenn Gabe, ChatGPT links in Google Search Console (2026-03-18; client properties)"
  - id: am-unassigned
    resource: "https://www.analyticsmania.com/post/unassigned-in-google-analytics-4/"
    title: "Analytics Mania, Unassigned in GA4 (updated 2026-09-18; plus reader comments)"
  - id: sp-track-ai-visibility
    resource: "https://sparktoro.com/blog/office-hours-can-you-actually-track-ai-visibility/"
    title: "SparkToro, Office Hours: Can you actually track AI visibility? (2026-05-07; SparkToro x Gumshoe.ai, ~600 volunteers, 142 prompts, 994 runs)"
  - id: mlseo-rank-tracker
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/rank-tracker-ai-search-measurement/"
    title: "MLforSEO, Your rank tracker is lying to you about AI search (2026-08-03; mostly unsourced figures)"
  - id: sp-similarweb-ai-mentions
    resource: "https://sparktoro.com/blog/new-research-from-similarweb-how-ai-brand-mentions-influence-direct-visits-traditional-search-queries/"
    title: "SparkToro, How AI brand mentions influence direct visits and search (2026-06-28; Similarweb clickstream, sample not stated)"
  - id: sp-ai-boondoggle
    resource: "https://sparktoro.com/blog/is-ai-visibility-a-marketing-boondoggle/"
    title: "SparkToro, Is AI visibility a marketing boondoggle? (2026-10-22; review of 4 third-party studies)"
  - id: mlseo-dark-ai
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/dark-ai-traffic-hidden-in-direct/"
    title: "MLforSEO, Dark AI traffic hidden in direct (2026-08-21, updated 2026-10-24; relays Loamly vendor data)"
  - id: mlseo-aio-tracker
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/track-ai-overviews-python/"
    title: "MLforSEO, How to track AI Overviews for your keywords (2026-10-24; 29-keyword run, US desktop)"
---

# AI-visibility tracking

How to count the traffic and visibility AI assistants bring, and why the analytics AI line is a floor rather than the whole channel. Run the [comparison checklist](search-console.md#1-before-every-comparison) first.

## Rules
- **Treat the analytics AI-referral line as a floor,** because some assistant clicks never carry a referrer or UTM. *Measured* — [section 1](#1-untagged-by-design)
- **Mark model-release weeks with lost referrers as reporting gaps** instead of reading them as a decline. *Measured, relayed* — [section 2](#2-untagged-by-accident)
- **Rule out bots before explaining a Direct rise with AI,** segmenting Direct by landing page, country, browser, OS and screen size. *Measured* — [section 3](#3-direct-spikes-are-mostly-bots-not-hidden-ai)
- **Build one custom channel group from assistant source names, anchored on hostnames,** and keep one definition per time series; AI-assistant links with `utm_source` but no `utm_medium` land in Unassigned, and GA4's own AI Assistant channel is still partial. *Practitioner* — [section 4](#4-one-channel-definition)
- **Report assistant sessions and conversions side by side, per vertical, next to Google organic,** and read them with exposure and branded search rather than by referral clicks alone. *Measured; practitioner* — [section 5](#5-scale-of-the-channel), [section 7](#7-how-to-track)
- **Report visibility per engine with a fixed model and reasoning mode, log the model per answer and re-baseline at every model change,** never as one blended AI score; count mentions separately from linked citations, since most mentions carry no link. *Measured, small samples; single brand for links* — [section 6](#6-one-ai-score-hides-more-than-it-shows), [section 11](#11-re-baseline-at-every-model-change)
- **Sample AI answers every 2–3 days, with several simultaneous runs per prompt drawn from real demand and from category entry points,** and report presence % with share of voice next to it, not position. *Measured, vendor data; practitioner* — [section 7](#7-how-to-track), [section 10](#10-what-prompt-trackers-dont-tell-you), [section 14](#14-share-of-voice-not-only-presence), [section 15](#15-building-the-prompt-set)
- **Track from clean, unconnected, logged-out accounts and label it a non-personalised baseline;** ask vendors for model, version and access method (API or app). *Measured, relayed* — [section 10](#10-what-prompt-trackers-dont-tell-you)
- **Keep a brand canon of checkable facts and track accurate, wrong and no-answer rates,** fixing wrong facts on your own site and profiles first. *Measured, one brand* — [section 13](#13-brand-canon-accurate-wrong-no-answer)
- **Publish the margin and read AI as a brand channel:** state run counts and ± points per pass (one pass of 490 results ≈ ±5 points), and judge AI visibility by correlation with branded search and Direct rather than by referral traffic. *Measured, vendor data; practitioner* — [section 16](#16-runs-phrasings-and-margin-of-error), [section 17](#17-ai-as-a-brand-channel)
- **Split AI referrals by landing-page type** (homepage, category, product, content); a link-format change can move them between types overnight. *Measured, agency sample* — [section 8](#8-chatgpt-link-change-may-2026)

## 1. Untagged by design
- About 95 % of the links ChatGPT displays carry `utm_source=chatgpt.com`; pages the model opened itself never do. *Measured.*[^chatgpt-retrieval] Some assistant traffic is always Direct.

## 2. Untagged by accident
- **Example.** For one week after a model release, ChatGPT's inline links had neither referrer nor UTM; assistant sessions halved and Direct rose 25 %.[^field-notes] Mark such weeks as a reporting gap.
- This was industry-wide: after the GPT-6 rollout (from ~9 Oct 2026) reported ChatGPT traffic fell 22–57 % across datasets, Adobe saw ChatGPT visits down ~31,000 a day and Direct up ~26,000 across ~500 pages, and a fix began on 15 Oct.[^ignite-news] Server logs date the UTM bug 7–16 Oct 2026 and show the loss larger in logs (68–74 %) than in GA4 (20–60 %).[^nz-aimeas] Referrer and UTM behaviour per assistant, and bots inside the AI channel: [analytics](analytics.md#7-ai-assistant-referrals-referrers-utms-and-bots).

## 3. Direct spikes are mostly bots, not hidden AI
- In 12 GA4 properties Direct grew in Aug–Sep 2026, by over 100 % in some; one site had 409,000 Direct sessions with 198 engaged; AI-traced sessions were 0.003 % of Direct; correlations between AI share of voice and Direct failed placebo tests. *Measured, B2B-skewed.*[^gm-direct]
- Segment Direct by landing page, country, browser, OS and screen size before reading anything into it ([test 10](diagnostic-tests.md#10-is-a-direct-spike-real)).

> **Conflict:** an older estimate that ~70 % of AI traffic lands as Direct vs AI traces in 0.003 % of Direct in the later, placebo-tested study[^ipr-brand][^gm-direct] — [details](../reference/conflicts.md#is-ai-traffic-hiding-in-direct)

## 4. One channel definition
- **GA4's own AI channel.** GA4 added a native "AI Assistant" default channel (medium `ai-assistant`) in May 2026 (dated 13 May 2026 in a later source).[^ignite-news][^nz-aimeas] Check whether it matches your own source regex before switching; keep one definition per time series. Analytics Mania (a practitioner who sells GA4/GTM courses) called its coverage "partial and still changing" in September 2026; don't rely on it alone. *Practitioner.*[^am-unassigned]
- **Split over channels.** In GA4's default grouping, assistant traffic lands across "AI Assistant", "Unassigned" and "Referral". Build one custom group from source names (chatgpt.com, perplexity, gemini, copilot, claude.ai…). Links tagged `utm_source=chatgpt.com` without `utm_medium` land in Unassigned: once GA4 sees any UTM it ignores the referrer, and a source without a medium matches no channel rule. Check Session source / medium. *Practitioner.*[^am-unassigned] More UTM leaks: [analytics](analytics.md#12-ga4-attribution-leaks-utms-consent-and-cross-domain).
- **Anchor the regex on hostnames.** One published GA4 setup matches 16 source patterns (chatgpt.com, chat.openai.com, perplexity.ai, gemini.google.com, claude.ai, copilot, meta.ai, poe.com, you.com, jina.ai…); unanchored patterns also match unrelated sources that merely contain the word. *Practitioner.*[^bp-ga4-ai] Example: `^(chatgpt\.com|chat\.openai\.com|(www\.)?perplexity\.ai|gemini\.google\.com|claude\.ai|copilot\.microsoft\.com)$` on session source, extended as new assistants appear (*inference*).
- **Email tools with non-standard mediums** (e.g. `campaign`/`flow` instead of `email`) fall into "Unassigned" too.

## 5. Scale of the channel
- Across 100 GA4 properties and >145M sessions over 12 months, ChatGPT brought 0.62 % as many sessions as Google organic, all assistants 0.73 %.[^sp-ai-boondoggle] Of 55 sites tracking conversions, ChatGPT sessions converted at 13.8 % vs 3.02 % for Google organic, but Google organic still drove 96.5 % of the conversions. ChatGPT referrals plateaued after August 2025. *Measured, one author, method not published.*[^mh-geo]
- In panel data for 40 US sites, AI traffic was about 0.19 % of visits against about 20.45 % organic (shopping/retail: 0.18 % vs 21.79 %); AI Mode was 8.1 % of retail AI traffic.[^aleyda-traffic]
- **AI Mode sends few clicks.** Under ~3 % of AI Mode searches led to an external click in a 100K-user panel (May – Aug 2025), flat over the period; top destinations were Reddit, YouTube, Wikipedia, Amazon and Facebook.[^ipr-aimode-referrals]
- Whether assistant traffic converts better is disputed: 13.8 % vs 3.02 % in the sample above, but parity for ecommerce (1.01×) across 78 GA4 properties.[^siege-conversion] Report sessions and conversions side by side, per vertical.

> **Conflict:** AI traffic converts far better (55 sites) vs parity for ecommerce (78 properties) — [details](../reference/conflicts.md#does-ai-traffic-convert-better)

> **Conflict:** GEO citation tracking called "a distraction" given the channel's size vs AI shortlists deciding before the click[^mh-geo][^ipr-brand] — [details](../reference/conflicts.md#is-geo-worth-the-effort)

## 6. One AI score hides more than it shows
- Engines cite almost disjoint sources; report per engine and with a fixed model and reasoning mode.[^gm-consensus] Why they differ: [AI assistants](../how-it-works/ai-assistants.md).
- **Cited pages and clicked pages differ** — the pages assistants cite are mostly not the pages AI visitors land on. Classify cited URLs separately from landing pages ([AI assistants](../how-it-works/ai-assistants.md)).
- **Most mentions carry no link.** For one brand's 31,000+ AI mentions, the share that linked to the brand was AI Overviews 10.7 %, Gemini 16.8 %, ChatGPT 26.9 %, AI Mode 36.8 %, Perplexity 51.6 % (~28 % overall). *Measured, single brand, vendor data.*[^ah-mentions-links] Track mentions and linked citations as separate series, per engine; referral clicks can't show mentions at all.

## 7. How to track
- **Exposure in Google:** Search Console's Generative AI report gives impressions only ([Search Console](search-console.md#4-ai-reports-search-console-and-bing)).
- **Prompt runs per engine,** citations and mentions apart, with enough runs per prompt: [test 9](diagnostic-tests.md#9-prompt-tracking-per-engine).
- **Sampling rhythm.** AI Overview text changed in 70 % of consecutive observations (average persistence 2.15 days) and consecutive answers shared 54.5 % of their URLs.[^ah-aio-change] Sample every 2–3 days and report share of voice across many prompts, never one snapshot ([Google AI features](../how-it-works/google-ai-features.md#9-ai-overviews-change-every-few-days)).
- **Monthly read** of exposure, behaviour and outcomes together: [test 11](diagnostic-tests.md#11-monthly-read-exposure-behaviour-outcomes).
- **Third-party citations** for your category prompts: [test 14](diagnostic-tests.md#14-third-party-citation-audit).
- **Full audit outline:** [test 15](diagnostic-tests.md#15-full-ai-search-audit-skeleton).
- **After-purchase survey** with an "AI assistant" option: [analytics](analytics.md#6-self-reported-attribution).

## 8. ChatGPT link change (May 2026)
- From 7 May 2026 ChatGPT changed how it links, without an announcement from OpenAI. Across 52 client sites (43 B2C, 9 B2B), GA4 ChatGPT referral sessions rose from 183,497 (26 Mar – 6 May) to 363,089 (7 May – 17 Jun 2026), +97.9 %; the median site grew +54 %. The gain was concentrated: the top site took 64 % of the net gain, the top 5 took 91 %, and the other 47 sites grew +10 % combined. *Measured, observational, one agency's clients.*[^bp-chatgpt-links]
- **The landing mix moved to homepages.** Homepage sessions rose +1,316 % (7,990 → 113,183), from 4.4 % to 31.2 % of ChatGPT sessions; other landing pages grew +60 % but fell from 71 % to 57 % of the share; blog pages fell −28 %. 12 of 17 ecommerce stores grew, and 16 of the 17 sites that lost product-page traffic gained homepage traffic.[^bp-chatgpt-links]
- **Do:** split AI referrals by landing-page type (homepage, category, product, content) and mark 7 May 2026 as a break in that split. If homepage share jumps, make sure bestsellers and category entry points sit above the fold there ([homepage and brand](../page-types/homepage-and-brand.md)).

## 9. Bing AI Performance: what it covers
- **Citation gaps (beta).** Bing Webmaster Tools' Topics Portfolio adds "Opportunity Queries": queries where other sites are cited in AI answers and yours isn't. *Practitioner report of a beta feature; no figures.*[^chuleta-timelines]
- Across 6 sites, Bing's query-to-page mapping covered 24.6–96.6 % of citations and 10–25 % of pages on mid-sized and large sites; the report is of little use under about 200 citations. *Measured, 6 sites.*[^nz-bingai]
- 7–33 % of grounding queries (0.4–20 % weighted by citations) had no Google or Bing impressions, and URLs cited only in AI (with no search impressions) were 0.009–0.9 % of citations. Most AI citations go to pages that already rank in search — it supports "rank in search first". *Measured, 6 sites.*[^nz-bingai][^nz-trackers]
- **Do:** treat the report as a sample of your citations, not the total; set-up in [AI crawlers and controls](../technical/ai-crawlers-and-controls.md), Search Console's equivalent in [Search Console](search-console.md#4-ai-reports-search-console-and-bing).

## 10. What prompt trackers don't tell you
A review of vendor studies, plus own Bing data. *Measured, relayed vendor studies.*[^nz-trackers]
- **API ≠ app.** ChatGPT through the API averaged 7 sources vs 16 in the app; for Perplexity the overlap between the two was 8 %. Ask a vendor which model, version and access method (API or app UI) it uses.
- **Language.** 43 % of ChatGPT's sub-queries for non-English prompts were in English (Peec data).
- **Randomness.** There is less than a 1-in-100 chance of getting the same brand list twice (SparkToro); errors on related prompts are correlated, so the real standard error is more than 3× what independent runs suggest.
- **Memory.** ChatGPT injects `user_profile`, `turn_summary` and `summarized_turn_messages` from other chats into answers, so logged-out tracking misses personalised citations. *Measured, one account; author works at Peec AI.*[^mt-memory] Label tracking a non-personalised baseline.
- **Connected accounts.** In an iPullRank test (May 2026; 1,922 AI Mode responses, 8 product categories, few accounts, opt-in), brands seeded into the account appeared in 66.8 % of responses with Personal Intelligence on, up from 23.9 %, while the control fell from 21.9 % to 18.9 %; Gmail-seeded brands reached 53.6 %, Photos-seeded 10.5 %, and top-3 placement rose about 23 points. *Measured, relayed, few accounts.*[^ls-context] Track from clean accounts with no connected apps; signed-in users with connected apps can see very different brand lists.
- **Do:** 3–5 simultaneous runs per prompt, prompts from real demand (e.g. Search Console queries, [Search Console](search-console.md#12-bot-like-llm-query-bursts)), presence % rather than position, citations apart from mentions.[^nz-trackers] How many runs give a usable margin: [test 9](diagnostic-tests.md#9-prompt-tracking-per-engine).

> **Conflict:** 3–5 runs per prompt vs ±44 points of error at 5 runs — [details](../reference/conflicts.md#how-many-prompt-runs)

## 11. Re-baseline at every model change
- **A model change can flip brand mentions.** One brand was mentioned in 1 of 7 answers on Gemini 3.5 Flash and 7 of 7 on a newer Gemini model ("Argon") on the same day, from the same pages (p = 0.005): the newer model added a consumer-testing organisation's name to its fan-out, which surfaced a retailer's "ranking per <organisation>" page. AI Mode showed the brand 0 of 20 times. *Measured, small samples.*[^nz-model] Why: [AI assistants](../how-it-works/ai-assistants.md).
- **Fan-out volume changes with the model.** In 196,692 OpenAI fan-outs collected via the API, fan-outs per searched response fell from 6.16 (March 2026) to 1.10 (August 2026); `site:` queries were 5–6 % on gpt-5.2 / 5.4 and 0.15 % on gpt-5.5 (Google 0.062 %, Anthropic 0); long ad-hoc prompts produced 7–91× more `site:` queries than short tracking prompts. *Measured, API only; consumer app not tested.*[^dj-sitefanout] In consumer-app logs, a vendor saw `site:` fan-outs rise from < 0.11 % to 26.2 % of weekly ChatGPT queries in August 2026. *Measured, vendor data, not reproducible outside the vendor.*[^mt-sitequeries]
- **A default-model switch moves citations platform-wide.** ChatGPT's default became GPT-5.6 "Luna" on 2026-07-09. Across 346 matched prompts in 6 industries, `site:` appeared in 76 % of fan-outs vs 21.6 % on GPT-5.5 (non-brand prompts 20.6 % → 77.3 %), sources consulted fell 43 % (6,134 → 3,481), open searches fell from 575 to 175 and inline citations fell 12.9 %. *Measured, 346 prompts.*[^seer-luna] Treat a platform-wide citation drop around 2026-07-09 as a model change, not a content problem.
- **Fan-out is volatile even within one model.** Two identical ChatGPT runs 8 minutes apart shared none of their query strings; the URLs retrieved for one prompt grew from 14 to 40 over 13 days, 34 of the 40 never cited; one session switched from gpt-5-6 to gpt-5-6-mini mid-way; the payload format changed within two weeks. *Measured, one prompt, signed-in network payloads.*[^seer-chatgpt-structure]
- **Do:** note the model version next to every tracking series and every fan-out count — per answer, not per run date — start a new baseline at each model change, report fan-out metrics (queries, retrieved URLs, `site:` share) as ranges rather than single values, keep the raw captures, and don't build a prompt set only from short prompts.[^seer-chatgpt-structure] Test for your own prompts: [test 20](diagnostic-tests.md#20-which-sites-does-chatgpt-search-inside).

> **Conflict:** `site:` fan-outs at 26.2 % (consumer app, vendor logs) and 76 % on GPT-5.6 (346 prompts) vs 0.15–6 % (API) — [details](../reference/conflicts.md#how-often-does-chatgpt-search-inside-sites)

## 12. Entity tracking with search on and off
- An alternative to prompt tracking: track canonical entities (your brand, product lines) with one fixed prompt each, run with web search on and off — off is the model's parametric baseline — up to 100 samples per brand–entity pair, and report the share of answers that name you. *Practitioner method.*[^dj-prompt]
- **Do:** use the search-off series to see what the model "knows" without retrieval, and the gap between on and off to see what retrieval adds; re-baseline at model changes ([section 11](#11-re-baseline-at-every-model-change)).

## 13. Brand canon: accurate, wrong, no answer
- **Silence is the bigger gap than error.** In one B2B brand's study of its own brand (1,562 prompts a day across 6 AI surfaces, 28,123 responses, 87 attributes, 1 May – 9 June 2026), answers were accurate 95.9 % of the time when the engine answered, but 31.2 % of prompts got no answer and 2.8 % were wrong. Claude declined most (46.3 %), AI Mode least (24.1 %). Comparative prompts were only 18.8 % accurate because 80.3 % went unanswered. The brand's own domain supplied about 35 % of 219,349 citations, and wrong answers traced back to stale third-party profiles (location, headcount, services). *Measured, one brand, B2B.*[^seer-brand-accuracy]
- **Do:** keep a "brand canon" — a list of checkable facts (for a shop: locations and pickup, delivery countries and times, returns, payment options, services offered and not offered, assortment boundaries) — ask about each on a schedule, and track accurate / wrong / no-answer rates per engine. Fix wrong facts on your own site and the profiles engines cite first ([third-party presence](../channels/third-party-presence.md), [homepage and brand](../page-types/homepage-and-brand.md)). Method, including obscure attributes: [test 22](diagnostic-tests.md#22-brand-canon-accuracy).

## 14. Share of voice, not only presence
- **Presence can rise while share falls.** In one client case, visibility rose from 38 % to 44 % while brands per answer rose from 3.8 to 5.1 and share of voice fell from 26 % to 21 %; a category "owner" lost the "best overall" recommendation in 35 % of the answers that mentioned it. *Measured, case plus hypotheticals.*[^seer-visibility-lying] Report share of voice, and clean vs caveated recommendations, next to presence %.
- **Inclusion is not preference.** Prompt tracking partly measures interface volatility; being listed doesn't mean being chosen. One framework reads AI visibility against six dimensions: experience integrity, physical availability, mental availability (needs surveys), distinctiveness, reputation and commercial proof. *Practitioner, argument.*[^ja-clicks]
- **Excess share of voice as a leading indicator.** Share of voice minus market share (excess share of voice) leads; direct plus branded traffic lags, and messaging-app "dark traffic" inflates Direct. Roll out changes staggered by topic group, with holdout groups, so the effect can be read. *Practitioner, essay.*[^brief-availability]
- **Scoring mentions.** The RAPP audit scores each mention as Regular (across runs and time), Accurate (price, locations, offer current), Prominent (listed first) and Positive (sentiment, including caveats). Keep presence % as the headline, log accuracy and sentiment, and treat position as a secondary, noisy field. *Practitioner framework.*[^cc-rapp]

> **Conflict:** answer position ("Prominent") as a KPI vs presence % given run-to-run volatility — [details](../reference/conflicts.md#track-answer-position-or-presence)

## 15. Building the prompt set
- **Seed from category entry points, not only your own queries.** Measure AI presence like brand salience: a representative set of category entry points (the needs and situations in which buyers think of the category), relative to competitors, presence rather than sentiment. A topic set seeded only from your own Search Console or Bing queries shows only where you already compete. *Practitioner, relays an Ehrenberg-Bass paper.*[^brief-topical]
- **Mine shared ChatGPT conversations.** Shared ChatGPT conversations appear as a linking domain in Search Console's Links report — "thousands of links" for some sites — marked noindex/nofollow, but they show real questions and the citations given; sometimes they appear only in directory properties. *Practitioner, client properties.*[^gg-gsclinks] Export them soon (they may disappear) and use the questions as prompts.
- **Size AI use per audience before setting KPIs.** In SparkToro audience data relayed by one practitioner, "programming" searchers were 111.7 % more likely than average US users to use ChatGPT for search, while ChatGPT wasn't among the top seven discovery channels for "potatoes" searchers. *Relayed vendor data.*[^cc-kpis] Check how much your buyers use assistants before setting AI-visibility targets.
- Other seeds: Search Console queries rewritten conversationally ([Search Console](search-console.md#12-bot-like-llm-query-bursts)); runs and sizing in [test 9](diagnostic-tests.md#9-prompt-tracking-per-engine).

## 16. Runs, phrasings and margin of error
From SparkToro (which sells audience research) with Gumshoe.ai (which sells AI-visibility tracking): ~600 volunteers over 5 surveys and 3 months, 142 human-written prompts, 994 runs across 7 model families.[^sp-track-ai-visibility]
- **Lists don't repeat; presence does.** Getting the same brand list twice took ~124 runs and the same brands in the same order ~1,429 (one prompt). Yet the average visibility of the top 3 brands was stable: ChatGPT 64 %, Claude 73 %, Google AI 68 % (SD ~20 %). One hospital appeared in 69 of 71 ChatGPT answers but ranked first in only about a third. B2B prompts showed much lower visibility. *Measured.*[^sp-track-ai-visibility]
- **People phrase one goal very differently:** the average pairwise semantic similarity of the prompts was 0.0809. Use several realistic phrasings per need (e.g. derived from search keywords), not one synthetic prompt. *Measured.*[^sp-track-ai-visibility]
- **Sampling rule:** 10 prompts × 7 phrasings × 7 models = 490 results per pass gives about ±5 points; about 20 passes give ±1 point. Disclose the margin, and distrust tools that don't publish run counts. *Measured; vendor data.*[^sp-track-ai-visibility] Per-prompt margins: [test 9](diagnostic-tests.md#9-prompt-tracking-per-engine).
- **Drop position as a KPI;** position in an AI answer is close to random. Read citation-correlation studies like ranking-factor correlations, since citations are often added after the answer. *Practitioner.*[^sp-track-ai-visibility]
- **Missing method.** MLforSEO (which sells courses) recommends citation rate over a fixed question set but gives no number of prompts, runs per prompt or confidence intervals. *Practitioner.*[^mlseo-rank-tracker] The same posts give unsourced figures (visible AI referrals ~0.15 % of traffic, ChatGPT crawl-to-referral ~3,700:1, citation rate 5–15 % unoptimised vs 40–60 % optimised); don't quote them. *Inference (unsourced).*[^mlseo-rank-tracker]

> **Conflict:** drop answer position as a KPI (SparkToro) vs "Prominent" as one of four scored fields in the RAPP audit ([section 14](#14-share-of-voice-not-only-presence)). — [details](../reference/conflicts.md#track-answer-position-or-presence)

## 17. AI as a brand channel
- **A visit lift after AI recommendations.** In Similarweb clickstream data, devices that saw AI answers recommending a brand were more likely to visit it within 7 days: +7.2 % and +14.2 % for two credit-card brands; recommended brands gained more direct visits and branded search than brands not mentioned (no numbers given). *Measured; vendor data, sample not stated.*[^sp-similarweb-ai-mentions]
- **Caveats from the author:** only large brands in finance, travel and beauty; no counterfactual; no comparison with a #1 ranking or video presence; B2B unclear. In the same data traditional search was still about 100× more used than AI to start a journey. *Measured + inference.*[^sp-similarweb-ai-mentions]
- **Small as a traffic channel.** Across 100 sites LLMs sent 0.73 % of referral traffic (ChatGPT 0.62 %), less than DuckDuckGo, and Google drove 97 % of conversions (Marie Haynes); organic search sent ~39× more traffic than AI (SEOWorks). *Measured, relayed.*[^sp-ai-boondoggle]
- **Budget it as a brand channel** (a "digital billboard"), not a traffic channel. *Practitioner.*[^sp-ai-boondoggle] Read it by correlation with branded search and Direct ([analytics](analytics.md#18-demand-by-correlation-not-last-click)).

> **Conflict:** brand-visit lift after AI recommendations (Similarweb, large brands)[^sp-similarweb-ai-mentions] vs no reliable correlation between AI visibility and branded search or direct traffic on 12 sites (Kevin Indig, relayed)[^sp-ai-boondoggle]. — [details](../reference/conflicts.md#do-ai-recommendations-lift-brand-demand)

## 18. Dark AI traffic
- **70.6 % of identified AI visits arrived without a referrer** and landed in Direct, in Loamly's data (about 446,000 visits), relayed by MLforSEO; the author calls it one measurement, not a constant, and the headline "70 % of your AI influence" overstates it. *Measured, vendor data, relayed.*[^mlseo-dark-ai]
- **Proxy:** compare the Direct trend with the Search Console branded-search trend (illustrative: Direct +18 % vs branded +3 %), plus a ten-question citation audit across ChatGPT, Perplexity and Claude. *Practitioner.*[^mlseo-dark-ai] Bot-check Direct first ([test 10](diagnostic-tests.md#10-is-a-direct-spike-real)).
- AI-referred visits converted at 10.2 % vs 2.5 % for other traffic in the same dataset. *Measured, vendor data, relayed.*[^mlseo-dark-ai]

> **Conflict:** 70.6 % of identified AI visits land in Direct (Loamly) vs AI traces in 0.003 % of Direct in a placebo-tested study ([section 3](#3-direct-spikes-are-mostly-bots-not-hidden-ai)). — [details](../reference/conflicts.md#is-ai-traffic-hiding-in-direct)

> **Conflict:** AI referrals convert 4× better (Loamly, 10.2 % vs 2.5 %) vs parity for ecommerce and worse than organic on 23 of 63 sites (SEOWorks, relayed)[^sp-ai-boondoggle] ([section 5](#5-scale-of-the-channel)). — [details](../reference/conflicts.md#does-ai-traffic-convert-better)

## 19. AI Overview citation tracking
- **Cited domains differ from ranking domains.** On 29 keywords (US desktop, 2026-10-25) an AI Overview showed on all 29; the median overlap between cited and organically ranking domains was 22 %, and 0 % for seven keywords; one domain was cited first while absent from the organic top 10. *Measured, small sample, vendor tool (DataForSEO).*[^mlseo-aio-tracker]
- **Method:** run weekly on a fixed set of 50–200 keywords with fixed location, language and device; report share of citations and keyword coverage separately (two domains each had 4 of 19 citations but coverage of 0.667 vs 0.333). Cost is up to ~$0.40 per 100 keywords. Citations aren't clicks. *Practitioner.*[^mlseo-aio-tracker] Rank-tracker view: [rank tracking](rank-tracking.md#7-cited-vs-ranking-domains-across-keywords).

Related: [analytics](analytics.md), [Search Console](search-console.md), [diagnostic tests](diagnostic-tests.md), [AI assistants](../how-it-works/ai-assistants.md), [third-party presence](../channels/third-party-presence.md).

[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: GSC impression inflation (week of 2026-04-04), GA4 AI Assistant channel (2026-05-09), GA4 bug (2026-08-29), GPT-6 referral loss with Adobe data (2026-10-10), Comscore, Seer and the field experiment on AIO clicks (2026-04-25), SparkToro zero-click; secondary reporting, primary sources not checked.
[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: utm on ~95 % of displayed links; model-opened pages untagged.
[^gm-direct]: Growth Memo, 2026-10-19: 12 GA4 properties (B2B-skewed), 4 brands, 632 correlation tests; 409,000 Direct sessions with 198 engaged on one site; AI traces 0.003 % of Direct; correlations failed placebo and split-period tests.
[^ipr-brand]: iPullRank, 2026-10-22: cites Growth Memo correlations and the ~70 % estimate (older than Growth Memo's 2026-10-19 test); BrightEdge 3.2× mentions vs citations; Pew, 900 adults.
[^mh-geo]: Marie Haynes, 2026-10-21: 100 GA4 properties, >145M sessions; method not published; 0.62 % / 0.73 % of Google organic sessions; CR 13.8 % vs 3.02 % on 55 sites; 964 vs 36 conversions.
[^siege-conversion]: Siege Media, 2026-06-30: 78 of 120 screened GA4 properties, session key-event rate, Jan–May 2026; AI 0.2–3 % of sessions.
[^aleyda-traffic]: Aleyda Solis, ~Apr–May 2026, via search extracts: 4 verticals × 10 US sites, Semrush and Similarweb estimates; some AI traffic may be agents.
[^ipr-aimode-referrals]: iPullRank (Sussman), 2025-09-26: SimilarWeb panel 20 May – 19 Aug 2025.
[^gm-consensus]: Growth Memo, 2026-05-11: 91.07 % of cited URLs in only one engine; 2.37 % all three; 1.2 % product, 1.6 % category; author calls it directional.
[^bp-chatgpt-links]: Botpresso, ≈2026-07: 52 client sites (43 B2C, 9 B2B), GA4 ChatGPT referrals 26 Mar – 6 May vs 7 May – 17 Jun 2026; observational, no control; OpenAI didn't announce the change.
[^bp-ga4-ai]: Botpresso, ≈2025-09: GA4 AI-traffic channel with 16 source patterns; warns that unanchored patterns produce false matches.
[^ah-mentions-links]: Ahrefs, 2025-11-26: Ahrefs' own brand, 31,000+ AI mentions; linked share by platform, ~28 % overall. Single brand.
[^ah-aio-change]: Ahrefs, 2025-11-11: 43,000+ keywords, ≥ 16 observations each over ~1 month; 70 % changed text, persistence 2.15 days, 54.5 % shared URLs.
[^nz-aimeas]: Natzir Turrado, 2026-05-17, updated to 2026-10: server logs vs GA4 on several sites; GA4 AI Assistant channel since 2026-05-13; UTM bug 2026-10-07 to 16, −68 to −74 % ChatGPT-attributed visits in logs, −20 to −60 % in GA4.
[^nz-bingai]: Natzir Turrado, 2026-05-18: Bing Webmaster Tools AI Performance exports for 6 sites; query–page mapping coverage 24.6–96.6 % of citations, 10–25 % of pages on mid/large sites; little use under 200 citations; 7–33 % of grounding queries (0.4–20 % weighted) without Google/Bing impressions; AI-only URLs 0.009–0.9 % of citations.
[^nz-trackers]: Natzir Turrado, 2026-01-29: review of vendor studies (API vs UI 7 vs 16 sources, Perplexity 8 % overlap; Peec 43 % English sub-queries; SparkToro < 1-in-100 same list; correlated errors, SE > 3×) plus own Bing data from 6 sites; vendor studies not re-checked.
[^nz-model]: Natzir Turrado, 2026-10-21: 4 Gemini models, 7–20 runs per model per prompt, ablations, 5 categories; 1/7 vs 7/7, p = 0.005; AI Mode 0/20; small samples.
[^mt-memory]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2025-12-20: hidden metadata in one account's ChatGPT responses.
[^dj-prompt]: DEJAN, 2026-10-04: practitioner method — one fixed prompt per canonical entity, search on and off, up to 100 samples per brand–entity pair, share of answers.
[^dj-sitefanout]: DEJAN, 2026-08-25: 551,695 fan-outs, 196,692 from OpenAI, collected via the API; fan-outs per searched response 6.16 (Mar 2026) → 1.10 (Aug 2026); `site:` share by model; consumer app not tested.
[^mt-sitequeries]: Metehan Yeşilyurt (works at Peec AI), 2026-08-21: Peec consumer-app logs, 14.9M queries a week; `site:` share < 0.11 % (mid-May – late Jul 2026) → 10.2 % (week of Aug 3) → 26.2 % (week of Aug 10); not reproducible outside Peec.
[^ls-context]: Lazarina Stoy, 2026-10-25: relays iPullRank's Personal Intelligence test (May 2026; 1,922 AI Mode responses, 8 product categories, few accounts, opt-in): seeded brands 23.9 % → 66.8 %, control 21.9 % → 18.9 %, Gmail-seeded 53.6 %, Photos-seeded 10.5 %, top-3 placement +~23 points; primary not re-checked.
[^seer-brand-accuracy]: Seer Interactive, 2026-08-27: own (B2B) brand; 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, 2026-05-01 – 2026-06-09; accurate 95.9 % when answered, no answer 31.2 %, wrong 2.8 %; Claude declined 46.3 %, AI Mode 24.1 %; comparative prompts 18.8 % accurate, 80.3 % unanswered; own domain ~35 % of 219,349 citations; wrong answers from stale profiles.
[^seer-luna]: Seer Interactive, 2026-09-24: 346 matched prompts, 6 industries, GPT-5.5 vs GPT-5.6 "Luna" (ChatGPT default since 2026-07-09); `site:` in 76 % vs 21.6 % of fan-outs; non-brand 20.6 % → 77.3 %; sources 6,134 → 3,481; open searches 575 → 175; inline citations −12.9 %.
[^seer-chatgpt-structure]: Seer Interactive, 2026-10-22: one prompt captured 3 times plus a 6-prompt suite, signed-in network payloads; identical runs 8 minutes apart shared no query strings; retrieved URLs 14 → 40 over 13 days, 34 never cited; mid-session model switch gpt-5-6 → gpt-5-6-mini; payload format changed within two weeks; n = 1 prompt.
[^seer-visibility-lying]: Seer Interactive, 2026-08-31: 2 client cases plus hypotheticals; visibility 38 % → 44 %, brands per answer 3.8 → 5.1, share of voice 26 % → 21 %; category leader lost "best overall" in 35 % of answers mentioning it.
[^ja-clicks]: Jono Alderson, 2026-03-12: argument; prompt tracking measures interface volatility; "inclusion is not preference"; six dimensions.
[^brief-availability]: Jes Scholz, SEO Brief, 2026-07-08: essay and methods; excess share of voice as leading indicator, direct + branded as lagging; dark traffic inflates Direct; staggered rollout by topic group with holdouts.
[^cc-rapp]: Crystal Carter, ≈2026-03: RAPP audit (Regular, Accurate, Prominent, Positive); practitioner framework, no measured study.
[^brief-topical]: Jes Scholz, SEO Brief, 2026-04-08: essay relaying an Ehrenberg-Bass salience paper; category entry points, relative to competitors, presence not sentiment; topic sets from own queries show only where you compete.
[^gg-gsclinks]: Glenn Gabe (GSQi), 2026-03-18: shared ChatGPT conversations in the GSC Links report on client properties ("thousands of links" for some), noindex/nofollow, sometimes only in directory properties.
[^cc-kpis]: Crystal Carter, Wix AI Search Lab, 2025-07-29 (updated 2025-08-03): relays SparkToro audience data ("programming" searchers +111.7 % likelier to use ChatGPT for search; ChatGPT not in the top seven discovery channels for "potatoes" searchers); framework.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page; one-week loss of ChatGPT referrer and UTM in October 2026. Dates and sizes from the shop's caveat list are omitted so the shop can't be identified.
[^am-unassigned]: Analytics Mania, updated 2026-09-18: AI-assistant links with utm_source but no utm_medium land in Unassigned; GA4's AI Assistant channel coverage partial (Sep 2026); custom channel group advised.
[^sp-track-ai-visibility]: SparkToro (Rand Fishkin), 2026-05-07: SparkToro x Gumshoe.ai study, ~600 volunteers, 142 prompts × 7 model families = 994 runs; ~124 / ~1,429 runs for repeat lists; top-3 visibility 64 / 73 / 68 %; prompt similarity 0.0809; 490 results per pass ≈ ±5 points; video transcript, figures approximate.
[^mlseo-rank-tracker]: MLforSEO (Beatrice Gamba), 2026-08-03: recommends citation rate without a sampling method; most figures unsourced.
[^sp-similarweb-ai-mentions]: SparkToro with Similarweb, 2026-06-28: clickstream panel, 7-day window, credit-card answers (+7.2 %, +14.2 %); large brands in finance, travel, beauty only; sample not stated; video transcript.
[^sp-ai-boondoggle]: SparkToro (Rand Fishkin), 2026-10-22: relays Marie Haynes (100 sites, 12 months), SEOWorks (Sep 2025 – Aug 2026; site count given as 95 and as 63), Kevin Indig (12 sites); citing Mike King for "digital billboard".
[^mlseo-dark-ai]: MLforSEO (Beatrice Gamba), 2026-08-21, updated 2026-10-24: relays Loamly vendor data (~446,000 identified AI visits; 70.6 % without referrer; CR 10.2 % vs 2.5 %); Direct vs branded proxy is illustrative.
[^mlseo-aio-tracker]: MLforSEO (Lazarina Stoy), 2026-10-24: DataForSEO-based tracker, 29 keywords, US desktop, 2026-10-25; median cited/organic domain overlap 22 %; cost estimate at October 2026 list prices.
[^chuleta-timelines]: Chuleta SEO, 2026-10-22, Spanish, read in full; claims translated. Paraphrases Gary Illyes at Search Central Live Barcelona (no direct quote or recording given): new page discovered in ~20 hours, existing page re-crawled ~30 days, link signals processed in minutes to 3 weeks, title updates 1–2 days, site migration 1–3 months, core-update recovery 3–6 months (up to a year); the author notes the steps add up. Also relays a Cloudflare–OpenAI discovery pilot ("hundreds of millions" of pages, no method) and Bing's Topics Portfolio beta.
