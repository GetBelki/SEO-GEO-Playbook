---
type: Playbook
title: Local search and Maps
description: Local visibility in Maps and AI answers — the business profile's primary category and identity data, category diversity in local results, the business website as the most-cited local source, directories (Foursquare, Yelp, Bing Places) as verification and ChatGPT's Foursquare dependence, reviews and which ones get shown, photos, local-inventory results, Gemini in Maps, and profiles and location pages for multi-location retail.
tags: [local, maps, business-profile, reviews, directories, foursquare, ai-mode, chatgpt, geo, location-pages, multi-location]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: maps
    resource: "https://think.resoneo.com/google-map-dissected/"
    title: "Resoneo, Google Maps dissected (Aug 2026)"
  - id: ipr-local
    resource: "https://ipullrank.com/local-ai-search-data"
    title: "iPullRank (Francine Monahan), Local AI search data (2025-12-16; Yext, 1.6M questions, 6.9M citations)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: thrive-sources
    resource: "https://thriveagency.com/news/what-sources-do-ai-platforms-use-to-evaluate-businesses/"
    title: "Thrive, What sources do AI platforms use (2026-09-10; relays Moz, SearchAtlas, Ahrefs)"
  - id: thrive-gbp-directories
    resource: "https://thriveagency.com/news/google-business-profile-vs-business-directories-which-matters-more-for-ai-visibility/"
    title: "Thrive, Google Business Profile vs business directories: which matters more for AI visibility (2026-09-03; relays the SteadyDemand AI Citation Ledger, 14,000+ citations)"
  - id: thrive-ai-mode-local
    resource: "https://thriveagency.com/news/10-local-seo-tips-to-increase-your-visibility-in-ai-mode/"
    title: "Thrive, 10 local SEO tips to increase your visibility in AI Mode (2026-03-02; relays Whitespark)"
  - id: thrive-ask-maps
    resource: "https://thriveagency.com/news/google-ask-maps-is-here-how-does-this-impact-your-local-business/"
    title: "Thrive, Google Ask Maps is here (2026-08-31; practitioner report, no Google source)"
  - id: thrive-reviews
    resource: "https://thriveagency.com/news/do-google-reviews-help-my-business-rank-higher-on-google-maps/"
    title: "Thrive, Do Google reviews help my business rank higher on Google Maps? (2026-09-30; relays Local Falcon, Whitespark, SteadyDemand and a Google blog post)"
  - id: ah-maps
    resource: "https://ahrefs.com/blog/google-maps-seo/"
    title: "Ahrefs, Google Maps SEO (2026-02-02)"
  - id: ah-locations
    resource: "https://ahrefs.com/blog/location-pages/"
    title: "Ahrefs, Location pages (2023-12-22) and franchise SEO (2024-05-29)"
  - id: ah-restaurant
    resource: "https://ahrefs.com/blog/restaurant-seo/"
    title: "Ahrefs, Restaurant SEO (2024-08-26; cites Google 2019, BrightLocal)"
  - id: nz-gptleak
    resource: "https://natzir.com/en/seo/chatgpt-leaks-seo-for-ai/"
    title: "Natzir Turrado, What the ChatGPT leaks teach about SEO for AI (2025-08-20; leaked system prompt/config, 50 local prompts Spain May 2025)"
  - id: sbs-localdiversity
    resource: "https://www.seobythesea.com/2019/09/category-diversity/"
    title: "SEO by the Sea, Category diversity in local results (2019-09-05; patent US 10,289,648, filed 2016-11-14)"
  - id: sbs-reviews
    resource: "https://www.seobythesea.com/2011/05/how-google-might-choose-high-quality-reviews-to-display-for-products-and-businesses/"
    title: "SEO by the Sea, How Google might choose reviews to display (2011-05-26; application US 2011/0125736)"
---

# Local search and Maps

What decides whether a business with physical locations shows in Google Maps, the local pack and AI answers to local questions. Most local AI figures below are relayed by one agency blog with no published method; treat them as directional. Confidence labels follow the [scale](../reference/sources-and-confidence.md).

## Rules
- **Fix the business profile's primary category and identity data (name, address, hours) before anything else.** *From code* — [evidence](#1-maps-ranking-signals)
- **Keep the same facts on your website and in every listing**, because AI answers cite the website first and use listings to verify it. *Measured; Practitioner, relayed* — [evidence](#2-ai-answers-cite-the-website-first-listings-verify)
- **Check and complete your Foursquare and Bing Places listings, not only Google's**, and keep name, address and phone identical everywhere; ChatGPT's local answers have drawn mainly on Foursquare. *Practitioner, relayed; From the leak, May 2025* — [evidence](#2-ai-answers-cite-the-website-first-listings-verify)
- **Ask every customer for a review, with a prompt for specific detail (use, fit, delivery), and never buy, gate or incentivise them.** *Official (removals, policy); Practitioner, relayed (weights); Patent application (selection)* — [evidence](#3-reviews)
- **Pick a truthful primary or secondary category where fewer competitors crowd the results**, if one honestly fits. *Patent* — [evidence](#6-category-diversity-in-local-results)
- **Supply local inventory through local inventory feeds and the business profile** so products appear in Shopping's local results. *Practitioner* — [evidence](#4-local-inventory-and-new-surfaces)
- **Keep reviews, photos, attributes and hours complete in the profile** for conversational Maps features — unverified, but the same work helps Maps ranking anyway. *Practitioner, relayed, unverified* — [evidence](#4-local-inventory-and-new-surfaces)
- **Work on the local pack and Maps first; track AI features on local queries at lower priority** — estimates of how often they appear range from 7.9 % to 57 %. *Measured, vendor data; Practitioner, relayed* — [evidence](#4-local-inventory-and-new-surfaces)
- **Give every location its own Business Profile and its own location page**, linked to each other, and create no pages for areas without a store. *Practitioner, one case* — [evidence](#5-multi-location-retail)

## 1. Maps ranking signals
Maps ranks on 72 named signals (reviews, direction requests, homepage clicks, brand query volume, Wikipedia). Only the primary category acts as a switch; identity errors weigh more than unoptimised fields. *From code; weights unknown.*[^maps] **Rule:** correct primary category and clean identity data (name, address, hours) before anything else.
- **Practitioners agree.** A 2026 expert survey ranks the primary category as the #1 Maps factor, and unstructured citations (mentions on other sites) #4 for AI visibility. *Practitioner survey, relayed (Whitespark).*[^ah-maps]
- **Photos pay off.** Profiles with photos got 42 % more direction requests and 35 % more website clicks (Google, 2019); profiles with 100+ photos got 520 % more calls (BrightLocal). *Relayed, dated surveys.*[^ah-restaurant] Upload real photos of each store, its interior and its range.

## 2. AI answers cite the website first, listings verify
- **Local answers cite websites first.** Across 1.6M local questions and 6.9M citations in ChatGPT, Gemini and Perplexity, the business's own website led and was growing; listings acted as verification. *Measured, vendor data (Yext).*[^ipr-local] Keep the same facts on the site and in every listing.
- **Websites ~60 %, directories 20–30 %.** Business websites were reported at about 60 % of AI citations and directories at 20–30 % depending on query type, from a ledger of 14,000+ citations. *Practitioner, relayed; method not described.*[^thrive-gbp-directories] Same direction as the Yext study above.
- **ChatGPT leans on Foursquare.** Foursquare was reported as ChatGPT's main local business data provider, in about 70 % of local queries, and Yelp in about 33 %. *Relayed; no method published.*[^thrive-sources] **Do:** check your Foursquare and Bing Places listings, and keep name, address and phone (NAP) identical across them, the business profile and your site.
- **The leak points the same way.** Leaked ChatGPT response data from 50 local prompts in Spain (May 2025) showed Foursquare Places as the main source — 60–70 % of the top-listed businesses, by the analyst's count. ChatGPT truncated results to 10 venues, and their order followed the data provider's response latency, not rating. *From the leak, May 2025; may be stale.*[^nz-gptleak] It corroborates the relayed ~70 % above. **Do:** complete the Foursquare listing — hours, price level, categories, photos (about 4:3).

## 3. Reviews
- **Reviews are one part of local-pack weight.** A 2026 expert survey put review signals at 20 % and business-profile signals at 32 % of local-pack ranking weight. *Practitioner survey, relayed (Whitespark).*[^thrive-reviews] A study of 50 million Google Maps results gave median review counts of 3-pack businesses by category. *Measured, relayed (Local Falcon).*[^thrive-reviews] Compare your review count with the businesses in your own category's 3-pack, not with a global benchmark.
- **Google removes fake reviews at scale.** Google blocked or removed 292 million fake and policy-violating reviews from Maps in 2025. *Official, relayed (Google blog).*[^thrive-reviews] Bought or gated reviews are a risk, not a shortcut.
- **Asking works.** 69 % of consumers left a review when asked. *Relayed, dated survey (BrightLocal).*[^ah-restaurant] Ask every customer; don't offer anything in return.
- **Which reviews get shown.** A Google patent application describes choosing displayed reviews by clustering them (by topic and star band) and then picking by quality: grammar, length, no all-caps or profanity, and vocabulary specific to that kind of review. *Patent application; current use unknown.*[^sbs-reviews] **Do:** when asking for reviews, prompt for specific detail — how the product was used, fit, delivery — rather than a generic "rate us".
- **Don't adopt: incentives for reviews.** One practitioner guide suggests offering discounts or free items for reviews.[^ah-maps] That breaches Google's review policy, which forbids incentivised reviews. *Practitioner advice, non-compliant.*
- **Rating of AI-recommended businesses.** ChatGPT-recommended businesses were reported to average 4.76 stars (SteadyDemand)[^thrive-reviews] and 4.3 stars (Soci.ai).[^thrive-sources] *Relayed, no method published for either.*

  > **Conflict:** two Thrive posts give 4.76 and 4.3 as the average rating of ChatGPT-recommended businesses; neither method is published, and one post uses 4.3 as Local Falcon's competitive minimum. Don't plan on a rating threshold.

## 4. Local inventory and new surfaces
- **Local stores.** A "Stores" tab in Shopping shows local-inventory results (Mar 2026); local inventory feeds and the business profile supply it.[^brodie-notes] Feed setup in [feeds and Merchant Center](feeds-and-merchant-center.md).
- **AI features on local queries.** 57 % of local queries showed an AI Overview or AI Mode. *Practitioner, relayed (Whitespark); no method published.*[^thrive-ai-mode-local] A large US crawl found AI Overviews on only 7.9 % of local searches (Sept 2025, desktop). *Measured, vendor data.*[^ah-maps] **Do:** work on the local pack and Maps first; track AI answers to local prompts at lower priority.

  > **Conflict:** 57 % (AI Overview or AI Mode, relayed, no method) vs 7.9 % (AI Overviews only, US desktop crawl, Sept 2025). The surfaces, dates and query sets differ; check your own local queries before planning on either — [details](../reference/conflicts.md#how-often-do-ai-overviews-show).
- **"Ask Maps".** Gemini in Google Maps was reported to rank places by reviews, photos, attributes and hours. *Practitioner report, relayed, without a Google source — unverified.*[^thrive-ask-maps]

## 5. Multi-location retail
For shops with several physical stores. *Practitioner, one case.*[^ah-locations]
- **One profile per location** on Google Business Profile, Bing Places and Apple Business Connect. Name it "Brand + location" and link it to that location's page, not the homepage.
- **Location pages from one template, with unique elements:** address, opening hours, map pin, real photos of that store, local services and offers, reviews. Put menus, catalogues and price lists on the page as mobile-friendly HTML, not as PDFs.[^ah-restaurant]
- **URL pattern.** Several cities: `/location/service`; one area: `/service/location`.
- **Regional hubs only where a store and demand exist.** No city-swap pages, no pages for areas where you have no presence.
- **Case.** A fitness franchise's location pages reached ~45,000 monthly visits in ~10 months.[^ah-locations] One brand, self-reported by the publisher.
- Local inventory for these stores: [section 4](#4-local-inventory-and-new-surfaces) and [feeds and Merchant Center](feeds-and-merchant-center.md).

## 6. Category diversity in local results
- A Google patent describes enforcing category diversity in local results: when one business category is over-represented, its results are scaled down so other categories get room. *Patent; current use unknown.*[^sbs-localdiversity]
- **Do:** if a truthful, less crowded primary or secondary category fits the store (for example a specialist category next to a generic one), use it; it can surface the store where the generic category is saturated. Never pick a category the business doesn't serve — the primary category is still the main Maps switch ([section 1](#1-maps-ranking-signals)). *Inference.*

Related: [Google AI features](../how-it-works/google-ai-features.md), [AI assistants](../how-it-works/ai-assistants.md), [third-party presence](third-party-presence.md), [homepage and brand](../page-types/homepage-and-brand.md), [AI visibility tracking](../measure/ai-visibility-tracking.md).

[^maps]: Resoneo, Google Maps dissected, Aug 2026: 72 RankSignal values, primary category, identity.
[^ipr-local]: iPullRank, 2025-12-16: Yext study; Google doesn't cite Business Profiles.
[^brodie-notes]: Brodie Clark notes (month anchor #mar-2026): "Stores" tab with local-inventory results in Shopping.
[^thrive-gbp-directories]: Thrive, 2026-09-03, relaying the SteadyDemand AI Citation Ledger (14,000+ citations; method not described); the quoted sentence doesn't itself say "local", the article frames it as local business information. Primary study not checked.
[^thrive-sources]: Thrive, 2026-09-10, relaying MapAtlas (Foursquare ~70 % of ChatGPT local recommendation queries, Yelp ~33 %; no method) and a Soci.ai 2026 study (4.3-star average for recommended businesses; no sample or method). The post also has an uncited 3.4-star exclusion claim that conflicts with its own 4.0+ minimum. Read 2026-10-28.
[^thrive-ai-mode-local]: Thrive, 2026-03-02, relaying Whitespark: 57 % of local queries with AIO/AI Mode; no method published.
[^thrive-ask-maps]: Thrive, 2026-08-31: "Ask Maps" ranking factors; practitioner reading, no Google source cited.
[^thrive-reviews]: Thrive, 2026-09-30, read 2026-10-28: Local Falcon whitepaper (50 million Google Maps results; 4.3-star minimum, 4.5–4.8 optimal); Whitespark 2026 survey (reviews 20 %, GBP 32 %); SteadyDemand 4.76-star average for ChatGPT-recommended businesses; Google blog, 292 million fake reviews removed in 2025.
[^ah-maps]: Ahrefs, Google Maps SEO, 2026-02-02: AI Overviews on 7.9 % of local searches (from Ahrefs' AI Overview trigger study, 146.1M US desktop SERPs, Sept 2025); Whitespark 2026 survey (primary category #1 Maps factor, unstructured citations #4 for AI visibility); also suggests discounts or free items for reviews, which Google's review policy forbids.
[^ah-locations]: Ahrefs, location pages (2023-12-22) and franchise SEO (2024-05-29): practitioner advice; one profile per location (Google, Bing Places, Apple Business Connect); template with unique elements; URL patterns; no city-swap pages; one fitness-franchise case (~45,000 monthly visits in ~10 months).
[^ah-restaurant]: Ahrefs, restaurant SEO, 2024-08-26, citing Google (2019: photos → 42 % more direction requests, 35 % more website clicks) and BrightLocal (100+ photos → 520 % more calls; 69 % left a review when asked); menus as mobile HTML, not PDF. Dated surveys, not re-checked at source.
[^nz-gptleak]: Natzir Turrado, 2025-08-20: leaked ChatGPT system prompt, config and local response JSON; 50 local prompts in Spain, May 2025; Foursquare Places 60–70 % of top-listed businesses (his figure); truncation to 10 venues; order by response latency. May be stale.
[^sbs-localdiversity]: SEO by the Sea (Bill Slawski), 2019-09-05: patent US 10,289,648 (filed 2016-11-14), category diversity in local results. Patent analysis; blog inactive since 2022.
[^sbs-reviews]: SEO by the Sea (Bill Slawski), 2011-05-26: application US 2011/0125736, review selection by clustering (topic, star band) then quality (grammar, length, no caps or profanity, high-IDF vocabulary per review type). Grant status not verified.
