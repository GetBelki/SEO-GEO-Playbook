---
type: Playbook
title: Feeds and Merchant Center
description: Feed audit checklist for Shopping and AI product cards — plain-word attributes, specific categories, data-source hygiene, feed-only title tests, feed links as landing URLs, promotions, reviews — plus constraint copy that answers "will it fit?", consistent product-line naming, Merchant Center limits, GTIN rules, price matching and the 2026 attribute and API changes.
tags: [geo, feeds, merchant-center, shopping, agentic-commerce, product-data, gtin, merchant-api, product-lines]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: aleyda-ecom
    resource: "https://www.aleydasolis.com/en/ai-search/ecommerce-ai-search-citations-optimization/"
    title: "Aleyda Solis, Ecommerce AI search citations (May 2026; 25 US ecommerce sites, 5 subverticals; search extracts)"
  - id: ipr-agentic-ecom
    resource: "https://ipullrank.com/agentic-ecommerce-strategy"
    title: "iPullRank (Angela Clark), Agentic ecommerce strategy (2025-12-04; cites a Bain survey)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: brodie-loyalty
    resource: "https://brodieclark.com/loyalty-program-promotion-gmc/"
    title: "Brodie Clark, Loyalty programme and promotions in Merchant Center (2025-08-13)"
  - id: gm-2027
    resource: "https://www.growth-memo.com/p/organic-growth-in-e-commerce-in-2027"
    title: "Growth Memo, Organic growth in e-commerce in 2027 (2026-10-12)"
  - id: gmc-audit
    resource: "https://searchind.com/the-google-merchant-center-audit-i-run-for-every-client/"
    title: "Searchind, The Google Merchant Center Audit I run for every client (Aug 2026, updated Oct 2026)"
  - id: ucp
    resource: "https://searchind.com/ucp-agentic-ecommerce-seo/"
    title: "Searchind, Google's shift to Agentic Commerce (May 2026)"
  - id: pim
    resource: "https://searchind.com/pim-for-ecommerce-and-shopify/"
    title: "Searchind, PIM for Ecommerce and Shopify (Sep 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2026 (Search Console by search appearance and country; feed export)"
  - id: bp-gmc
    resource: "https://botpresso.com/how-to-add-products-google-merchant-centre/"
    title: "Botpresso, How to add products to Google Merchant Center (updated ≈2026)"
  - id: sbs-productlines
    resource: "https://www.seobythesea.com/2020/01/new-product-lines"
    title: "SEO by the Sea, Google Product Search and new product lines (2020-01-27; patent US 10,394,816, filed 2012-12-27)"
  - id: dj-tags
    resource: "https://dejan.ai/blog/ai-mode-tags/"
    title: "DEJAN, AI Mode layout tags (2026-09-20; prompt-leak content, unverified)"
---

# Feeds and Merchant Center

What a product feed needs so that products are eligible for Shopping and AI product cards at all, and how to write copy an agent can use to answer "will it fit?". Where the cards come from, Google checkout and the 2026 EEA free-listings removal are in [shopping surfaces](../how-it-works/shopping-surfaces.md). Confidence labels follow the [scale](../reference/sources-and-confidence.md).

## Rules
- **Fill plain-word attributes and a specific product category on every item**, and separate feed fixes from product-data gaps. *Practitioner* — [checklist](#1-feed-audit-checklist). Name each brand's product lines the same way in titles, feed and filters. *Patent* — [product lines](#4-product-line-naming-and-ai-mode-layouts)
- **Clean up the account before optimising:** delete auto-created data sources, export disapprovals by issue type and monitor the feed daily. *Practitioner* — [checklist](#1-feed-audit-checklist)
- **Change titles in the feed only, never in the shop backend, and test each pattern against an untouched control set.** *Practitioner* — [checklist](#1-feed-audit-checklist)
- **Treat the feed `link` as a landing URL** and check it for redirects, lost parameters and the right variant. *Practitioner* — [checklist](#1-feed-audit-checklist)
- **Use Merchant Center promotions and loyalty, and keep "was" prices honest**, because price history is shown to shoppers. *Practitioner* — [checklist](#1-feed-audit-checklist)
- **Collect product-type-specific reviews, Q&A and use videos**, and ask several assistants about your products to find wrong answers to fix at the source. *Practitioner* — [checklist](#1-feed-audit-checklist)
- **Gate items with required fields per category** before they sync to the feed. *Practitioner* — [checklist](#1-feed-audit-checklist)
- **State what a product is best for, its limits, what it is not for and exact dimensions**, consistently in feed and page. *Practitioner; per-category uncertainty Measured* — [copy](#2-copy-that-lets-an-agent-answer-will-it-fit)
- **Validate every GTIN before upload** (GS1 check digit, no restricted prefixes), send `identifier_exists=false` only for items that truly have none, and keep the feed price identical to the site price. *Practitioner* — [limits and identifiers](#3-limits-identifiers-and-2026-changes)
- **Plan integrations on the Merchant API**, which replaces the Content API. *Practitioner* — [limits and identifiers](#3-limits-identifiers-and-2026-changes)

## 1. Feed audit checklist
Based on a practitioner's standard Merchant Center audit, *practitioner*:[^gmc-audit]
1. **Attributes in plain words.** Material, colour, size/dimensions, use. Material is the attribute most often missing. Dimensions held in custom columns aren't read as `size`.
2. **Specific product category** on every item; generic top-level categories cause disapprovals.
3. **Delete auto-created data sources** that Merchant Center made next to your own feed.
4. **Export disapprovals** as CSV and track them by issue type.
5. **Titles:** search the main keyword of 20–30 top products in Shopping, record competitor title patterns, pick 2–3 patterns. Remove internal model names, use one dimension format, add material, use the local-language term.
6. **Change titles in the feed only** (supplemental feed or feed-tool rule), never in the shop backend: a backend rename can change the URL slug and needs redirects and an ads URL check.
7. **Test** each title pattern on 20–30 products against an untouched control set ([test design](../measure/diagnostic-tests.md#5-feed-attribute-coverage-and-title-tests)).
8. **Monitor daily**, for example via the Merchant Center data transfer to a warehouse (products, product performance, price competitiveness).
9. **Treat the feed `link` as a landing URL.** Free-listing clicks now go straight to the retailer page set in the feed — in the Shopping tab (tested Jun 2026), as the Chrome default (Sep 2026) and in AI Mode grids (Sep 2026).[^brodie-notes] Check feed links for redirects, lost parameters and the right variant, as for ads.
10. **Promotions and loyalty.** Promotions and a loyalty programme in Merchant Center can show on free listings and in the merchant knowledge panel; long-running promotions (maximum 6 months) help the store-quality promotions metric. Merchant Center data "takes precedence over structured data". Loyalty was eligible in the US, UK, Germany, France and Australia; the article predates the [EEA change](../how-it-works/shopping-surfaces.md). *Practitioner how-to.*[^brodie-loyalty]
11. **Price history.** Product results can show a "typical / low / high" price insight "based on the last 90 days".[^brodie-notes] A long-inflated "was" price can surface as "high".
12. **Reviews, Q&A and video.** Agents lean on reviews and Q&A and need real-time price and stock. Ask for reviews 7–14 days after delivery with prompts specific to the product type (e.g. assembly difficulty for furniture), add Q&A to product pages, add assembly or use videos. In a Bain survey 30–45 % of consumers used AI for product research and 51 % didn't trust agents to complete a purchase. *Practitioner, anecdotal tests.*[^ipr-agentic-ecom]
13. **Ask the assistants.** Ask several assistants what you sell, what it costs and what your return policy is; fix wrong answers at the source (feed, page, [third-party listing](third-party-presence.md)). *Practitioner.*[^gm-2027]

- **Example.** A feed of ~28,000 items had a specific Google category on all but one, but `material` on only 22 % and the size field empty on every item; dimensions sat in custom columns. The shop didn't record material for every product, so only part of the gap was a feed fix — the rest was a product-data gap.[^field-notes]
- **Quality gate.** For large, multi-supplier catalogues a PIM helps; the transferable part is the gate itself — required fields per category before an item syncs to the feed.[^pim]

## 2. Copy that lets an agent answer "will it fit?"
Write what a product is best for, its limits, what it is *not* for, and exact dimensions — in the feed description and in the opening of the product page.[^ucp] Each category has its own main uncertainty — suitability for beauty, fit and returns for fashion, specs and compatibility for electronics, activity and skill level for sports — and AI answers cite guides, support pages and communities to resolve it, while shoppers click product and category pages. *Measured, 25 US ecommerce sites; search extracts.*[^aleyda-ecom] Answer each category's uncertainty on one focused page, consistent with the feed and product pages. Same direction as the factual first sentence on [product pages](../page-types/product-pages.md). Check return reasons first: a recurring reason is the "not suitable for" line. *Practitioner.*

## 3. Limits, identifiers and 2026 changes
From a practitioner's setup guide, *practitioner*, ≈2026;[^bp-gmc] check against Merchant Center Help before relying on a limit.
- **Account limits.** A standard account holds 150,000 items and 200 data sources. Titles take up to 150 characters, descriptions up to 5,000.
- **GTINs.** A GTIN must pass the GS1 check digit and must not start with the restricted prefixes 02, 04, 2, 05, 98 or 99. Items without a GTIN are rejected unless `identifier_exists` is set to `false` — use that only for products that really have no manufacturer identifier.
- **Price mismatch.** A feed price that differs from the landing-page price is a top disapproval reason. Update feed price and site price from the same source, on the same schedule. *Inference.*
- **New attributes in 2026:** `handling_cutoff_time`, `minimum_order_value`, `pickup_cost`.
- **Naming and API.** The "Merchant Center Next" name was dropped in July 2026. The Merchant API replaces the Content API for Shopping; move feed and inventory integrations to it.
- **Not covered:** setting up feeds per country and language. See [new market](../situations/new-market.md).

## 4. Product-line naming and AI Mode layouts
- **Product lines are detected from titles.** A Google patent for product search detects brand product lines from the pattern [brand][line][attribute] and adds them to the category's attribute dictionary. *Patent; use in today's Shopping systems unknown.*[^sbs-productlines] **Do:** write each line's name identically in product titles, the feed and filter labels, and give each line a filterable, linkable facet on the category page ([faceted navigation](../technical/technical-foundations.md#1-faceted-navigation)).
- **AI Mode layout tags (hypothesis).** A leaked AI Mode prompt reads as if product offers are shown only for "single, concrete product iterations" (a SKU-level product with a GTIN), and carousels or image grids need at least 3 validated items of one entity type. *Hypothesis only — prompt-leak content, unverified.*[^dj-tags] It points the same way as the rules above: one item per real SKU, with a valid GTIN. How the cards are built: [shopping surfaces](../how-it-works/shopping-surfaces.md).

Related: [shopping surfaces](../how-it-works/shopping-surfaces.md), [product pages](../page-types/product-pages.md), [third-party presence](third-party-presence.md), [local](local.md), [diagnostic tests](../measure/diagnostic-tests.md#5-feed-attribute-coverage-and-title-tests), [product variants](../technical/technical-foundations.md#4-product-variants).

[^ucp]: Searchind, agentic commerce, read 2026-10-27: eligibility over rank, constraint-based copy. No Google sources cited.
[^gmc-audit]: Searchind, Merchant Center audit, read 2026-10-27: title test design, feed-only changes, material most missing, specific categories, auto-created data sources, disapproval CSV, warehouse transfer.
[^pim]: Searchind, PIM, read 2026-10-27: quality gates and approval workflow.
[^aleyda-ecom]: Aleyda Solis, May 2026, via search extracts: Semrush Enterprise AIO + Similarweb, 25 US sites; directional.
[^ipr-agentic-ecom]: iPullRank (Clark), 2025-12-04: review timing and prompts, Q&A, video; Bain survey figures.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^brodie-loyalty]: Brodie Clark, 2025-08-13: promotions add-on, 6-month maximum, promotions rejection rate, loyalty markets, Merchant Center over structured data, no organic loyalty reporting.
[^gm-2027]: Growth Memo, 2026-10-12: shortlist figures restated; feed and PDP advice is opinion.
[^field-notes]: Anonymised shop: feed export of 2026-10-27; Search Console by search appearance and country, 17 Aug – 13 Sep vs 28 Sep – 25 Oct 2026.
[^bp-gmc]: Botpresso, how to add products to Google Merchant Center, updated ≈2026 (no publish date shown): account limits, title and description lengths, GTIN check digit and restricted prefixes, `identifier_exists`, price mismatch, 2026 attributes, "Merchant Center Next" name dropped July 2026, Merchant API replacing the Content API. Agency how-to; not re-checked against Google's help pages.
[^sbs-productlines]: SEO by the Sea (Bill Slawski), 2020-01-27: patent US 10,394,816 (filed 2012-12-27) on detecting new product lines ([brand][line][attribute]) and adding them to category attribute dictionaries. Patent analysis; blog inactive since 2022.
[^dj-tags]: DEJAN, 2026-09-20: AI Mode layout tags from leaked prompt content (`<ShoppingOffers>` for SkuLevelProduct with GTIN; `<Carousel>` / `<ImageGrid>` with ≥ 3 validated children of one entity type). Unverified; hypothesis only.
