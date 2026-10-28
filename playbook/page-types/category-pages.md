---
type: Playbook
title: Category pages
description: What to do on a category or listing page — factual opening sentence, the searcher's exact terms in title and H1, one idea per passage, filter pages only with demand, crawlable pagination, internal links and section quality, the buyer's main uncertainty, consolidation, satisfaction per page type, listings near zero stock, body copy and a real meta description, customer vocabulary, URLs that mirror the taxonomy, links to complementary categories, footer category links and cross-sell blocks in `<aside>`, and feed-generated category templates audited before spam updates.
tags: [seo, geo, category-pages, ecommerce, faceted-navigation, pagination, internal-links, consolidation, secondary-keywords, soft-404, meta-description, taxonomy, gemini, spam-update, programmatic, semantic-html]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026; 1,249 answers, 88k results, server logs of 325k URLs)"
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10)"
  - id: qus
    resource: "https://www.resoneo.com/qus-query-expansion-google-and-mysterious-scoring/"
    title: "Resoneo, QUS query expansion and term scoring (Jul 2025; few US examples)"
  - id: mh-vector
    resource: "https://www.mariehaynes.com/could-optimizing-for-vector-search-do-more-harm-than-good/"
    title: "Marie Haynes, Could optimizing for vector search do more harm than good (2025-06-26)"
  - id: ipr-chunking
    resource: "https://ipullrank.com/misinformation-about-chunking"
    title: "iPullRank, Misinformation about chunking (2026-01-15)"
  - id: g-facets
    resource: "https://developers.google.com/search/docs/crawling-indexing/crawling-managing-faceted-navigation"
    title: "Google Search Central, Managing crawling of faceted navigation URLs (updated 2025-12-18)"
  - id: not-enough
    resource: "https://searchind.com/ecommerce-seo-for-google-is-not-enough/"
    title: "Searchind, eCommerce SEO for Google Is Not Enough (Oct 2025)"
  - id: organic-analysis
    resource: "https://searchind.com/organic-seo-analysis-for-ecommerce/"
    title: "Searchind, The complete guide for Search/SEO analysis for eCommerce (Jun 2025, updated Apr 2026)"
  - id: decisions-api
    resource: "https://think.resoneo.com/chrome-decisions-api/"
    title: "Resoneo, Chrome Decisions API test (Oct 2026; Canary only)"
  - id: g-pagination
    resource: "https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading"
    title: "Google Search Central, Pagination and incremental page loading (updated 2025-12-10)"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6: how Google Search works (Oct 2024)"
  - id: leak-2
    resource: "https://www.resoneo.com/google-leak-part-2-understanding-the-twiddler-framework/"
    title: "Resoneo, Google leak part 2: twiddlers (Oct 2024)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: aleyda-ecom
    resource: "https://www.aleydasolis.com/en/ai-search/ecommerce-ai-search-citations-optimization/"
    title: "Aleyda Solis, Ecommerce AI search citations (May 2026; 25 US ecommerce sites, 5 subverticals; search extracts)"
  - id: gm-2027
    resource: "https://www.growth-memo.com/p/organic-growth-in-e-commerce-in-2027"
    title: "Growth Memo, Organic growth in e-commerce in 2027 (2026-10-12)"
  - id: aleyda-priorities
    resource: "https://www.aleydasolis.com/en/ai-search/content-prioritization-ai-search/"
    title: "Aleyda Solis, Content prioritization for AI search (Aug 2026; search extracts)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026; trial testimony, 2024 leak, author's schema compilation)"
  - id: gm-consensus
    resource: "https://www.growth-memo.com/p/the-consensus-gap"
    title: "Growth Memo, The consensus gap (2026-05-11; 3.7M citations, 20,000-prompt sample, Omnia data)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2025–2026"
  - id: ah-secondary
    resource: "https://ahrefs.com/blog/secondary-keywords/"
    title: "Ahrefs, Secondary keywords (2026-03-06)"
  - id: ah-onpage
    resource: "https://ahrefs.com/blog/on-page-seo-checklist/"
    title: "Ahrefs, On-page SEO checklist (updated 2026-03-05)"
  - id: ah-navigation
    resource: "https://ahrefs.com/blog/website-navigation/"
    title: "Ahrefs, Website navigation (2023-02-08; one jewelry ecommerce case)"
  - id: bp-soft404
    resource: "https://botpresso.com/what-is-a-soft-404-issue-how-to-fix-it/"
    title: "Botpresso, Soft 404 issues and fixes (≈2026-07)"
  - id: nz-meta
    resource: "https://natzir.com/en/seo/meta-descriptions-impact-gemini-ai/"
    title: "Natzir Turrado, Are meta descriptions back? Impact on Gemini (2026-10-22; Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts)"
  - id: sbs-catquality
    resource: "https://www.seobythesea.com/2019/06/categorical-quality/"
    title: "SEO by the Sea, Ranking results based on categorical quality (2019-06-10; application US 2019/0155948, filed 2015-03-31; grant status unconfirmed)"
  - id: sbs-rewrite
    resource: "https://www.seobythesea.com/2013/12/rewrite-search-terms/"
    title: "SEO by the Sea, How Google may rewrite queries (2013-12-08; patent US 8,600,973, filed 2012-01-03)"
  - id: sbs-urlcategories
    resource: "https://www.seobythesea.com/2013/07/google-classify-pages-hierarchical-categories-urls/"
    title: "SEO by the Sea, Classifying pages using hierarchical categories in URLs (2013-07-12; patent US 8,484,194, filed 2012-01-13)"
  - id: dj-fanout2
    resource: "https://dejan.ai/blog/fanout2/"
    title: "DEJAN, Fanout V2: complementary query sets (2026-09-16; summary of Google Research arXiv 2603.06397)"
  - id: gg-spam
    resource: "https://www.gsqi.com/marketing-blog/august-2026-google-spam-update-case-studies/"
    title: "Glenn Gabe, August 2026 spam update case studies (2026-08-31; 4 cases)"
  - id: ls-links
    resource: "https://lazarinastoy.com/how-to-incorporate-machine-learning-in-internal-linking-audits/"
    title: "Lazarina Stoy, ML in internal linking audits (2026-10-25; relays SearchPilot, InLinks)"
  - id: gn-html
    resource: "https://www.seoforgooglenews.com/p/why-semantic-html-matters-for-seo"
    title: "Barry Adams, Why semantic HTML matters for SEO and AI (2025-08-06; practitioner)"
---

# Category pages

For anyone writing, templating or auditing a category, subcategory or filtered listing page in an online shop.

## Rules
- **Open with one factual sentence** after the H1 — what the range is, key attributes, sizes, price from, delivery. *Measured* for assistants; Google says no special writing is needed ([§1](#1-the-opening-and-the-words)).
- **Use the searcher's exact term in title and H1**, including the compound noun people actually type, and the main facet variants in H2s; use customers' own word variants in copy and filter labels; test before renaming slugs. *From code, observed output, few US examples; Practitioner; Patent* ([§1](#1-the-opening-and-the-words), [§8](#8-body-copy-meta-description-and-customer-words)).
- **Keep one idea per passage** under a descriptive heading that names the subject; don't tune text to similarity scores. *Practitioner, one test* ([§1](#1-the-opening-and-the-words)).
- **Block facet crawling by default; index only filter combinations with proven search demand**, built to Google's URL rules. *Official* + *Practitioner* ([§2](#2-filters-and-pagination)).
- **Paginate with real `<a href>` links, one URL per page, each self-canonical.** *Official* ([§2](#2-filters-and-pagination)).
- **Link to every page you want found** — subcategory links rendered in the HTML, not added by JavaScript, plus complementary and accessory categories; split-test footer category links rather than packing the footer — and keep the section free of thin URL sets. *Measured* / *From the leak* / *Practitioner, one case*; complementary links *Inference from research*; footer *Measured, split test, relayed* ([§3](#3-internal-links-and-section-quality), [§9](#9-structure-demand-taxonomy-and-adjacent-needs)).
- **Name the category's main buyer uncertainty and link to the guide that answers it.** *Measured, 25 US sites, search extracts* ([§4](#4-the-buyers-main-uncertainty)).
- **Consolidate near-duplicate category and keyword-variant pages into one URL per intent**, in a path that mirrors the taxonomy; strengthen categories that already draw direct and navigational demand instead of spinning up thin hubs, and audit feed-generated category templates before a spam-update window. *From the leak* / *Practitioner* / *Patent*; spam update *Practitioner, 4 cases* ([§5](#5-one-url-per-intent), [§9](#9-structure-demand-taxonomy-and-adjacent-needs), [§10](#10-feed-generated-templates-and-spam-updates)).
- **Judge a category's visitor satisfaction against other category pages, per device.** *Trial / leak* ([§6](#6-satisfaction-against-its-own-type)).
- **Decide in advance what happens to a listing near zero stock**, and watch the Soft 404 count for category pages. *Practitioner* ([§7](#7-listings-near-zero-stock)).
- **Give the page visible body copy that answers its head queries, and write the meta description as if it were the only text read** — brands, ranges, prices, criteria. *Measured, observational, Gemini API only* ([§8](#8-body-copy-meta-description-and-customer-words)).

## Checklist
- [ ] The first ~200 characters after the H1 state facts (range, attributes, price from, delivery), in static HTML ([test](../measure/diagnostic-tests.md#4-fetch-a-page-the-way-an-ai-assistant-does)).
- [ ] The query's exact phrase is in title and H1 ([test](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries)).
- [ ] The main facet variants (material, size, use) appear as H2s or section openers; the title keeps the primary term.
- [ ] Each section has a heading that names its subject; no "it" or "this" openers.
- [ ] Facet URLs are disallowed in robots.txt unless a combination has demand; indexable ones use `&`, a fixed order, and 404 when empty.
- [ ] Page 2+ is reachable by link, has its own URL and a self-canonical.
- [ ] The page links to its subcategories and top products in the raw HTML (view-source, not only the rendered page), and is linked from navigation, not only the sitemap.
- [ ] A near-empty listing has a written rule (keep, merge or noindex below N items); Soft 404s for category pages are watched.
- [ ] The category's main uncertainty is named and linked to one focused guide.
- [ ] No second page targets the same intent; the product page and the category page don't split one query.
- [ ] Engagement compared with the category median on mobile and desktop ([test](../measure/diagnostic-tests.md#2-satisfaction-per-page-type)).
- [ ] Visible body copy answers the head queries; the meta description names brands, ranges, price range and buying criteria.
- [ ] Filter labels and copy use the words customers search with (check Search Console queries), not only internal names.
- [ ] The URL path mirrors the category tree (`/parent/child/`), not a flat ID.
- [ ] The page links to complementary and accessory categories, not only to synonyms of itself.
- [ ] Listing and copy sit in `<main>`; cross-sell and recommendation blocks sit in `<aside>`.
- [ ] Any change to footer category links runs as a split test.
- [ ] Category pages generated from a feed have images, unique copy and enough products each; audited before the next spam-update window.

## 1. The opening and the words
- ChatGPT sees title, URL and **~202 characters from the H1**, and ignores meta descriptions. *Measured.*[^chatgpt-retrieval] **Example.** A category opening with "Anyone looking into desks will sooner or later come across…" gave an assistant nothing to cite; no dimensions, material or price appeared in its static HTML.[^field-notes]
- Query understanding scores each term per URL; a term in the title adds ~3.5 on average and some terms must match exactly.[^qus] **Example.** Of seven lost queries, six already had their phrase in title and H1; the one exception — a compound noun no page carried — was the sharpest drop.[^field-notes] *Illustrative:* searchers type the single compound word for "desk lamp" while the page only says "lamps for the desk".
- **Secondary keywords in H2s.** Use 3–5 secondary keywords deliberately in H2/H3 headings, section openers and accurate alt text, at most 1–2 in the meta description; the title keeps the primary keyword. *Practitioner.*[^ah-secondary] On a category: the primary term in title and H1, the main facet variants (material, size, use) in H2s. Finding and mapping the terms: [keyword research](../channels/keyword-research.md).
- Optimising for embeddings "is literally keywords stuffing" (Google's John Mueller); micro-intent rewrites gained and then lost.[^mh-vector] Passage-level retrieval still favours self-contained sections under descriptive headings.[^ipr-chunking]

> **Conflict:** Google says "no requirement to break your content into tiny pieces";[^google-ai-guide] iPullRank measured better retrieval from self-contained passages — [details](../reference/conflicts.md#writing-for-embeddings-and-chunking)

## 2. Filters and pagination
- Google's default: "Use robots.txt to disallow crawling of faceted navigation URLs"; facets that should rank use `&`, a fixed order and **404** for empty or nonsensical combinations.[^g-facets] Rules: [faceted navigation](../technical/technical-foundations.md#1-faceted-navigation).
- Filter pages can be a long-tail source,[^not-enough] but only after technical issues are fixed.[^organic-analysis] *Practitioner.*
- "Google's crawlers don't 'click' buttons": load-more and infinite scroll need crawlable paginated links; page 2+ is self-canonical, not canonicalised to page 1.[^g-pagination] Rules: [pagination](../technical/technical-foundations.md#5-pagination-and-infinite-scroll).
- **Watch:** if Chrome's Decisions API ships (Canary only in 2026), every filter value will need a one-sentence description.[^decisions-api]

## 3. Internal links and section quality
- GPTBot followed internal links and never fetched sitemap-only URLs. *Measured.*[^chatgpt-retrieval]
- **Render subcategory links in the HTML.** Category pages need a visible forward-navigation block to their subcategories. In one jewelry shop, JavaScript filtering hid those links; the fix went live by Dec 2021 and gains followed by Mar 2022 (no figures published). *Practitioner, one case.*[^ah-navigation] Put only commercially important pages in the global navigation, generate related-category and related-product links from the taxonomy and "bought together" data, and give each new page 3+ contextual links from exact mentions on existing pages. *Practitioner.*[^ah-onpage][^ah-navigation] Methods and the raw-vs-rendered link check: [internal linking](../technical/internal-linking.md).
- Quality is scored per section, and a new page inherits its section's average. *From the leak.*[^leak-6] Hundreds of thousands of filter or variant URLs are a quality problem for the whole section; thin category and list pages were among those dropped from the index from 27 May 2025.[^mh-deindex] Background: [Google ranking](../how-it-works/google-ranking.md).
- **Footer category links: test, don't pack.** In a SearchPilot split test relayed by a practitioner, growing a footer from 30 to 100+ category links gave about +10 % organic desktop traffic (95 % confidence) and +5 % mobile (90 %); SearchPilot itself warns against packing footers. *Measured, split test, relayed.*[^ls-links] **Do:** change footer category links only as a split test. Methods: [internal linking](../technical/internal-linking.md).
- **Cross-sell in `<aside>`.** Wrap the listing and copy in `<main>`, and put cross-sell and recommendation blocks in `<aside>`, so machines can tell the page's own content from the extras. *Practitioner.*[^gn-html] Product-page structure: [product pages](product-pages.md#8-markup-structure-machines-can-read).

## 4. The buyer's main uncertainty
- Each category has one main uncertainty — fit and returns for fashion, specs and compatibility for electronics, skill level for sports — and AI answers cite guides and support pages to resolve it, while shoppers click product and category pages.[^aleyda-ecom] Answer it on one focused guide ([comparison pages and guides](comparison-and-guides.md)) and link to it from the category.
- Answer 8–10 real buyer questions on each category page. *Opinion.*[^gm-2027]
- Only 1.6 % of cited category URLs appear in all three of ChatGPT, Perplexity and AI Overviews[^gm-consensus] — measure per engine.

## 5. One URL per intent
- Twiddlers cap results per host; near-identical URLs compete instead of adding slots. *From the leak.*[^leak-2] **Example.** A product page and its category page split one query's impressions about half and half, at positions ~4 and ~9.[^field-notes]
- Fold fragmented keyword-variant pages serving one intent into the canonical page. *Practitioner; search extracts.*[^aleyda-priorities] Redirect with one hop ([migration](../situations/migration.md)).

## 6. Satisfaction against its own type
- NavBoost keeps ~13 months of click memory per query and page, by country and device; compare short visits within a page type.[^navboost]
- **Example.** One category's pages lost clicks, yet their visitors bounced less than the category median (12.5 % vs 20.8 %): the loss was ranking and vanished sitelinks, not disappointed visitors.[^field-notes]

## 7. Listings near zero stock
- **Thin listings drift into Soft 404.** Listings slip into Soft 404 as their inventory approaches zero, and so do JavaScript product grids that fail to render. The same source recommends noindexing listings below an item threshold, without giving a value. *Practitioner, vendor.*[^bp-soft404]
- **Do:** write down at what item count a category is merged into its parent or noindexed, render the grid in HTML, and watch the Soft 404 count for category pages in Search Console ([scaling content and templates](../situations/scaling-content-and-templates.md#6-soft-404s-on-inventory)). Out-of-stock product pages: [product pages](product-pages.md#7-out-of-stock-and-discontinued).

> **Conflict:** noindex near-empty or stocked-out pages vs keep them indexed — [details](../reference/conflicts.md#out-of-stock-pages-noindex-or-keep-indexed)

## 8. Body copy, meta description and customer words
- **A meta excerpt is a symptom of thin body copy.** When Gemini grounds on Google Search, it gets one excerpt per result; across 2,580 excerpts, 23 % of category-page excerpts were the meta description (homepages 43 %, articles 3.8 %). Category pages were cited 6 % of the time when the excerpt was the meta, 58 % when it was body text; where the meta was used, the best body paragraph covered 56 % vs 71 % of the query's terms. *Measured, observational, Gemini API only (not AI Overviews or AI Mode).*[^nz-meta] That better metas raise citations is untested.
- **Do:** give the category visible body copy that answers its head queries, and write the meta description as if it were the only text an engine reads: brands, ranges, prices, criteria. Evidence: [Google AI features](../how-it-works/google-ai-features.md).

> **Conflict:** Gemini sometimes reads only the meta description; ChatGPT ignores it and Google often rewrites it — [details](../reference/conflicts.md#do-meta-descriptions-still-matter)

- **Customer vocabulary.** A Google patent prunes synonym substitutions when the substituted term rarely appears in the returned pages or the rewritten results get no clicks. *Patent.*[^sbs-rewrite] **Do:** use the variants customers type (from Search Console and site search) in category copy and filter labels ([keyword research](../channels/keyword-research.md)).

## 9. Structure: demand, taxonomy and adjacent needs
- **Strengthen categories with real demand.** A Google application reranks the top 20–30 results for broad category queries by a query-independent category quality score (traffic, being the navigational destination for related queries, authority, selection rates) once enough results pass a popularity test. *Patent (application, grant unconfirmed); click and popularity inputs are supported by trial testimony.*[^sbs-catquality] **Do:** invest in category pages that already attract direct and navigational traffic; don't spin up thin hubs.
- **URL mirrors the taxonomy.** A Google patent trains page classification on URL directory paths. *Patent.*[^sbs-urlcategories] **Do:** let the category URL path follow the category tree; avoid flat or ID-only paths for category pages.
- **Link complementary categories.** Google Research on fan-out rewards sub-queries that are complementary rather than paraphrases — for a camping kit: shelter, sleep, cooking, lighting. *Research paper; production use unconfirmed.*[^dj-fanout2] **Do:** from each category, link the accessory and companion categories a buyer needs next, and cluster topics by distinct sub-need, not synonym. *Inference.* Methods: [internal linking](../technical/internal-linking.md).

## 10. Feed-generated templates and spam updates
- The August 2026 spam update targeted content, not links. A thin affiliate site whose category and product pages were built programmatically from a marketplace feed — some without images, footer text 97 %+ likely AI-written — lost 14K+ queries; a 1.5M-URL product-information site, ~85 % programmatic, took a site-wide, core-like hit. Recovery takes months. *Practitioner, 4 cases.*[^gg-spam]
- **Do:** before a spam-update window, audit category templates generated from a feed: does each page have images, copy of its own and enough products to exist for users? Merge or noindex those that don't ([scaling content and templates](../situations/scaling-content-and-templates.md), [core update recovery](../situations/core-update-recovery.md), [update dates](../reference/google-updates-timeline.md)).

Related: [product pages](product-pages.md), [homepage and brand](homepage-and-brand.md), [traffic drop](../situations/traffic-drop.md), [core update recovery](../situations/core-update-recovery.md), [keyword research](../channels/keyword-research.md), [internal linking](../technical/internal-linking.md).

[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: funnel 58k retrieved → 7.6k shown → 5k cited → 760 opened; ~202-character snippet from the H1; JSON-LD stripped; bot roles and cache; utm on ~95 % of displayed links; instant vs thinking search counts.
[^google-ai-guide]: Google generative-AI optimization guide, updated 2026-07-10.
[^qus]: Resoneo, QUS, 2025-07-22: per-term scores 0–~10, title +3.5, numbers 0, exact vs derived match.
[^mh-vector]: Marie Haynes, 2025-06-26: Mueller quote; anecdotal case screenshots.
[^ipr-chunking]: iPullRank, 2026-01-15: passage-level retrieval, descriptive headings; one own test with its own tool.
[^g-facets]: Google, faceted navigation, read 2026-10-27.
[^not-enough]: Searchind, "not enough", read 2026-10-27: indexed filter pages as long tail.
[^organic-analysis]: Searchind, organic analysis guide: faceted navigation only after technical issues are fixed.
[^decisions-api]: Resoneo, Chrome Decisions API, updated 2026-10-08: Canary only; accuracy rises with tuned descriptions.
[^g-pagination]: Google, pagination and incremental loading, read 2026-10-27.
[^leak-6]: Resoneo, leak part 6, 2024-10-31: index tiers, crawl skipping, siteFocusScore/siteRadius, new pages inherit the sitechunk average.
[^leak-2]: Resoneo, leak part 2, 2024-10-31: OfficialPageTwiddler, host diversity caps.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^aleyda-ecom]: Aleyda Solis, May 2026, via search extracts: Semrush Enterprise AIO + Similarweb, 25 US sites; directional.
[^gm-2027]: Growth Memo, 2026-10-12: answer 8–10 buyer questions per page (opinion).
[^aleyda-priorities]: Aleyda Solis, Aug 2026, via search extracts: six-dimension scoring, consolidation rules.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: click-signal families, 13-month history per query and page by country and device, Glue for SERP blocks, compare short visits per page type. No measured ranking effects shown.
[^gm-consensus]: Growth Memo, 2026-05-11: 91.07 % single-engine, 2.37 % all three; 1.2 % product, 1.6 % category; author calls it directional.
[^field-notes]: Anonymised shop: GA4 google / organic landing pages vs page-type medians, 34 days in Sep–Oct 2026; Search Console query × page, same 5 weeks 2025 vs 2026; live title/H1/slug check; static-HTML spot check of category pages.
[^ah-secondary]: Ahrefs, secondary keywords, 2026-03-06: 3–5 secondary keywords in H2/H3, section openers and alt text, ≤ 1–2 in the meta description, primary keyword kept in the title. Practitioner advice.
[^ah-onpage]: Ahrefs, on-page SEO checklist, updated 2026-03-05: link new pages from exact in-text mentions on existing pages (find them by site search or crawl). Practitioner advice.
[^ah-navigation]: Ahrefs, website navigation, 2023-02-08: one jewelry ecommerce case (JS filtering hid subcategory links; fix live by Dec 2021, gains by Mar 2022, no figures); global navigation for commercially important pages only; related links from taxonomy and "bought together" data.
[^bp-soft404]: Botpresso, soft 404 guide, ≈2026-07 (no publish date shown): practitioner advice from an agency promoting its own tools; the noindex recommendations partly contradict the common reading of Google's ecommerce guidance.
[^nz-meta]: Natzir Turrado, 2026-10-22: Gemini API with Search grounding, 115 prompts (EN-US, ES-ES) × 3 runs, 2,580 excerpts; meta description in 7.6 % of excerpts; meta share by page type (home 43 %, category 23 %, article 3.8 %); category citation 6 % (meta) vs 58 % (body); best body paragraph 56 % vs 71 % query-term coverage. Observational; not AI Overviews or AI Mode.
[^sbs-rewrite]: SEO by the Sea, 2013-12-08: patent US 8,600,973 on query rewriting; substitution rules pruned by term presence in results and clicks.
[^sbs-catquality]: SEO by the Sea, 2019-06-10: application US 2019/0155948 (filed 2015-03-31, grant status unconfirmed); categorical quality score on the top 20–30 once enough results pass a popularity test (example 70 %).
[^sbs-urlcategories]: SEO by the Sea, 2013-07-12: patent US 8,484,194; URL directory paths as training data for hierarchical page classification.
[^dj-fanout2]: DEJAN, 2026-09-16: summary of Google Research arXiv 2603.06397 (R4T): penalises paraphrase collapse, rewards diverse, grounded, root-aligned sub-queries; production use unconfirmed.
[^gg-spam]: Glenn Gabe, 2026-08-31: 4 August 2026 spam update cases; content, not links; feed-built affiliate site (some pages without images, footer text 97 %+ likely AI-written) lost 14K+ queries; 1.5M-URL product-information site ~85 % programmatic, site-wide hit; recovery takes months.
[^ls-links]: Lazarina Stoy, 2026-10-25: relays a SearchPilot split test (footer 30 → 100+ category links: ~+10 % organic desktop at 95 % confidence, +5 % mobile at 90 %) and SearchPilot's warning against packing footers; primary test not read.
[^gn-html]: Barry Adams, 2025-08-06: one `<h1>`, `<article>`/`<main>` around main content, `<aside>` for sidebars and recommendations; practitioner advice from a publisher context.
