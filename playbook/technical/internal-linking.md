---
type: Guide
title: Internal linking
description: Internal links that crawlers and AI bots can see — links in the initial HTML, forward navigation on category pages, contextual links for new pages, a lean global navigation, related links generated from taxonomy and purchase data, click depth and orphan pages, anchor text and redirected link targets, physical and virtual silos without stripping relevant cross-links, linking to pages that satisfy, split-testing footer category links, finding link opportunities with embeddings, linking key category and product pages within two clicks of pages that AI assistants cite, automating link suggestions with embeddings, Search Console data and LLM anchors under human approval, and redirect mapping by fuzzy matching.
tags: [seo, geo, internal-links, navigation, category-pages, orphan-pages, crawl-depth, javascript, anchor-text, siloing, breadcrumbs, footer, embeddings, llm, fuzzy-matching, redirects, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: bp-rendered-links
    resource: "https://botpresso.com/python-script-to-find-inlinks-missing-from-rendered-html/"
    title: "Botpresso, Inlinks missing from rendered HTML (≈2023)"
  - id: ah-navigation
    resource: "https://ahrefs.com/blog/website-navigation/"
    title: "Ahrefs, Website navigation (2023-02-08; one jewelry ecommerce case)"
  - id: ah-onpage
    resource: "https://ahrefs.com/blog/on-page-seo-checklist/"
    title: "Ahrefs, On-page SEO checklist (updated 2026-03-05)"
  - id: bp-graph-linking
    resource: "https://botpresso.com/graph-theory-based-internal-linking-50-to-1-orphan-pages/"
    title: "Botpresso, Graph-based internal linking: orphan pages 50 % → 1 % (≈2022; one travel site, self-reported)"
  - id: ah-overopt
    resource: "https://ahrefs.com/blog/over-optimization/"
    title: "Ahrefs, Over-optimization (updated 2024-03-28)"
  - id: bc-silo
    resource: "https://www.bruceclay.com/blog/8-common-mistakes-in-seo-silo-implementation/"
    title: "Bruce Clay, 8 common mistakes in SEO silo implementation (2026-06-02; practitioner method)"
  - id: bc-virtual-silo
    resource: "https://www.bruceclay.com/blog/internal-linking-strategies-for-seo-siloing-virtual-siloing/"
    title: "Bruce Clay, Internal linking strategies: virtual siloing (2026-05-26; method)"
  - id: sbs-reachability
    resource: "https://www.seobythesea.com/2012/11/google-reachability-scores/"
    title: "SEO by the Sea, Google reachability scores (2012-11-07; patent US 8,307,005, filed 2010-06-30)"
  - id: sbs-urlcategories
    resource: "https://www.seobythesea.com/2013/07/google-classify-pages-hierarchical-categories-urls/"
    title: "SEO by the Sea, Classifying pages using hierarchical categories in URLs (2013-07-12; patent US 8,484,194, filed 2012-01-13)"
  - id: mt-gptbot
    resource: "https://metehan.ai/blog/i-built-a-60-000-page-ai-website-for-10-gptbot-crawled-it-30-000-times-in-12-hours/"
    title: "Metehan Yeşilyurt, A 60,000-page site crawled 30,000 times by GPTBot (2026-03-04; server logs, one site)"
  - id: ls-links
    resource: "https://lazarinastoy.com/how-to-incorporate-machine-learning-in-internal-linking-audits/"
    title: "Lazarina Stoy, ML in internal linking audits (2026-10-25; relays SearchPilot, InLinks)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: mlseo-internal-linking
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/internal-link-analysis/automate-internal-linking-ai/"
    title: "MLforSEO (Lazarina Stoy), 10 Ways to Automate Internal Linking with AI (2026-10-22; one 68–79-post blog, 12-suggestion LLM test, synthetic DiD demo)"
  - id: mlseo-migration
    resource: "https://www.mlforseo.com/machine-learning-tutorials/fuzzy-matching/seo-site-migration-checklist/"
    title: "MLforSEO (Lazarina Stoy), The SEO Site Migration Checklist I Use (2026-10-24; procedure)"
  - id: mlseo-404-fuzzy
    resource: "https://www.mlforseo.com/machine-learning-tutorials/fuzzy-matching/404-and-redirect-mapping-with-fuzzy-matching-in-google-colab-python/"
    title: "MLforSEO (Lazarina Stoy), 404 and Redirect Mapping with Fuzzy Matching (2025-08-09; method, no benchmarks)"
---

# Internal linking

How to link an ecommerce site internally so that Google and AI crawlers find every page that matters, and which links carry weight. Confidence labels follow the [scale](../reference/sources-and-confidence.md). Rules for which filter URLs should be linkable at all are in [faceted navigation](technical-foundations.md#1-faceted-navigation).

## Rules
- **Every link that matters must be an `<a href>` in the initial HTML**; diff view-source against the rendered HTML per template. *Practitioner; AI-bot discovery measured* — [evidence](#1-links-in-html-not-after-javascript)
- **Every category template renders links to its subcategories in the HTML**, visible on the page, not only inside JavaScript filters. *Practitioner, one case, dated 2023* — [evidence](#2-category-pages-need-forward-navigation)
- **Give each new page 3+ contextual links from existing pages that already mention its topic.** *Practitioner* — [evidence](#3-contextual-links-for-new-pages)
- **Put only commercially important pages in the global navigation.** *Practitioner* — [evidence](#4-global-navigation)
- **Generate related-product and related-category links from taxonomy and "bought together" data**, not by hand. *Practitioner* — [evidence](#5-automated-related-links)
- **Keep important pages within a few clicks and fix orphans**; give high-demand pages more internal links. *Practitioner, one site, self-reported, dated 2022* — [evidence](#6-depth-and-orphan-pages)
- **Use descriptive, varied anchors and link straight to the final URL**, not through redirects. *Practitioner* — [evidence](#7-anchor-text-and-link-targets)
- **Mirror the category hierarchy in navigation, URLs and breadcrumbs, but keep relevant cross-category links** — there is no evidence for "pure" silos. *Practitioner, no data; Patent (URLs)* — [evidence](#8-silos-mirror-the-taxonomy-keep-relevant-cross-links), [virtual silos](#9-virtual-silos)
- **From category and guide pages, link to products and subcategories that satisfy; prune links to dead-end, out-of-stock or thin pages.** *Patent* — [evidence](#10-link-to-pages-that-satisfy)
- **Split-test footer category links before rolling them out, and find in-text link targets with passage embeddings and Search Console striking-distance queries**, a human approving each link and a control group measuring it. *Measured, one relayed SEO split test; Practitioner* — [evidence](#11-footer-links-and-link-opportunities), [automation](#13-automating-link-suggestions)
- **Link key category and product pages within two clicks of the pages AI assistants already cite.** *Practitioner, low confidence* — [evidence](#12-link-key-pages-close-to-cited-pages)

## 1. Links in HTML, not after JavaScript
- Compare the internal links in view-source (raw HTML) with those in the rendered HTML (URL Inspection or the Rich Results Test). Links that exist only after rendering are invisible to AI bots and some crawlers. *Practitioner, dated 2023.*[^bp-rendered-links]
- **AI crawlers discover by links.** GPTBot followed internal links and never fetched sitemap-only URLs ([AI assistants](../how-it-works/ai-assistants.md#3-discovery-and-caching-openai)). A sitemap entry is not a substitute for a link. *Measured, linked page.*

  > **Conflict:** another one-site log study saw GPTBot find a brand-new site through its XML sitemap within minutes, with no links pointing to it[^mt-gptbot] — [details](../reference/conflicts.md#do-ai-crawlers-use-sitemaps). Keep the links either way.
- Google's own rules for links and JavaScript rendering: [technical foundations](technical-foundations.md#7-javascript).

## 2. Category pages need forward navigation
- On one jewelry ecommerce site, JavaScript filtering hid the subcategory links on category pages. A visible forward-navigation block to subcategories, rendered in HTML, went live by December 2021, and gains followed by March 2022; no figures were published. *Practitioner, one case.*[^ah-navigation]
- **Do:** every category template renders its subcategory links as plain `<a href>` in the HTML, above or beside the product grid.[^ah-navigation][^ah-onpage] What else a category page needs: [category pages](../page-types/category-pages.md).
- Filters that should rank get crawlable links; all others stay unlinked or blocked ([faceted navigation](technical-foundations.md#1-faceted-navigation)).

## 3. Contextual links for new pages
- Link a new page from existing pages that already mention its topic in their text: find them by site search or a crawl for the exact phrase, and link that phrase.[^ah-onpage]
- **Do:** each new page gets at least 3 contextual links on the day it goes live. *Practitioner.*[^ah-onpage]
- New URLs start from their section's quality average in Google's scoring, so where you link a page from also places it ([Google ranking](../how-it-works/google-ranking.md#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)). *From the leak; the linking consequence is inference.*

## 4. Global navigation
- Only commercially important pages belong in the global navigation; every item there is linked from every page and dilutes the rest.[^ah-navigation] *Practitioner.*
- Main categories and the top-selling subcategories go in the menu; guides and long-tail pages get contextual links instead. *Inference.*

## 5. Automated related links
- Generate related-product and related-category links from the taxonomy and from "bought together" data, so links follow what customers actually combine and stay current as the range changes.[^ah-onpage] *Practitioner.*
- These blocks must also be in the initial HTML ([section 1](#1-links-in-html-not-after-javascript)).

## 6. Depth and orphan pages
- On one travel site (28 domains), graph-based internal linking cut orphan pages from 50 % to ~1 %. It targeted 90 % of pages within a click depth of 5 and gave high-demand pages more links. *Practitioner, self-reported, dated 2022.*[^bp-graph-linking]
- Working definitions from one practitioner: weak page = exactly one contextual inlink; deep = more than 4 clicks from the start page; orphan = a URL in the sitemap, Search Console or GA4 that the crawl didn't find. *Practitioner.*[^mlseo-internal-linking]
- **Do:** crawl regularly, compare crawled URLs with sitemap and Search Console URLs to find orphans, and check click depth for revenue pages. Pages predicted low quality are crawled less and lose anchors ([Google ranking](../how-it-works/google-ranking.md#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)).

## 7. Anchor text and link targets
- Exact-match anchor patterns and keyword stuffing still risk manual actions; Ahrefs ranks #1 for "canonical tagging" without the phrase on the page. Use descriptive anchors that vary naturally. *Practitioner.*[^ah-overopt]
- Redirect chains: fix at 5+ hops (Mueller); Google follows up to 10.[^ah-overopt] Point internal links at the final URL so no chain starts inside your own site; after a migration, switch internal links the same day ([migration](../situations/migration.md)).

## 8. Silos: mirror the taxonomy, keep relevant cross-links
- **Physical siloing** as one agency practises it: nest URLs by topic, one hub page per silo, most links inside the silo, subpages linking to the hub or to siblings, cross-silo links only when highly relevant, and the same hierarchy in navigation, URLs and breadcrumbs. *Practitioner method, no data.*[^bc-silo]
- A Google patent describes training page classification from URL directory paths, which supports URLs that mirror the taxonomy ([URL hierarchy](technical-foundations.md#14-url-hierarchy-mirrors-the-taxonomy)). *Patent.*[^sbs-urlcategories]
- **Do:** use the hierarchy for category URLs, navigation and breadcrumbs. **Don't** strip relevant cross-category links — accessories, companion products, the same product line in another category — to keep silos "pure": no source here shows a gain from that, and those links follow what customers buy together ([section 5](#5-automated-related-links), [keyword research](../channels/keyword-research.md)). *Inference.*

## 9. Virtual silos
- Where the URL structure can't change, build the silo with links: supporting pages link to the silo's landing page and back, with descriptive anchors that carry the target's primary term, placed in body copy or in a small sitemap-style link block. *Practitioner method.*[^bc-virtual-silo]
- On ecommerce, guides and comparisons are the supporting pages and the category is the landing page ([comparison and guides](../page-types/comparison-and-guides.md), [category pages](../page-types/category-pages.md)). Vary anchors ([section 7](#7-anchor-text-and-link-targets)). *Inference.*

## 10. Link to pages that satisfy
- A Google patent describes boosting or demoting a page by the aggregate engagement of the pages reachable from it within a few hops. *Patent; current use unknown.*[^sbs-reachability]
- **Do:** from category and guide pages, link to products and subcategories that satisfy visitors (in stock, well reviewed, complete); prune links to dead ends, out-of-stock items without a successor and thin pages (retired products: [product pages](../page-types/product-pages.md)). *Inference.*

## 11. Footer links and link opportunities
- **Footer test.** In a SearchPilot split test, growing a footer from 30 to 100+ category links gave ~+10 % organic traffic on desktop (95 % confidence) and +5 % on mobile (90 % confidence). SearchPilot itself warns against packing footers, so read it as one test, not a rule. *Measured, one SEO split test, relayed by a practitioner.*[^ls-links]
- **Unlinked mentions are common.** An InLinks analysis found 82 % of entity-mention link opportunities unlinked (5,112 projects). *Vendor data, relayed.*[^ls-links]
- **Similarity threshold.** Screaming Frog's semantic-similarity default of 0.95 is set for finding near-duplicates; lower it when you look for link opportunities, or you only find pages that say the same thing. *Practitioner.*[^ls-links][^mlseo-internal-linking]
- **Do:** split-test added footer category links on part of the templates before a full rollout; find in-text link targets by comparing passage embeddings with the target page, and have a human approve each link ([section 3](#3-contextual-links-for-new-pages), [section 7](#7-anchor-text-and-link-targets)). *Practitioner.*[^ls-links]

## 12. Link key pages close to cited pages
- A conference talk (Jori Ford, relayed) reported that AI retrieval bots rarely go more than ~3 pages deep from where they land. *Practitioner, low confidence, sample not given.*[^lr-techseo]
- **Do:** find the pages assistants already cite ([AI visibility tracking](../measure/ai-visibility-tracking.md)) and link your key category and product pages within two clicks of them, in the initial HTML ([section 1](#1-links-in-html-not-after-javascript)). *Inference from a low-confidence claim; cheap to do.*

## 13. Automating link suggestions
*From MLforSEO, a site that sells ML-for-SEO courses; one blog as the test bed.*
- **Embeddings.** Compare paragraphs, not whole pages, by cosine similarity; keep only unlinked pairs in the top 10 % of the site's own similarity distribution (not a fixed cutoff), drop pairs ≥ 0.95 (near-duplicates), and cap new links at 3 per source and per target per batch. A human approves every link before anything is written: "automate the finding, not the deciding". *Practitioner.*[^mlseo-internal-linking]
- **Search Console.** Take pages at average position 4–20 with ≥ 50 impressions for 2–7-word queries and link to them from pages that mention the query; check for cannibalisation first. On one blog, 242 striking-distance queries gave 110 suggestions. It misses the long tail, which Search Console omits. *Practitioner.*[^mlseo-internal-linking]
- **LLM anchors.** With guardrails (2–7 words, a verbatim span of the source text, confidence ≥ 0.5, one anchor used at most twice per target), Claude Opus 5.5 passed 7 of 12 suggestions (the author would publish 5 unchanged) for ~$0.05; Claude Haiku 4.5 passed 6, often broke the length rule, for ~$0.01. The guardrails check form, not meaning. *Measured, one case, small sample.*[^mlseo-internal-linking]
- **Measuring.** Compare test and control page groups with difference-in-differences, waiting about a week after the change. On synthetic data with a planted 15 % uplift the script reported +11.8 points, so it under-estimated the true effect. *Practitioner, synthetic validation.*[^mlseo-internal-linking]
- **Do:** generate suggestions from embeddings and Search Console, cap them per page, have a person approve each link and anchor, and roll out on a test group with a control group ([diagnostic tests](../measure/diagnostic-tests.md)). *Practitioner.*

## 14. Redirect mapping by fuzzy matching
*Same publisher; methods without accuracy benchmarks.*
- Map old to new URLs by fuzzy matching (Levenshtein via TheFuzz, RapidFuzz or PolyFuzz) on URL, title, H1, H2 and meta description, scored 0–100, and count how many algorithms agree. Flag matches below 70 for review; prioritise URLs with ≥ 100 clicks or ≥ 5 referring domains. In the author's example a 71-score partial still pointed to the wrong page, and a 38 led to a 410 rather than a homepage redirect. *Practitioner.*[^mlseo-migration]
- For 404s, thresholds depend on the data: 60–70 for inconsistent datasets, 85–90 for minor URL variations; labels Exact = 100, Partial = 50–< 100, No match = < 50; partials ≥ 70 can be pre-built as redirects but still need a manual check. No-code tools suffice below ~100–300 URLs, Python above ~1,000. No accuracy figures. *Practitioner.*[^mlseo-404-fuzzy]
- Each mapped redirect should go in one hop to a 200, and internal links should then point to the final URL ([section 7](#7-anchor-text-and-link-targets)); the full launch bar is in [migration](../situations/migration.md). *Practitioner.*[^mlseo-migration]

Related: [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md), [technical foundations](technical-foundations.md), [AI crawlers and controls](ai-crawlers-and-controls.md), [links and digital PR](../channels/links-and-digital-pr.md), [keyword research](../channels/keyword-research.md), [diagnostic tests](../measure/diagnostic-tests.md), [migration](../situations/migration.md), [ML methods for SEO](../measure/ml-methods-for-seo.md).

[^bp-rendered-links]: Botpresso, ≈2023: script diffing internal links in raw vs rendered HTML; claim that render-only links are missed by AI bots and some crawlers. Practitioner, no measured sample.
[^ah-navigation]: Ahrefs, 2023-02-08: one jewelry ecommerce case (JS filtering hid subcategory links; fix live by Dec 2021, gains by Mar 2022, no figures); global navigation only for commercially important pages.
[^ah-onpage]: Ahrefs, updated 2026-03-05: contextual links from exact in-text mentions; forward navigation; related links from taxonomy and purchase data.
[^bp-graph-linking]: Botpresso, ≈2022: one travel site, 28 domains, self-reported; orphan pages 50 % → ~1 %; 90 % of pages within depth 5.
[^ah-overopt]: Ahrefs, updated 2024-03-28: exact-match anchor risk; "canonical tagging" example; redirect chains (fix at 5+ hops per Mueller, Google follows up to 10).
[^bc-silo]: Bruce Clay, 2026-06-02: physical siloing method (nested URLs, hub per silo, links mostly inside, cross-silo only when highly relevant, matching navigation, URLs and breadcrumbs). Agency blog, no data.
[^bc-virtual-silo]: Bruce Clay, 2026-05-26: virtual siloing (supporting pages ↔ landing page, descriptive anchors with the target's primary term, in body copy or a mini sitemap block). Method, no data.
[^sbs-reachability]: SEO by the Sea (Bill Slawski), 2012-11-07: patent US 8,307,005 (filed 2010-06-30), reachability scores from engagement of pages reachable within N hops. Patent analysis; blog inactive since 2022.
[^sbs-urlcategories]: SEO by the Sea (Bill Slawski), 2013-07-12: patent US 8,484,194 (filed 2012-01-13), URL directory paths used to train taxonomic page classification.
[^mt-gptbot]: Metehan Yeşilyurt, 2026-03-04: server logs of one new 60,000-page site; GPTBot found it through the XML sitemap within minutes, no links. Author works at Peec AI.
[^ls-links]: Lazarina Stoy, 2026-10-25: relays a SearchPilot footer test (30 → 100+ category links: ~+10 % organic desktop at 95 % confidence, +5 % mobile at 90 %; SearchPilot warns against packing footers) and InLinks (82 % of entity-mention link opportunities unlinked, 5,112 projects, vendor); Screaming Frog semantic-similarity default 0.95; passage embeddings plus human approval. Primaries not read.
[^lr-techseo]: Lily Ray, 2025-12-05, her summary of Tech SEO Connect 2025; this item is Jori Ford's talk (retrieval bots rarely go more than ~3 pages deep). Sample and method not given.
[^mlseo-internal-linking]: MLforSEO (Lazarina Stoy), 2026-10-22: one 68–79-post blog — paragraph embeddings (top 10 % of the site's own distribution, skip ≥ 0.95, cap 3 per source/target), Search Console striking distance (position 4–20, ≥ 50 impressions, 2–7-word queries; 242 queries → 110 suggestions), LLM anchors with guardrails on 12 suggestions (Opus 5.5 7 passed, ~$0.05; Haiku 4.5 6 passed, ~$0.01), synthetic DiD (+11.8 points vs planted 15 %), weak/deep/orphan definitions, Screaming Frog 0.95 default. Course seller.
[^mlseo-migration]: MLforSEO (Lazarina Stoy), 2026-10-24: migration checklist — fuzzy redirect mapping on URL, title, H1, H2, meta description, 0–100 score, < 70 flagged, priority ≥ 100 clicks or ≥ 5 referring domains; one-hop 301/308 to a 200. Procedure, no benchmarks.
[^mlseo-404-fuzzy]: MLforSEO (Lazarina Stoy), 2025-08-09: 404-to-live-page fuzzy thresholds (60–70 / 85–90), Exact/Partial/No-match tiers, no-code vs Python by URL count. Method, no accuracy benchmark.
