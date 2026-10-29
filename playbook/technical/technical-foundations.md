---
type: Checklist
title: Technical foundations (Google's official rules)
description: Google's documented rules for the technical basics that decide what gets crawled, indexed and shown — faceted navigation, canonicals, site moves, product variants, pagination, crawl budget, JavaScript, structured data policies, Core Web Vitals, hreflang and link spam — plus labelled additions on rendering checks, 404 vs 410 vs 301, URL hierarchy, server location, Gemini reading the indexed copy, Chrome-side AI features, Google-selected canonicals carrying over to ChatGPT, the Removals tool, PDF deindexing, viewport and CSS rendering pitfalls, signal drift between outputs, semantic landmarks, and HTML size limits for Googlebot and Bing.
tags: [seo, technical-seo, google, crawling, indexing, canonical, migration, hreflang, structured-data, core-web-vitals, rendering, status-codes, url-structure, hosting, pdf, lazy-loading, semantic-html, html-size, cdn, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: g-facets
    resource: "https://developers.google.com/search/docs/crawling-indexing/crawling-managing-faceted-navigation"
    title: "Google Search Central, Managing crawling of faceted navigation URLs (updated 2025-12-18)"
  - id: g-canonical
    resource: "https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls"
    title: "Google Search Central, How to specify a canonical URL (updated 2026-07-10)"
  - id: g-site-move
    resource: "https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes"
    title: "Google Search Central, Site moves with URL changes (updated 2026-08-20)"
  - id: g-variants
    resource: "https://developers.google.com/search/docs/appearance/structured-data/product-variants"
    title: "Google Search Central, Product variant structured data (updated 2026-09-08)"
  - id: g-pagination
    resource: "https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading"
    title: "Google Search Central, Pagination and incremental page loading (updated 2025-12-10)"
  - id: g-crawl-budget
    resource: "https://developers.google.com/search/docs/crawling-indexing/large-site-managing-crawl-budget"
    title: "Google Search Central, Large site owner's guide to managing crawl budget"
  - id: g-js
    resource: "https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics"
    title: "Google Search Central, JavaScript SEO basics (updated 2026-03-04)"
  - id: g-sd-policies
    resource: "https://developers.google.com/search/docs/appearance/structured-data/sd-policies"
    title: "Google Search Central, General structured data guidelines (updated 2026-07-10)"
  - id: g-cwv
    resource: "https://web.dev/articles/vitals"
    title: "web.dev, Web Vitals (updated 2024-10-31), and Search Console Core Web Vitals report help"
  - id: g-hreflang
    resource: "https://developers.google.com/search/docs/specialty/international/localized-versions"
    title: "Google Search Central, Tell Google about localized versions of your page (updated 2026-09-21)"
  - id: g-spam
    resource: "https://developers.google.com/search/docs/essentials/spam-policies"
    title: "Google Search Central, Spam policies for Google web search (updated 2026-08-28)"
  - id: learningseo
    resource: "https://learningseo.io/"
    title: "LearningSEO.io (Aleyda Solis), curated SEO roadmap — used as a gap checklist, read 2026-10-27"
  - id: nz-render
    resource: "https://natzir.com/en/seo/googlebot-full-fetch-render-search-console/"
    title: "Natzir Turrado, Googlebot's full fetch and render in Search Console (2026-09-30; tool/method)"
  - id: bc-404
    resource: "https://www.bruceclay.com/blog/how-to-manage-404-pages-effectively-for-seo-and-user-experience/"
    title: "Bruce Clay, Managing 404 pages (2026-06-16)"
  - id: sbs-urlcategories
    resource: "https://www.seobythesea.com/2013/07/google-classify-pages-hierarchical-categories-urls/"
    title: "SEO by the Sea, Classifying pages using hierarchical categories in URLs (2013-07-12; patent US 8,484,194, filed 2012-01-13)"
  - id: bc-servers
    resource: "https://www.bruceclay.com/blog/servers-and-seo-the-impact-of-servers-and-hosting-on-seo-success/"
    title: "Bruce Clay, Servers and SEO (2026-06-30; Mueller quotes, Deloitte study)"
  - id: dj-notlive
    resource: "https://dejan.ai/blog/googles-still-doesnt-see-your-live-page/"
    title: "DEJAN, Google still doesn't see your live page (2026-05-07; probing, 2 URLs)"
  - id: nz-lens
    resource: "https://natzir.com/en/seo/passage-lens-see-your-page-like-google-chrome/"
    title: "Natzir Turrado, Passage Lens: see your page the way Chrome does (2026-08-06; Chromium source)"
  - id: nz-adcrux
    resource: "https://natzir.com/en/seo/crux-ad-metrics-chrome-ad-density-checker/"
    title: "Natzir Turrado, CrUX ad metrics (2026-10-05)"
  - id: dj-decision
    resource: "https://dejan.ai/blog/chrome-decisions-api-decisionmodel/"
    title: "DEJAN, Chrome Decisions API DecisionModel (2026-10-08; Chromium source, n=10 test questions)"
  - id: gg-canonical
    resource: "https://www.gsqi.com/marketing-blog/rel-canonical-hint-cascade-chatgpt/"
    title: "Glenn Gabe, Rel canonical is just a hint — cascade to ChatGPT (2026-02-17; 3 client cases)"
  - id: gg-pdf
    resource: "https://www.gsqi.com/marketing-blog/how-to-find-all-pdfs-deindexed-url-inspection-api/"
    title: "Glenn Gabe, Finding deindexed PDFs with the URL Inspection API (2026-09-16; method + client observations)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: ja-cloak
    resource: "https://www.jonoalderson.com/conjecture/cloaking-is-dead-long-live-cloaking/"
    title: "Jono Alderson, Cloaking is dead, long live cloaking (2026-10-26; argument + relayed Mueller 2017, Dave Smart 2026-07 test)"
  - id: ja-brain
    resource: "https://www.jonoalderson.com/conjecture/your-website-needs-a-brain/"
    title: "Jono Alderson, Your website needs a brain (2026-10-04; worked examples)"
  - id: gn-html
    resource: "https://www.seoforgooglenews.com/p/why-semantic-html-matters-for-seo"
    title: "Barry Adams, Why semantic HTML matters for SEO and AI (2025-08-06; practitioner)"
  - id: wd-html
    resource: "https://web.dev/learn/performance/general-html-performance"
    title: "web.dev (Google Chrome team), General HTML performance considerations (2023-11-01; guidance)"
  - id: dbb-2mb
    resource: "https://www.debugbear.com/blog/googlebot-crawler-file-size-limit"
    title: "DebugBear, What Googlebot's 2MB Crawl Size Limit Means For SEO (2026-02-16; Google docs, forum report, author's own URL Inspection tests)"
  - id: dbb-cdn-seo
    resource: "https://www.debugbear.com/blog/cdn-seo"
    title: "DebugBear, Can A Content Delivery Network Boost Website SEO? (2026-05-04; explainer)"
  - id: dbb-psi
    resource: "https://www.debugbear.com/blog/pagespeed-insights"
    title: "DebugBear, How To Use PageSpeed Insights (2025-03-09, upd. 2026-10-08; explainer)"
---

# Technical foundations (Google's official rules)

These are Google's own documented rules, so they rank above every practitioner claim in this playbook ([confidence scale](../reference/sources-and-confidence.md)). The topic list follows the gaps found against the LearningSEO roadmap.[^learningseo] Quotes were extracted on 2026-10-27; spot-check the live page before quoting it in a decision, since Google edits these docs often (the update dates are in the sources). Sections 12–24 add practitioner, patent and from-code material next to these rules; each item there carries its own, lower confidence label.

## Rules
- **Keep facet URLs out of the crawl with a robots.txt disallow**, and open only filter combinations with real search demand, using `&` separators, a fixed order and a 404 for empty results. *Official* — [evidence](#1-faceted-navigation)
- **Canonicalise with redirects or `rel="canonical"`, one method per page**, never with robots.txt or noindex — and watch which canonical Google actually selects per page type, because the hint can be overridden and the choice carries over to ChatGPT. *Official; Practitioner, 3 cases* — [evidence](#2-canonicals-and-duplicates), [Google-selected canonicals](#18-google-selected-canonicals-carry-over-to-ai-answers)
- **Move URLs with a full old-to-new map and server-side permanent redirects without chains**, kept for at least a year. *Official* — [evidence](#3-site-moves-and-url-renames)
- **Give every product variant a URL that preselects it**, then either one group canonical or full self-contained markup per variant page. *Official* — [evidence](#4-product-variants)
- **Paginate with crawlable `<a href>` links and self-canonical page URLs**; load-more buttons and infinite scroll need crawlable links behind them. *Official* — [evidence](#5-pagination-and-infinite-scroll)
- **Return real status codes and keep links, canonicals and key content in server-rendered HTML**: 404 or 410 for removed pages, no soft 404s, no noindex removed by script. 301 only to a relevant replacement, 410 for content deliberately removed without one, never every 404 to the homepage. *Official; Practitioner (410 vs 301)* — [evidence](#6-crawl-budget), [JavaScript](#7-javascript), [removed pages](#13-removed-pages-404-410-or-301)
- **Mark up only what is visible and true on the page**, with all required properties. *Official* — [evidence](#8-structured-data-policies)
- **Make hreflang reciprocal, self-referencing and ISO-coded**, with an `x-default`. *Official* — [evidence](#10-international-and-hreflang)
- **Check what Google stored, not the live page**: below-the-fold product grids and links in URL Inspection's rendered HTML (Googlebot doesn't scroll), and indexing before expecting a change in Gemini or AI Mode. *Practitioner (tool observation); Measured, 2 URLs* — [rendering](#12-rendering-checks-in-url-inspection), [indexed copy](#16-gemini-reads-the-indexed-copy)
- **Let category URL paths mirror the category taxonomy**; avoid flat or ID-only paths for category pages. *Patent* — [evidence](#14-url-hierarchy-mirrors-the-taxonomy)
- **Keep what Google renders identical to what people see, from one source of truth**: no prices, stock or labels in CSS `::before`/`::after`, no height-based media queries that change content, `<picture>` variants of the same subject; derive sitemaps, hreflang, canonicals and availability from one product record. *Practitioner; Official (cloaking by intent)* — [rendering](#21-viewport-css-and-rendering-differences), [signal drift](#22-signal-drift-one-record-for-every-output)

## 1. Faceted navigation
- **Default: don't let facets be crawled.** "Use robots.txt to disallow crawling of faceted navigation URLs" — e.g. disallow `*?*color=` and `*?*size=` patterns.[^g-facets]
- Filters behind a `#` fragment have "no impact on crawling (positive or negative)" — Google "generally doesn't support URL fragments".[^g-facets]
- Canonicalising facets to the unfiltered page "may, over time, decrease the crawl volume"; `nofollow` only works if every link to the facet carries it. Both are weaker than robots.txt.[^g-facets]
- **If some facets should rank** (filter combinations with real search demand — see [page patterns](../page-types/category-pages.md)):
  - use `&` as the parameter separator, not commas, semicolons or brackets;
  - in path-based filters, keep a fixed order so no duplicate combination can exist;
  - return **404** for empty results, nonsensical combinations and nonexistent page numbers, at the URL where they occur — no redirect to a generic error page.[^g-facets]

## 2. Canonicals and duplicates
- **Signal strength:** redirects and `rel="canonical"` are "a strong signal"; sitemap inclusion is "a weak signal". Signals add up.[^g-canonical]
- **Don't:**
  - use robots.txt to canonicalise — Google "may still index URLs that are disallowed in robots.txt without their content";
  - use noindex for it: "We don't recommend using noindex to prevent selection of a canonical page within a single site";
  - send mixed signals: "Don't specify different URLs as canonical for the same page using different canonicalization techniques";
  - use fragments or the URL removal tool.[^g-canonical]
- **Do:** absolute URLs, the link element in `<head>` only, a self-referencing canonical on canonical pages, one method per page. Canonicals that carry `hreflang`, `lang`, `media` or `type` attributes "are not used for canonicalization". Use HTTPS URLs in sitemaps and hreflang.[^g-canonical]

## 3. Site moves and URL renames
- "It's important to map your old site's URLs to the URLs for the new site"; use the map to update internal links and sitemaps.[^g-site-move]
- "Use HTTP permanent redirects if possible, such as 301 and 308" — server-side, no chains. Keep them "for as long as possible, generally at least 1 year".[^g-site-move] web.dev adds the speed side: each redirect costs a request, so link straight to the final URL, including the right trailing-slash form (HTTP→HTTPS then slash is a typical chain). *Official.*[^wd-html]
- New URLs: self-canonical, updated hreflang, temporary noindex removed; submit the new sitemap (redirect warnings on the old one can be ignored during the move).[^g-site-move]
- Change of Address in Search Console is for domain or subdomain moves only — not for HTTP→HTTPS, www or path changes.[^g-site-move]
- Expect "a few weeks or more" for a medium site until the new URLs show; larger sites take longer.[^g-site-move]
- Add, from [how Google ranks](../how-it-works/google-ranking.md) and [migration](../situations/migration.md): switch internal links and sitemaps on the same day as the redirects, and keep an unchanged control set to measure against.

## 4. Product variants
- "The site must have the ability to preselect each variant directly with a distinct URL (using URL query parameters)" — preselection means the right image, price, availability and add-to-cart.[^g-variants]
- **One page for all variants:** "only one distinct canonical URL for the overall ProductGroup", usually the base URL. **One page per variant:** no group canonical, no `ProductGroup.url`, and "full and self-contained markup" on each page.[^g-variants]
- Markup: `ProductGroup` with `hasVariant` (or variants with `isVariantOf`), `variesBy` (color, size, suggestedAge, suggestedGender, material, pattern), matching `productGroupID` / `inProductGroupWithID`; "Each variant must have a unique ID".[^g-variants] Keep the variant structure consistent with the feed's item groups ([feeds](../channels/feeds-and-merchant-center.md#1-feed-audit-checklist)).

## 5. Pagination and infinite scroll
- Link each page to the next with `<a href>` and link back to page 1; each page gets its own URL (`?page=n`) — "Google ignores fragment identifiers".[^g-pagination]
- Don't canonicalise page 2+ to page 1; each page is self-canonical. `rel=prev/next` is no longer used.[^g-pagination]
- "Google's crawlers don't 'click' buttons": load-more buttons and infinite scroll need crawlable paginated links, a sitemap or a Merchant Center feed behind them.[^g-pagination]
- Sort and filter variants of a list: noindex or robots.txt, "to avoid indexing variations of the same list of results".[^g-pagination]

## 6. Crawl budget
- It matters for sites with roughly "1 million+ unique pages" changing weekly, "10,000+ unique pages" changing daily, or many "Discovered – currently not indexed" URLs — "These are not exact thresholds."[^g-crawl-budget]
- Block crawling with robots.txt, not noindex; don't use robots.txt to "temporarily reallocate crawl budget".[^g-crawl-budget]
- Removed pages return 404 or 410 — a 404 is "a strong signal not to crawl that URL again". Fix soft 404s, avoid redirect chains, keep `<lastmod>` in sitemaps.[^g-crawl-budget]
- Server errors (5xx) and rate limiting (429) lower the crawl limit: "Google crawls less".[^g-crawl-budget]

## 7. JavaScript
- Crawl, render, index: "Googlebot queues all pages with a 200 HTTP status code for rendering"; JavaScript from blocked files isn't rendered.[^g-js]
- "Google can only discover your links if they are `<a>` HTML elements with an href attribute." Route with the History API, not fragments.[^g-js]
- Single-page apps must return real status codes; to avoid soft 404s, redirect to a real 404 URL or add noindex. A noindex in the original HTML may stop rendering, so never remove one with JavaScript. Set the canonical in HTML; a canonical set by script must match it.[^g-js]
- Server-side rendering or prerendering is "still a great idea" — "not all bots can run JavaScript". AI assistant fetchers can't at all ([how AI assistants retrieve](../how-it-works/ai-assistants.md)).[^g-js]

## 8. Structured data policies
- JSON-LD is recommended; don't block markup pages with robots.txt or noindex.[^g-sd-policies]
- "Your structured data must be a true representation of the page content"; don't mark up content that isn't visible; put markup on the page it describes; use the most specific type.[^g-sd-policies]
- "Items that are missing required properties are not eligible for rich results." Image URLs in markup "must be crawlable and indexable".[^g-sd-policies]
- Deceptive markup (e.g. fake reviews) can bring a manual action that removes rich-result eligibility; it doesn't affect web ranking. Passing the Rich Results Test doesn't guarantee a rich result.[^g-sd-policies]
- For AI assistants, markup isn't read on live fetches — the same facts must be visible text ([how AI assistants retrieve](../how-it-works/ai-assistants.md)).

## 9. Core Web Vitals
| Metric | Good | Needs improvement | Poor |
|---|---|---|---|
| LCP (loading) | ≤ 2.5 s | ≤ 4 s | > 4 s |
| INP (responsiveness) | ≤ 200 ms | ≤ 500 ms | > 500 ms |
| CLS (layout stability) | ≤ 0.1 | ≤ 0.25 | > 0.25 |

Measured at "the 75th percentile of page loads, segmented across mobile and desktop". Search Console uses the last 28 days, and a URL group's status "defaults to the slowest status assigned to it for that device type".[^g-cwv][^dbb-psi] For AI crawlers, timeouts matter more than these scores ([page reliability](../how-it-works/ai-assistants.md)). Caching headers, fonts and navigation that move these numbers: [performance and caching](performance-and-caching.md).

## 10. International and hreflang
- HTML link elements, HTTP headers or the sitemap: "The three methods are equivalent".[^g-hreflang]
- Each version lists "itself as well as all other language versions"; "If two pages don't both point to each other, the tags will be ignored." Use fully qualified URLs.[^g-hreflang]
- "Only language codes listed in ISO 639-1 and region codes listed in ISO 3166-1 Alpha 2 are supported"; "You can't specify the country code by itself."[^g-hreflang]
- `x-default` "is used when no other language/region matches the user's browser setting".[^g-hreflang]
- "Google doesn't use hreflang or the HTML lang attribute to detect the language of a page" — the visible content decides.[^g-hreflang]

## 11. Links and spam policies
- "Link spam is the practice of creating links to or from a site primarily for the purpose of manipulating search rankings" — buying or selling links for ranking, "excessive link exchanges", automated link creation.[^g-spam]
- Paid links are fine "as long as they are qualified with a rel="nofollow" or rel="sponsored"".[^g-spam]
- The same policy page defines **scaled content abuse** ("many pages are generated for the primary purpose of manipulating search rankings"), **site reputation abuse** and **expired domain abuse** — relevant to programmatic pages and to AI-written content at scale.[^g-spam] Spam update dates are in the [timeline](../reference/google-updates-timeline.md).

## 12. Rendering checks in URL Inspection
*Practitioner, tool observation.*[^nz-render]
- The live-test screenshot is cut at about 1,750 px; the stored rendered HTML keeps the first 100,000 nodes.
- Googlebot doesn't scroll: lazy-loaded images below the viewport and images lazy-loaded by script fail to load. Shadow DOM is flattened into the rendered HTML.
- **Do:** on long category pages, check that the product grid below the fold and its links exist in the rendered HTML, not only in the screenshot; use native lazy loading or server-rendered markup for product tiles ([JavaScript](#7-javascript), [internal linking](internal-linking.md)).

## 13. Removed pages: 404, 410 or 301
*Practitioner, consistent with Google's docs ([crawl budget](#6-crawl-budget)).*[^bc-404]
- **410** for content removed deliberately with no replacement.
- **301** only when a relevant replacement exists (a successor product, the parent category).
- "Avoid redirecting all 404s to the homepage." Retired products: [product pages](../page-types/product-pages.md); during a move: [migration](../situations/migration.md).

## 14. URL hierarchy mirrors the taxonomy
- A Google patent describes using the directory paths in URLs to train a classifier that assigns pages to hierarchical categories. *Patent; current use unknown.*[^sbs-urlcategories]
- **Do:** let category URLs mirror the category taxonomy (`/parent/child/`), and avoid flat or ID-only paths for category pages. Don't restructure live URLs for this alone — a URL change is a migration ([site moves](#3-site-moves-and-url-renames)). The linking side of the same hierarchy: [internal linking](internal-linking.md). *Inference.*

## 15. Hosting and server location
- "With regards to SEO, the server's location is not used for geotargeting" (Mueller, relayed). *Official statement, relayed.*[^bc-servers] Geotargeting comes from [hreflang](#10-international-and-hreflang) and content.
- Speed still pays: a Deloitte study ("Milliseconds Make Millions") found a 0.1 s mobile speed gain went with ≈ 10 % more retail spend. *Measured, relayed.*[^bc-servers]
- A CDN doesn't directly boost rankings; it lowers TTFB and LCP, keeps the site up under traffic spikes and makes crawling cheaper. *Practitioner, vendor data.*[^dbb-cdn-seo] Caching HTML at the edge: [performance and caching](performance-and-caching.md#3-cdn-notes).
- **Do:** don't move hosting for SEO when entering a new market ([new market](../situations/new-market.md)); use a CDN for latency.

## 16. Gemini reads the indexed copy
- When Gemini is asked to read a URL, unindexed pages come back as `URL_FETCH_STATUS_NOT_IN_SEARCH_INDEX` or `URL_FETCH_STATUS_EMPTY_CONTENTS_IN_INDEX`: the indexed copy counts, and live-test tools don't show what Gemini sees. *Measured, probing, 2 URLs.*[^dj-notlive]
- **Do:** confirm a page is indexed (and re-crawled after a change) before expecting the change in Gemini or AI Mode ([Search Console](../measure/search-console.md), [Google AI features](../how-it-works/google-ai-features.md)).

## 17. Chrome-side AI: chunking, ad metrics, Decisions API
Watch only; none of these is a ranking rule.
- **DocumentChunker.** Chrome splits pages greedily into passages of ≤ 200 words (minimum 5 words, cap 1,024 characters); `nav` and `footer` act as boundaries but aren't removed; History Embeddings keeps the first 30 passages per page. *From code (Chromium).*[^nz-lens] The analyst's own advice: don't restructure pages for this — every system chunks differently.
- **CrUX ad metrics.** Experimental ad metrics in CrUX since 2026-09-15, with no thresholds; the Better Ads limits are 30 % ad density on mobile and 50 % on desktop. Per Google's docs, page-experience aspects other than Core Web Vitals don't directly help rankings. *Practitioner, minor.*[^nz-adcrux]
- **Decisions API (DecisionModel).** Behind `chrome://flags#decisions-api`, desktop only: 1–16 questions, 2–26 options, EmbeddingGemma at temperature 0.05; uncalibrated; ~9.6 s for 8 questions on CPU. *From code, n=10 test questions.*[^dj-decision] Agent-facing browser features (WebMCP) are in [AI crawlers and controls](ai-crawlers-and-controls.md).

## 18. Google-selected canonicals carry over to AI answers
*Practitioner, 3 client cases; the carry-over to ChatGPT is his inference from matching citations.*[^gg-canonical]
- `rel="canonical"` is a hint ([section 2](#2-canonicals-and-duplicates)). In one case Google chose weaker secondary pages as canonical on "tens of thousands" of URLs, and the URLs Google selected were the ones ChatGPT cited.
- The canonical tag alone didn't fix it; adding noindex to the near-duplicate pages that exist only for on-site users did. This is not canonicalising with noindex (which Google advises against in [section 2](#2-canonicals-and-duplicates)): the pages were taken out of search because they had no search purpose.
- **Do:** monitor the Google-selected canonical per page type in URL Inspection or the Page indexing report ([Search Console](../measure/search-console.md)); noindex near-duplicates that serve only on-site users (internal print views, session or comparison states); add every subdomain as its own property in Search Console so a stray one is visible. *Practitioner.*

## 19. The Removals tool hides, it doesn't deindex
*Practitioner, one case.*[^gg-canonical]
- The Removals tool hid a public login subdomain from results in ~8–10 hours, but the block is temporary and doesn't deindex the URLs.
- **Do:** pair it with a lasting fix — 404 or 410, noindex, or authentication. A robots.txt disallow is not a fix: blocked URLs can stay indexed without content ([section 2](#2-canonicals-and-duplicates)).

## 20. PDFs: deindexing from August 2026
*Practitioner observation across client sites.*[^gg-pdf]
- Google deindexed PDFs at scale from ~25 August 2026; they showed as "Crawled – currently not indexed", and some were reindexed later.
- The URL Inspection API allows 2,000 URLs per property per day, counted separately per property — adding directory properties multiplies the quota for checking large PDF sets.
- **Do:** convert PDFs that drive traffic (spec sheets, size guides, manuals) into HTML pages and link the PDF from them; check PDF index status with the URL Inspection API across directory properties ([daily index status](../measure/diagnostic-tests.md#17-daily-index-status-per-url)). *Practitioner.*

## 21. Viewport, CSS and rendering differences
- **Bots don't scroll or click.** Google expands the viewport height once to trigger lazy loading; lazy load with Intersection Observer, not on scroll events. *Practitioner (Giacomo Zecchini, relayed).*[^lr-techseo] Consistent with [section 12](#12-rendering-checks-in-url-inspection).
- **How tall is the viewport?** Google renders mobile pages with a very tall viewport; Mueller suggested ~9,000 px in 2017 (old, unconfirmed). A 2026 observation found the URL Inspection screenshot cut at ~1,750 px with no scrolling ([section 12](#12-rendering-checks-in-url-inspection)). *Relayed official statement, dated; Practitioner observation.*[^ja-cloak][^nz-render]
  > **Not a conflict:** the two numbers measure different things — the ~9,000 px is the height Google renders at, the ~1,750 px is how much of it the screenshot shows. So a short screenshot doesn't mean content below it went unrendered: check the rendered HTML, not the screenshot, and keep key content and links early in the HTML.
- **Unintended human/Google differences.** Text in CSS `::before`/`::after` isn't in the DOM and isn't indexed; `@media (min-height: …)` rules that change content, and `<picture>` sources showing different subjects, make the tall-viewport render differ from what people see. Google judges cloaking by intent, but the result can still mislead. *Practitioner, with Google docs and relayed talks.*[^ja-cloak][^lr-techseo]
- Use `visibility: hidden` rather than `display: none` for content that must keep its dimensions; cap `vh`-based hero sections with `max-height`, or the tall viewport stretches them over the content. *Practitioner (Zecchini, relayed).*[^lr-techseo]
- **No 5-second render limit.** A July 2026 test (Dave Smart, relayed) found the "5-second limit" is a myth: the Web Rendering Service can pause its virtual JavaScript clock while waiting on the network. Still server-render links, canonicals and key content ([section 7](#7-javascript)) — AI fetchers don't render at all. *Practitioner test, relayed.*[^ja-cloak]
- **Do:** never put prices, stock, labels or other indexable text in CSS pseudo-content; make every `<picture>` variant show the same subject; avoid height-based media queries that change content; cap hero heights.

## 22. Signal drift: one record for every output
*Practitioner, worked examples.*[^ja-brain]
- Outputs that are generated on different schedules contradict each other: a page noindexed at 09:00 stays in a sitemap regenerated at midnight, giving ~15 hours of conflicting signals. The same happens to hreflang siblings, canonicals, schema availability and feeds. Valid-but-wrong output passes every validator.
- **Do:** derive sitemaps, hreflang, canonicals, structured-data availability and the feed from one product record and update them on events (publish, noindex, sell-out), not on a nightly job ([feeds](../channels/feeds-and-merchant-center.md)); test outputs against the intended state, not only for validity; before replatforming, trace a few ordinary edits and list every output that reacts ([migration](../situations/migration.md)).

## 23. Semantic landmarks
*Practitioner.*[^gn-html]
- LLM fetchers other than Gemini don't render JavaScript ([section 7](#7-javascript)), so the HTML structure is what they parse: one `<h1>` at the start of the main content, `<article>` around headline and body, `<aside>` for sidebars and recommendations, real `<p>`, lists and `<a href>` links.
- **Do:** wrap the main content of product, category and guide templates in `<main>` (and `<article>` where it is one piece of content); put cross-sell, "customers also bought" and recommendation blocks in `<aside>`, so parsers can separate the page's own content from the rest. *Practitioner; transfer from editorial to shop templates is inference.*

## 24. HTML size limits
*Measured and relayed by DebugBear, a vendor that sells performance monitoring.*
- Google's Googlebot docs now list a 2 MB limit on uncompressed HTML (previously 15 MB; changed around February 2026 without an announcement). Each subresource is fetched separately under the same limit; PDFs are excepted. *Official (Google docs), relayed.*[^dbb-2mb]
- Few pages come near it: median uncompressed HTML is ~20 KB, the 90th percentile ~392 KB. Bing has a 1 MB soft limit ("HTML size is too long" in Bing Webmaster Tools), and Bing problems also reach DuckDuckGo. *Measured, relayed (Dave Smart analysis).*[^dbb-2mb]

> **Conflict:** Google's documentation and a forum report (truncation at ~1.9 MB) point to a hard 2 MB cut-off, but the author's own URL Inspection live tests did not truncate pages above 2 MB; enforcement is unclear. — [details](../reference/conflicts.md#is-the-2-mb-html-limit-enforced)

- **Do:** keep category and product HTML well under 1 MB uncompressed (for Bing); move base64-inlined images and fonts and large inline JSON state into separate files; check the largest templates (long category pages, product pages with many variants) in Bing Webmaster Tools. *Practitioner; thresholds from the sources, template choice inference.*[^dbb-2mb]

Related: [migration](../situations/migration.md), [AI crawlers and controls](ai-crawlers-and-controls.md), [performance and caching](performance-and-caching.md), [Search Console](../measure/search-console.md), [diagnostic tests](../measure/diagnostic-tests.md), [category pages](../page-types/category-pages.md).

[^learningseo]: LearningSEO.io, read 2026-10-27: section map used as a gap checklist; its migration, pagination and ecommerce sections link practitioner guides, so the Google docs were read directly.
[^g-facets]: Google, faceted navigation, read 2026-10-27.
[^g-canonical]: Google, canonical URLs, read 2026-10-27.
[^g-site-move]: Google, site moves with URL changes, read 2026-10-27.
[^g-variants]: Google, product variant structured data, read 2026-10-27 (Merchant Center `item_group_id` not covered on that page).
[^g-pagination]: Google, pagination and incremental loading, read 2026-10-27.
[^g-crawl-budget]: Google, crawl budget guide, read 2026-10-27.
[^g-js]: Google, JavaScript SEO basics, read 2026-10-27.
[^g-sd-policies]: Google, general structured data guidelines, read 2026-10-27.
[^g-cwv]: web.dev Web Vitals and Search Console help, read 2026-10-27.
[^g-hreflang]: Google, localized versions, read 2026-10-27; nothing explicit on IP-based redirects in the extracted text.
[^g-spam]: Google, spam policies, read 2026-10-27.
[^nz-render]: Natzir Turrado, 2026-09-30: URL Inspection observations — screenshot cut at ~1,750 px, rendered HTML capped at the first 100,000 nodes, no scrolling (below-viewport and script-lazy images fail), Shadow DOM flattened. Tool observation, not a Google statement.
[^bc-404]: Bruce Clay, 2026-06-16: 410 for deliberately removed content, 301 only with a relevant replacement, "avoid redirecting all 404s to the homepage". Agency blog, no first-party data.
[^sbs-urlcategories]: SEO by the Sea (Bill Slawski), 2013-07-12: patent US 8,484,194 (filed 2012-01-13), training taxonomic page classification from URL directory paths. Patent analysis; blog inactive since 2022.
[^bc-servers]: Bruce Clay, 2026-06-30: Mueller quote on server location and geotargeting; Deloitte "Milliseconds Make Millions" (0.1 s mobile speed gain ≈ 10 % more retail spend). Agency blog relaying both; no first-party data.
[^dj-notlive]: DEJAN, 2026-05-07: probing Gemini URL access with 2 URLs; status codes `URL_FETCH_STATUS_NOT_IN_SEARCH_INDEX`, `URL_FETCH_STATUS_EMPTY_CONTENTS_IN_INDEX`.
[^nz-lens]: Natzir Turrado, 2026-08-06: Chromium DocumentChunker source (≤ 200 words, min 5 words, 1,024-character cap, nav/footer boundaries, first 30 passages in History Embeddings).
[^nz-adcrux]: Natzir Turrado, 2026-10-05: CrUX experimental ad metrics since 2026-09-15, no thresholds; Better Ads density limits; Google docs on page experience beyond CWV.
[^dj-decision]: DEJAN, 2026-10-08: Chromium source and 10 test questions; flag, limits, model, temperature, CPU timing.
[^gg-canonical]: Glenn Gabe (GSQi), 2026-02-17: 3 client cases; Google-selected canonicals on "tens of thousands" of URLs, matching ChatGPT citations (cascade is his inference); noindex on on-site-only pages fixed it where the canonical didn't; Removals tool hid a public login subdomain in ~8–10 hours without deindexing; list every subdomain in Search Console.
[^gg-pdf]: Glenn Gabe (GSQi), 2026-09-16: PDFs deindexed at scale from ~25 August 2026 ("Crawled – currently not indexed"), some reindexed; URL Inspection API quota 2,000 URLs per property per day, separate per property. Client observations, no aggregate count.
[^lr-techseo]: Lily Ray, 2025-12-05, her summary of Tech SEO Connect 2025; these items are Giacomo Zecchini's talk (viewport expansion, Intersection Observer, CSS pseudo-content not indexed, `visibility` vs `display`, `max-height` on `vh` heroes). Not checked against the slides.
[^ja-cloak]: Jono Alderson, 2026-10-26: argument on unintended cloaking (tall viewport, `min-height` media queries, `<picture>` sources, CSS content; Google judges by intent); relays Mueller 2017 (~9,000 px, unconfirmed) and Dave Smart's July 2026 test (no 5-second render limit; WRS pauses its virtual clock).
[^ja-brain]: Jono Alderson, 2026-10-04: worked examples of signal drift (noindex at 09:00 vs midnight sitemap, ~15 h), one record for hreflang, canonicals, availability and feeds; event-driven updates; trace edits before replatforming. No measurements.
[^gn-html]: Barry Adams, 2025-08-06: semantic HTML for search and LLM parsers (one `<h1>`, `<article>`, `<aside>`, real paragraphs, lists, links; non-Gemini fetchers don't render JS). Publisher-focused practitioner advice.
[^wd-html]: web.dev, 2023-11-01: avoid redirects and chains (HTTP→HTTPS then trailing slash), link to final URLs; each redirect adds a request. Guidance.
[^dbb-2mb]: DebugBear, 2026-02-16: Googlebot docs list 2 MB uncompressed HTML (was 15 MB, changed ~Feb 2026), subresources separate, PDFs excepted; forum report of truncation at ~1.9 MB vs the author's URL Inspection tests without truncation; relays Dave Smart (median ~20 KB, p90 ~392 KB); Bing 1 MB soft limit, also affects DuckDuckGo. Vendor blog.
[^dbb-cdn-seo]: DebugBear, 2026-05-04: a CDN improves TTFB/LCP, reliability and crawl efficiency, no direct ranking boost. Explainer, no before/after data.
[^dbb-psi]: DebugBear, 2025-03-09 (upd. 2026-10-08): confirms the thresholds and 28-day p75 CrUX window; field data can take 28 days to reflect a fix. Explainer, vendor.
