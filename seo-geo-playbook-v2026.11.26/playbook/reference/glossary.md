---
type: Reference
title: Glossary
description: Short definitions of the terms, systems and acronyms used across the playbook — Google systems from the leak and trial, AI-search surfaces, crawlers, feeds and measurement terms — each linked to the page that explains it.
tags: [glossary, reference, terms]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T11:50:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T11:56:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: playbook
    resource: "start-here.md"
    title: "Definitions summarise the playbook pages linked from each entry; evidence and sources are on those pages"
---

# Glossary

One-line definitions; follow the link for evidence and sources.[^playbook] Terms from the 2024 leak and the trial are real names of unknown current weight ([sources and confidence](sources-and-confidence.md)).

## Google systems
- **NavBoost** — Google's click memory per query and page (about 13 months, by country and device): long last clicks count as good, quick returns to the results as bad. → [Google ranking](../how-it-works/google-ranking.md)
- **Glue** — the click log used to decide results-page blocks (sitelinks, packs) and record clicks, hovers and time on the results page. → [Google ranking](../how-it-works/google-ranking.md)
- **RankEmbed** — a ranking model trained on about 70 days of search logs plus rater scores; FastSearch builds on its signals. → [Google ranking](../how-it-works/google-ranking.md)
- **NSR, sitechunk, siteFocusScore, siteRadius** — leaked quality scores at site and section level, and measures of how far a page sits from the site's main topic; new pages start from their section's average. → [Google ranking](../how-it-works/google-ranking.md)
- **Twiddler** — a re-ranking step after the main ranking, e.g. limiting results per host or favouring the official page for exact-name queries. → [Google ranking](../how-it-works/google-ranking.md)
- **QUS** — Google's query understanding: a score per query term per URL, with exact vs derived matching. → [Google ranking](../how-it-works/google-ranking.md)
- **Core update / spam update** — announced ranking changes with rollout dates on Google's Search Status Dashboard. → [timeline](google-updates-timeline.md)

## AI search surfaces
- **AI Overviews (AIO)** — the AI answer block on Google's normal results; few citations, little fan-out. → [Google AI features](../how-it-works/google-ai-features.md)
- **AI Mode** — Google's conversational search mode; many sub-queries per turn, many citations, low overlap with AI Overviews. → [Google AI features](../how-it-works/google-ai-features.md)
- **Fan-out** — an engine rewriting one question into many sub-queries and merging the results. → [Google AI features](../how-it-works/google-ai-features.md), [AI assistants](../how-it-works/ai-assistants.md)
- **Grounding** — retrieving web or index content to base an AI answer on; FastSearch is Google's grounding layer per trial documents. → [Google AI features](../how-it-works/google-ai-features.md)
- **Citation vs mention** — a citation lists your URL as a source; a mention names your brand in the answer. They barely correlate. → [third-party presence](../channels/third-party-presence.md)
- **GEO / AEO / LLMO** — names for optimising visibility in AI answers. Google's position: it "is ... still SEO". → [conflicts](conflicts.md#googles-guidance-vs-assistant-findings)
- **Shortlist** — the few products an AI answer recommends; most shoppers accept it as given. → [shopping surfaces](../how-it-works/shopping-surfaces.md)

## Crawlers and controls
- **Training bot vs search bot vs user fetcher** — separate AI crawler roles; blocking a training bot doesn't remove you from that vendor's answers, blocking the others does. → [AI crawlers and controls](../technical/ai-crawlers-and-controls.md)
- **Google-Extended** — robots.txt token limiting Gemini training and grounding outside Search; not an AI Overviews opt-out. → [AI crawlers and controls](../technical/ai-crawlers-and-controls.md)
- **llms.txt** — a proposed file summarising a site for LLMs; no engine is shown to use it, Google Search ignores it. → [sources and confidence](sources-and-confidence.md)
- **IndexNow** — a protocol that pushes changed URLs to Bing and other participating engines. → [AI crawlers and controls](../technical/ai-crawlers-and-controls.md)
- **nosnippet / data-nosnippet / max-snippet** — Google controls that also limit how content appears in AI features. → [AI crawlers and controls](../technical/ai-crawlers-and-controls.md)

## Shopping and feeds
- **Merchant Center** — Google's product data hub; its feed drives Shopping, product grids, AI Mode product units and agent checkout. → [feeds and Merchant Center](../channels/feeds-and-merchant-center.md)
- **Free listings / merchant listings** — unpaid product results in Google; removed in the EEA from September 2026. → [shopping surfaces](../how-it-works/shopping-surfaces.md)
- **UCP (Universal Commerce Protocol), AP2** — Google's protocols for agents to read catalogues and check out; UCP runs on Merchant Center. → [shopping surfaces](../how-it-works/shopping-surfaces.md)
- **CSS (Comparison Shopping Service)** — a third-party service listing products in Google Shopping in the EEA. → [shopping surfaces](../how-it-works/shopping-surfaces.md)
- **PDP / PLP** — product detail page / product listing (category) page. → [product pages](../page-types/product-pages.md), [category pages](../page-types/category-pages.md)

## Keywords, links and site structure
- **Search volume** — a tool's estimate of monthly searches for a keyword; often merged across variants and averaged over a year, so check it against Search Console impressions. → [keyword research](../channels/keyword-research.md)
- **Traffic potential** — the organic traffic the current top page for a topic gets across all its keywords; a better value estimate than one keyword's volume (an Ahrefs metric). → [keyword research](../channels/keyword-research.md)
- **Keyword cannibalisation** — two of your own pages competing for the same intent; fix with one URL per intent. → [keyword research](../channels/keyword-research.md)
- **Domain Rating (DR)** — Ahrefs' link-based authority score; not a Google factor and only weakly correlated with rankings. → [links and digital PR](../channels/links-and-digital-pr.md)
- **Disavow** — telling Google to ignore links to your site; only for a manual action or a clear pattern of bought links. → [links and digital PR](../channels/links-and-digital-pr.md)
- **Discussions and forums** — a Google results block of forum threads, dominated by Reddit. → [third-party presence](../channels/third-party-presence.md)
- **Orphan page** — a page no internal link points to; crawlers that discover by links won't find it. → [internal linking](../technical/internal-linking.md)
- **Soft 404** — a page that returns 200 but looks empty or missing to Google, e.g. out-of-stock products or empty listings. → [conflicts](conflicts.md#out-of-stock-pages-noindex-or-keep-indexed)
- **sameAs / Wikidata** — Organization markup and the open knowledge base that tie your brand to one entity in Google's Knowledge Graph. → [homepage and brand](../page-types/homepage-and-brand.md)
- **Scaled content abuse** — Google's spam policy against generating many pages mainly to manipulate rankings. → [scaling content and templates](../situations/scaling-content-and-templates.md)

## Surfaces, personalisation and rendering
- **Google Discover** — Google's personalised feed of articles; volatile, rewards strong images and headlines; a bonus channel for editorial content. → [Google Discover](../channels/google-discover.md)
- **Preferred Sources** — a Google feature letting users favour publishers; global since April 2026, influencing AI Overviews and AI Mode since May 2026. → [Google ranking](../how-it-works/google-ranking.md)
- **Personal Intelligence** — AI Mode personalisation from connected Google data (Gmail, Photos); it changes which brands appear. → [Google AI features](../how-it-works/google-ai-features.md)
- **bfcache** — the browser's back/forward cache; instant back navigation, broken by `no-store` on HTML and many single-page-app setups. → [performance and caching](../technical/performance-and-caching.md)
- **Speculation rules** — browser instructions to prefetch or prerender pages; can be abused by third parties against uncached URLs. → [performance and caching](../technical/performance-and-caching.md)
- **Brand canon** — the list of checkable facts about a brand (locations, services, delivery, returns) used to score AI answers as accurate, wrong or unanswered. → [homepage and brand](../page-types/homepage-and-brand.md)

## Speed, behaviour and ML methods
- **CrUX, field vs lab** — Chrome's real-user data (75th percentile over 28 days) is what Google uses; Lighthouse lab scores are for debugging and aren't a ranking signal. → [performance and caching](../technical/performance-and-caching.md)
- **LCP, INP, CLS, TTFB** — time to the largest content, response to input, layout shift, and time to the first byte. → [performance and caching](../technical/performance-and-caching.md)
- **fetchpriority, preload scanner** — a hint that raises a resource's loading priority; the browser's early scan of HTML, which only sees resources written in the markup. → [performance and caching](../technical/performance-and-caching.md)
- **No-Vary-Search** — a header telling caches which URL parameters (such as utm) don't change the page. → [performance and caching](../technical/performance-and-caching.md)
- **Facade** — a lightweight placeholder that loads an embed, such as a video player, only on click. → [performance and caching](../technical/performance-and-caching.md)
- **Rage, dead and error clicks** — repeated clicks in one spot, clicks that do nothing, clicks followed by an error: signs of friction. → [analytics](../measure/analytics.md)
- **Dark AI traffic** — visits from AI assistants that arrive without a referrer and land in Direct. → [conflicts](conflicts.md#is-ai-traffic-hiding-in-direct)
- **Commodity content, information gain** — content that repeats what already ranks, versus content that adds something new. → [Google ranking](../how-it-works/google-ranking.md)
- **Content decay, striking distance** — clicks down 30 % or more between two three-month periods; pages ranking 4–20 that a small push could lift. → [Search Console](../measure/search-console.md)
- **Adjusted Rand index (ARI)** — a measure of how far two clusterings agree (1 = identical, around 0 = chance). → [ML methods for SEO](../measure/ml-methods-for-seo.md)
- **Entity salience** — how central an entity is to a text, as scored by NLP APIs. → [ML methods for SEO](../measure/ml-methods-for-seo.md)
- **Difference-in-differences** — comparing a changed group with an unchanged one before and after, to separate the change's effect from the trend. → [diagnostic tests](../measure/diagnostic-tests.md)
- **Fuzzy matching** — pairing old and new URLs by text similarity when building redirect maps. → [migration](../situations/migration.md)
- **Retrieved vs cited** — the pages an assistant fetches or scores, versus the ones it shows as sources; most retrieved pages go uncited. → [AI visibility tracking](../measure/ai-visibility-tracking.md)
- **Pronoun query** — an AI Mode follow-up ("does it ship…") that shows up in Search Console and reveals the conversation behind it. → [diagnostic tests](../measure/diagnostic-tests.md#36-rebuild-ai-mode-conversations-from-pronoun-queries)
- **Text fragment** — a link ending in `#:~:text=` that opens a page scrolled to the quoted words, as in Gemini's citations. → [analytics](../measure/analytics.md)

## Measurement
- **num=100** — a results parameter Google stopped supporting in September 2025; Search Console impressions fell and average position improved without real change. → [Search Console](../measure/search-console.md)
- **Zero-click** — a search that ends without a click to any site; about 68 % of US Google searches in early 2026, with rates differing by method and country. → [conflicts](conflicts.md#how-high-is-zero-click)
- **Poisoned SERP** — a rank-tracker capture that doesn't match what users see. → [rank tracking](../measure/rank-tracking.md)
- **Prompt tracking** — running a fixed set of prompts through AI engines repeatedly to measure citations and mentions. → [diagnostic tests](../measure/diagnostic-tests.md#9-prompt-tracking-per-engine)
- **Exposure / behaviour / outcomes** — a monthly read of AI visibility, branded search and Direct, and orders together. → [diagnostic tests](../measure/diagnostic-tests.md#11-monthly-read-exposure-behaviour-outcomes)
- **Unassigned** — GA4's bucket for sessions no channel rule matches, e.g. a `utm_source` without `utm_medium`; AI-assistant links often land here. → [analytics](../measure/analytics.md)
- **Consent Mode** — Google's signals telling tags whether analytics and ad storage are allowed; denied events are only modelled, and a misconfigured setup can block purchases. → [analytics](../measure/analytics.md)
- **Content group** — a GA4 dimension grouping pages by type (product, category, guide), set per page; it isn't retroactive. → [analytics](../measure/analytics.md)
- **_gl linker** — the URL parameter GA4 uses to carry a visitor's IDs across domains, e.g. to an external checkout. → [analytics](../measure/analytics.md)
- **Structural break** — a change in measurement or the results page that makes before/after comparisons misleading. → [Search Console](../measure/search-console.md), [analytics](../measure/analytics.md)

Related: [start here](../start-here.md), [conflicts register](conflicts.md).

[^playbook]: Definitions condense the linked pages; see their footnotes for the evidence.
