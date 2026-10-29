---
type: Guide
title: How AI assistants retrieve and cite
description: What ChatGPT, Gemini, Claude and Perplexity actually read — the ~200 characters after the H1 and per-chunk scores on fetched pages, mostly static HTML (Gemini reads JavaScript content), no schema, discovery, mode and model effects, English fan-out, engines that don't agree, citations outside Google's top 10, fresher content, ChatGPT's search config, rerankers and hybrid retrieval, HTML extraction, shrinking, volatile and site-restricted fan-outs, updated-vs-published recency, what models already know about brands, what academic GEO tests found, and how Perplexity's own index (Photon) ranks pages.
tags: [geo, chatgpt, gemini, perplexity, claude, crawling, citations, fan-out, schema, freshness, rerankers, reddit, javascript, bing]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: pplx-photon
    resource: "https://www.perplexity.ai/hub/blog/photon"
    title: "Perplexity Engineering, Photon: retrieval and ranking engine (2026-09-24)"
  - id: serprecon-photon
    resource: "https://www.serprecon.com/blog/how-to-rank-in-perplexity-photon"
    title: "SERPrecon (Ryan Jones), How to rank in Perplexity Photon (2026-10-14; vendor commentary, no own test)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays third-party studies)"
  - id: ipr-cloaking
    resource: "https://ipullrank.com/cloaking-for-llms"
    title: "iPullRank, Cloaking for LLMs (2026-05-14; cites Vercel/MERJ, >500M GPTBot fetches, and Cloudflare)"
  - id: ipr-pagespeed
    resource: "https://ipullrank.com/page-speed-impacts"
    title: "iPullRank, Page speed impacts on AI citation (2026-05-08; cites Profound, 700K pages, April 2026)"
  - id: ipr-personalisation
    resource: "https://ipullrank.com/query-fan-out-personalization"
    title: "iPullRank (Lazarina Stoy), Query fan-out personalization (2026-03-20)"
  - id: gm-consensus
    resource: "https://www.growth-memo.com/p/the-consensus-gap"
    title: "Growth Memo, The consensus gap (2026-05-11; 3.7M citations, 20,000-prompt sample, Omnia data)"
  - id: gm-reasoning
    resource: "https://www.growth-memo.com/p/reasoning-lift-what-happens-to-ai"
    title: "Growth Memo, Reasoning lift (2026-05-18; 100 prompts × 2 reasoning modes, Semrush data)"
  - id: gm-agents
    resource: "https://www.growth-memo.com/p/where-ai-agents-get-stuck-on-your"
    title: "Growth Memo, Where AI agents get stuck on your site (2026-07-13; 100 B2B products × 3 tasks × 5 runs)"
  - id: gm-shorter
    resource: "https://www.growth-memo.com/p/shorter-focused-content-wins-in-chatgpt"
    title: "Growth Memo, Shorter, focused content wins in ChatGPT (2026-04-13; 815,000 query-page pairs; body paywalled)"
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026; 1,249 answers, 88k results, server logs of 325k URLs)"
  - id: chatgpt-53
    resource: "https://think.resoneo.com/chatgpt/5.3-5.4/"
    title: "Resoneo, ChatGPT Search on GPT-5.3/5.4 (Mar–Apr 2026; 27k answers to 400 prompts)"
  - id: chatgpt-not-se
    resource: "https://think.resoneo.com/chatgpt/"
    title: "Resoneo, ChatGPT is not a search engine (Feb 2026; network traffic and decompiled frontend)"
  - id: gemini-convo
    resource: "https://think.resoneo.com/gemini-convo/"
    title: "Resoneo, How Gemini searches and cites (Oct 2026; 76,450 conversations, 222,753 searches)"
  - id: llm-crawler
    resource: "https://think.resoneo.com/sentinel/geo-llm-crawler-report.html"
    title: "Resoneo, LLM crawler test (Jan 2026; one test page, 8 assistants)"
  - id: chrome-class
    resource: "https://think.resoneo.com/chrome-classification/"
    title: "Resoneo, How Chrome classifies websites (May 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2026"
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10)"
  - id: aleyda-traffic
    resource: "https://www.aleydasolis.com/en/ai-search/ai-traffic-citations-research/"
    title: "Aleyda Solis, AI traffic vs citations research (~Apr–May 2026; 40 US sites, Semrush + Similarweb; search extracts)"
  - id: aleyda-local
    resource: "https://www.aleydasolis.com/en/ai-search/local-vs-global-ai-citations/"
    title: "Aleyda Solis, Local vs global AI citations (Oct 2026; ChatGPT, Gemini, AI Mode; US/UK/ES/BR; search extracts)"
  - id: thrive-aio-mode
    resource: "https://thriveagency.com/news/ai-overviews-vs-ai-mode-whats-the-difference-for-brands/"
    title: "Thrive, AI Overviews vs AI Mode (2026-08-27; relays Ahrefs, >730,000 responses)"
  - id: ah-aio-vs-mode
    resource: "https://ahrefs.com/blog/ai-overviews-vs-ai-mode/"
    title: "Ahrefs, AI Overviews vs AI Mode (Sept 2025, US; 540,000 query pairs for citation overlap, 730,000 for semantic similarity)"
  - id: bp-schema-test
    resource: "https://botpresso.com/ai-assistants-schema-markup-test/"
    title: "Botpresso, Do AI assistants read schema? (≈2026-10; 4 assistants × 3 test pages = 12 responses)"
  - id: ah-ai-overlap
    resource: "https://ahrefs.com/blog/ai-search-overlap/"
    title: "Ahrefs, AI search overlap with Google's top 10 (2025-08-11; 15,000 long-tail queries)"
  - id: ah-freshness
    resource: "https://ahrefs.com/blog/do-ai-assistants-prefer-to-cite-fresh-content/"
    title: "Ahrefs, Do AI assistants prefer fresh content? (2025-07-28; ~16.975M cited URLs)"
  - id: ah-refresh-case
    resource: "https://ahrefs.com/blog/taught-agent-to-refresh-data-content/"
    title: "Ahrefs, Teaching an agent to refresh data content (2026-06-25; own case)"
  - id: bp-mentions
    resource: "https://botpresso.com/how-do-brands-get-mentioned-by-chatgpt-and-perplexity/"
    title: "Botpresso, How brands get mentioned by ChatGPT and Perplexity (≈2026-10; synthesis of third-party studies)"
  - id: mt-chunks
    resource: "https://metehan.ai/blog/inside-chatgpt-leak-how-ranks-chunks-from-fetched-pages/"
    title: "Metehan Yeşilyurt, How ChatGPT ranks chunks from fetched pages (2026-09-09; ChatGPT UI stream capture, 1 prompt, 96 fetched pages, 76 scored)"
  - id: mt-config
    resource: "https://metehan.ai/blog/chatgpt-5-search-configuration/"
    title: "Metehan Yeşilyurt, ChatGPT GPT-5 search configuration files (2025-08-20; page source of one Plus session)"
  - id: mt-recency
    resource: "https://metehan.ai/blog/i-found-it-in-the-code-science-proved-it-in-the-lab-the-recency-bias-thats-reshaping-ai-search/"
    title: "Metehan Yeşilyurt, Recency bias in AI search (2025-10-03; config + Fang et al. arXiv:2509.11353, 7 LLMs)"
  - id: nz-gptleak
    resource: "https://natzir.com/en/seo/chatgpt-leaks-seo-for-ai/"
    title: "Natzir Turrado, What the ChatGPT leaks teach about SEO for AI (2025-08-20; leaked system prompt/config, 50 local prompts Spain May 2025)"
  - id: nz-hybrid
    resource: "https://natzir.com/en/seo/hybrid-search-ai-search/"
    title: "Natzir Turrado, Hybrid search and AI search (2025-08-29; review)"
  - id: mt-hypotheses
    resource: "https://metehan.ai/blog/the-rrf-top-n-playbook-how-to-get-cited-by-chatgpts-web-mode/"
    title: "Metehan Yeşilyurt, RRF top-n playbook and related posts on Perplexity patterns, Public Suffix List, CC Rank (2025; hypotheses, code partly simulated)"
  - id: mt-rerank
    resource: "https://metehan.ai/blog/rerankers-for-geo-aeo-how-ai-search-chooses-passages-and-sources/"
    title: "Metehan Yeşilyurt, Rerankers for GEO (2026-08-06; 12 open rerankers × 2 passages × 1 query)"
  - id: mt-token
    resource: "https://metehan.ai/blog/reverse-engineering-the-gpt-5-tokenizer-aeo-geo/"
    title: "Metehan Yeşilyurt, Reverse-engineering the GPT-5 tokenizer (2026-02-13; o200k_base analysis)"
  - id: nz-extract
    resource: "https://natzir.com/en/seo/llm-html-content-extraction/"
    title: "Natzir Turrado, HTML content extraction in LLMs with search tools (2025-11-06; 16 HTML variants of one product, mainly Claude)"
  - id: mt-sitequeries
    resource: "https://metehan.ai/blog/reddit-lost-most-its-visibility-chatgpt-site-filled-gap/"
    title: "Metehan Yeşilyurt, Reddit lost its ChatGPT visibility and the site parameter filled the gap (2026-08-21; Peec logs, 14.9M queries/week)"
  - id: dj-sitefanout
    resource: "https://dejan.ai/blog/site-fanouts/"
    title: "DEJAN, OpenAI fan-out data shows no rise in site: use (2026-08-25; 551,695 fan-outs, 196,692 OpenAI, via API)"
  - id: dj-reddit
    resource: "https://dejan.ai/blog/reddit-ai/"
    title: "DEJAN, AI doesn't prefer Reddit, search does (2026-07-21; ~78k OpenAI probes, 697,768 Google citations, 139,601 Anthropic sources)"
  - id: dj-grounding
    resource: "https://dejan.ai/blog/grounding/"
    title: "DEJAN, How AI search grounding works: Google vs OpenAI vs Anthropic (2026-06-13; probing, 1 query)"
  - id: dj-parametric
    resource: "https://dejan.ai/blog/parametric-memory-impacts-brands/"
    title: "DEJAN, AI models encode brand data but fail to recall a third of it (2026-08-17; summary of a Google Research study, 13 LLMs, 2,150 facts)"
  - id: nz-model
    resource: "https://natzir.com/en/seo/model-change-most-mentioned-brand-ai/"
    title: "Natzir Turrado, How a model change can make your brand one of the most mentioned by AI (2026-10-21; 4 Gemini models, 7–20 runs per model per prompt, ablations, 5 categories)"
  - id: mt-memory
    resource: "https://metehan.ai/blog/chatgpts-personal-memory-affects-everything-in-responses-openai-is-using-google-analytics/"
    title: "Metehan Yeşilyurt, ChatGPT's memory affects responses (2025-12-20; hidden metadata, one account)"
  - id: mt-gptbot
    resource: "https://metehan.ai/blog/i-built-a-60-000-page-ai-website-for-10-gptbot-crawled-it-30-000-times-in-12-hours/"
    title: "Metehan Yeşilyurt, A 60,000-page site crawled 30,000 times by GPTBot (2026-03-04; server logs, one site)"
  - id: gg-js
    resource: "https://www.gsqi.com/marketing-blog/can-ai-search-platforms-render-javascript/"
    title: "Glenn Gabe (GSQi), Are AI search platforms still unable to render JavaScript? (2026-10-19; 3 test page types × 5 assistants)"
  - id: gg-chatgpt-bing
    resource: "https://www.gsqi.com/marketing-blog/surging-in-chatgpt-dead-in-google/"
    title: "Glenn Gabe, Surging in ChatGPT, dead in Google (2026-06-22, updated 2026-08-03; 1 case, Ahrefs Brand Radar)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: lr-gullible
    resource: "https://lilyray.nyc/which-ai-search-tools-llms-are-the-most-gullible/"
    title: "Lily Ray, Which AI search tools are the most gullible? (2025-06-17; one planted page, 5 questions, 6 engines, one run)"
  - id: ls-context
    resource: "https://lazarinastoy.com/context-not-content-is-king-ai-search/"
    title: "Lazarina Stoy, Context (not content) is king in AI search (2026-10-25; review of patents and third-party studies)"
  - id: seer-luna
    resource: "https://www.seerinteractive.com/insights/gpt-5.5-vs-gpt-5.6-luna"
    title: "Seer Interactive, ChatGPT-5.6 Luna runs more targeted searches (2026-09-24; 346 matched prompts, 6 industries)"
  - id: seer-chatgpt-structure
    resource: "https://www.seerinteractive.com/insights/chatgpt-data-structure"
    title: "Seer Interactive, Same prompt, different data structure (2026-10-22; 1 prompt captured 3 times + 6-prompt suite, signed-in network payloads)"
  - id: seer-recency
    resource: "https://www.seerinteractive.com/insights/study-content-recencys-impact-on-ai-visibility-in-2026"
    title: "Seer Interactive, Content recency's impact on AI visibility (2026-07-24; 7,683 dated pages, 47,097 citations, ChatGPT/Gemini/Perplexity, 4 brands, Mar–Jun 2026)"
  - id: cc-sd
    resource: "https://www.wix.com/seo/learn/resource/structured-data-for-seo"
    title: "Crystal Carter, Structured data for SEO (2026-03-30, updated 2026-04-06; Wix SEO Hub; one-query comparison)"
  - id: cc-entity
    resource: "https://www.crystalcarter.ai/post/managing-your-brand-entity-for-generative-search"
    title: "Crystal Carter, Managing your brand entity for generative search (≈2026-03; practitioner)"
  - id: sp-public-evidence
    resource: "https://sparktoro.com/blog/if-search-captures-demand-public-evidence-creates-it/"
    title: "SparkToro, If search captures demand, public evidence creates it (2026-04-01; search-share study, relayed Seer and Foundation data)"
  - id: sp-search-vs-prompt
    resource: "https://sparktoro.com/blog/how-much-is-your-audience-searching-google-vs-prompting-ai-tools-sparktoros-answers-just-got-an-upgrade/"
    title: "SparkToro, How much is your audience searching Google vs prompting AI tools? (2026-03-08; Datos, 41 sites)"
  - id: sp-track-ai-visibility
    resource: "https://sparktoro.com/blog/office-hours-can-you-actually-track-ai-visibility/"
    title: "SparkToro, Office Hours: Can you actually track AI visibility? (2026-05-07; SparkToro x Gumshoe.ai, 142 prompts, 994 runs, 7 model families)"
  - id: sp-influence-5000
    resource: "https://sparktoro.com/blog/new-research-influence-happens-everywhere-an-analysis-of-the-5000-most-visited-sites-on-the-mobile-and-desktop-web/"
    title: "SparkToro, Influence happens everywhere: the 5,000 most-visited sites (2026-03-25; Similarweb, Jan 2026)"
  - id: sp-similarweb-ai-mentions
    resource: "https://sparktoro.com/blog/new-research-from-similarweb-how-ai-brand-mentions-influence-direct-visits-traditional-search-queries/"
    title: "SparkToro with Similarweb, How AI brand mentions influence direct visits and search (2026-06-28; clickstream panel, sample not stated)"
  - id: sp-ai-boondoggle
    resource: "https://sparktoro.com/blog/is-ai-visibility-a-marketing-boondoggle/"
    title: "SparkToro, Is AI visibility a marketing boondoggle? (2026-10-22; review of 4 third-party studies)"
  - id: sp-click-optional
    resource: "https://sparktoro.com/blog/zero-click-search-what-still-works/"
    title: "SparkToro, The click is now optional (2026-06-10; synthesis of SparkToro, Adobe and other data)"
  - id: sp-affinity-vs-traffic
    resource: "https://sparktoro.com/blog/audience-affinity-vs-traffic-why-high-affinity-media-belongs-in-your-earned-media-strategy/"
    title: "Fractl on the SparkToro blog, Audience affinity vs traffic (2026-06-17; SparkToro affinity data, 8 industries)"
  - id: sp-website-matters
    resource: "https://sparktoro.com/blog/does-your-website-still-matter-in-the-zero-click-era/"
    title: "SparkToro, Does your website still matter in the zero-click era? (2026-08-14; opinion)"
  - id: sp-ultimate-guide
    resource: "https://sparktoro.com/blog/the-death-of-the-ultimate-guide/"
    title: "SparkToro, The death of the ultimate guide? (2026-04-27; relays Indig/AirOps, 16,851 queries)"
---

# How AI assistants retrieve and cite

This page answers what ChatGPT, Gemini, Claude and Perplexity actually fetch, read and cite, and what that requires of a page.

**In short.** AI assistants decide from very little text. They mostly see the title, the URL and a short passage from the top of the page; most read static HTML, not JavaScript (Gemini is the exception), and not live JSON-LD; they find pages mainly through links (sitemaps are disputed); ChatGPT scores fetched pages chunk by chunk; their source sets depend on mode and model; and the engines rarely agree. Confidence labels follow the [scale](../reference/sources-and-confidence.md). Google's own AI features work differently: see [Google AI features](google-ai-features.md).

## Rules

- Open every product, category and guide page with one self-contained factual sentence directly after the H1, and start every later section with a sentence that answers one sub-question. *Measured; per-chunk scoring from code, one capture* [why](#1-the-opening-of-the-page-carries-it) · [chunks](#9-what-each-engine-receives-and-how-chatgpt-scores-it)
- Put prices, specs and availability as visible text in the server-rendered HTML, in one main container with the product name, and keep any schema in sync with that text: assistants answer from visible text, and stale schema can mislead them. *Measured, small tests* [why](#2-visible-server-rendered-html) · [extraction](#12-keep-the-product-block-in-one-container)
- Keep key pages reliably fetchable for AI bots, and watch their status codes in server logs. *Measured* [why](#2-visible-server-rendered-html)
- Link every new page internally and keep it in the XML sitemap; sources disagree whether a sitemap alone gets it discovered. *Measured, one site each* [why](#3-discovery-and-caching-openai)
- Fix the model and mode for every prompt-tracking run, log the model per answer and rollouts as events, and report fan-out counts as dated ranges per model, never one run. *Measured* [why](#4-fewer-sources-known-sources-english-queries) · [fan-outs](#13-fan-outs-shrink-and-sometimes-search-inside-sites)
- Keep an English version of key pages and English entity data, but measure local-language citations per market. *Measured* [why](#4-fewer-sources-known-sources-english-queries)
- Report AI visibility per engine and classify cited URLs separately from landing pages. *Measured* [why](#6-the-engines-dont-agree)
- Don't use Google top-10 rankings as a proxy for assistant citations; most cited URLs don't rank for the query. *Measured, vendor data* [why](#7-assistants-cite-outside-googles-top-10)
- Refresh data-driven, comparison and brand pages with real changes, show a true "updated" date and keep `dateModified` and sitemap `lastmod` accurate; never fake one. *Measured, vendor data; from code; cadence is practitioner* [why](#8-assistants-cite-fresher-content-than-search) · [config](#10-chatgpts-search-configuration)
- Get your brand known by name in your category, and earn "need or category → brand" statements, because models recall brands they know and add them to their sub-queries. *Practitioner synthesis; research summary* [why](#4-fewer-sources-known-sources-english-queries) · [recall](#14-what-the-model-already-knows)
- Treat AI assistants as a brand channel, not a traffic channel: search still has ~20× the search activity and AI referrals are small, so report both, and keep your own site the current source of facts. *Measured, vendor data; one case* [why](#17-how-much-people-prompt-versus-search)

## 1. The opening of the page carries it
- **ChatGPT** retrieves about 20 pages per answer, shows about 5 and cites about 3; it usually opens none of them. For each candidate the model sees the title, the URL and a **~202-character snippet starting at the H1**. Meta descriptions are ignored. *Measured.*[^chatgpt-retrieval]
- **Two layers, not a contradiction.** The ~202-character snippet and "about 20 pages" describe the search-result cards. Pages ChatGPT actually fetches are split into chunks and each chunk gets its own neural score; in one capture a comparison prompt ran 4 searches and fetched 96 pages, so retrieval per turn can exceed 20. *From code, one prompt; author works for an AI-visibility vendor.*[^mt-chunks] Details in [section 9](#9-what-each-engine-receives-and-how-chatgpt-scores-it).

  > **Conflict:** sources give very different sizes for what AI engines read per page — [details](../reference/conflicts.md#how-much-of-a-page-do-ai-engines-read)
- **Gemini**: 33 % of cited passages start in the first 10 % of the page and 80 % in the first half; half are 43 words or fewer; 70 % of answer sentences paraphrase the source. *Measured.*[^gemini-convo]
- **Chrome's page classifier** reads ~10 chunks of ~100 words, each cut to 64 tokens. *From code.*[^chrome-class]
- **Do:** open every product, category and guide page with one self-contained factual sentence directly after the H1 — what it is, key attributes (material, size, use), price from, availability — then the brand prose. Pattern in [product pages](../page-types/product-pages.md) and [category pages](../page-types/category-pages.md).
- **Not for Google.** Google's own guide says you "don't need to write in a specific way just for generative AI search" and that there's "no requirement to break your content into tiny pieces".[^google-ai-guide] The findings in this section are about ChatGPT and Gemini as assistants; for Google's AI features, normal SEO applies ([Google AI features](google-ai-features.md#1-googles-official-line-its-still-seo)). A factual opening helps readers either way.
- **Example.** A category page whose first 200 characters were "Anyone looking into desks will sooner or later come across…" gave an assistant nothing to cite; no dimensions, material or price appeared anywhere in its static HTML.[^field-notes]

> **Conflict:** Google says no special writing is needed for AI, while assistant studies reward a factual opening — [details](../reference/conflicts.md#googles-guidance-vs-assistant-findings)

## 2. Visible, server-rendered HTML
- **Most assistant fetchers don't run JavaScript.** ChatGPT-User, Claude-User, Gemini and Perplexity-User read static HTML; Copilot, Grok and DeepSeek render JavaScript. Perplexity-User failed to read the test page at all. *Thin: one test page.*[^llm-crawler] (The Gemini part is contradicted by the retest below.)
- **Retest: Gemini reads JavaScript content.** Three test pages (main content injected by JavaScript; a static shell with JavaScript main content; a parallax/WebGL page) were put to five assistants: ChatGPT, Claude and Perplexity failed all three; Gemini read the content of all three; Copilot passed the two JavaScript tests and failed WebGL. *Measured, small test (3 page types × 5 assistants).*[^gg-js] The likely explanation is that Gemini answers from Google's rendered index rather than its own fetch ([Google AI features](google-ai-features.md#11-gemini-reads-the-index-not-the-live-page)). *Inference.*

  > **Conflict:** one test lists Gemini as static-only, a later retest found it reading JavaScript content in 3 of 3 cases — [details](../reference/conflicts.md#do-ai-assistants-render-javascript)
- **JSON-LD doesn't reach the model on live reads.** It is stripped when ChatGPT reads a page, and user-triggered fetchers don't extract it. *Measured / one test.*[^chatgpt-retrieval][^llm-crawler] Structured data still helps Google's own features; for assistants, the same facts must also be visible text.
- **Schema-only facts aren't used.** ChatGPT, Perplexity, Claude and Gemini were asked about three test pages (schema facts that differ from the visible text; schema with an empty body; JSON-LD plus Microdata with no visible content): 0 of 12 responses returned a fact that existed only in schema; 10 said they had no answer and 2 answered from the open web. The same post relays a test (Ramos) in which 0 of 280 fetched pages kept their JSON-LD, and Gemini preferred a stale FAQPage answer over the visible text in 8 of 20 trials. *Measured, n=12, directional; the Ramos figures are relayed.*[^bp-schema-test] Adding schema didn't raise AI citations at scale either ([Google AI features](google-ai-features.md#1-googles-official-line-its-still-seo)). **Do:** state facts as visible text in the initial HTML and keep any schema in sync with it — stale schema can hurt.
- **"Google and Microsoft say LLMs use structured data."** One practitioner guide states this for retrieval-augmented answers but gives no quote or source. *Unverified claim.*[^cc-sd] The measured tests above stand: treat schema as a Google rich-result tool and keep the facts in visible text.
- **Confirmed at scale.** Across more than 500 million GPTBot fetches, no JavaScript was executed; ClaudeBot and GPTBot download JS files (about 24 % and 11.5 % of fetches) but don't run them; 69 % of 23 AI crawlers can't execute JS. *Measured, third-party (Vercel/MERJ).*[^ipr-cloaking]
- **Serving Markdown to AI bots** cuts tokens by about 80 % (16,180 → 3,150 in Cloudflare's example), and iPullRank proposes it via an edge worker.[^ipr-cloaking] Treat it as risky: serving different content per user agent is cloaking if it diverges. If you try it, keep the content identical to what Googlebot gets and verify after each deploy.
- **Google AI Mode** worked from Google's index and never fetched the live page.[^llm-crawler]
- **Unreliable pages don't get cited.** Pages that AI crawlers time out on (HTTP 499) more than 75 % of the time got "roughly 18x fewer citation events" from OpenAI across 700K pages. *Measured, correlational (Profound).*[^ipr-pagespeed] It acts as a gate, not a ranking factor. **Do:** watch AI-bot status codes and cache hits in server logs ([test](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs)); edge-cache HTML for AI bots, never cart, checkout or account pages.
- **Hidden or unreachable facts send agents elsewhere.** Across 100 products, agents answered pricing questions from the vendor's own site 79 % of the time; with no price disclosed, 45 % of runs cited a third party; fetch errors raised third-party fallback on pricing from 17 % to 77 %. *Measured, B2B sample.*[^gm-agents] What you don't state in reachable text, someone else states for you.
- **Do:** check key templates with a plain HTTP fetch using an assistant's user agent ([diagnostic tests](../measure/diagnostic-tests.md#4-fetch-a-page-the-way-an-ai-assistant-does)), and ask each assistant for the first and last paragraph of the page to see what it actually read.[^gg-js] Prices, specs and availability must be in the response body, not injected by script.

## 3. Discovery and caching (OpenAI)
- **Separate bots, separate jobs.** OAI-SearchBot feeds the snippet index; ChatGPT-User fills a shared full-page cache (refreshed ~every 30 minutes, kept 90+ days, ignores `noindex` and `no-store`); GPTBot is for training and feeds neither. *Measured from server logs.*[^chatgpt-retrieval] OpenAI now documents a fourth, OAI-AdsBot, for ad landing pages. Every vendor's bots, what blocking each costs and how they treat robots.txt: [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).
- **Discovery is by links — on one site.** GPTBot followed internal links and never fetched sitemap-only URLs.[^chatgpt-retrieval] A new page needs internal links; a sitemap entry alone isn't enough.
- **…but by sitemap on another.** On a new 60,000-page test site with no inbound links, GPTBot found the XML sitemap within minutes and made 29,000+ requests in 12 hours, ~470× Googlebot's; in a 3-hour snapshot OAI-SearchBot made 94 requests and ChatGPT-User 1. A client-side tracker saw zero bots, so read server logs, and verify bots against OpenAI's published IP ranges because user agents get spoofed. *Measured, one site, server logs; author works for an AI-visibility vendor.*[^mt-gptbot] **Do:** link new pages internally *and* list them in the sitemap.

  > **Conflict:** one log study saw no sitemap-only fetches by GPTBot, another saw GPTBot crawl a site from its sitemap alone — [details](../reference/conflicts.md#do-ai-crawlers-use-sitemaps)
- **Retrieval goes shallow.** One speaker reported that retrieval bots rarely go more than ~3 pages deep from where they enter. *Practitioner, relayed (Jori Ford, conference talk); low confidence, no data shown.*[^lr-techseo] **Do:** link key pages within two clicks of the pages that already get cited ([internal linking](../technical/internal-linking.md)).
- **Blocking choices are separate.** Blocking a training crawler (GPTBot, Google-Extended, ClaudeBot) is a different decision from blocking search or user fetchers (OAI-SearchBot, ChatGPT-User, Claude-User, PerplexityBot). Check that a CDN's "block AI bots" toggle doesn't block the search and user fetchers you want. *Inference from the bot roles above.*
- **Example.** A CDN's managed robots.txt setting silently put a block above the shop's own rules: it disallowed 17 AI training crawlers and added a `Content-Signal: ai-train=no` line, while search and answer crawlers stayed allowed. It sat there for about two weeks until a new daily robots.txt check flagged it. **Do:** watch robots.txt daily against a written policy.[^field-notes]

## 4. Fewer sources, known sources, English queries
- **Answers concentrate.** After one model release (4 March 2026) the domains per ChatGPT answer fell from 19.1 to 15.2. *Measured.*[^chatgpt-53]
- **Free vs paid differ.** Free instant mode runs about 1 search over ~11 pages, mostly OpenAI's own index; paid "thinking" runs ~6 searches over ~100 pages, mostly scraped Google results.[^chatgpt-retrieval]
- **The count depends on the mode.** With GPT-5.2 at high vs minimal reasoning, sources per answer rose from 2.6 to 4.5 and fan-out queries 4.6×; only 25.6 % of cited domains overlapped between the modes. *Measured, 100 prompts.*[^gm-reasoning] Fix model and mode when tracking prompts ([test](../measure/diagnostic-tests.md#9-prompt-tracking-per-engine)).
- **The model version moves it too.** Brand-site citations were reported at 56 % on GPT-5.4, 22 % on GPT-5.2 and 8 % on GPT-5.3 (Writesonic); Reddit's share of ChatGPT search citations fell from 3.83 % to 0.52 % in four days in August 2026 (Promptwatch, which couldn't rule out a data issue). *Relayed, samples not stated.*[^ignite-news] Log the model with every tracking run and mark rollouts as events. A model change can flip a brand from absent to always named: in one test the same brand appeared in 1 of 7 answers on one Gemini model and 7 of 7 on another, same day, same pages, because the newer model added a reviewer's name to its fan-out. *Measured, small samples.*[^nz-model] What that means for third-party work: [third-party presence](../channels/third-party-presence.md).
- **Reddit follows search, and ChatGPT dropped it.** Reddit's share of ChatGPT citations fell from ~4.6 % to 0.23 % between early August and 21 August 2026 (−95 %), in steps on 8 and 14 August, while Google's AI surfaces weren't affected the same way. *Measured, vendor log data (Peec), not reproducible outside it.*[^mt-sitequeries] Separately, OpenAI selected 0.61 % of 491,024 Reddit retrievals vs 12.85 % for all sources; Reddit was 2.0 % of 697,768 Google AI citations and 0 of 139,601 Anthropic grounding sources. *Measured, biased to the author's prompts.*[^dj-reddit] **Do:** invest in forums only where they already rank in Google for your queries; details in [third-party presence](../channels/third-party-presence.md).
- **Authority explains little, freshness and URLs more.** A talk on 250M AI responses reported that backlinks and authority explain only "4% and 7%" of citation behaviour; natural-language URLs of 5–7 words got "11.4% more citations"; "50% of top-cited content is less than 13 weeks old"; across models, Reddit was the most-cited domain and YouTube second. *Vendor data (Profound, Josh Blyskal), method unpublished, relayed by Lily Ray.*[^lr-techseo] **Do:** give new pages descriptive URLs; never rename existing URLs for this.

  > **Conflict:** studies put Reddit anywhere from most-cited to near zero, depending on engine, period and method — [details](../reference/conflicts.md#how-much-do-ai-engines-cite-reddit)
- **Known sources win.** The model prefers sources it knows from training.[^chatgpt-53] Being named on the few trusted lists, guides and comparison pages per category likely matters more than on-page tweaks. *Inference.* Which third parties get cited, and how to get onto them: [third-party presence](../channels/third-party-presence.md). What the model recalls without searching: [section 14](#14-what-the-model-already-knows).
- **ChatGPT puts known brands into its sub-queries.** It adds brand names it already knows to its fan-out queries, so brands it doesn't know get left out. Engines also differ in how many sources they cite: Perplexity 21.87 vs ChatGPT 7.92 citations per question (Qwairy), 16.35 vs 6.88 per prompt (arXiv 2604.25707); 79 % of ChatGPT retrievals were corporate or institutional domains (Peec, 1,500 chats); editorial and reference sites took 29 % of Perplexity's citations vs 9 % of ChatGPT's. In a 252,000-trial study, topical relevance and position in the retrieved results had the strongest effect on which source is cited first; explicit pricing and recent timestamps helped. *Relayed; an agency's synthesis of third-party studies, not checked at the originals.*[^bp-mentions]
- **Each engine has its own index.** Claude's citations overlapped 86.7 % with Brave's top organic results.[^ipr-personalisation] Ranking in Bing and Brave matters for assistants that use them.
- **ChatGPT citations can ignore Google — and even Bing.** A site with almost no Google rankings was cited in "over 90K" ChatGPT prompts, in line with its Bing visibility; Bing deindexed it on 10 July 2026, yet its ChatGPT citations rose to "over 464K" responses by 3 August. Where ChatGPT grounded those answers is unresolved. *Practitioner, one case, Ahrefs Brand Radar data.*[^gg-chatgpt-bing] **Do:** track Bing indexing too; don't read ChatGPT citations as a quality signal. Google losses usually do carry over: see [Google ranking](google-ranking.md#9-spam-handling-brand-size-and-preferred-sources).
- **Personalisation acts before retrieval.** Memory and chat context change the sub-queries themselves, not only the order of results; content can shape an answer without being cited. *Patents plus anecdotal tests.*[^ipr-personalisation] Logged-in tracking is contaminated by memory: ChatGPT injects `user_profile`, `turn_summary` and `summarized_turn_messages` from other chats into the context of an answer. *From code, one account.*[^mt-memory] Label logged-out tracking as a non-personalised baseline ([AI visibility tracking](../measure/ai-visibility-tracking.md)).
- **Local answers** draw on the business's own website and listings: see [local](../channels/local.md).
- **Focused pages over "ultimate guides".** Shorter, focused pages got cited more in ChatGPT across 815,000 query-page pairs. *Headline only; method paywalled.*[^gm-shorter]

  > **Conflict:** other data finds long pages cited more often than short ones — [details](../reference/conflicts.md#short-or-long-pages)
- **English fan-out.** More than half of ChatGPT's sub-queries are English;[^chatgpt-not-se] Gemini sends an English query for 55 % of non-English questions.[^gemini-convo] **Do:** keep an English version of key pages and English entity data even in a non-English market.
- **But local sources still win a large minority.** Local ccTLDs took about 41 % of citations in Brazil, 38 % in the UK and 24 % in Spain; Gemini's local share ranged from 51.7 % (Brazil) to 16.6 % (Spain), AI Mode's stayed at 22.6–27.5 %. Home/DIY had among the highest local shares. *Measured; read from search extracts.*[^aleyda-local] Measure per market and per engine; don't assume English sources cover local prompts ([new market](../situations/new-market.md)).

## 5. Shopping answers are a separate system
Product cards don't come from web citations; they come from merchant feeds and shopping graphs. See [shopping surfaces](shopping-surfaces.md).

## 6. The engines don't agree
- For the same prompt, 91.07 % of cited URLs appeared in only one of ChatGPT, Perplexity and AI Overviews; 2.37 % appeared in all three. For product pages the three-way overlap was 1.2 %, for category pages 1.6 %. Stable from Q3 2025 to Q1 2026. *Measured, 3.7M citations; skewed to Spain/EU, fintech, travel, SaaS.*[^gm-consensus]
- **Google's two surfaces disagree too.** AI Overviews and AI Mode cited the same sources only 13.7 % of the time (540,000 query pairs, US, Sept 2025; 16.3 % among the top-3 citations) while their answers averaged 86 % semantic similarity (730,000 pairs). 45 % of AIO citations change between generations, so the true overlap may be higher. *Measured, vendor data.*[^ah-aio-vs-mode] AI Mode named about 2.5× more entities (3.3 vs 1.3 per answer). *Relayed.*[^thrive-aio-mode] (Earlier versions of this page gave >730,000 responses as the sample for the 13.7 %; that was the semantic-similarity sample.)
- **Do:** report visibility per engine, never as one blended "AI visibility" score.
- **Cited pages and clicked pages differ.** Across 40 US sites, discovery and evaluation pages took about 57.0 % of citations but 8.9 % of AI traffic; homepages and brand-entry pages took about 57.7 % of AI traffic but 3.0 % of citations. *Measured, third-party panel estimates; search extracts.*[^aleyda-traffic] Classify cited URLs separately from landing pages.
- How to track prompts, tag AI traffic and size the channel: [AI visibility tracking](../measure/ai-visibility-tracking.md).

## 7. Assistants cite outside Google's top 10
- Across 15,000 long-tail queries (Jul–Aug 2025), only about 12 % of AI-assistant citations ranked in Google's top 10 for the query: Perplexity 28.6 %, ChatGPT 8.00 % for in-text citations and 6.10 % for its reference list. About 80 % of cited URLs didn't rank anywhere for the original query — they come from the assistants' own sub-queries (fan-out). *Measured, vendor data.*[^ah-ai-overlap]
- **Do:** don't read Google rankings as assistant visibility; track citations per engine ([AI visibility tracking](../measure/ai-visibility-tracking.md)) and check coverage of the likely sub-queries ([fan-out test](../measure/diagnostic-tests.md#13-fan-out-coverage)). Google's own AI Overviews draw more on its top 10: see [Google AI features](google-ai-features.md#3-citations-go-to-passages-not-ranks).
- **One query, two patterns.** For a recipe question, 7 of Perplexity's 8 sources matched Google's 9 recipe rich results, against 2 of ChatGPT's 5. *Anecdote, one query.*[^cc-sd] Directional only: Perplexity may lean closer to Google's results than ChatGPT does.

## 8. Assistants cite fresher content than search
- Across ~16.975M cited URLs, AI-assistant citations averaged 1,064 days since publication vs 1,432 days for pages in organic results; ChatGPT's citations were 458 days newer than organic ones. AI Overviews went the other way, citing pages 16 days *older* than organic. *Measured, vendor data.*[^ah-freshness]
- **Updated beats published.** Across 7,683 dated pages and 47,097 citations (ChatGPT, Gemini, Perplexity; 4 brands incl. pet retail; Mar–Jun 2026; dates from schema, sitemaps and headers), 75 % of cited pages had been updated within the past year but only 42 % published within it (subset of 4,124 pages); more than 25 % of "fresh" pages were first published 2+ years earlier. Updated within a year, by engine: Gemini 78 %, ChatGPT 73 %, Perplexity 65 %; by type: marketplaces 78 %, comparison/review pages 77 %, brand pages 72 %, blogs/guides 67 %. Pages cited once had a median update age of 0.16 years, pages cited every month 0.47 years; brands owned ~2 % of cited content. *Measured, correlational, 4 brands.*[^seer-recency] The talk data in [section 4](#4-fewer-sources-known-sources-english-queries) points the same way ("50% of top-cited content is less than 13 weeks old").[^lr-techseo]
- **Do:** keep `dateModified` and sitemap `lastmod` accurate; refresh comparison and brand pages that keep getting cited; never change dates alone.
- **Do:** refresh data-driven pages (prices, specs, statistics, comparisons) with real changes; a new date alone is not an update, and Google's John Mueller warns against date-only changes.[^ah-freshness] No study gives an evidence-based cadence; Ahrefs moved 14 of its own datasets from quarterly to monthly refreshes without reporting a measured result. *Practitioner, own case.*[^ah-refresh-case] ChatGPT's search configuration has a freshness profile switched on, and LLM rerankers favour newer dates: see [section 10](#10-chatgpts-search-configuration).

## 9. What each engine receives and how ChatGPT scores it
- **Three engines, one query.** For the same query, Google's grounding received 7 sources and cited 7; OpenAI received 39 and cited 2, as "…"-joined sliding windows of 100 or 200 words; Anthropic received 14 and cited 9, with ~3,200–4,800 bytes of encrypted content per page. Google's citation links are wrapped in `vertexaisearch.cloud.google.com/grounding/...`; OpenAI tags cited links `utm_source=openai`. *Probing, 1 query.*[^dj-grounding] **Do:** segment `utm_source=openai` in analytics ([analytics](../measure/analytics.md)). Google's grounding budget per page: [Google AI features](google-ai-features.md#10-how-much-of-a-page-grounding-uses).
- **ChatGPT scores fetched pages per chunk.** In a captured ChatGPT stream, search results carry `snippet::parts` and `snippet::scores`: one neural score per chunk from a ranker named `sonic-re-fh-chunk-ev3-sx4`, max-normalised so the best chunk scores 1.0 (news results 0.5, n=8). Pages not yet in OpenAI's index were split into "hundreds of small fragments at runtime". One comparison prompt ran 4 searches and fetched 96 pages, of which 76 were scored. *From code, 1 prompt; author works for an AI-visibility vendor.*[^mt-chunks]
- **Do:** make every section a self-contained passage whose first sentence answers one sub-question, so the best chunk can stand alone.

## 10. ChatGPT's search configuration
Leaked and dumped configs are snapshots of 2025; values may have changed since.
- **When it searches and how fresh.** ChatGPT runs a web search when its classifier's `search_prob` exceeds 0.54. Freshness need is rated QDF 0–5 (1 = 18 months, 2 = 6 months, 3 = 90 days, 4 = 60 days, 5 = this month/30 days). Results from several queries are fused with Reciprocal Rank Fusion, score = 1/(60 + rank), then reranked by `ret-rr-skysight-v3`. *From the leak.*[^nz-gptleak][^nz-hybrid] Natzir Turrado's reading: RRF rewards ranking across many fan-out queries over a single #1. *Inference.*
- **The config of one session.** A GPT-5 Plus session's page source showed `reranker_model: "ret-rr-skysight-v3"`, `use_freshness_scoring_profile: true`, `enable_query_intent: true`, `vocabulary_search_enabled: true` and `enable_source_filtering: true`. *From code, one session, Aug 2025; author works for an AI-visibility vendor.*[^mt-config]
- **Rerankers prefer newer dates.** Fang et al. (arXiv:2509.11353, 7 LLMs): injecting newer dates alone shifted LLM rerankers' top 10 toward content +0.82 to +4.78 years newer, with jumps of up to 95 ranks and 8.25–25.23 % preference reversals. *Measured, peer study, relayed.*[^mt-recency]
- **Hypotheses, not evidence.** The same author proposes that RRF with k=60 runs across fan-outs (he observed 38–65 sources per query), that Perplexity uses thresholds and curated ecommerce domain lists (his code is labelled simulated), that ChatGPT groups citations by Public Suffix List domain, and that Common Crawl harmonic centrality predicts citations (correlational). *Inference, author's hypotheses; RRF 1/(60 + rank) is independently reported from the leak above.*[^mt-hypotheses]
- **Do:** date and genuinely refresh guides and comparisons for freshness-sensitive queries, with a visible "updated" date; never fake dates; aim for coverage across the sub-query set ([comparison pages and guides](../page-types/comparison-and-guides.md)).

## 11. What rerankers and hybrid retrieval reward
- **Open rerankers punish indirect passages.** For one query, a direct-answer passage beat a descriptive one by orders of magnitude: MiniLM-L6 scored the descriptive passage 0.0019 % vs > 99.9 %, Qwen3-Reranker-0.6B 0.27 % vs > 99.9 %; missing query concepts hurt more than word order. Classic BERT rerankers see 512 tokens; OpenAI File Search defaults to 800-token chunks with 400-token overlap. *Measured, small controlled test with open models (12 rerankers × 2 passages × 1 query); no evidence ChatGPT uses these models; vendor author.*[^mt-rerank] **Do:** name the entity in each section, cover the decision criteria, put the answer sentence first; optionally test key passages with 2–3 open rerankers before publishing.
- **Hybrid retrieval keeps exact codes alive.** Lexical matching catches exact IDs, model numbers and codes that dense vectors treat as noise; diversification (MMR, xQuAD) penalises redundant passages; Anthropic's contextual retrieval cut retrieval misses by 35 / 49 / 67 % across its variants; Microsoft (2026) describes Bing as semantic-first with lexical matching downstream. *Review of published work.*[^nz-hybrid] **Do:** put MPNs and model codes in visible text, and give each section enough context to stand alone ([product pages](../page-types/product-pages.md)).
- **Tables cost tokens.** In GPT-5's `o200k_base` tokenizer, markdown tables run 2.7 characters per token vs 5.9 for prose (~2.2× more tokens); Spanish and French need 1.25–1.29× the tokens of English (German not measured). *From code; effect on retrieval untested.*[^mt-token] **Do:** keep comparison tables, and state the key conclusion in a prose sentence too.

## 12. Keep the product block in one container
- In 16 HTML variants of one product page, read mostly by Claude with its search tool, extraction failed when the price sat outside the main container, at a different nesting depth or in the footer, or when the description sat in an `<aside>`; Microdata didn't rescue it; the H1 was read as the product name. *Measured, one product, mostly one assistant.*[^nz-extract]
- **Do:** keep product name (H1), price and description in one main container at the same nesting level; never in `aside` or `footer` ([product pages](../page-types/product-pages.md), [technical foundations](../technical/technical-foundations.md)).

## 13. Fan-outs shrink, and sometimes search inside sites
- **Fewer fan-outs per answer (API).** Across 196,692 OpenAI fan-outs collected via the API, fan-out queries per searched response fell from 6.16 (March 2026) to 1.10 (August 2026). `site:` queries were 5–6 % of fan-outs on gpt-5.2/5.4 and 0.15 % on gpt-5.5; Google 0.062 %, Anthropic 0. Long ad-hoc prompts produced 7–91× more `site:` queries than short tracking prompts. *Measured via API; the consumer app wasn't tested.*[^dj-sitefanout]
- **Many site searches (consumer app).** In vendor logs of 14.9M ChatGPT queries a week, `site:` fan-outs rose from < 0.11 % (mid-May – late July 2026) to 10.2 % (week of 3 Aug) and 26.2 % (week of 10 Aug; 3.9M of 14.9M), with a daily peak of ~29.2 %. They mostly targeted official brand sites, documentation, help centres and review platforms; < 1 % went to reddit.com. *Measured, large vendor log sample (Peec), not reproducible outside it.*[^mt-sitequeries]

- **A third data point: the model switch.** In 346 matched prompts across 6 industries, GPT-5.6 "Luna" (ChatGPT's default since 2026-07-09) used `site:` in 76 % of fan-outs vs 21.6 % on GPT-5.5; for non-brand prompts 20.6 % → 77.3 %. Sources consulted fell 43 % (6,134 → 3,481), open searches from 575 to 175, inline citations by 12.9 %. *Measured, agency study.*[^seer-luna] It disagrees with the API sample's 0.15 % for gpt-5.5. **Do:** treat a platform-wide citation drop around 2026-07-09 as a model change, not a content problem; group `site:` fan-outs by topic.

  > **Conflict:** the consumer-app logs (26.2 %), the Luna comparison (76 %) and the API sample (0.15–6 %) disagree on how often ChatGPT searches inside sites — [details](../reference/conflicts.md#how-often-does-chatgpt-search-inside-sites)
- **Fan-outs are volatile.** Two identical runs of one prompt, 8 minutes apart, shared none of their query strings; the URLs retrieved for one prompt grew from 14 to 40 over 13 days, and 34 of the 40 were never cited; one session switched from gpt-5-6 to gpt-5-6-mini mid-way; the payload format changed within two weeks. *Measured, n=1 prompt (plus a 6-prompt suite), signed-in captures.*[^seer-chatgpt-structure] **Do:** report fan-out metrics as ranges, log the model per answer, and keep raw captures ([AI visibility tracking](../measure/ai-visibility-tracking.md)).
- **Do:** make sure specs, delivery, returns and prices exist on your own crawlable pages, since ChatGPT may search inside your site for them; date-stamp fan-out counts per model; don't build tracking only from short prompts ([AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 14. What the model already knows
- A Google Research study (13 LLMs, 2,150 facts), as summarised by DEJAN: models encode 95–98 % of facts but fail to recall 26–34 % of them; long-tail recall is 20–35 points lower; reverse questions (feature → brand) work worse than brand → feature; thinking modes recover 40–65 % of the missed facts. *Research study, relayed.*[^dj-parametric]
- **Training cut-off.** A recent launch can be missing from answers that rely on training data simply because it postdates the model's cut-off. *Practitioner.*[^cc-entity] **Do:** recheck after the next model update before treating the gap as a content problem.
- **Do:** publish and earn "need or category → brand" statements (on your own pages and on third-party lists), not only brand-centred copy; test recall with web search off as a parametric baseline ([AI visibility tracking](../measure/ai-visibility-tracking.md)). Model changes can flip which brands get named: see [section 4](#4-fewer-sources-known-sources-english-queries) and [third-party presence](../channels/third-party-presence.md).

## 15. What changes generative answers
- **Academic GEO tests.** Aggarwal et al. (KDD 2024) found that adding citations, quotations and statistics to a page raised its visibility in generative answers "by up to 40%", while keyword stuffing had little effect. Liu et al. (2023) found that only 51.5 % of generative-search sentences were fully supported by their citations. *Research papers, relayed by Lazarina Stoy; both predate today's production engines.*[^ls-context] **Do:** back claims with sources, quotes and numbers; don't stuff keywords.
- **One page can plant a claim.** In a one-run test, a page with invented claims on uncovered questions was repeated by AI Mode for 4 of 5 questions, by ChatGPT, Perplexity and Gemini for 2 each, and by Claude for none; engines that sought agreement across sources resisted more. *Measured, one run.*[^lr-gullible] Details and what to do: [Google AI features](google-ai-features.md#13-thinly-covered-questions-are-easy-to-sway).

## 16. Perplexity's own index (Photon)
- **Perplexity ranks from its own web index.** Photon, in service since September 2026, retrieves and ranks candidates per index shard, then merges them into the shortlist the answer model reads. *Official.*[^pplx-photon]
- **Lexical matching first.** Candidates are scored on weighted query-term coverage plus term frequency. Strict coverage of the query's terms comes first, and the requirement is relaxed only when too few pages qualify. Term frequency is length-normalised and capped, so repeating a term stops paying off quickly. Each field (unnamed) is matched in its own pass and weighted. *Official.*[^pplx-photon]
- **A per-document "usefulness" signal decides which pages are checked first.** Perplexity doesn't define it. *Official; the definition is unknown.*[^pplx-photon]
- **Fast refresh.** The full index rebuilds in a single-digit number of hours, and documents in freshness-sensitive verticals arrive within minutes. *Official.*[^pplx-photon]
- **Do:** use the buyer's exact terms (including attribute words) in the title, headings and the opening passage, rather than repeating the head term. Cover every term of the question a page should answer, so it passes the strict-coverage pass. *Inference from the published ranking design; a practitioner tool vendor gives the same advice.*[^pplx-photon][^serprecon-photon]
- **Read vendor write-ups carefully.** One SEO tool vendor's summary adds BM25 and "answers quote passages" to Perplexity's design. The post names neither. *Practitioner, vendor.*[^serprecon-photon]

## 17. How much people prompt versus search
SparkToro sells audience research; most figures below come from clickstream panels (Datos, a Semrush company, and Similarweb).
- **Search still dwarfs prompting.** Across 41 major US desktop sites in Q4 2025, Google had 73.7 % of searches, traditional engines together ~80 %, commerce sites ~10 %, social 5.5 % and AI tools 3.2 %; Amazon, Bing and YouTube each had more search activity than ChatGPT. *Measured, vendor data.*[^sp-public-evidence]
- **Not every visit is a prompt.** 97 % of Google's visitors search there, 56 % of ChatGPT's prompt. *Measured, vendor data (Datos, 41 sites).*[^sp-search-vs-prompt] On desktop, AI tools had ~2.9 % of visits vs 34 % for search engines; ChatGPT visits were ~75 % desktop, Google search ~66 % mobile. *Measured, relayed; video transcript.*[^sp-track-ai-visibility] Among the 5,000 most-visited sites, AI tools' share of visits was tiny next to their share of press coverage. *Measured, vendor data.*[^sp-influence-5000]
- **AI mentions may lift brand visits.** Devices that saw AI answers recommending a credit card brand were more likely to visit it within 7 days (+7.2 % and +14.2 % for two brands). Only large brands in three sectors, and no counterfactual. *Measured, vendor data, sample not stated.*[^sp-similarweb-ai-mentions]

  > **Conflict:** the Similarweb study finds a brand-visit lift after AI recommendations, while Kevin Indig found no reliable correlation between AI visibility and branded or direct traffic on 12 sites.[^sp-ai-boondoggle] — [details](../reference/conflicts.md#do-ai-recommendations-lift-brand-demand)
- **Small traffic, disputed conversion.** LLMs sent 0.73 % of referral traffic across 100 sites, less than DuckDuckGo, and Google drove 97 % of conversions (Marie Haynes); organic search sent ~39× more traffic than AI (SEOWorks). *Measured, relayed.*[^sp-ai-boondoggle] Adobe reports AI-sourced US retail traffic up almost 400 % year on year and converting ~42 % better. *Measured, relayed.*[^sp-click-optional]

  > **Conflict:** Adobe says AI referrals convert ~42 % better, while SEOWorks found AI converting worse than organic on 23 of 63 sites and Haynes found Google drove 97 % of conversions. — [details](../reference/conflicts.md#does-ai-traffic-convert-better)
- **Earned media gets cited.** 95 % of AI citations come from non-paid media and 89 % from earned media (Muck Rack); stories distributed through third-party outlets had ~325 % more AI citation visibility than owned-only publishing (Stacker). *Measured, relayed by a digital PR agency.*[^sp-affinity-vs-traffic] Where to earn them: [third-party presence](../channels/third-party-presence.md#16-audience-affinity-and-public-evidence).
- **Keep the website the current source of facts.** SparkToro found AI answers about its own products were wrong because they drew on old content, and built a new help hub. *Practitioner, one case.*[^sp-website-matters]
- **Do:** budget AI assistants as a brand channel, not a traffic channel, and report search and AI demand side by side ([AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 18. What ChatGPT's retrieval cites
- In ChatGPT's retrieval pipeline (16,851 queries, 353,799 pages; Kevin Indig and AirOps), the first retrieved result was cited 58.4 % of the time vs 14.2 % at position 10; heading similarity to the query was the strongest content signal; pages covering 26–50 % of the fan-out subtopics beat pages covering all of them; domain authority and backlinks didn't correlate positively with citation. *Measured, relayed; associations only.*[^sp-ultimate-guide] It supports [section 4](#4-fewer-sources-known-sources-english-queries) on focused pages and authority.
- **Do:** one clear question per page, with headings that match how the question is asked. *Practitioner.*[^sp-ultimate-guide]

Related: [Google AI features](google-ai-features.md), [Google ranking](google-ranking.md), [third-party presence](../channels/third-party-presence.md), [AI crawlers and controls](../technical/ai-crawlers-and-controls.md), [AI visibility tracking](../measure/ai-visibility-tracking.md).

[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: funnel 58k retrieved → 7.6k shown → 5k cited → 760 opened; ~202-character snippet from the H1; JSON-LD stripped; bot roles and cache; utm on ~95 % of displayed links; instant vs thinking search counts.
[^chatgpt-53]: Resoneo, ChatGPT 5.3/5.4, read 2026-10-27: domains per answer 19.1 → 15.2 after 4 Mar 2026; preference for known sources.
[^chatgpt-not-se]: Resoneo, "ChatGPT is not a search engine" (data Jan 2026): >50 % English fan-outs.
[^gemini-convo]: Resoneo, Gemini conversations, read 2026-10-27: cited-passage positions and lengths; 55 % English queries for non-English questions.
[^llm-crawler]: Resoneo, LLM crawler report, Jan 2026: which assistants run JavaScript; Perplexity-User failure; AI Mode from index; JSON-LD not extracted. One test page.
[^chrome-class]: Resoneo, Chrome classification, May 2026: 10 chunks of ~100 words cut to 64 tokens.
[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: Writesonic model comparison (week of 2026-03-14), Promptwatch Reddit share (14–17 Aug 2026), Growth Memo retrieval vs citation (week of 2026-03-21); secondary reporting.
[^google-ai-guide]: Google generative-AI optimization guide, updated 2026-07-10: no special writing, no chunking requirement, no AI text files or Markdown, llms.txt ignored.
[^aleyda-traffic]: Aleyda Solis, ~Apr–May 2026, via search extracts: 4 verticals × 10 US sites, Semrush and Similarweb estimates; some AI traffic may be agents.
[^aleyda-local]: Aleyda Solis, Oct 2026, via search extracts: 10 topics, US/UK/ES/BR, ChatGPT, Gemini, AI Mode.
[^thrive-aio-mode]: Thrive, 2026-08-27, relaying Ahrefs (>730,000 responses); entity and Wikipedia figures without method.
[^ah-aio-vs-mode]: Ahrefs, AI Overviews vs AI Mode, US, Sept 2025: citation overlap 13.7 % on 540,000 query pairs, top-3 overlap 16.3 %; 86 % semantic similarity on 730,000 pairs; 45 % of AIO citations change between generations.
[^bp-schema-test]: Botpresso, ≈2026-10 (no publish date shown): ChatGPT, Perplexity, Claude, Gemini × 3 test pages = 12 responses; relays Ramos (0 of 280 pages kept JSON-LD; Gemini stale FAQPage 8 of 20). Agency promoting its own tools.
[^ah-ai-overlap]: Ahrefs, 2025-08-11: 15,000 long-tail queries, Jul–Aug 2025; ~12 % of assistant citations in Google's top 10; Perplexity 28.6 %, ChatGPT 8.00 % in-text / 6.10 % references; ~80 % not ranking for the original query.
[^ah-freshness]: Ahrefs, 2025-07-28: ~16.975M cited URLs; average age 1,064 days (assistants) vs 1,432 (organic); ChatGPT 458 days newer; AIO 16 days older; Mueller's warning against date-only updates.
[^ah-refresh-case]: Ahrefs, 2026-06-25: own case, 14 datasets moved from quarterly to monthly refresh by an agent; no measured outcome.
[^bp-mentions]: Botpresso, ≈2026-10: synthesis of Qwairy, arXiv 2604.25707, Peec (1,500 chats) and a 252,000-trial study; figures relayed, originals not checked.
[^ipr-cloaking]: iPullRank, 2026-05-14: Vercel/MERJ crawler data; Cloudflare Markdown example; the Markdown and asset-hiding proposals are King's.
[^ipr-pagespeed]: iPullRank, 2026-05-08: Profound, 700K pages; >75 % failure rate → ~18× fewer OpenAI citation events; one client anecdote (+22 %).
[^ipr-personalisation]: iPullRank, 2026-03-20: patents WO2025102041A1, US20240289407A1 (interpreted); Claude–Brave overlap via Profound.
[^mt-chunks]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2026-09-09: ChatGPT UI stream capture, 1 prompt, 4 searches, 96 fetched pages, 76 scored; `snippet::parts`, `snippet::scores`, ranker `sonic-re-fh-chunk-ev3-sx4`; max-normalised scores; news 0.5 (n=8).
[^mt-config]: Metehan Yeşilyurt (Peec AI), 2025-08-20: page source of one ChatGPT Plus session (GPT-5); config keys quoted.
[^mt-recency]: Metehan Yeşilyurt (Peec AI), 2025-10-03: config plus Fang et al., arXiv:2509.11353, 7 LLMs; +0.82 to +4.78 years, up to 95-rank jumps, 8.25–25.23 % reversals.
[^nz-gptleak]: Natzir Turrado, 2025-08-20: leaked ChatGPT system prompt and config; `search_prob` > 0.54, QDF 0–5 scale, RRF, `ret-rr-skysight-v3`. May be stale.
[^nz-hybrid]: Natzir Turrado, 2025-08-29: review of hybrid retrieval (lexical + dense), MMR/xQuAD, Anthropic contextual retrieval (35/49/67 % fewer misses), Microsoft on Bing (2026); restates the RRF formula.
[^mt-hypotheses]: Metehan Yeşilyurt (Peec AI), 2025: RRF top-n playbook and posts on Perplexity patterns, Public Suffix List, CC Rank; hypotheses, partly simulated code; 38–65 sources per query observed.
[^mt-rerank]: Metehan Yeşilyurt (Peec AI), 2026-08-06: 12 open rerankers × 2 passages × 1 query; reproducible with open models.
[^mt-token]: Metehan Yeşilyurt (Peec AI), 2026-02-13: `o200k_base` analysis; 2.7 vs 5.9 characters per token; Spanish and French 1.25–1.29× English.
[^nz-extract]: Natzir Turrado, 2025-11-06: 16 HTML variants of one product page, mainly Claude with search tools.
[^mt-sitequeries]: Metehan Yeşilyurt (Peec AI), 2026-08-21: Peec query logs, 14.9M queries a week; `site:` share by week; Reddit citation share ~4.6 % → 0.23 % (early Aug – 21 Aug 2026). Vendor data, not reproducible outside Peec.
[^dj-sitefanout]: DEJAN, 2026-08-25: 551,695 fan-outs, 196,692 from OpenAI, collected via API; fan-outs per searched response 6.16 → 1.10; `site:` share by model; consumer app not tested.
[^dj-reddit]: DEJAN, 2026-07-21: ~78k OpenAI probes (491,024 Reddit retrievals), 697,768 Google AI citations (3,450-search sample: Reddit in 26.6 %), 139,601 Anthropic grounding sources; author's own prompt sets.
[^dj-grounding]: DEJAN, 2026-06-13: probing Google, OpenAI and Anthropic grounding for 1 query; source counts, window sizes, link wrappers and UTM tags.
[^dj-parametric]: DEJAN, 2026-08-17: summary of a Google Research study, 13 LLMs, 2,150 facts; original not checked.
[^nz-model]: Natzir Turrado, 2026-10-21: 4 Gemini models, 7–20 runs per model per prompt, ablations, 5 categories; 1/7 vs 7/7 (p = 0.005) on the same day and pages.
[^mt-memory]: Metehan Yeşilyurt (Peec AI), 2025-12-20: hidden metadata in one account's ChatGPT responses.
[^mt-gptbot]: Metehan Yeşilyurt (Peec AI), 2026-03-04: server logs of one new 60,000-page site; GPTBot 29,000+ requests in 12 h (~470× Googlebot); 3-hour snapshot OAI-SearchBot 94, ChatGPT-User 1.
[^gm-consensus]: Growth Memo, 2026-05-11: 91.07 % single-engine, 2.37 % all three; 1.2 % product, 1.6 % category; author calls it directional.
[^gm-reasoning]: Growth Memo, 2026-05-18: citation rate 50 → 68 %, sources 2.6 → 4.5, fan-out 4.6×, 25.6 % domain overlap.
[^gm-agents]: Growth Memo, 2026-07-13: 79 % own-site pricing answers; 45 % third-party when undisclosed; fetch errors 17 → 77 %.
[^gm-shorter]: Growth Memo, 2026-04-13: headline and subtitle only; body paywalled.
[^field-notes]: Anonymised shop, 2026: static-HTML spot check of category pages; CDN-managed robots.txt block (12–27 Oct 2026); one-week loss of ChatGPT referrer and UTM in October 2026.
[^gg-js]: Glenn Gabe, 2026-10-19: 3 test page types (JS main content; static shell + JS main; parallax/WebGL) × 5 assistants; ChatGPT, Claude, Perplexity 0/3; Gemini 3/3; Copilot 2/3; first-and-last-paragraph check as method.
[^gg-chatgpt-bing]: Glenn Gabe, 2026-06-22, updated 2026-08-03: 1 case, Ahrefs Brand Radar; "over 90K" ChatGPT prompts before, Bing deindexing on 10 July 2026, "over 464K" responses by 3 August; grounding source unresolved.
[^lr-techseo]: Lily Ray, 2025-12-05, Tech SEO Connect 2025 summaries: Josh Blyskal (Profound; 250M AI responses, method unpublished — authority "4% and 7%", 5–7-word URLs "11.4% more citations", "50% of top-cited content is less than 13 weeks old", Reddit then YouTube most-cited); Jori Ford (~3 pages retrieval depth, low confidence).
[^lr-gullible]: Lily Ray, 2025-06-17: one page with invented claims, 5 questions, 6 engines, one run; per-engine counts as given.
[^ls-context]: Lazarina Stoy, 2026-10-25: relays Aggarwal et al. (KDD 2024; "by up to 40%") and Liu et al. (2023; 51.5 % of sentences fully supported); originals not checked.
[^seer-luna]: Seer Interactive, 2026-09-24: 346 matched prompts, 6 industries, GPT-5.5 vs GPT-5.6 Luna (default since 2026-07-09); `site:` 21.6 % → 76 %, non-brand 20.6 % → 77.3 %, sources 6,134 → 3,481, open searches 575 → 175, inline citations −12.9 %.
[^seer-chatgpt-structure]: Seer Interactive, 2026-10-22: 1 prompt captured 3 times plus a 6-prompt suite, signed-in network payloads; 0 shared query strings 8 minutes apart; retrieved URLs 14 → 40 in 13 days, 34 never cited; mid-session model switch; payload format change.
[^seer-recency]: Seer Interactive, 2026-07-24: 7,683 dated pages, 47,097 citations, ChatGPT/Gemini/Perplexity, 4 brands incl. pet retail, Mar–Jun 2026; dates from schema, sitemaps and headers; correlational.
[^cc-sd]: Crystal Carter, Wix SEO Hub, 2026-03-30 (updated 2026-04-06): one-query comparison (7 of 8 Perplexity sources vs 2 of 5 ChatGPT sources matching Google's 9 recipe rich results); the "Google and Microsoft say" statement has no quote or source.
[^cc-entity]: Crystal Carter, ≈2026-03: practitioner note on training cut-offs and recent launches.
[^pplx-photon]: Perplexity Engineering, 2026-09-24: Photon architecture; scoring by "weighted query-term coverage and a frequency contribution", strict then relaxed coverage, "document-length normalization and a cap on gains from repeated terms", per-field passes with field weights, posting lists ordered by "usefulness"; index rebuild in single-digit hours, freshness-sensitive documents in single-digit minutes. Fields and usefulness not specified.
[^serprecon-photon]: SERPrecon (sells an SEO/GEO measurement tool), 2026-10-14: summary of Perplexity's post plus recommendations; BM25 and passage-level quoting are the author's reading; no own test; case study without method.
[^sp-public-evidence]: SparkToro, 2026-04-01: share of searches across 41 major US desktop sites, Q4 2025 (Google 73.7 %, commerce ~10 %, social 5.5 %, AI tools 3.2 %); relays a Seer Interactive case (one brand) and Foundation Inc (8,566 keywords, 14 B2B SaaS domains).
[^sp-search-vs-prompt]: SparkToro, 2026-03-08: Datos (a Semrush company) data on 41 sites with search activity; share of visitors who search or prompt there: Google 97 %, ChatGPT 56 %, Yahoo 35 %.
[^sp-track-ai-visibility]: SparkToro x Gumshoe.ai (Gumshoe sells AI visibility tracking), 2026-05-07: ~600 volunteers, 142 human-written prompts, 994 runs across 7 model families; average pairwise semantic similarity of prompts 0.0809; Office Hours desktop figures (AI tools ~2.9 % of visits vs search engines 34 %). Video transcript.
[^sp-influence-5000]: SparkToro, 2026-03-25: Similarweb panel, top 5,000 domains, Jan 2026, apps excluded; Gmail counted as google.com; category shares only in charts.
[^sp-similarweb-ai-mentions]: SparkToro with Similarweb, 2026-06-28: clickstream panel, sample not stated; 7-day visit lift after an AI recommendation in credit-card answers (American Express +7.2 %, Capital One +14.2 %); only large finance, travel and beauty brands; no counterfactual. Video transcript.
[^sp-ai-boondoggle]: SparkToro, 2026-10-22: review of studies — Marie Haynes (100 sites, 12 months: LLMs 0.73 % of referral traffic, Google 97 % of conversions), SEOWorks (Sep 2025–Aug 2026: organic ~39× AI traffic; AI converted worse than organic on 23 of 63 sites), Kevin Indig (12 sites: no reliable correlation between AI visibility and branded search or direct traffic). Video transcript; SEOWorks site count given as 95 and as 63.
[^sp-click-optional]: SparkToro, 2026-06-10: synthesis; SparkToro analysis of 332 million queries (branded ~44 %); relays Adobe Digital Insights Q2 2026 (AI-sourced US retail traffic almost +400 % YoY, converting ~42 % better).
[^sp-affinity-vs-traffic]: Fractl (a digital PR agency) on the SparkToro blog, 2026-06-17: SparkToro affinity data, 8 industries, aggregate, sample undisclosed; relays Muck Rack 2025 and Stacker.
[^sp-website-matters]: SparkToro, 2026-08-14: opinion, one case (AI answers about SparkToro's products drew on old content; it built a new help hub).
[^sp-ultimate-guide]: SparkToro, 2026-04-27: relays Kevin Indig and AirOps, 16,851 queries and 353,799 pages in ChatGPT's retrieval pipeline; associations only.
