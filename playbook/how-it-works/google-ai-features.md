---
type: Guide
title: How Google's AI features pick sources
description: AI Overviews, AI Mode and Gemini — Google's official "still SEO" line, schema and AI citations, grounding from ranking (FastSearch), passage citation, top-10 overlap, fan-out depth, how users behave, ads and citation UI, personalisation, when AI Overviews trigger, the click loss by position, how often answers change, the grounding word budget, reading from the index, uncited Knowledge Graph facts, Personal Intelligence, Pew's click data and how easily thinly covered questions sway AI answers.
tags: [seo, geo, google, ai-overviews, ai-mode, gemini, citations, fan-out, ctr, branded-search, grounding, knowledge-graph, personalisation, misinformation]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10)"
  - id: thrive-aio-cited
    resource: "https://thriveagency.com/news/how-do-i-get-my-website-cited-in-ai-overviews/"
    title: "Thrive, How do I get cited in AI Overviews (2026-10-08; relays Ahrefs, 863,000 SERPs, 4M AIO URLs)"
  - id: thrive-sources
    resource: "https://thriveagency.com/news/what-sources-do-ai-platforms-use-to-evaluate-businesses/"
    title: "Thrive, What sources do AI platforms use (2026-09-10; relays Moz, 40,000 queries)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays third-party studies)"
  - id: ipr-ai-mode
    resource: "https://ipullrank.com/how-ai-mode-works"
    title: "iPullRank, How AI Mode works (2025-05-27; patents WO2024064249A1, US20240362093A1, US20250124067A1)"
  - id: ipr-agentic-rag
    resource: "https://ipullrank.com/agentic-rag"
    title: "iPullRank, Agentic RAG (2026-05-20)"
  - id: ipr-generative
    resource: "https://ipullrank.com/generative-serps"
    title: "iPullRank, Generative SERPs (2026-10-15; Google Research paper; Nozzle, 27.5M results)"
  - id: mh-doj-ai
    resource: "https://www.mariehaynes.com/google-doj-trial-on-ai/"
    title: "Marie Haynes, What the DOJ trial says about Google's AI (2025-09-11)"
  - id: mh-fanout
    resource: "https://www.mariehaynes.com/ai-mode-query-fan-out/"
    title: "Marie Haynes, AI Mode query fan-out (2025-11-18)"
  - id: gm-behaviour
    resource: "https://www.growth-memo.com/p/users-behave-differently-in-ai-overviews"
    title: "Growth Memo, Users behave differently in AI Overviews (2026-05-25; clickstream, ~846,000 US Google sessions, Feb–Mar 2026)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: aio-aim
    resource: "https://think.resoneo.com/aio-aim-deepdive/"
    title: "Resoneo, AI Overviews / AI Mode deep dive (Feb 2026, work in progress)"
  - id: intent-engine
    resource: "https://think.resoneo.com/google-intent-engine/"
    title: "Resoneo, What Google is building (Jun 2026; decompiled Google app)"
  - id: ah-schema
    resource: "https://ahrefs.com/blog/schema-ai-citations/"
    title: "Ahrefs, Does schema help AI citations? (2026-05-11; difference-in-differences, 1,885 treated pages vs ~4,000 controls)"
  - id: ah-aio-top10
    resource: "https://ahrefs.com/blog/ai-overview-citations-top-10/"
    title: "Ahrefs, AI Overview citations and the top 10 (863K SERPs, ~4M AIO URLs)"
  - id: ah-aio-vs-mode
    resource: "https://ahrefs.com/blog/ai-overviews-vs-ai-mode/"
    title: "Ahrefs, AI Overviews vs AI Mode (Sept 2025, US; 540,000 query pairs for citation overlap, 730,000 for semantic similarity)"
  - id: ah-aio-triggers
    resource: "https://ahrefs.com/blog/ai-overview-triggers/"
    title: "Ahrefs, What triggers AI Overviews (2025-11-10; 146,122,391 US desktop SERPs, Sept 2025)"
  - id: ah-aio-branded
    resource: "https://ahrefs.com/blog/ai-overviews-on-branded-searches/"
    title: "Ahrefs, AI Overviews on branded searches (2026-10-02; 232.8M US desktop crawls Jul–Sep 2026; 100-brand panel)"
  - id: ah-aio-ctr
    resource: "https://ahrefs.com/blog/ai-overviews-reduce-clicks-update/"
    title: "Ahrefs, AI Overviews reduce clicks — update (300,000 keywords, Dec 2023 vs Dec 2025, desktop, aggregated GSC)"
  - id: ah-aio-change
    resource: "https://ahrefs.com/blog/ai-overview-change/"
    title: "Ahrefs, How often AI Overviews change (2025-11-11; 43,000+ keywords)"
  - id: nz-chunk
    resource: "https://natzir.com/en/seo/chunking-content-bad-seo-ai/"
    title: "Natzir Turrado, Why chunking your content is bad for SEO and AI (2025-12-20; review)"
  - id: nz-meta
    resource: "https://natzir.com/en/seo/meta-descriptions-impact-gemini-ai/"
    title: "Natzir Turrado, Are meta descriptions back? Impact on Gemini (2026-10-22; Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts)"
  - id: nz-sdkg
    resource: "https://natzir.com/en/seo/structured-data-kg-google-ai/"
    title: "Natzir Turrado, How structured data reaches AI Overviews and AI Mode (2026-10-27; intern CV, Google Earth WASM strings, 2024 leak, DOJ exhibits; small AI Mode tests)"
  - id: bc-aio-clicks
    resource: "https://www.bruceclay.com/blog/google-ai-overviews-changing-click-behavior-seo-metrics/"
    title: "Bruce Clay, AI Overviews and click behaviour (2025-08-07; cites Advanced Web Ranking Q4 2024, Authoritas)"
  - id: mt-aimode
    resource: "https://metehan.ai/blog/reverse-engineering-google-ai-mode/"
    title: "Metehan Yeşilyurt, Reverse-engineering Google AI Mode via Discovery Engine (2025-11-26; Vertex AI Search docs, extrapolated)"
  - id: dj-chunks
    resource: "https://dejan.ai/blog/how-big-are-googles-grounding-chunks/"
    title: "DEJAN, How big are Google's grounding chunks? (2025-12-20, restated 2026-06-21; 7,060 queries, 2,275 pages, 883,262 snippets; private data)"
  - id: dj-ablation
    resource: "https://dejan.ai/blog/ablation/"
    title: "DEJAN, Grounding snippet ablation (2026-10-20; tool, 1 query, 1 page, n=188 rankings)"
  - id: dj-firstread
    resource: "https://dejan.ai/blog/rank-signal-recipe/"
    title: "DEJAN, Gemini picks whichever page it reads first 92 % of the time (2026-07-26; 24,445 + 5,200 pairwise votes, synthetic pages)"
  - id: dj-notlive
    resource: "https://dejan.ai/blog/googles-still-doesnt-see-your-live-page/"
    title: "DEJAN, Google still doesn't see your live page (2026-05-07; probing, 2 URLs)"
  - id: dj-kg-bio
    resource: "https://dejan.ai/blog/knowledge-graph-biography-ai-mode/"
    title: "DEJAN (Dan Petrovic), Knowledge Graph facts reach AI Mode as uncited Biography results (2026-10-28; Google Earth wasm proto schemas + probing, 2 sessions)"
  - id: dj-fanout2
    resource: "https://dejan.ai/blog/fanout2/"
    title: "DEJAN, Fanout V2: complementary query sets (2026-09-16; summary of Google Research arXiv 2603.06397)"
  - id: pew-aio-clicks
    resource: "https://www.pewresearch.org/short-reads/2025/07/22/google-users-are-less-likely-to-click-on-links-when-an-ai-summary-appears-in-the-results/"
    title: "Pew Research Center, Google users are less likely to click when an AI summary appears (2025-07-22; 900 US adults, 68,879 searches, March 2025)"
  - id: ls-context
    resource: "https://lazarinastoy.com/context-not-content-is-king-ai-search/"
    title: "Lazarina Stoy, Context (not content) is king in AI search (2026-10-25; review of patents and third-party studies)"
  - id: ls-serp
    resource: "https://lazarinastoy.com/how-to-incorporate-machine-learning-into-your-serp-analysis/"
    title: "Lazarina Stoy, ML in SERP analysis (2026-10-25; one-keyword time series)"
  - id: lr-gullible
    resource: "https://lilyray.nyc/which-ai-search-tools-llms-are-the-most-gullible/"
    title: "Lily Ray, Which AI search tools are the most gullible? (2025-06-17; one planted page, 5 questions, 6 engines, one run)"
  - id: gn-aiyear
    resource: "https://www.seoforgooglenews.com/p/googles-ai-adventure-year-one"
    title: "Barry Adams, Google's AI adventure — one year on (2025-05-08; relays Sistrix, Datos/SparkToro)"
  - id: gn-aimode
    resource: "https://www.seoforgooglenews.com/p/initial-thoughts-on-google-ai-mode"
    title: "Barry Adams, Initial thoughts on AI Mode (2025-06-09; Similarweb tab usage)"
  - id: sp-zero-click-2026
    resource: "https://sparktoro.com/blog/in-2026-less-than-one-third-of-google-searches-still-send-a-click/"
    title: "SparkToro, In 2026, less than one third of Google searches still send a click (2026-06-09; Similarweb US web panel, Jan–Apr 2026)"
  - id: srp-commodity-content
    resource: "https://serprecon.com/blog/what-is-commodity-content"
    title: "SERPrecon, What is commodity content? (2026-10-15; Google guide and statements relayed, patents, vendor scoring method)"
  - id: mlseo-aio-tracker
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/track-ai-overviews-python/"
    title: "MLforSEO, How to track AI Overviews for your keywords (2026-10-24; 29-keyword run, US desktop)"
---

# How Google's AI features pick sources

This page answers how AI Overviews and AI Mode choose and show their sources, and how they differ from the blue links and from each other.

**In short.** Google says its AI features need nothing beyond normal SEO, and grounding starts from its own ranking. But citations go to passages, most cited URLs rank outside the top 10, AI Overviews and AI Mode fan out to different depths, and users behave differently on each. Treat organic results, AI Overviews and AI Mode as three linked but separate surfaces ([confidence scale](../reference/sources-and-confidence.md)).

## Rules

- Do normal SEO first, and confirm a page is indexed before expecting Gemini or AI Mode to reflect a change: Google asks for no special files, markup or writing style, and its AI reads the indexed copy, not the live page. *Official; probing, n=2* [why](#1-googles-official-line-its-still-seo) · [index](#11-gemini-reads-the-index-not-the-live-page)
- Rank well for the core query and its sub-queries, because AI grounding starts from Google's ranking. *Trial documents* [why](#2-grounding-starts-from-ranking)
- Make the passage that answers a sub-question easy to lift and put the answer, specs and differentiators in the first ~500 words, because citations go to passages and the grounding budget per page is small. *Measured; budget from private data, directional* [why](#3-citations-go-to-passages-not-ranks) · [budget](#10-how-much-of-a-page-grounding-uses)
- Keep "as of" dates and `dateModified` true and current. *Practitioner* [why](#4-ai-overviews-and-ai-mode-are-separate-but-linked)
- Don't count on a brand query to bring a click when an AI Overview shows; about two thirds of US Google searches end without any click. *Measured; vendor data* [why](#5-users-behave-differently-on-each-surface) · [zero-click](#14-most-searches-end-without-a-click)
- Track organic position, AIO citation and AI Mode citation separately, sample every 2–3 days rather than one snapshot, and keep Search Console as the source of truth. *Measured, vendor data; inference* [why](#6-the-results-page-keeps-changing) · [volatility](#9-ai-overviews-change-every-few-days)
- Before blaming content for a click change on an AI surface, check for UI tests and new ad units. *Practitioner* [why](#6-the-results-page-keeps-changing)
- Keep schema for rich results, not as an AI-citation lever: adding it didn't raise AI citations; put key facts in visible text and keep them identical everywhere, since Knowledge Graph facts reach AI Mode without a link. *Measured, vendor data; from code* [why](#1-googles-official-line-its-still-seo) · [KG](#12-knowledge-graph-facts-arrive-without-a-citation)
- Expect AI Overviews mostly on informational and question queries; commercial, transactional and Shopping queries rarely trigger them (Sept 2025). *Measured, vendor data* [why](#7-when-ai-overviews-show)
- Check monthly what the AI Overview says for your brand name, and keep the facts on Wikipedia/Wikidata, YouTube and LinkedIn current. *Measured, vendor data* [why](#7-when-ai-overviews-show)
- Publish correct facts on your own pages early for poorly covered brand and product questions, because one page can sway AI Mode and AI Overviews when nothing else covers the question. *Measured, one run* [why](#13-thinly-covered-questions-are-easy-to-sway)

## 1. Google's official line: it's still SEO
- Google's 2026 guide: you "don't need to create new machine readable files, AI text files, markup, or Markdown"; Google Search ignores llms.txt; "no requirement to break your content into tiny pieces"; you "don't need to write in a specific way just for generative AI search" — optimising for it "is ... still SEO". Merchant Center and Business Profile help in "both AI responses and other Google Search results". *Official.*[^google-ai-guide]
- **Google-Extended** covers Gemini training and Gemini's grounding, not Search's AI Overviews or AI Mode.[^mh-doj-ai][^nz-sdkg] (Earlier versions of this page said "training only".) Whether opting out also strips Knowledge Graph facts from Gemini is unconfirmed: see [section 12](#12-knowledge-graph-facts-arrive-without-a-citation).
- **Google and Bing advise against bite-sized pages.** Google (Danny Sullivan, Jan 2026) advises against chunking content into bite-sized pieces; Bing (Dec 2025) says near-duplicate pages blur signals. Natzir Turrado's test before splitting: if the target queries share search results, consolidate; if not, keep separate pages. *Official statements, relayed; the test is practitioner.*[^nz-chunk] **Do:** consolidated guides with anchors and a table of contents, the direct answer in the first two lines of each section, tables for comparisons ([scaling content and templates](../situations/scaling-content-and-templates.md)).
- **Adding schema didn't raise AI citations.** Ahrefs compared 1,885 pages that added JSON-LD (Aug 2025 – Mar 2026) with ~4,000 matched controls, 30 days before and after (difference-in-differences): AI Overview citations −4.6 % (significant, but the pages were already declining before), AI Mode +2.4 % and ChatGPT +2.2 % (indistinguishable from zero). Cited pages were ~3× more likely to carry JSON-LD, but that is correlation only. *Measured, vendor data.*[^ah-schema] Keep schema for rich results; assistants don't read it either ([AI assistants](ai-assistants.md#2-visible-server-rendered-html)).
- Eligibility rules, snippet controls (`nosnippet`, `max-snippet`, `noindex`) and every bot are covered in [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).

> **Conflict:** Google says no special writing is needed for its AI features, while assistant studies reward factual, self-contained openings — [details](../reference/conflicts.md#googles-guidance-vs-assistant-findings)

## 2. Grounding starts from ranking
- Trial documents describe FastSearch, "based on RankEmbed signals" and "faster than a full web search, but not as high quality", as the retrieval layer for AI answers; MAGIT is a Gemini version tuned for the AI Overview format. *Trial documents; how links are picked isn't stated.*[^mh-doj-ai] Ranking well is the entry ticket to being cited. How classic ranking works: [Google ranking](google-ranking.md).
- AI Mode anchors answers in Knowledge Graph entities, the Shopping Graph and Places.[^aio-aim] Product units come from feeds: see [shopping surfaces](shopping-surfaces.md).

## 3. Citations go to passages, not ranks
- Patents describe synthetic sub-queries (follow-up, generalisation, specification, translation, entailment…) and pairwise LLM ranking of passages; the cited passage is the one that most directly supports the answer. Ranking #1 for the core query gave "only… a 25% chance" of appearing in the AI Overview (ZipTie, method not given). *Patents; pipeline details are iPullRank's interpretation.*[^ipr-ai-mode]
- **Two patents in detail.** US11663201B2 names eight synthetic query variant types — equivalent, follow-up, generalisation, specification, canonicalisation, translation, entailment and clarification — and stops refining on result quality, not after a fixed count. US11769017B1 links generated text to a source only when their embedding similarity is close enough, so a page can be retrieved and still get no link. *Patent; Lazarina Stoy's interpretation.*[^ls-context] **Do:** build fan-out lists by variant type; for shops, specification (size, material, use), entailment and comparison, and translation variants matter most ([fan-out test](../measure/diagnostic-tests.md#13-fan-out-coverage)).
- **Most AI Overview citations rank outside the top 10.** Ahrefs' study of 863,000 SERPs and ~4M AIO URLs: about 38 % of cited URLs rank in the organic top 10 for that query, 31.2 % at positions 11–100, 31 % outside the top 100.[^thrive-aio-cited] A second cut gives 37.10 % / 26.2 % / 36.70 %, with YouTube 18 % of the non-ranking citations.[^ignite-news] Read at the source: the text says 37.9 % in the top 10, the table 37.10 % (the source is inconsistent), and 18.2 % of cited non-ranking URLs are YouTube. *Measured, vendor data.*[^ah-aio-top10] The earlier "76 % on page 1" figure came from a different Ahrefs study (1.9M citations) that also counted ads, featured snippets, People Also Ask and video blocks, so the two are **not comparable** — not a fall from 76 % to 38 %.[^ah-aio-top10] For AI Mode, Moz found 88 % of citations outside the top 10.[^thrive-sources] *Measured, relayed.* An older Authoritas figure: "46% of AI Overview citations come from the top 10". *Measured, relayed via Bruce Clay; method and date not checked, not comparable with Ahrefs.*[^bc-aio-clicks] Top-10 rank is no proxy for AI presence.
- **AI Mode quotes passages.** 47.7 % of about 15.7M AI Mode citations were scroll-to-text highlights of a specific passage (Pillarbase, one year, relayed).[^ignite-news]
- **Meta descriptions in Gemini grounding.** In Gemini API tests with Search grounding, 7.6 % of the excerpts Google passed to Gemini were the page's meta description, mostly on homepages and category pages, and those pages were cited far less than pages passed body text. *Measured, observational, Gemini API only.*[^nz-meta] What to do on category pages: [category pages](../page-types/category-pages.md).

  > **Conflict:** Gemini grounding sometimes passes the meta description as the only text, while ChatGPT ignores it and Google rewrites most snippets — [details](../reference/conflicts.md#do-meta-descriptions-still-matter)

## 4. AI Overviews and AI Mode are separate, but linked
- **AI Overviews**: about 5–15 citations, little fan-out. **AI Mode**: 8–12 sub-queries per turn, 20–40+ citations. The overlap between the three surfaces' sources is low. *Work in progress, small sample.*[^aio-aim] AI Mode merges many sub-searches, so its sources come in a different order from classic results.[^mh-fanout] How often the two surfaces cite the same sources: [AI assistants](ai-assistants.md#6-the-engines-dont-agree).
- **Same meaning, different sources.** Across 540,000 query pairs (US, Sept 2025), AI Overviews and AI Mode cited the same URLs 13.7 % of the time, and 16.3 % among their top-3 citations; across 730,000 pairs their answers averaged 86 % semantic similarity. Because 45 % of AIO citations change between generations of the same answer, the true overlap may be higher. *Measured, vendor data.*[^ah-aio-vs-mode]
- **Depth differs by surface:** AI Mode about 5–20 sub-queries, AI Overviews 3–8, deep-research modes often 20+; a critic stage drops weak sources, and freshness is checked late ("a reflection-stage gate"). *Practitioner estimate, no method.*[^ipr-agentic-rag] Keep "as of" dates and `dateModified` true and current. Check coverage of likely sub-queries with the [fan-out test](../measure/diagnostic-tests.md#13-fan-out-coverage).
- **Ranking for the sub-queries pays.** Pages ranking for both the main query and its fan-out queries were 161 % more likely to be cited in AI Overviews (Surfer). *Measured, vendor data, relayed.*[^nz-chunk]
- **Fan-out research aims at complementary needs.** A Google Research paper (arXiv 2603.06397) trains sub-query generation (R4T) to penalise paraphrase collapse and to reward diversity (Vendi score), groundedness and alignment with the root query, so sub-queries become complementary product categories — for a camping kit: shelter, sleep, cooking, lighting. Its diffusion retriever ran 12–20× faster with 128-dimension Matryoshka embeddings. *Research paper, summarised by DEJAN; production use unconfirmed.*[^dj-fanout2] **Do:** cluster keywords by distinct sub-need and adjacent category, not by synonym, and link accessory and companion categories from hubs ([keyword research](../channels/keyword-research.md), [internal linking](../technical/internal-linking.md)).
- **Separate, but linked.** "Show more" under an AI Overview opens AI Mode (mobile since Oct 2025, desktop overlay since Apr 2026, auto-expanded AIOs with a sticky AI Mode box tested Apr 2026).[^brodie-notes][^mh-fanout] A query's journey can cross both surfaces.

## 5. Users behave differently on each surface
- With an AIO on the page, cursors covered 83 % of the viewport (66 % without), stayed still 44 % of the time, and about half of all scrolling went back up. In AI Mode users mostly take the answer and stop. With an AIO, 41.9–48.5 % of searchers of every intent were still on the results page after 21 s — for navigational queries up from 12 % to 45.8 %. *Measured, ~846,000 US sessions.*[^gm-behaviour] A brand query is no longer a guaranteed click.
- **AI Mode started small.** In June 2025, "just over 1%" of US Google searches used the AI Mode tab, about half the News tab's share. *Measured, Similarweb, relayed; historical baseline only.*[^gn-aimode]

## 6. The results page keeps changing
- **Both surfaces now carry ads** (back in AI Overviews from Nov 2025; in AI Mode from Nov 2025, inline in product lists from May 2026), and the citation UI changes often (link feeds, "bubble" brand links, favicons, side-by-side link opening in Chrome from Apr 2026).[^brodie-notes] Clicks from AI surfaces can move because of UI tests, not your content.
- Personalisation (57 on-device signals, LLM rerankers) means there is no single reference results page. Rank trackers drift further from Search Console's average position. *From code.*[^intent-engine]
- **Personal Intelligence changes the brand list.** In 1,922 AI Mode responses across 8 product categories (few accounts, opt-in), brands seeded into a connected account appeared in 66.8 % of responses with Personal Intelligence on, up from 23.9 %, while control brands went from 21.9 % to 18.9 %; Gmail-seeded brands appeared in 53.6 %, Photos-seeded in 10.5 %; top-3 placement rose by about 23 points. *Measured, small sample; iPullRank study (May 2026) relayed by Lazarina Stoy.*[^ls-context] **Do:** track from clean, unconnected accounts and label the result a baseline; real users with connected apps see very different lists ([AI visibility tracking](../measure/ai-visibility-tracking.md)).
- **Generated result pages.** A Google Research paper reports generated results pages preferred over the top result 90 % of the time on LMArena prompts (73.5 % on information-seeking prompts); one rank-tracking vendor saw anomalous ("poisoned") captures rise from 0.17 % to 8.0 % after 13 Sep 2026.[^ipr-generative] See [rank tracking](../measure/rank-tracking.md).
- **Do:** for important guides, track organic position, AIO citation and AI Mode citation separately. Keep Search Console as the source of truth; use trackers as a trend ([Search Console](../measure/search-console.md), [AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 7. When AI Overviews show
- **By intent (Sept 2025).** Across 146.1M US desktop SERPs, 20.5 % showed an AI Overview: informational queries 21.4 %, commercial 4.3 %, transactional 2.1 %, navigational 0.9 % (the article's body text says "0.09%", its table 0.9 %). Questions 57.9 % vs 15.5 % for non-questions; non-brand 24.9 % vs brand 13.1 %; queries of 7+ words 46.4 % vs one word 9.5 %. By category: Shopping 3.2 %, Home & Garden 18.4 %; local searches 7.9 %. CPC barely correlates with AIO presence. *Measured, vendor data.*[^ah-aio-triggers] For a shop, product and category queries were among the least exposed in this data (*inference* from the intent and category splits).

> **Conflict:** other studies put AI Overviews on far more searches, including commercial and price/buy queries — [details](../reference/conflicts.md#how-often-do-ai-overviews-show)

- **UK, spring 2025.** Sistrix put AI Overviews on ~18 % of UK queries, up from 4 %, with ~6 cited sources per AI Overview. *Measured, Sistrix, relayed.*[^gn-aiyear]

- **Branded queries caught up fast.** In September 2026, AI Overviews showed on 73.3 % of branded keywords on average (83 % on 29 Sept) against 78.3 % of non-branded, up from 13.1 % branded in the Sept 2025 data above. In a panel of 100 bare brand names, 63 showed an AIO, 76.2 % of those at position 1; the AIOs cited Wikipedia 71.9 %, YouTube 38.6 % and LinkedIn 22.8 % of the time (n=57), and 3.4 % mentioned competitors. *Measured, vendor data, US desktop.*[^ah-aio-branded]
- **Do:** check monthly what the AI Overview says for your brand name; keep the facts on Wikipedia/Wikidata, YouTube and LinkedIn current, because that is what it quotes ([homepage and brand](../page-types/homepage-and-brand.md)).

## 8. What an AI Overview costs in clicks
- Ahrefs' updated estimate (300,000 keywords, December 2023 vs December 2025, desktop, aggregated Search Console data of its users): with an AI Overview present, CTR is −58.0 % at position 1, −50.8 % at position 2, −46.4 % at position 3 and −19.4 % at position 10. It is a counterfactual forecast, not an experiment, and follows the −34.5 % Ahrefs reported in spring 2025. *Measured (modelled), vendor data.*[^ah-aio-ctr]
- An earlier measurement: for informational queries with an AI Overview, "the top four organic results on desktop lost a combined 7.31 percentage points in CTR" (Advanced Web Ranking, Q4 2024). *Measured, relayed via Bruce Clay.*[^bc-aio-clicks]
- **Pew's panel (March 2025).** Across 900 US adults and 68,879 searches, users clicked a traditional result in 8 % of visits with an AI summary vs 15 % without, clicked a link inside the summary in 1 % of visits, and ended their browsing session on the results page in 26 % of visits with a summary vs 16 % without. *Measured, primary study.*[^pew-aio-clicks] The often-quoted "under 1 % click" is a misquote: the 1 % counts only clicks on links inside the summary.

  > **Conflict:** sources explain falling organic CTR differently — [details](../reference/conflicts.md#why-is-organic-ctr-falling)
- **Do:** when clicks fall while impressions and positions hold, check whether the queries gained an AI Overview before blaming the page ([Search Console](../measure/search-console.md#5-where-ai-overviews-show)).

## 9. AI Overviews change every few days
- Across 43,000+ keywords observed at least 16 times each (~1 month), the AIO text changed in 70 % of consecutive observations (average persistence 2.15 days); consecutive answers shared 54.5 % of their cited URLs, while meaning stayed close (semantic similarity 0.95). *Measured, vendor data.*[^ah-aio-change]
- **Overlap with the top 10 can drift to zero.** For one keyword checked on 5 dates in 2026, 2–4 of the AIO-cited URLs were also in the organic top 10 from January to August; on 22 October none of the 8 cited URLs was. *Anecdote, one keyword.*[^ls-serp] **Do:** track AIO citations as their own series, not as a by-product of rank tracking.
- **Do:** never judge AIO presence or citation from one snapshot; sample every 2–3 days and report share of voice across many queries ([rank tracking](../measure/rank-tracking.md), [AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 10. How much of a page grounding uses
- **A fixed word budget per query.** Across 7,060 queries, 2,275 pages and 883,262 snippets, Google's grounding passed a median 1,929 words per query (p95 2,798), split by rank: the #1 result got 531 words (28 %), #5 got 266 (13 %); the median per source was 377 words. Selection levels off at ~540 words (~3,500 characters), so the share of a page covered falls with its length: 61 % of pages under 1,000 words vs 13 % of pages over 3,000. Selection is extractive: sentences are scored against the query, non-adjacent ones joined with "…", with a strong lead bias; the average chunk is 15.5 words. *Measured, private data, directional.*[^dj-chunks] This is a different unit from Gemini's cited passages ("half 43 words or fewer", [AI assistants](ai-assistants.md#1-the-opening-of-the-page-carries-it)): one is what Google hands the model, the other what the answer quotes.

  > **Conflict:** studies give very different sizes for what AI engines read per page — [details](../reference/conflicts.md#how-much-of-a-page-do-ai-engines-read)
- **One specific sentence moves the result.** In an ablation test (1 query, 1 page, n=188 rankings, DEJAN's own tool), adding one specific factual sentence gained +4.10 ± 0.10 of 5 rank places; 20 % of the text held 80 % of the gain; repeating the brand name 4× gave +0.10 ± 0.10 (≈ 0); a tangential sentence cost −0.20. *Measured, single case, vendor tool.*[^dj-ablation] It supports "one clear, specific passage", not repetition. **Do:** find and protect the answering sentence; cut off-topic promotional lines.
- **Order beats content.** With Gemini as the grounding judge on synthetic ~500-word pages, the page read first won 92.4 % of the time; pages rewritten to 31 factors won 15.2 % of second-slot cases (396/2,600) vs 0/2,600 unguided; with thinking on, 50.7 %; 215 of 260 pairs flipped winner when the order was reversed. *Measured, synthetic pages, one model.*[^dj-firstread] Retrieval order dominates and content breaks ties, so ranking in the retrieved set comes first ([section 2](#2-grounding-starts-from-ranking)). **Do:** when testing pages with an LLM, run every comparison in both orders ([diagnostic tests](../measure/diagnostic-tests.md)).
- **A documented analogue.** Google Cloud's Vertex AI Search (Discovery Engine) caps chunks at 500 tokens, can prepend ancestor headings to a chunk, fuses base rank, Gecko embeddings, "Jetstream" relevance, BM25, predicted conversion (Popularity → PCTR → personalised PCTR) and freshness, and has an "Ignore low relevant content" gate. Whether AI Mode works the same way is **unconfirmed**. *Official docs for the Cloud product; the AI Mode link is the author's extrapolation; author works for an AI-visibility vendor.*[^mt-aimode] **Do:** write H2/H3 headings that still make sense when prepended to a chunk.

## 11. Gemini reads the index, not the live page
- Gemini's URL access returns `URL_FETCH_STATUS_NOT_IN_SEARCH_INDEX` or `URL_FETCH_STATUS_EMPTY_CONTENTS_IN_INDEX` for pages that aren't indexed; what it reads is Google's indexed copy, and live-test tools don't show that copy. *Probing, 2 URLs.*[^dj-notlive] It matches the earlier finding that AI Mode never fetched the live page ([AI assistants](ai-assistants.md#2-visible-server-rendered-html)).
- **Do:** confirm indexing (and a re-crawl after a change) before expecting a change to show in Gemini or AI Mode ([Search Console](../measure/search-console.md)).

## 12. Knowledge Graph facts arrive without a citation
- **Uncited, textualized facts.** Knowledge Graph facts reach Gemini and AI Mode as sentences without URLs (`TextualizedData`, `PerQueryResult`, `WorldFactSource`); AI Mode receives them as uncited "Person/Organization Biography" results. Triples carry provenance values (`THIRD_PARTY`, `CURATION`, `PARTNER_FEED`, `EXTRACTION`, `REQUIRES_CITATION`) and `LLM_RESTRICTION_*` flags (`SEARCH_GROUNDING`, `GOOGLE_EXTENDED_OPT_OUT`, `SEARCH_NO_GENAI`). A "Query Result Service" serves "100+ structured attributes"; public WASM strings show 484 result types and 97 providers (Oct 2026). *From the leak (`LlmPolicyMetadata`, `REQUIRES_CITATION`) and from code (public Google Earth WASM strings; meaning inferred); usage from probing, n=2; a cited intern CV is unverified.*[^nz-sdkg][^dj-kg-bio]
- **Small tests.** KG data appeared in 10 of 10 quoted queries vs 0 of 10 unquoted; schema markup hasn't visibly shown up in AI answers in these tests. *Measured, small sample.*[^dj-kg-bio][^nz-sdkg]
- **Do:**
  - Keep brand and product facts identical across the site, feeds and third parties, and put key attributes in visible text and tables, not only in JSON-LD.
  - Audit and correct the brand's Knowledge Graph entity ([homepage and brand](../page-types/homepage-and-brand.md)).
  - Weigh Google-Extended blocking against entity coverage: the `GOOGLE_EXTENDED_OPT_OUT` flag suggests opted-out facts are filtered, but that is unconfirmed. *Inference.* Bot controls: [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).

## 13. Thinly covered questions are easy to sway
- **One planted page was enough.** A page with made-up claims on questions no other page covered was indexed "within 12 hours" and repeated "within 24 hours". AI Mode used it for 4 of 5 questions, AI Overviews for 2, Gemini 2, ChatGPT 2, Perplexity 2 (once without a caveat), Claude 0. Engines that looked for agreement across several sources resisted more. *Measured, one run, one page.*[^lr-gullible] AI Mode was the easiest to sway in this test.
- **Do:** for brand and product questions few pages answer (compatibility, materials, care, delivery to unusual regions), publish the correct facts on your own crawlable page early, and include such obscure attributes in the monthly brand check ([homepage and brand](../page-types/homepage-and-brand.md), [AI visibility tracking](../measure/ai-visibility-tracking.md)). How assistants compare: [AI assistants](ai-assistants.md#15-what-changes-generative-answers).

## 14. Most searches end without a click
SparkToro sells audience research; its numbers come from Similarweb's clickstream panel.
- **68 % zero-click.** 68.01 % of US Google web searches ended without a click in January–April 2026. The panel excludes the Google app, so the true rate is likely higher. *Measured, vendor data.*[^sp-zero-click-2026] A click counts any click, including paid results and Google's own properties.
- **AI Mode is still small.** Only 0.34 % of US Google searches reached AI Mode in the same period, so AI Mode did not cause the zero-click rise; Google's claim of 1bn+ monthly AI Mode users is relayed unverified. *Measured, vendor data.*[^sp-zero-click-2026]

  > **Conflict:** AI Mode at 0.34 % of US searches (Jan–Apr 2026) vs "just over 1%" of searches using the AI Mode tab in June 2025 (section 5); both Similarweb, but different periods and possibly different definitions. — [details](../reference/conflicts.md#how-many-searches-reach-ai-mode)
- The same post relays Ahrefs: AI Overviews on 20 %+ of searches, cutting CTR by nearly 60 % when present. *Measured, relayed.*[^sp-zero-click-2026] It confirms [section 8](#8-what-an-ai-overview-costs-in-clicks).
- **Do:** read flat clicks with rising impressions as the market norm before blaming a page ([Search Console](../measure/search-console.md)).

## 15. Google asks for non-commodity content
- Google's generative-AI features guide has a section headed "Create valuable, non-commodity content"; by SERPrecon's reading (it sells a content-scoring tool), Google says this likely influences AI search presence more than any other suggestion. Its example contrasts a generic "7 tips" listicle with a first-hand article. *Official, relayed.*[^srp-commodity-content] What Google says, and doesn't say, about ranking: [Google ranking](google-ranking.md#13-commodity-content-and-information-gain).
- **AI Overview citations barely overlap the organic top 10.** On 29 US desktop keywords (25 Oct 2026), every keyword showed an AI Overview; the median overlap between cited and organically ranking domains was 22 %, and 0 % for seven keywords. One domain was cited first while absent from the organic top 10. *Measured, small sample; MLforSEO, which sells courses.*[^mlseo-aio-tracker] Confirms [section 3](#3-citations-go-to-passages-not-ranks).
- How to test a page's coverage of likely sub-queries: [keyword research](../channels/keyword-research.md#11-checking-a-pages-fan-out-coverage).

Related: [Google ranking](google-ranking.md), [AI assistants](ai-assistants.md), [shopping surfaces](shopping-surfaces.md), [AI crawlers and controls](../technical/ai-crawlers-and-controls.md), [comparison pages and guides](../page-types/comparison-and-guides.md).

[^google-ai-guide]: Google generative-AI optimization guide, updated 2026-07-10.
[^thrive-aio-cited]: Thrive, 2026-10-08, relaying Ahrefs Brand Radar; other figures on that page (theStacc) have no method.
[^thrive-sources]: Thrive, 2026-09-10, relaying Moz (40,000 queries).
[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: Ahrefs AIO citations (week of 2026-03-01), Pillarbase scroll-to-text (2026-07-25), Zyppy 400 sites (2026-04-11); secondary reporting, primary studies not checked.
[^ipr-ai-mode]: iPullRank, 2025-05-27, and Lazarina Stoy, 2025-12-11 (fan-out variant taxonomy): patents WO2024064249A1, US20240362093A1, US20250124067A1; ZipTie 25 % figure.
[^ipr-agentic-rag]: iPullRank, 2026-05-20: sub-retrieval depth per surface, critic and freshness stages; no method stated.
[^ipr-generative]: iPullRank, 2026-10-15: Google Research generative-UI paper; Nozzle, 27.5M results, 2026-08-20 – 2026-10-09; "scraper degradation" is King's inference.
[^mh-doj-ai]: Marie Haynes, 2025-09-11: FastSearch, MAGIT, Google Common Corpus, Google-Extended scope.
[^mh-fanout]: Marie Haynes, 2025-11-18 and 2026-03-09: AI Mode fan-out, two example queries; AIO → AI Mode on mobile.
[^gm-behaviour]: Growth Memo, 2026-05-25 and 2026-06-01: clickstream metrics with and without AIO, share still active at 21 s by intent.
[^brodie-notes]: Brodie Clark notes, Oct 2025 – Sep 2026 (month anchors #oct-2025, #nov-2025, #feb-2026, #mar-2026, #apr-2026, #may-2026): screenshots, some backed by Google posts.
[^aio-aim]: Resoneo, AIO / AI Mode deep dive, Feb 2026: citation counts and fan-out per surface; low overlap; KG, Shopping Graph and Places anchoring.
[^intent-engine]: Resoneo, "What Google is building", Jun 2026: personalisation signals, rerankers.
[^ah-schema]: Ahrefs, 2026-05-11: difference-in-differences, 1,885 pages that added JSON-LD between Aug 2025 and Mar 2026 vs ~4,000 matched controls, 30 days before/after; AIO −4.6 % (significant, pre-trend already declining), AI Mode +2.4 %, ChatGPT +2.2 % (not distinguishable from zero); ~3× JSON-LD rate among cited pages is correlational. Replaces the "−0.04 to +0.04" schema correlation relayed elsewhere, which is not in Ahrefs' data (Ahrefs' 0.04 Spearman is word count vs AIO citation).
[^ah-aio-top10]: Ahrefs, AI Overview citations and the top 10: 863K SERPs, ~4M AIO URLs; text 37.9 % vs table 37.10 % in the top 10; 18.2 % of cited non-ranking URLs YouTube; the earlier 76 % study (1.9M citations) counted ads, snippets, PAA and video blocks.
[^ah-aio-vs-mode]: Ahrefs, AI Overviews vs AI Mode, US, Sept 2025: citation overlap 13.7 % on 540,000 query pairs, top-3 overlap 16.3 %; 86 % semantic similarity on 730,000 pairs; 45 % of AIO citations change between generations.
[^ah-aio-triggers]: Ahrefs, 2025-11-10: 146,122,391 US desktop SERPs, Sept 2025; trigger rates by intent, question form, brand, length, category and CPC; navigational given as "0.09%" in the text and 0.9 % in the table.
[^ah-aio-branded]: Ahrefs, 2026-10-02: 232.8M US desktop crawls, Jul–Sep 2026; branded 73.3 % monthly average in Sept 2026 (83 % on Sep 29) vs non-branded 78.3 %; 100-brand panel, citation shares on n=57.
[^ah-aio-ctr]: Ahrefs, AI Overviews reduce clicks (update): 300,000 keywords, Dec 2023 vs Dec 2025, desktop, aggregated GSC of Ahrefs users; counterfactual CTR forecast by position.
[^ah-aio-change]: Ahrefs, 2025-11-11: 43,000+ keywords, ≥ 16 observations each over ~1 month; 70 % of consecutive observations changed text, persistence 2.15 days, 54.5 % shared URLs, semantic similarity 0.95.
[^nz-chunk]: Natzir Turrado, 2025-12-20: review; Sullivan (Jan 2026) and Bing (Dec 2025) statements relayed; SERP-overlap consolidation test; Surfer's 161 % figure (vendor study, not checked at the original).
[^nz-meta]: Natzir Turrado, 2026-10-22: Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts; not AI Overviews or AI Mode; observational.
[^nz-sdkg]: Natzir Turrado, 2026-10-27: `TextualizedData`, `PerQueryResult`, `WorldFactSource`, `LLM_RESTRICTION_*` flags and provenance values from the 2024 leak and Google Earth WASM strings (Oct 2026: 484 result types, 97 providers); intern CV unverified and inconsistent; Google-Extended scope from Google's docs; small AI Mode tests (10/10 quoted vs 0/10 unquoted).
[^bc-aio-clicks]: Bruce Clay, 2025-08-07: relays Advanced Web Ranking Q4 2024 (desktop CTR, informational queries with AIO) and Authoritas (46 % of AIO citations from the top 10); originals not checked.
[^mt-aimode]: Metehan Yeşilyurt (works at Peec AI, an AI-visibility vendor), 2025-11-26: Vertex AI Search / Discovery Engine documentation, extrapolated to AI Mode.
[^dj-chunks]: DEJAN, 2025-12-20, restated 2026-06-21: 7,060 queries, 2,275 pages, 883,262 snippets; median 1,929 words per query (p95 2,798), 531 words for #1, 266 for #5, 377 median per source, plateau ~540 words, average chunk 15.5 words. Private data, not reproducible.
[^dj-ablation]: DEJAN, 2026-10-20: own paid tool, 1 query, 1 page, n=188 rankings.
[^dj-firstread]: DEJAN, 2026-07-26: 24,445 + 5,200 pairwise votes on synthetic ~500-word pages, Gemini as judge; 92.4 % first-read wins; 396/2,600 vs 0/2,600; 50.7 % with thinking; 215 of 260 pairs flipped.
[^dj-notlive]: DEJAN, 2026-05-07: probing Gemini URL access on 2 URLs; fetch status values quoted.
[^dj-kg-bio]: DEJAN, 2026-10-28: Google Earth WASM proto schemas plus probing in 2 sessions; Biography result type, provenance and restriction flags; cites Natzir's 10/10 vs 0/10 test.
[^dj-fanout2]: DEJAN, 2026-09-16: summary of Google Research arXiv 2603.06397 (R4T, Vendi diversity, diffusion retriever 12–20× faster, 128-dim Matryoshka embeddings); production use unconfirmed.
[^pew-aio-clicks]: Pew Research Center, 2025-07-22: 900 US adults, browsing data for 68,879 searches in March 2025; traditional-result clicks 8 % with an AI summary vs 15 % without; summary-link clicks 1 %; session ended on the page 26 % vs 16 %.
[^ls-context]: Lazarina Stoy, 2026-10-25: relays iPullRank's Personal Intelligence study (May 2026; 1,922 AI Mode responses, 8 product categories, few opt-in accounts) and interprets patents US11663201B2 (8 variant types, quality-based stopping) and US11769017B1 (embedding-similarity threshold for links).
[^ls-serp]: Lazarina Stoy, 2026-10-25: one keyword, 5 dates in 2026; 2–4 AIO-cited URLs in the organic top 10 Jan–Aug, 0 of 8 on 22 Oct. Anecdote.
[^lr-gullible]: Lily Ray, 2025-06-17: one page with invented claims on uncovered questions, 5 questions, 6 engines, one run; indexed within 12 h, repeated within 24 h; per-engine counts as given.
[^gn-aiyear]: Barry Adams, 2025-05-08: relays Sistrix (spring 2025) — UK AIO share ~18 %, up from 4 %; ~6 cited sources per AIO. Primary not checked.
[^gn-aimode]: Barry Adams, 2025-06-09: relays Similarweb — US AI Mode tab usage "just over 1%" in June 2025, about half the News tab.
[^sp-zero-click-2026]: SparkToro (Rand Fishkin; SparkToro sells audience research), 2026-06-09: Similarweb US desktop+mobile web panel, Jan–Apr 2026; zero-click 68.01 % (Google app excluded; device mix assumed 2/3 mobile, 1/3 desktop); AI Mode 0.34 % of searches; relays Ahrefs on AIO presence (20 %+) and CTR (nearly −60 % when present).
[^srp-commodity-content]: SERPrecon, 2026-10-15: relays Google's generative-AI features guide section on non-commodity content, Danny Sullivan and John Mueller (via Search Engine Journal), the leak's OriginalContentScore and patent US11354342B2; the vendor's commodity metric is not validated against rankings.
[^mlseo-aio-tracker]: MLforSEO, 2026-10-24: AI Overview tracker run on 29 keywords, US desktop, 2026-10-25, DataForSEO data.
