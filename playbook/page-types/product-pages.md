---
type: Playbook
title: Product pages
description: What to do on a product page — factual opening sentence, price, specs and stock as server-rendered text in one main container (never in CSS pseudo-content), model codes as visible text, descriptive titles and URLs, variant URLs and markup, the same facts as the feed, "will it fit?" and use-case copy tested with task-style prompts, reviews and Q&A, own images for Lens and indexing, the page as ad landing page, "confirm and go" for AI visitors, and out-of-stock and discontinued products.
tags: [seo, geo, product-pages, ecommerce, structured-data, variants, feeds, lens, google-ads, out-of-stock, soft-404, html-extraction, reviews, indexing, rendering, css]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026; 1,249 answers, 88k results, server logs of 325k URLs)"
  - id: gemini-convo
    resource: "https://think.resoneo.com/gemini-convo/"
    title: "Resoneo, How Gemini searches and cites (Oct 2026; 76,450 conversations, 222,753 searches)"
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10)"
  - id: llm-crawler
    resource: "https://think.resoneo.com/sentinel/geo-llm-crawler-report.html"
    title: "Resoneo, LLM crawler test (Jan 2026; one test page, 8 assistants)"
  - id: gm-agents
    resource: "https://www.growth-memo.com/p/where-ai-agents-get-stuck-on-your"
    title: "Growth Memo, Where AI agents get stuck on your site (2026-07-13; 100 B2B products × 3 tasks × 5 runs)"
  - id: g-variants
    resource: "https://developers.google.com/search/docs/appearance/structured-data/product-variants"
    title: "Google Search Central, Product variant structured data (updated 2026-09-08)"
  - id: g-sd-policies
    resource: "https://developers.google.com/search/docs/appearance/structured-data/sd-policies"
    title: "Google Search Central, General structured data guidelines (updated 2026-07-10)"
  - id: leak-2
    resource: "https://www.resoneo.com/google-leak-part-2-understanding-the-twiddler-framework/"
    title: "Resoneo, Google leak part 2: twiddlers (Oct 2024)"
  - id: gm-intents
    resource: "https://www.growth-memo.com/p/traditional-intents-can-no-longer"
    title: "Growth Memo, Traditional intents can no longer… (2026-06-01; ~846,000 US sessions; recommendations partly paywalled)"
  - id: aleyda-ucp
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/ugc-agentic-commerce-seo/"
    title: "Aleyda Solis, UCP and agentic commerce (~2026-10-10; search extracts)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: gmc-audit
    resource: "https://searchind.com/the-google-merchant-center-audit-i-run-for-every-client/"
    title: "Searchind, The Google Merchant Center Audit I run for every client (Aug 2026, updated Oct 2026)"
  - id: ucp
    resource: "https://searchind.com/ucp-agentic-ecommerce-seo/"
    title: "Searchind, Google's shift to Agentic Commerce (May 2026)"
  - id: ipr-agentic-ecom
    resource: "https://ipullrank.com/agentic-ecommerce-strategy"
    title: "iPullRank (Angela Clark), Agentic ecommerce strategy (2025-12-04; cites a Bain survey)"
  - id: gm-2027
    resource: "https://www.growth-memo.com/p/organic-growth-in-e-commerce-in-2027"
    title: "Growth Memo, Organic growth in e-commerce in 2027 (2026-10-12)"
  - id: mh-june2025
    resource: "https://www.mariehaynes.com/analyzing-pages-that-improved-following-the-june-2025-core-update/"
    title: "Marie Haynes, Pages that improved after the June 2025 core update (2025-07-18; 5 cases)"
  - id: lens
    resource: "https://think.resoneo.com/google-lens/"
    title: "Resoneo, How Google Lens works (Feb 2026)"
  - id: lens-shopping
    resource: "https://think.resoneo.com/google-lens/shopping/"
    title: "Resoneo, Google Lens shopping categories (Oct 2026)"
  - id: google-ads
    resource: "https://think.resoneo.com/google-ads/"
    title: "Resoneo, Google Ads deep dive (Sep 2026; decompiled app, trial exhibits)"
  - id: siege-bofu
    resource: "https://www.siegemedia.com/research/ai-buying-advice"
    title: "Siege Media, AI buying advice (2026-03-24; ~1,000 bottom-funnel prompts)"
  - id: aleyda-ecom
    resource: "https://www.aleydasolis.com/en/ai-search/ecommerce-ai-search-citations-optimization/"
    title: "Aleyda Solis, Ecommerce AI search citations (May 2026; 25 US ecommerce sites, 5 subverticals; search extracts)"
  - id: gm-consensus
    resource: "https://www.growth-memo.com/p/the-consensus-gap"
    title: "Growth Memo, The consensus gap (2026-05-11; 3.7M citations, 20,000-prompt sample, Omnia data)"
  - id: ipr-aimode-referrals
    resource: "https://ipullrank.com/early-referral-data-ai-mode"
    title: "iPullRank (Garrett Sussman), Early referral data from AI Mode (2025-09-26; SimilarWeb panel, 100K+ users)"
  - id: mh-lighthouse
    resource: "https://www.mariehaynes.com/lighthouse-report-for-agents/"
    title: "Marie Haynes, Lighthouse report for agents (2026-05-29)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: bp-schema-test
    resource: "https://botpresso.com/ai-assistants-schema-markup-test/"
    title: "Botpresso, Do AI assistants read schema? (≈2026-10; 4 assistants × 3 test pages = 12 responses)"
  - id: bp-soft404
    resource: "https://botpresso.com/what-is-a-soft-404-issue-how-to-fix-it/"
    title: "Botpresso, Soft 404 issues and fixes (≈2026-07)"
  - id: g-product-snippet
    resource: "https://developers.google.com/search/docs/appearance/structured-data/product-snippet"
    title: "Google Search Central, Product snippet structured data (updated 2026-09-08)"
  - id: nz-extract
    resource: "https://natzir.com/en/seo/llm-html-content-extraction/"
    title: "Natzir Turrado, HTML content extraction in LLMs with search tools (2025-11-06; 16 HTML variants of one product, mainly Claude)"
  - id: nz-hybrid
    resource: "https://natzir.com/en/seo/hybrid-search-ai-search/"
    title: "Natzir Turrado, Hybrid search and AI search (2025-08-29; review)"
  - id: sbs-reviews
    resource: "https://www.seobythesea.com/2011/05/how-google-might-choose-high-quality-reviews-to-display-for-products-and-businesses/"
    title: "SEO by the Sea, How Google might choose reviews to display (2011-05-26; application US 2011/0125736)"
  - id: dj-shopclf
    resource: "https://dejan.ai/blog/google-shopping-classifier/"
    title: "DEJAN, Chrome's shopping classifier (2026-04-03; extracted TFLite models)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: ja-cloak
    resource: "https://www.jonoalderson.com/conjecture/cloaking-is-dead-long-live-cloaking/"
    title: "Jono Alderson, Cloaking is dead, long live cloaking (2026-10-26; argument + relayed Mueller 2017, Dave Smart 2026-07 test)"
  - id: seer-ai-interview
    resource: "https://www.seerinteractive.com/insights/ai-doesnt-just-answer-questions-it-rewrites-which-brands-you-even-consider"
    title: "Seer Interactive, Can a prompt undo years of brand building? (2026-07-01; 28 participants × 3 tasks = 84 sessions)"
---

# Product pages

For anyone writing, templating or auditing a single product page (PDP) that has to rank in Google, feed shopping surfaces and survive an AI assistant's quick read.

## Rules
- **Open with one factual sentence** after the H1 — what it is, key attributes, sizes, price from, availability or delivery time. *Measured* for assistants; Google says no special writing is needed ([§1](#1-the-facts-up-top-as-text)).
- **Put price, specs and availability in the server-rendered HTML**, not only in JSON-LD or script — in one main container with the name and description, never in an aside or footer, with MPN and model codes as visible text — never as CSS `::before`/`::after` content. *Measured / one test; one product, mostly Claude*; CSS *Practitioner, relayed* ([§1](#1-the-facts-up-top-as-text), [§8](#8-markup-structure-machines-can-read), [§10](#10-what-css-and-responsive-images-hide)).
- **Give every variant its own preselecting URL** and pick one model: one canonical for the product group, or full self-contained markup per variant page. *Official* ([§2](#2-variants-and-markup)).
- **Mark up only what is visible, and keep markup in sync with the visible text**; treat Product markup as a Google feature, not an assistant lever. *Official*; assistants *Measured, n=12* ([§2](#2-variants-and-markup)).
- **State the same facts as the feed** — price, availability, variants, return and support policies. *Practitioner* ([§3](#3-the-same-facts-as-the-feed)).
- **Say what the product is best for, its limits, what it is not for and its exact dimensions, and test the copy with task-style prompts that name no brand.** *Practitioner*; shopper panel *Measured, 84 sessions* ([§4](#4-answer-will-it-fit)).
- **Add reviews, Q&A and a use or assembly video, and answer the real buyer questions**; ask reviewers for specific detail (use, fit, shipping). *Practitioner*; review selection *Patent* ([§4](#4-answer-will-it-fit)).
- **Use your own images — one dominant, centred product per image, the same image as in the feed, never a placeholder — and every `<picture>` source showing the same product.** *From code* for Lens; indexing *Practitioner, correlation, relayed*; the rule is practitioner ([§5](#5-images-and-ads), [§9](#9-what-gets-a-crawled-page-indexed), [§10](#10-what-css-and-responsive-images-hide)).
- **Treat the page as ad creative**: check ad copy when the page changes, and keep the query string on every redirect. *From code* ([§5](#5-images-and-ads)).
- **Let AI visitors confirm and go**: the cited fact and its proof above the fold. *Measured, panel data* ([§6](#6-what-a-product-page-earns)).
- **Keep temporarily out-of-stock products indexable** with the right availability value and alternatives on the page; 410 or 301 discontinued ones. *Official definitions; the rule is inference* ([§7](#7-out-of-stock-and-discontinued)).

## Checklist
- [ ] First sentence after the H1 states what, key attributes, price from and availability.
- [ ] A plain fetch with an assistant's user agent shows price, specs and stock in the HTML ([test](../measure/diagnostic-tests.md#4-fetch-a-page-the-way-an-ai-assistant-does)).
- [ ] Each variant opens preselected (image, price, availability, add-to-cart) at its own URL; canonical model matches the markup.
- [ ] Markup values match the visible text and the feed; no markup for hidden content; markup changes ship with every price or stock change.
- [ ] Copy has "best for", limits, "not suitable for" and exact dimensions; top return reason answered.
- [ ] Reviews, Q&A and a use or assembly video are on the page.
- [ ] Main image: one product, centred; same file as the feed.
- [ ] Ad and feed landing URLs answer 200 and keep gclid and UTM through any redirect.
- [ ] Buttons, variant picker and add-to-cart are labelled in the accessibility tree.
- [ ] Out-of-stock pages show the availability value and alternatives; discontinued products return 410 or 301 to a successor; Soft 404 count per page type watched.
- [ ] Title follows the product title template ([titles and snippets](../technical/titles-and-snippets.md)); title and URL name the specific product, not only the brand or a code.
- [ ] Name, price and description sit in one main container at the same nesting level; nothing essential in `<aside>` or the footer.
- [ ] MPN, model number or article code appears as visible text.
- [ ] Product text comes before shared boilerplate (shipping, trust blocks) in the HTML.
- [ ] Review requests ask for specifics: what it was used for, fit, delivery.
- [ ] Copy names the use cases and who the product is not for; a few task-style prompts ("I need something to…") checked in assistants.
- [ ] Main images are the product's own photos, not placeholders; `<picture>` sources for every breakpoint show the same product.
- [ ] No price, stock, label or other fact in CSS `::before`/`::after` content; no height-based media query changes the content.

## 1. The facts up top, as text
- ChatGPT judges each candidate by title, URL and a **~202-character snippet starting at the H1**; Gemini takes 80 % of cited passages from the first half of the page.[^chatgpt-retrieval][^gemini-convo] Pattern and before/after: [AI assistants](../how-it-works/ai-assistants.md).
- Most assistant fetchers read static HTML only, and JSON-LD is stripped on live reads.[^llm-crawler][^chatgpt-retrieval] With no price disclosed, 45 % of agent runs cited a third party instead.[^gm-agents] What you don't state, someone else states for you.
- **Titles.** Use a template such as "Product | Category" for the long tail and hand-write titles for the top-traffic products: [titles and snippets](../technical/titles-and-snippets.md).

> **Conflict:** Google says you "don't need to write in a specific way just for generative AI search";[^google-ai-guide] the assistant findings above say the opening carries the page — [details](../reference/conflicts.md#googles-guidance-vs-assistant-findings)

## 2. Variants and markup
- Google requires that each variant can be preselected "directly with a distinct URL"; one page for all variants means "only one distinct canonical URL for the overall ProductGroup", one page per variant means "full and self-contained markup".[^g-variants] Details: [technical foundations](../technical/technical-foundations.md#4-product-variants).
- Near-identical variant URLs compete for a host's limited result slots instead of adding slots. *From the leak.*[^leak-2]
- Markup "must be a true representation of the page content".[^g-sd-policies] Product markup supports Google's own results features (*opinion, no test shown*)[^gm-intents] but isn't read by assistants on live fetches ([policies](../technical/technical-foundations.md#8-structured-data-policies)).
- **Assistants answered nothing from schema alone.** ChatGPT, Perplexity, Claude and Gemini were asked about 3 test pages whose facts sat only in schema (schema facts differing from the visible text; schema with an empty body; JSON-LD and Microdata with no visible content): 0 of 12 responses returned a schema-only fact — 10 said there was no answer, 2 answered from the open web. *Measured, n=12, directional.*[^bp-schema-test] The same post relays a test in which 0 of 280 fetched pages kept their JSON-LD, and Gemini preferred a stale FAQPage answer over the visible text in 8 of 20 trials. *Relayed.*[^bp-schema-test]
- **Do:** state price, stock and specs as visible text in the initial HTML, and update the markup whenever the visible facts change — stale schema can hurt. Adding schema did not raise AI citations in a controlled test ([third-party presence](../channels/third-party-presence.md#2-most-citations-are-third-party)).

## 3. The same facts as the feed
- Markup that disagrees with the feed can block agent-made purchases; return and support data belong in Merchant Center. *Practitioner reading of Google's announcement.*[^aleyda-ucp]
- Google now writes AI "pros, cons" and "what to know" summaries for free listings, and free-listing clicks land on the feed `link`.[^brodie-notes] Attributes decide what is said; the feed link is a landing URL.
- Test title changes in the feed only, never in the shop backend, where a rename can change the slug.[^gmc-audit] More in [feeds and Merchant Center](../channels/feeds-and-merchant-center.md).

## 4. Answer "will it fit?"
- Write what a product is best for, its limits, what it is *not* for and exact dimensions — in the feed description and the page opening.[^ucp] Check return reasons first: a recurring reason is the "not suitable for" line. *Practitioner.*
- Agents lean on reviews and Q&A: ask for reviews 7–14 days after delivery with product-specific prompts, add Q&A and assembly or use videos. *Practitioner, anecdotal tests.*[^ipr-agentic-ecom]
- Answer 8–10 real buyer questions per page (*opinion*);[^gm-2027] pages that rose in a core update answered the follow-ups and showed first-hand testing and original photos (5 cases).[^mh-june2025]
- Product pages without original content were among those dropped from the index from 27 May 2025. *Case observations.*[^mh-deindex]
- **Prompt for detailed reviews.** A Google application describes choosing which reviews to display by clustering them (topic, star band) and then scoring quality: grammar, length, no all-caps or profanity, specific vocabulary for the review type. *Patent (application, status not verified).*[^sbs-reviews] **Do:** ask reviewers about use, fit and delivery rather than for a star rating alone.
- **Write for the task, not the brand.** In a shopper panel (28 participants × 3 tasks = 84 sessions), only 9.5 % of first prompts named a brand, and AI reshaped which brands shoppers considered — one brand's mentions fell from 18 to 8, another's rose from 3 to 9. *Measured, small panel, no significance test.*[^seer-ai-interview] **Do:** write product copy around use cases and who the product is not for, and test a few task-style prompts ("I need a … for …") per category to see whether your products come up ([AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 5. Images and ads
- Lens recompresses images, caps them at 1,600 px, and shows a shopping chip for furniture-type products but no longer for most stationery. *From code.*[^lens][^lens-shopping]
- Google Ads builds an LLM summary of each landing page and checks generated assets for faithfulness against it. *From code.*[^google-ads] When an ad's final URL changes, check its copy describes the new page.
- **Example.** Old URLs redirected without the query string, so ad clicks lost gclid and UTM and campaigns were undercounted for months.[^field-notes] Check weekly with a test gclid ([analytics](../measure/analytics.md)).

## 6. What a product page earns
- Product pages are cited at single-digit rates for bottom-funnel prompts,[^siege-bofu] and only 1.2 % of cited product URLs appear in all three of ChatGPT, Perplexity and AI Overviews.[^gm-consensus] But shoppers click product and category pages after guides resolve their doubt.[^aleyda-ecom] Measure them by clicks and conversions, not citations.
- AI Mode visitors stay 2.5–4 min (vs ~5) and see ~3–4 pages (vs ~6).[^ipr-aimode-referrals] They come to confirm: price, spec and stock above the fold.
- Label buttons, variant pickers and add-to-cart in the accessibility tree — that is what an agent operates. *Practitioner.*[^mh-lighthouse]

## 7. Out of stock and discontinued
- **Stockouts drift into Soft 404.** Out-of-stock product pages get flagged Soft 404 even when they show related products. The same practitioner source recommends 410 for discontinued products and a conditional noindex for temporary stockouts. *Practitioner, vendor.*[^bp-soft404]
- **Google's default.** Google's product markup defines availability values such as `OutOfStock`, `BackOrder` and `Discontinued`, but gives no rule on indexing.[^g-product-snippet] Keep temporarily out-of-stock products indexable with the right availability value and useful alternatives on the page, so they keep their rankings. *Official definitions; the rule is inference.*
- **Do:** 410 a permanently discontinued product, or 301 it to a close successor; consider a noindex only for long stockouts; write the rules down and watch the Soft 404 count per page type ([scaling content and templates](../situations/scaling-content-and-templates.md#6-soft-404s-on-inventory)).

> **Conflict:** noindex temporarily out-of-stock pages vs keep them indexed — [details](../reference/conflicts.md#out-of-stock-pages-noindex-or-keep-indexed)

## 8. Markup structure machines can read
- **One container for the core facts.** In a test of 16 HTML variants of one product page (mostly with Claude), the fetch failed to return the facts when the price sat outside the main container, at a different nesting depth or in the footer, or when the description sat in an `<aside>`; Microdata didn't rescue it; the H1 was read as the product name. *Measured, one product, mostly one assistant.*[^nz-extract] **Do:** keep name, price and description in one main container at the same nesting level. Background: [AI assistants](../how-it-works/ai-assistants.md).
- **Model codes as text.** Hybrid retrieval pairs dense vectors with lexical matching, and the lexical side is what catches exact IDs, model numbers and codes that embeddings treat as noise. *Review of published systems.*[^nz-hybrid] **Do:** show MPN, model number and article code as visible text, not only in the feed or markup.
- **Descriptive titles and URLs; product text first.** Chrome's on-device shopping classifier embeds the title plus URL and the mean of up to 10 passages of ≤ 100 words (truncated to 64 tokens), an effective view of ~400–450 words; it feeds Chrome features, not rankings. *From code.*[^dj-shopclf] **Do:** product-specific titles and URLs, and the product's own text above shared boilerplate. *Inference for search.* How much of a page each engine reads: [conflicts](../reference/conflicts.md#how-much-of-a-page-do-ai-engines-read).

## 9. What gets a crawled page indexed
- Among product pages stuck in "Crawled – currently not indexed", those with unique product images (not placeholders) and in stock were more likely to be indexed. *Practitioner talk (Tyler Gargula), correlation, sample not given; relayed by a conference recap.*[^lr-techseo]
- **Do:** replace placeholder images with the product's own photos before a page goes live, and when a product template has many crawled-not-indexed URLs, check image uniqueness and stock first. Index status by page type: [test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type); stock rules: [§7](#7-out-of-stock-and-discontinued).

## 10. What CSS and responsive images hide
- **CSS content isn't indexed.** Text in CSS `::before`/`::after` isn't in the DOM and isn't indexed; bots don't scroll or click, and Google expands the viewport height once to trigger lazy loading — so lazy-load with Intersection Observer, use `visibility:hidden` rather than `display:none` for content that must keep its dimensions, and cap `vh`-based hero images with `max-height`. *Practitioner talk (Giacomo Zecchini), relayed.*[^lr-techseo]
- **Unintended differences between what people and Google see.** Google renders mobile pages with a very tall viewport (an old Mueller remark from 2017 suggested ~9,000 px, unconfirmed; a newer 2026 observation saw a ~1,750 px screenshot cut-off and no scrolling), so `@media (min-height: …)` rules, `<picture>` sources with different subjects and CSS-generated text can show Google something other than what visitors see. Google judges cloaking by intent. *Practitioner, with Google docs and relayed statements.*[^ja-cloak]
- **Do:** never put prices, stock, labels or badges with facts in CSS pseudo-content; let every `<picture>` source show the same product; no height-based media queries that change content. Compare raw and rendered output: [diagnostic tests](../measure/diagnostic-tests.md), [technical foundations](../technical/technical-foundations.md).

Related: [category pages](category-pages.md), [comparison pages and guides](comparison-and-guides.md), [shopping surfaces](../how-it-works/shopping-surfaces.md), [satisfaction per page type](../measure/diagnostic-tests.md#2-satisfaction-per-page-type), [titles and snippets](../technical/titles-and-snippets.md).

[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: funnel 58k retrieved → 7.6k shown → 5k cited → 760 opened; ~202-character snippet from the H1; JSON-LD stripped; bot roles and cache; utm on ~95 % of displayed links; instant vs thinking search counts.
[^gemini-convo]: Resoneo, Gemini conversations, read 2026-10-27: cited-passage positions and lengths; 55 % English queries for non-English questions.
[^google-ai-guide]: Google generative-AI optimization guide, updated 2026-07-10: no special writing, no chunking requirement, no AI text files or Markdown, llms.txt ignored.
[^llm-crawler]: Resoneo, LLM crawler report, Jan 2026: which assistants run JavaScript; Perplexity-User failure; AI Mode from index; JSON-LD not extracted. One test page.
[^gm-agents]: Growth Memo, 2026-07-13: 79 % own-site pricing answers; 45 % third-party when undisclosed; fetch errors 17 → 77 %.
[^g-variants]: Google, product variant structured data, read 2026-10-27 (Merchant Center `item_group_id` not covered on that page).
[^g-sd-policies]: Google, general structured data guidelines, read 2026-10-27.
[^leak-2]: Resoneo, leak part 2, 2024-10-31: OfficialPageTwiddler, host diversity caps.
[^gm-intents]: Growth Memo, 2026-06-01: share still active at 21 s by intent with and without AIO; schema recommendations are opinion, no test shown.
[^aleyda-ucp]: Aleyda Solis, ~2026-10-10, via search extracts (direct fetch blocked); date unconfirmed.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^gmc-audit]: Searchind, Merchant Center audit, read 2026-10-27: title test design, feed-only changes, material most missing, specific categories, auto-created data sources, disapproval CSV, warehouse transfer.
[^ucp]: Searchind, agentic commerce, read 2026-10-27: eligibility over rank, constraint-based copy. No Google sources cited.
[^ipr-agentic-ecom]: iPullRank (Clark), 2025-12-04: review timing and prompts, Q&A, video; Bain survey figures.
[^gm-2027]: Growth Memo, 2026-10-12: answer 8–10 buyer questions per page (opinion).
[^mh-june2025]: Marie Haynes, 2025-07-18: shared traits of 5 pages that improved.
[^lens]: Resoneo, How Google Lens works, Feb 2026: JPEG recompression, 1,600 px cap.
[^lens-shopping]: Resoneo, Lens shopping categories, Oct 2026: allow / neutral / deny lists; stationery to neutral in 2026.
[^google-ads]: Resoneo, Google Ads deep dive, Sep 2026: LLM_LP_SUMMARY, LP_ASSET_FAITHFULNESS, productFidelityScore, pLQ vs pCTR; AdsBot and robots.txt.
[^siege-bofu]: Siege Media, 2026-03-24: ~1,000 BOFU prompts, 57,095 citations (Peec AI).
[^aleyda-ecom]: Aleyda Solis, May 2026, via search extracts: Semrush Enterprise AIO + Similarweb, 25 US sites; directional.
[^gm-consensus]: Growth Memo, 2026-05-11: 91.07 % single-engine, 2.37 % all three; 1.2 % product, 1.6 % category; author calls it directional.
[^ipr-aimode-referrals]: iPullRank (Sussman), 2025-09-26: SimilarWeb panel 20 May – 19 Aug 2025; time on site and pages per visit after AI Mode vs classic search.
[^mh-lighthouse]: Marie Haynes, 2026-05-29: Lighthouse Agentic Browsing category; accessibility-tree advice is her opinion.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^bp-schema-test]: Botpresso, ≈2026-10 (no publish date shown): ChatGPT, Perplexity, Claude and Gemini × 3 test pages = 12 responses, 0 schema-only facts returned; relays Ramos (0 of 280 fetched pages kept JSON-LD; Gemini chose a stale FAQPage answer in 8 of 20 trials), not checked at source. Agency promoting its own tools.
[^bp-soft404]: Botpresso, soft 404 guide, ≈2026-07 (no publish date shown): practitioner advice from an agency promoting its own tools; the noindex recommendations partly contradict the common reading of Google's ecommerce guidance.
[^nz-extract]: Natzir Turrado, 2025-11-06: 16 HTML variants of one product page, tested mainly with Claude's search tools; failures when price or description left the main container; Microdata no help; H1 read as name.
[^nz-hybrid]: Natzir Turrado, 2025-08-29: review of hybrid (lexical + dense) retrieval; exact IDs and codes caught lexically; diversification penalises redundant passages.
[^sbs-reviews]: SEO by the Sea, 2011-05-26: application US 2011/0125736 on selecting reviews to display (clustering, then quality scoring); grant status not verified.
[^dj-shopclf]: DEJAN, 2026-04-03: extracted Chrome TFLite models; input = 768-d title+URL embedding plus 768-d mean of passage embeddings; ≤ 10 passages of ≤ 100 words, 64 tokens each; content read 5 s after load; feeds History Journeys and a shopping-user segment, not rankings.
[^g-product-snippet]: Google product snippet structured data, read 2026-10-28: availability values; no guidance on indexing out-of-stock or discontinued products.
[^lr-techseo]: Lily Ray, Tech SEO Connect 2025 recap, 2025-12-05: Tyler Gargula on crawled-not-indexed pages (unique images, in stock; correlation, sample not given); Giacomo Zecchini on viewport expansion, lazy loading, CSS pseudo-content, `visibility:hidden` vs `display:none`, `vh` heroes. Her summaries of the speakers' talks.
[^ja-cloak]: Jono Alderson, 2026-10-26: argument with Google docs; relays Mueller (2017, ~9,000 px viewport, old and unconfirmed) and a 2026 observation of a ~1,750 px screenshot cut-off; height media queries, `<picture>` subjects, CSS content; cloaking judged by intent.
[^seer-ai-interview]: Seer Interactive, 2026-07-01: 28 participants × 3 tasks = 84 sessions; 9.5 % of first prompts named a brand; brand mentions 18 → 8 and 3 → 9; no statistical test.
