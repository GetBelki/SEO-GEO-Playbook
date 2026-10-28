---
type: Reference
title: Glossary
description: Short definitions of the terms, systems and acronyms used across the playbook — Google systems from the leak and trial, AI-search surfaces, crawlers, feeds and measurement terms — each linked to the page that explains it.
tags: [glossary, reference, terms]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
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

## Measurement
- **num=100** — a results parameter Google stopped supporting in September 2025; Search Console impressions fell and average position improved without real change. → [Search Console](../measure/search-console.md)
- **Zero-click** — a search that ends without a click to any site; rates differ widely by method. → [conflicts](conflicts.md#how-high-is-zero-click)
- **Poisoned SERP** — a rank-tracker capture that doesn't match what users see. → [rank tracking](../measure/rank-tracking.md)
- **Prompt tracking** — running a fixed set of prompts through AI engines repeatedly to measure citations and mentions. → [diagnostic tests](../measure/diagnostic-tests.md#9-prompt-tracking-per-engine)
- **Exposure / behaviour / outcomes** — a monthly read of AI visibility, branded search and Direct, and orders together. → [diagnostic tests](../measure/diagnostic-tests.md#11-monthly-read-exposure-behaviour-outcomes)
- **Structural break** — a change in measurement or the results page that makes before/after comparisons misleading. → [Search Console](../measure/search-console.md), [analytics](../measure/analytics.md)

Related: [start here](../start-here.md), [conflicts register](conflicts.md).

[^playbook]: Definitions condense the linked pages; see their footnotes for the evidence.
