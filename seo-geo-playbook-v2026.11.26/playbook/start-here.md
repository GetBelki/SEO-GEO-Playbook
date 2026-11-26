---
type: Guide
title: Start here
description: The playbook on one page — 51 rules for SEO, AI-search visibility and measurement, each with its confidence level and a link to the evidence, plus where to go next by task.
tags: [start-here, rules, seo, geo, measurement, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T11:50:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T11:56:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: playbook
    resource: "reference/sources-and-confidence.md"
    title: "Each rule condenses the linked page; the evidence and its sources are footnoted there"
---

# Start here

The playbook on one page, for an ecommerce site in any market. Each rule ends with its confidence level ([scale](reference/sources-and-confidence.md)) and links to the page with the evidence.[^playbook] Where sources disagree, the rule follows the [conflicts register](reference/conflicts.md).

## Pick your path
| You want to… | Go to |
|---|---|
| Fix or improve a page | [product pages](page-types/product-pages.md) · [category pages](page-types/category-pages.md) · [comparisons and guides](page-types/comparison-and-guides.md) · [homepage and brand](page-types/homepage-and-brand.md) |
| Handle a situation | [traffic drop](situations/traffic-drop.md) · [migration](situations/migration.md) · [new market](situations/new-market.md) · [seasonal peaks](situations/seasonal-peaks.md) · [core-update recovery](situations/core-update-recovery.md) · [scaling content and templates](situations/scaling-content-and-templates.md) |
| Understand how it works | [Google ranking](how-it-works/google-ranking.md) · [Google AI features](how-it-works/google-ai-features.md) · [AI assistants](how-it-works/ai-assistants.md) · [shopping surfaces](how-it-works/shopping-surfaces.md) |
| Work a channel | [Google Discover](channels/google-discover.md) · [keyword research](channels/keyword-research.md) · [feeds and Merchant Center](channels/feeds-and-merchant-center.md) · [third-party presence](channels/third-party-presence.md) · [links and digital PR](channels/links-and-digital-pr.md) · [local](channels/local.md) |
| Check the technical basics | [technical foundations](technical/technical-foundations.md) · [internal linking](technical/internal-linking.md) · [performance and caching](technical/performance-and-caching.md) · [titles and snippets](technical/titles-and-snippets.md) · [AI crawlers and controls](technical/ai-crawlers-and-controls.md) |
| Measure without fooling yourself | [Search Console](measure/search-console.md) · [analytics](measure/analytics.md) · [AI visibility tracking](measure/ai-visibility-tracking.md) · [rank tracking](measure/rank-tracking.md) · [diagnostic tests](measure/diagnostic-tests.md) · [ML methods for SEO](measure/ml-methods-for-seo.md) |

## Pages and content
1. **Open every product, category and guide page with one self-contained factual sentence** after the H1: what it is, key attributes, sizes, price from, availability. *Measured for ChatGPT and Gemini; good practice for Google.* → [AI assistants](how-it-works/ai-assistants.md)
2. **Put prices, specs and availability in visible, server-rendered HTML.** AI fetchers don't run JavaScript and don't read JSON-LD on live fetches. *Measured.* → [AI assistants](how-it-works/ai-assistants.md)
3. **Write one idea per passage under a descriptive heading — but don't write "for AI".** Google says AI search "is ... still SEO"; tuning text to embeddings is keyword stuffing. *Official.* → [conflict](reference/conflicts.md#writing-for-embeddings-and-chunking)
4. **Cover one topic per page, in depth.** Not thin pages, not catch-all guides. *Measured, mixed.* → [conflict](reference/conflicts.md#short-or-long-pages)
5. **Publish neutral comparison pages and buying guides for your category's main head-to-heads.** They're the most-cited page type for buying prompts; product pages and homepages rarely are. *Measured, vendor data.* → [comparisons and guides](page-types/comparison-and-guides.md)
6. **Answer each category's main buyer uncertainty on one focused page** (fit, compatibility, suitability, use). *Measured, directional.* → [category pages](page-types/category-pages.md)
7. **State verifiable proof points as text** — review score with count, years trading, assortment size — not only as badges. *Measured, correlational.* → [homepage and brand](page-types/homepage-and-brand.md)
8. **Keep seasonal URLs evergreen and give each branded question its own page** (discount codes, returns, student discount). *Practitioner.* → [seasonal peaks](situations/seasonal-peaks.md), [homepage and brand](page-types/homepage-and-brand.md)

## Google
9. **Treat quality as a section-level score.** Thin or bloated URL sets drag down the whole section, and new URLs start from the section's average. *From the leak.* → [Google ranking](how-it-works/google-ranking.md)
10. **Judge pages by whether searchers are satisfied, compared within their own page type and device.** *Trial and leak.* → [Google ranking](how-it-works/google-ranking.md), [test](measure/diagnostic-tests.md#2-satisfaction-per-page-type)
11. **Don't use top-10 rank as a proxy for AI presence.** Most AI Overview citations rank outside the top 10. *Measured, relayed.* → [Google AI features](how-it-works/google-ai-features.md)
12. **Follow Google's documented rules for facets, canonicals, variants, pagination and site moves** — robots.txt for facets, one canonical method, 301s kept a year. *Official.* → [technical foundations](technical/technical-foundations.md)
13. **Expect recovery from a core update to take months**, often until a later update; brands with clear identity and pages that fit intent and market won the 2026 updates. *Measured visibility, cases.* → [core-update recovery](situations/core-update-recovery.md)

## Shopping and agents
14. **Treat the product feed as the catalogue for AI shopping.** Fill material, size, colour and use in plain words; test titles in the feed only. *Measured and practitioner.* → [feeds and Merchant Center](channels/feeds-and-merchant-center.md)
15. **Fix Merchant Center before building other feeds.** ChatGPT's product carousels mostly mirror Google Shopping results. *Measured, relayed.* → [shopping surfaces](how-it-works/shopping-surfaces.md)
16. **Aim for the top of the AI shortlist** — most shoppers accept it as given and pick the first product. *Measured, usability study.* → [shopping surfaces](how-it-works/shopping-surfaces.md)
17. **Keep return, support and policy data in Merchant Center and make markup match the feed.** Agent checkout depends on it. *Practitioner, official announcement.* → [shopping surfaces](how-it-works/shopping-surfaces.md)

## Beyond your own site
18. **Most AI citations are third-party: audit and refresh your listings, marketplaces, reviews and affiliate placements.** *Measured.* → [third-party presence](channels/third-party-presence.md)
19. **Keep the same facts on your site and every local listing.** Local AI answers cite websites first and use listings to verify. *Measured, vendor data.* → [local](channels/local.md)
20. **Build per-market presence for new markets** — local marketplaces and natively written prompt sets, not just translation and hreflang. *Measured, directional.* → [new market](situations/new-market.md)

## Keywords, links and site structure
28. **Validate search volumes with Search Console impressions and value a topic by the traffic its top page gets**, not one keyword's volume; map one URL per intent. *Measured and practitioner, vendor data.* → [keyword research](channels/keyword-research.md)
29. **Render category-to-subcategory and related links as plain HTML links**, never only after JavaScript filtering. *Official and practitioner.* → [internal linking](technical/internal-linking.md)
30. **Write titles of about 50–60 characters with the main term first; write meta descriptions only for pages with traffic.** Google rewrites most of them anyway. *Measured, vendor data.* → [titles and snippets](technical/titles-and-snippets.md)
31. **Earn links with data, stockist pages and publishers that AI assistants cite; don't disavow "toxic" links a tool flags** — only for a manual action or a clear pattern of bought links. *Official statements and practitioner.* → [links and digital PR](channels/links-and-digital-pr.md)
32. **Don't add schema expecting AI citations.** Adding JSON-LD didn't raise them, and assistants don't read it on live fetches; keep it for rich results and in sync with the visible text. *Measured.* → [AI assistants](how-it-works/ai-assistants.md)
33. **Check monthly what the AI Overview says about your brand.** Most branded searches now show one, written largely from Wikipedia, YouTube and LinkedIn. *Measured, vendor data.* → [homepage and brand](page-types/homepage-and-brand.md)
34. **Scale programmatic or AI-assisted pages only where each page carries unique data and the template's indexation rate holds.** *Official policy plus measured correlation.* → [scaling content and templates](situations/scaling-content-and-templates.md)

## Grounding and AI answers
35. **Put the answer, specs and differentiators in the first ~500 words**, each in a self-contained sentence; Google's grounding takes a capped excerpt per page and favours the top. *Measured, private data.* → [comparisons and guides](page-types/comparison-and-guides.md)
36. **Give category and home pages body copy that answers their head queries, and a real meta description** — Gemini sometimes gets only the meta, and those pages were rarely cited. *Measured, small sample.* → [conflict](reference/conflicts.md#do-meta-descriptions-still-matter)
37. **Keep brand and product facts identical on your site, Wikidata, marketplaces and press.** Google merges facts only when they're corroborated across domains, and AI Mode receives Knowledge Graph facts without citations. *Patent, from code.* → [homepage and brand](page-types/homepage-and-brand.md)
38. **Invest in Reddit and forums only where they already rank in Google for your queries** — ChatGPT almost stopped citing Reddit in August 2026. *Measured, vendor data.* → [third-party presence](channels/third-party-presence.md)
39. **Re-baseline AI visibility at every model change and test page variants in both orders**: a model switch alone can flip which brands get named, and LLM judges favour whatever they read first. *Measured, small samples.* → [AI visibility tracking](measure/ai-visibility-tracking.md)

## Brand facts, rendering and measurement hygiene
40. **Keep a brand canon of checkable facts and track how AI answers it — accurate, wrong or no answer.** In one study AI declined a third of brand questions; wrong answers came from stale profiles. *Measured, one brand.* → [homepage and brand](page-types/homepage-and-brand.md)
41. **Track AI visibility from clean, unconnected accounts** — connected Gmail or Photos data roughly tripled how often seeded brands appeared in AI Mode. *Measured, small panel.* → [AI visibility tracking](measure/ai-visibility-tracking.md)
42. **Never put prices, stock or labels in CSS pseudo-content, and don't let height-based CSS change what Google renders.** *Official and practitioner.* → [technical foundations](technical/technical-foundations.md)
43. **Generate sitemaps, hreflang, canonicals and feed availability from one record**, so a change reaches every output at once. *Practitioner.* → [migration](situations/migration.md)
44. **When branded CTR drops but impressions and position hold, check the favicon and site name in the results first.** *One case.* → [traffic drop](situations/traffic-drop.md)
45. **Keep UTMs, click IDs and `_gl` intact from ad or AI link to purchase, and give AI sources their own channel group.** A link with `utm_source` but no `utm_medium` lands in Unassigned, and GA4's own AI Assistant channel is still partial. *Practitioner.* → [analytics](measure/analytics.md#12-ga4-attribution-leaks-utms-consent-and-cross-domain)
46. **Put the main product image in the server HTML with `fetchpriority="high"` and never lazy-load it; keep tracking parameters out of the cache key.** *Official; practitioner, vendor data.* → [performance and caching](technical/performance-and-caching.md#10-resource-hints-and-preload-pitfalls)
47. **Decide which keywords share a URL by SERP overlap, not embedding similarity.** *Measured, small sample.* → [conflict](reference/conflicts.md#embedding-clusters-or-serp-clusters)
48. **Read AI visibility as a brand channel and publish the margin of error:** one pass of ~500 answers is about ±5 points, and the order of names is noise. *Measured, vendor data.* → [AI visibility tracking](measure/ai-visibility-tracking.md#16-runs-phrasings-and-margin-of-error)
49. **Build redirect maps by fuzzy matching, check partial matches by hand, and send no-match URLs to 404 or 410, not the homepage.** *Practitioner.* → [migration](situations/migration.md#9-fuzzy-matched-redirect-maps)
50. **Count retrieved, cited and named separately:** assistants left half to three quarters of the pages they retrieved uncited. *Measured, vendor data, small sample.* → [AI visibility tracking](measure/ai-visibility-tracking.md#20-retrieved-cited-and-named-are-different-counts)
51. **Each month, pull AI Mode follow-ups from Search Console with a pronoun filter, and fix the pages they land on.** *Practitioner; official statement, relayed.* → [test](measure/diagnostic-tests.md#36-rebuild-ai-mode-conversations-from-pronoun-queries)

## Crawlers
21. **Decide AI crawler access per role:** allow search bots and user fetchers; training bots are a business decision. Check robots.txt daily against a written policy. *Official.* → [AI crawlers and controls](technical/ai-crawlers-and-controls.md)
22. **Make pages reliable for AI bots** — timeouts gate citations; watch AI-bot status codes in server logs. *Measured, correlational.* → [test](measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs)

## Measurement
23. **Before any comparison, list the measurement breaks between the two periods** — num=100, tracking bugs, untagged AI traffic, updates. *Measured.* → [Search Console](measure/search-console.md), [timeline](reference/google-updates-timeline.md)
24. **Report AI visibility per engine and separate citations, mentions, clicks and conversions.** Engines cite almost disjoint sources. *Measured.* → [AI visibility tracking](measure/ai-visibility-tracking.md)
25. **Assume AI traffic converts about like organic for ecommerce** until your data says otherwise. *Measured.* → [conflict](reference/conflicts.md#does-ai-traffic-convert-better)
26. **Run prompts enough times:** 3–5 runs to spot presence, 20 or more to measure a change. *Statistics.* → [conflict](reference/conflicts.md#how-many-prompt-runs)
27. **Split falling CTR into organic, paid and zero-click by query type** before blaming AI Overviews. *Measured, mixed.* → [traffic drop](situations/traffic-drop.md)

## How to use the playbook
- Every "Do" is a hypothesis for your site: test it with [diagnostic tests](measure/diagnostic-tests.md) before acting at scale.
- Pages carry a `stale_after` date; this field moves monthly.
- Terms are defined in the [glossary](reference/glossary.md); sources and their reliability in [sources and confidence](reference/sources-and-confidence.md).

[^playbook]: Rules condense the linked pages; numbers and sources are footnoted there.
