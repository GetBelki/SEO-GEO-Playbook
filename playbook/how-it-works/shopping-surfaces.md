---
type: Guide
title: How shopping surfaces pick products
description: Where AI product cards and grids come from (ChatGPT, AI Mode, Google Shopping), shortlist behaviour, ads in grids and in ChatGPT answers, checkout on Google and agent readiness (native controls, offer accuracy, standing conditions), the 2026 EEA free-listings removal, and how Google reads product lines, Chrome's shopping classifier and AI Mode layout tags.
tags: [geo, shopping, feeds, merchant-center, agentic-commerce, chatgpt, ai-mode, eea, dma, product-lines, chrome]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays third-party studies)"
  - id: ignite-ai-mode
    resource: "https://ignitevisibility.com/google-ai-mode/"
    title: "Ignite Visibility, Google AI Mode (2026-09-30)"
  - id: aleyda-ucp
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/ugc-agentic-commerce-seo/"
    title: "Aleyda Solis, UCP and agentic commerce (~2026-10-10; search extracts)"
  - id: aleyda-global
    resource: "https://www.aleydasolis.com/en/ai-search/global-ai-search-strategy/"
    title: "Aleyda Solis, Global AI search strategy (Mar–Apr 2026; Similarweb, 10 markets, ~87.6M AI visits; search extracts)"
  - id: ipr-openai-feed
    resource: "https://ipullrank.com/ecommerce-chatgpt-product-feeds"
    title: "iPullRank, Ecommerce ChatGPT product feeds (2025-10-20; on OpenAI's product feed spec)"
  - id: ipr-aimode-study
    resource: "https://ipullrank.com/ai-mode-ecommerce-study"
    title: "iPullRank (Francine Monahan), AI Mode ecommerce study (2025-09-17; 100 survey participants + 23 interviews, one task)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: gm-grids
    resource: "https://www.growth-memo.com/p/organic-rankings-vs-product-grids"
    title: "Growth Memo, Organic rankings vs product grids (2026-03-09; 4K+ keywords, 40K product grids; body paywalled)"
  - id: gm-highstakes
    resource: "https://www.growth-memo.com/p/how-consumers-navigate-high-stakes"
    title: "Growth Memo, How consumers navigate high-stakes purchases (2026-04-07; usability study, 185 purchase tasks)"
  - id: gm-2027
    resource: "https://www.growth-memo.com/p/organic-growth-in-e-commerce-in-2027"
    title: "Growth Memo, Organic growth in e-commerce in 2027 (2026-10-12)"
  - id: mh-lighthouse
    resource: "https://www.mariehaynes.com/lighthouse-report-for-agents/"
    title: "Marie Haynes, Lighthouse report for agents (2026-05-29)"
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026)"
  - id: chatgpt-53
    resource: "https://think.resoneo.com/chatgpt/5.3-5.4/"
    title: "Resoneo, ChatGPT Search on GPT-5.3/5.4 (Mar–Apr 2026)"
  - id: chatgpt-shopping
    resource: "https://think.resoneo.com/scrap-chatgpt-plugin/chatgpt-shopping.html"
    title: "Resoneo, ChatGPT Shopping stream and system prompt (Nov 2025; one session)"
  - id: aio-aim
    resource: "https://think.resoneo.com/aio-aim-deepdive/"
    title: "Resoneo, AI Overviews / AI Mode deep dive (Feb 2026)"
  - id: intent-engine
    resource: "https://think.resoneo.com/google-intent-engine/"
    title: "Resoneo, What Google is building (Jun 2026)"
  - id: ucp
    resource: "https://searchind.com/ucp-agentic-ecommerce-seo/"
    title: "Searchind, Google's shift to Agentic Commerce (May 2026)"
  - id: eea
    resource: "https://searchind.com/googles-eea-search-changes-are-reshaping-product-visibility/"
    title: "Searchind, Google's EEA Search Changes are reshaping Product Visibility (Sep 2026)"
  - id: eea-press
    resource: "https://www.seroundtable.com/google-drops-free-product-listings-eea-42113.html"
    title: "Search Engine Roundtable and trade press on the EEA free-listings removal, read 2026-10-27"
  - id: ai-visible
    resource: "https://searchind.com/ecommerce-visibile-in-ai-search/"
    title: "Searchind, How to make your e-commerce visible in AI search (Sep 2025)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2026 (Search Console by search appearance and country; feed export)"
  - id: sbs-productlines
    resource: "https://www.seobythesea.com/2020/01/new-product-lines"
    title: "SEO by the Sea, Google Product Search and new product lines (2020-01-27; patent US 10,394,816, filed 2012-12-27)"
  - id: dj-shopclf
    resource: "https://dejan.ai/blog/google-shopping-classifier/"
    title: "DEJAN, Chrome's shopping classifier (2026-04-03; extracted TFLite models)"
  - id: dj-tags
    resource: "https://dejan.ai/blog/ai-mode-tags/"
    title: "DEJAN, AI Mode layout tags (2026-09-20; prompt-leak content, unverified)"
  - id: seer-chatgpt-ads
    resource: "https://www.seerinteractive.com/insights/chatgpt-ads-insights"
    title: "Seer Interactive, Early view of ChatGPT ads (2026-07-15, updated 2026-07-28; ~2 weeks, 97 tracking workspaces, 3,697 ads)"
  - id: ja-condition
    resource: "https://www.jonoalderson.com/conjecture/query-to-condition/"
    title: "Jono Alderson, From query to condition (2026-09-27; argument)"
  - id: gn-html
    resource: "https://www.seoforgooglenews.com/p/why-semantic-html-matters-for-seo"
    title: "Barry Adams, Why semantic HTML matters for SEO and AI (2025-08-06; practitioner)"
---

# How shopping surfaces pick products

This page answers where AI product cards, product grids and shopping agents get their products from, and what a shop must have in place to appear and be bought from there.

**In short.** For products, AI visibility is a feed problem, not a page problem. ChatGPT's product cards, Google AI Mode's product units and Google's shopping agents all draw on merchant feeds and shopping graphs. Attribute completeness and correct price and availability decide whether a product is *eligible* at all. Confidence labels follow the [scale](../reference/sources-and-confidence.md). How to fix the feed itself: [feeds and Merchant Center](../channels/feeds-and-merchant-center.md).

## Rules

- Get Merchant Center data and Google Shopping rank right first, because ChatGPT's carousels mostly mirror Google Shopping. *Measured* [why](#1-where-ai-product-cards-come-from)
- Keep price, availability and promotions error-free in the feed, because feed errors take a product out of the AI layer. *Practitioner* [why](#1-where-ai-product-cards-come-from)
- Aim for the top of the AI shortlist, since shoppers mostly accept it as given. *Measured* [why](#1-where-ai-product-cards-come-from)
- Apply to the merchant programmes of the assistants that serve your market. *Practitioner* [why](#1-where-ai-product-cards-come-from)
- Fill Merchant Center's return, support and policy attributes and align on-page markup with the feed before agent checkout reaches you. *Practitioner* [why](#2-checkout-on-google-and-agent-readiness)
- Build add-to-cart, variant pickers and checkout steps from native `<button>` and `<form>` elements with clear labels in the accessibility tree, because that is what an agent operates; structured data can't tell it which button to press. *Practitioner* [why](#2-checkout-on-google-and-agent-readiness)
- Keep the offer (total price incl. fees, delivery, returns) identical on your site, feeds and third-party listings, because agents may re-check it before buying. *Inference* [why](#2-checkout-on-google-and-agent-readiness)
- Check your branded prompts in ChatGPT weekly for competitors' ads. *Measured, early, mostly B2B* [why](#1-where-ai-product-cards-come-from)
- Treat organic Shopping clicks in EEA countries after mid-September 2026 as a structural break. *Measured* [why](#3-eea-free-product-listings-removed-september-2026)
- Name brand product lines the same way in titles, feeds and filters, and give each line a filterable, linkable facet. *Patent* [why](#4-how-google-reads-product-lines-and-product-pages)

## 1. Where AI product cards come from
- **ChatGPT.** Shopping cards come from OpenAI's own catalogue, fed by merchant feeds; Google still supplies best price, part of the product data and reviews. Cards are cached for weeks and identical for all users. *Measured.*[^chatgpt-retrieval] Since GPT-5.4 a shopping answer shows about 10 products instead of 1–2.[^chatgpt-53]
- ChatGPT's shopping quiz asked for budget first, then attributes, then use. *One session.*[^chatgpt-shopping]
- **Google.** AI Mode anchors products in the Shopping Graph.[^aio-aim] In Google's agent plans (UCP, AP2 protocols; US-first), the Merchant Center feed *is* the catalogue the agent reads, compares and checks out from. *From code.*[^intent-engine]
- **Eligibility over rank.** Feed errors in price, availability or promotions take a product out of the AI layer altogether. *Practitioner, unsourced to Google docs.*[^ucp]
- **Product grids sit above the blue links.** "96 % of SERPs show product grids above the blue links" (4K+ keywords, 40K grids); the gap between blue-link and grid winners is "enormous". *Measured; body paywalled.*[^gm-grids] For shopping queries, the feed decides visibility more than organic rank.
- **People accept the AI shortlist.** In 185 purchase tasks, 88 % took AI Mode's shortlist as given and 74 % picked the top product; products at rank 3 and below got about 10 %. Only 5 % built their own shortlist in AI Mode, against 56 % in classic search. Brand recognition was the trust cue in 34 % of AI Mode sessions. *Measured, usability study.*[^gm-highstakes][^gm-2027] Being first in the shortlist is what counts.
- **Google writes the product copy.** AI Mode free listings carry AI-generated "pros, cons" and "what to know" summaries; the AI Mode grid shows availability and the top seller's name.[^brodie-notes] Attribute completeness, not your marketing copy, decides what is said.
- **Ads now sit inside the grids** that used to be organic-only: AI Mode (two to four ads), the Shopping tab, and main search ("up to four").[^brodie-notes] If free-listing clicks fall, check whether paid units were added before blaming the feed.
- **ChatGPT takes paid product feeds too.** Product-feed ads uploaded to OpenAI's campaign manager carry star ratings; a five-ad unit is the default (Jul–Aug 2026).[^brodie-notes] Organic cards and ads now sit side by side.
- **ChatGPT ads spread fast.** In an early US tracking sample (~2 weeks, 97 workspaces, 3,697 ads, mostly B2B), ads appeared in 77 % of tracked responses, up from 7.1 % in the first pull; a brand's own ad showed on 7.3 % of its branded prompts; the advertiser was also mentioned in the answer 5.4 % of the time; 38 % of ads were on-topic. No CTR or CPC data yet. *Measured, early, agency data.*[^seer-chatgpt-ads] **Do:** check branded prompts weekly for competitors' ads.
- **ChatGPT's carousels mostly mirror Google Shopping.** Of 43,000+ ChatGPT carousel products across 10 verticals, 83 %+ appeared in Google's top 40 organic Shopping results (about 60 % in the top 10, nearly 84 % in the top 20); Bing accounted for 11 %. *Measured, relayed, author not named.*[^ignite-news] So Merchant Center quality and Google Shopping rank drive ChatGPT shopping visibility too — fix those before building a separate OpenAI feed.
- **Marketplaces are the AI shopping destinations.** Across ~87.6M AI visits in 10 markets (March 2026), amazon.com took 28.0 % of US AI ecommerce clicks and the top 10 domains 73.4 %; Amazon.it took 46.2 % in Italy; local champions led elsewhere (bol.com in the Netherlands, Mercado Livre in Brazil). *Measured, Similarweb, one month; search extracts.*[^aleyda-global] Treat each market's leading marketplace as a citation and corroboration channel ([third-party presence](../channels/third-party-presence.md)).
- **OpenAI's feed is a second catalogue path.** Its product feed spec puts inventory, regional pricing, reviews and Q&A in one record, supports updates every 15 minutes (Merchant Center's default is daily), and adds per-product flags `enable_search` and `enable_checkout`, plus product relationships and 3D model links. *Official spec, as summarised by iPullRank; "freshness decides eligibility" is its opinion.*[^ipr-openai-feed]
- **Adoption was low in 2025.** In one AI Mode shopping study, 33 % of participants were shown AI Mode and 2 % used it; it showed only 5 product cards, low on the page. *100 participants, one task.*[^ipr-aimode-study] Compare with the 2026 shortlist acceptance above: the surface matters once used, but usage was still small then.
- **Do:** apply to the merchant programmes of the assistants that serve your market (OpenAI's; Perplexity's was US/CA-only in 2026).[^ai-visible]

## 2. Checkout on Google and agent readiness
- **Buy-now on Google is spreading.** UCP checkout reached main search results (May 2026) and more merchants (Jun 2026); add-to-cart returned on free listings "where Merchant Center enables it" (Aug 2026).[^brodie-notes] Orders completed on Google never reach your analytics: reconcile them separately ([analytics](../measure/analytics.md)).
- **UCP runs on Merchant Center.** Merchants publish a JSON manifest at `/.well-known/ucp`; return policies and customer-support data must be in Merchant Center; markup that disagrees with the feed can block agent-made purchases. No attribution guidance exists yet. *Practitioner reading of Google's announcement; search extracts.*[^aleyda-ucp] **Do:** fill Merchant Center's return, support and policy attributes, align on-page markup with the feed, and check whether your shop platform supports the manifest.
- **Search Console's AI opt-out and Merchant Center.** Ignite claims the generative-AI "Exclude" setting keeps text and links out of AI results while "maintaining standard search results, ads, and Merchant Center appearances". *Unsourced; confirm in Google's docs before relying on it.*[^ignite-ai-mode]
- **Agent audits exist.** Lighthouse in Chrome Canary has an "Agentic Browsing" category (agent discoverability, WebMCP, llms.txt). Google's Search docs say llms.txt isn't needed for AI features in Search. *Official tool, early.*[^mh-lighthouse]
- **Do:** label buttons, variant pickers and add-to-cart properly in the accessibility tree — that is what an agent operates. Run the Lighthouse agent audit on product and cart templates. *Practitioner.*[^mh-lighthouse]
- **Native controls, not schema.** Structured data can't tell an agent which button adds a product to the cart; use native `<button>` and `<form>` elements with clear labels rather than clickable `<div>`s. *Practitioner.*[^gn-html]
- **Agents check standing conditions.** An agent may hold a standing instruction ("buy when under X with free returns") and re-check offers repeatedly; whether a shop is eligible then hinges on offer accuracy across sources — total price including fees, policies, third-party listings. Repeated agent re-checks are not new demand. *Inference, argument without data.*[^ja-condition] **Do:** keep price, fees, delivery and return terms identical on the site, in feeds and on marketplaces, and exclude agent re-checks from demand counts ([analytics](../measure/analytics.md)).
- Local-inventory results in Shopping: see [local](../channels/local.md).

## 3. EEA: free product listings removed (September 2026)
- **What changed.** Google redesigned its results page in the EEA; free product listings and "Popular products" units disappeared around 15–18 Sep 2026. A "comparison sites" unit lists aggregators, with Google as one row — two clicks from search to the shop instead of one. Trade press links it to the Digital Markets Act (Commission decision 23 July, 60-day window). Paid Shopping ads, CSS and feeds are unchanged. *Several outside sources, no primary source.*[^eea][^eea-press]
- **Example.** In Search Console's "Merchant listings" appearance, a German shop lost 67 % of clicks and 88 % of impressions in Germany from the week of 14 Sep 2026, while Switzerland (outside the EEA) held. "Product snippets" on normal results did not fall.[^field-notes]
- **Do:**
  - Treat organic Shopping clicks in EEA countries after mid-September 2026 as a structural break ([Search Console](../measure/search-console.md), [traffic drop](../situations/traffic-drop.md)).
  - Read Merchant Center's own free-listing clicks for the same weeks.
  - Check whether comparison sites in the new unit list your products, and what a CSS listing would cost.
  - Paid Shopping / Performance Max now cover the product grid alone in the EEA; account for it in budget plans.

## 4. How Google reads product lines and product pages
- **Product lines.** A Google product-search patent detects brand product lines from the pattern [brand][line][attribute] and adds them to the category's attribute dictionaries. *Patent (US 10,394,816, filed 2012; status not verified).*[^sbs-productlines] **Do:** name each line consistently in titles, feeds and filter labels, and give it a filterable, linkable facet ([feeds and Merchant Center](../channels/feeds-and-merchant-center.md), [category pages](../page-types/category-pages.md)).
- **Chrome's shopping classifier is not a ranking input.** The extracted model takes `float32[1,1536]`: a 768-dimension embedding of title + URL plus the 768-dimension mean of passage embeddings. Content comes from AnnotatedPageContent 5 seconds after load: at most 10 passages of up to 100 words, each truncated to 64 tokens, with items under 5 words merged — an effective view of ~400–450 words. It feeds History Journeys and a "shopping user" segment, not rankings. *From code (extracted TFLite models).*[^dj-shopclf] It matches the 10 × ~100-word reading described in [AI assistants](ai-assistants.md#1-the-opening-of-the-page-carries-it). **Do:** use descriptive, product-specific titles and URLs, and put product text above boilerplate ([product pages](../page-types/product-pages.md)).
- **AI Mode layout tags.** Leaked prompt content suggests `<ShoppingOffers>` is used only for "single, concrete product iterations" (SkuLevelProduct, GTIN), and `<Carousel>` or `<ImageGrid>` need at least 3 validated children of one entity type. *Inference — hypothesis from unverified prompt-leak content.*[^dj-tags] If true, exact GTINs and SKU-level product data decide whether an offer unit can show at all.

Related: [feeds and Merchant Center](../channels/feeds-and-merchant-center.md), [AI assistants](ai-assistants.md), [Google AI features](google-ai-features.md), [product pages](../page-types/product-pages.md), [Google updates timeline](../reference/google-updates-timeline.md).

[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: shopping catalogue, Google data inputs, card caching.
[^chatgpt-53]: Resoneo, ChatGPT 5.3/5.4: ~10 products per shopping answer in 5.4.
[^chatgpt-shopping]: Resoneo, ChatGPT Shopping capture, 2025-11-26: quiz order. One session.
[^aio-aim]: Resoneo, AIO / AI Mode deep dive, Feb 2026: Shopping Graph anchoring.
[^intent-engine]: Resoneo, "What Google is building", Jun 2026: UCP/AP2, Merchant Center as agent catalogue.
[^ucp]: Searchind, agentic commerce, read 2026-10-27: eligibility over rank, constraint-based copy. No Google sources cited.
[^eea]: Searchind, EEA changes, read 2026-10-27: redesign, comparison-sites unit, paid Shopping unchanged.
[^eea-press]: Trade press, read 2026-10-27: removal ~15–18 Sep, Commission decision 23 Jul, 21 Sep deadline; sources disagree on some dates.
[^ai-visible]: Searchind, AI visibility, read 2026-10-27: OpenAI and Perplexity merchant programmes.
[^ignite-news]: Ignite Visibility weekly recap, week of 2026-03-01: ChatGPT carousel study (via Search Engine Land); primary study not checked.
[^ignite-ai-mode]: Ignite Visibility, 2026-09-30: claim about the Search Console opt-out, no source cited.
[^aleyda-ucp]: Aleyda Solis, ~2026-10-10, via search extracts (direct fetch blocked); date unconfirmed.
[^aleyda-global]: Aleyda Solis, Mar–Apr 2026, via search extracts: Similarweb, 10 markets, 39.3M of the AI visits ecommerce.
[^ipr-openai-feed]: iPullRank, 2025-10-20: OpenAI feed spec fields (enable_search, enable_checkout, relationships, q_and_a, model_3d_link), 15-minute updates.
[^ipr-aimode-study]: iPullRank (Monahan), 2025-09-17: 33 % shown, 2 % used; 5 product cards.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^gm-grids]: Growth Memo, 2026-03-09: sample and headline figure only; method paywalled.
[^gm-highstakes]: Growth Memo, 2026-04-07 (cut off after the 74 % figure) and 2026-10-12 (restates the rest).
[^gm-2027]: Growth Memo, 2026-10-12: shortlist figures restated; feed and PDP advice is opinion.
[^mh-lighthouse]: Marie Haynes, 2026-05-29: Lighthouse Agentic Browsing category; accessibility-tree advice is her opinion.
[^field-notes]: Anonymised shop: feed export of 2026-10-27; Search Console by search appearance and country, 17 Aug – 13 Sep vs 28 Sep – 25 Oct 2026.
[^sbs-productlines]: SEO by the Sea, 2020-01-27: patent US 10,394,816, filed 2012-12-27; product-line detection and category attribute dictionaries. Blog inactive since 2022.
[^dj-shopclf]: DEJAN, 2026-04-03: extracted Chrome TFLite models; input shape, AnnotatedPageContent timing and passage limits; uses (History Journeys, shopping-user segment).
[^dj-tags]: DEJAN, 2026-09-20: AI Mode layout tags from prompt-leak content; unverified.
[^seer-chatgpt-ads]: Seer Interactive, 2026-07-15 (updated 2026-07-28): ~2 weeks, 97 tracking workspaces, 3,697 ads, US, mostly B2B; 7.1 % → 77 % of responses with ads; own ad on 7.3 % of branded prompts; advertiser mentioned 5.4 %; 38 % on-topic; no CTR/CPC.
[^ja-condition]: Jono Alderson, 2026-09-27: argument that agents act on standing conditions and re-check; eligibility depends on offer accuracy across sources. No data.
[^gn-html]: Barry Adams, 2025-08-06: practitioner advice on semantic HTML; structured data can't identify the add-to-cart control, native buttons and forms can.
