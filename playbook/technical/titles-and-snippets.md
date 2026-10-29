---
type: Guide
title: Titles and snippets
description: How often Google rewrites titles and meta descriptions, where titles and descriptions are worth hand-writing (including meta descriptions as Gemini grounding text on category and home pages), why content length has no target, answer-first openings and the first ~500 words, self-explanatory headings, tables plus a prose conclusion, which changes count as a content update, and editorial headlines on guide pages (H1 vs title) — with the FAQ/HowTo schema advice and keyword-appended titles not adopted.
tags: [seo, geo, title-tags, meta-descriptions, snippets, content-length, on-page, headings, headlines, tables, grounding, freshness, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: ah-titles
    resource: "https://ahrefs.com/blog/title-tag-seo/"
    title: "Ahrefs, Title tag SEO (updated 2024-11-06; Site Audit, 1M+ sites)"
  - id: ah-overopt
    resource: "https://ahrefs.com/blog/over-optimization/"
    title: "Ahrefs, Over-optimization (updated 2024-03-28)"
  - id: ah-meta
    resource: "https://ahrefs.com/blog/meta-description-study/"
    title: "Ahrefs, Meta description study (2020; 20,000 keywords, 192,656 pages)"
  - id: ah-length
    resource: "https://ahrefs.com/blog/blog-post-length/"
    title: "Ahrefs, Blog post length (2020-07-14; ~900M pages)"
  - id: ah-onpage
    resource: "https://ahrefs.com/blog/on-page-seo-checklist/"
    title: "Ahrefs, On-page SEO checklist (updated 2026-03-05)"
  - id: nz-meta
    resource: "https://natzir.com/en/seo/meta-descriptions-impact-gemini-ai/"
    title: "Natzir Turrado, Are meta descriptions back? Impact on Gemini (2026-10-22; Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts)"
  - id: sbs-freshness
    resource: "https://www.seobythesea.com/2008/09/updating-googles-historical-data-patent-part-2-changing-content/"
    title: "SEO by the Sea, Google's historical data patent, part 2: changing content (2008-09-17; patent US 7,346,839; likely expired)"
  - id: mt-token
    resource: "https://metehan.ai/blog/reverse-engineering-the-gpt-5-tokenizer-aeo-geo/"
    title: "Metehan Yeşilyurt, Reverse-engineering the GPT-5 tokenizer (2026-02-13; o200k_base analysis)"
  - id: mt-aimode
    resource: "https://metehan.ai/blog/reverse-engineering-google-ai-mode/"
    title: "Metehan Yeşilyurt, Reverse-engineering Google AI Mode via Discovery Engine (2025-11-26; Vertex AI Search docs, extrapolated)"
  - id: dj-chunks
    resource: "https://dejan.ai/blog/how-big-are-googles-grounding-chunks/"
    title: "DEJAN, How big are Google's grounding chunks? (2025-12-20, restated 2026-06-21; 7,060 queries, 2,275 pages, 883,262 snippets; private data)"
  - id: gn-article
    resource: "https://www.seoforgooglenews.com/p/perfectly-optimised-news-article-for-seo"
    title: "Barry Adams, The 'perfectly optimised' article (2025-02-10; practitioner)"
  - id: lr-seoweek
    resource: "https://lilyray.nyc/seo-in-the-age-of-agents-takeaways-from-nyc-seo-week/"
    title: "Lily Ray, SEO Week 2025 takeaways (2025-05-08; talk summaries)"
---

# Titles and snippets

What goes into titles, meta descriptions and the opening of a page, how much Google rewrites them, and why page length has no target. Confidence labels follow the [scale](../reference/sources-and-confidence.md).

## Rules
- **Keep titles to about 50–60 characters (under ~600 px), primary keyword first.** Longer or very short titles get rewritten. *Measured, vendor data; the length is practitioner guidance* — [evidence](#1-titles)
- **Template titles for the long tail ("Product | Category"); hand-write them for top-traffic pages.** *Practitioner* — [evidence](#1-titles)
- **Rework titles first on pages ranking 4–10, and prioritise title and meta rewrites by organic traffic.** *Practitioner* — [evidence](#1-titles)
- **Write meta descriptions for pages with organic traffic or social sharing, and always for category and home pages** — as if they were the only text read (brands, ranges, prices, criteria) — and give those pages visible body copy that answers their head queries. Google rewrote metas about 63 % of the time and ChatGPT ignores them, but Gemini's grounding used them, mostly on home and category pages, where body text was cited far more often. *Measured, vendor data, dated 2020; Measured, observational, Gemini API only* — [evidence](#2-meta-descriptions)
- **Set no word-count targets**; cover what the top-ranking pages share, briefly. *Measured correlation, dated 2020; Official (Google statement)* — [evidence](#3-length)
- **Open with the answer**: a definition on informational pages, a recommendation on commercial pages; put the answer, specs and differentiators in the first ~500 words. *Practitioner; Measured, private data, directional* — [evidence](#4-answer-first-openings), [first 500 words](#7-the-first-500-words-carry-grounding)
- **Write H2/H3 headings that make sense on their own**, and keep tables but restate their conclusion in a sentence. *Inference from vendor docs; From code* — [headings](#5-headings-that-stand-alone), [tables](#6-tables-plus-a-prose-conclusion)
- **Refresh titles and main content substantively; never bump dates alone**, and don't force freshness on evergreen queries. *Patent, supported by the leak* — [evidence](#8-what-counts-as-a-content-update)
- **On guides and editorial pages, write the H1 as a headline of up to ~110 characters with the topic in the first 8 words, and follow it with a one-sentence summary**; the `<title>` keeps its own length rules. *Practitioner, from news publishing* — [evidence](#9-headlines-on-guides-and-editorial-pages)

## 1. Titles
- In Ahrefs' Site Audit data for 1M+ sites, 68.54 % of sites had pages whose title in the SERP differed from the page's title tag. Titles were too long on 63.19 % of sites, too short on 32.76 %, missing on 5.55 %, and 3.04 % had multiple title tags (site-level shares). *Measured, vendor data.*[^ah-titles]
- Google truncates or rewrites titles over ~600 px, and short titles invite rewrites. Mueller (2021) called the title a "tiny ranking factor". *Measured; Official statement, relayed, dated 2021.*[^ah-titles]
- **Do:** ~50–60 characters, primary keyword first; templates such as "Product | Category" for the long tail, hand-written titles for top-traffic pages; rework titles first for pages at positions 4–10.[^ah-titles] Prioritise title and meta rewrites by organic traffic.[^ah-overopt]
- For categories, the title and H1 carry the searcher's exact term ([category pages](../page-types/category-pages.md)); which keyword is primary comes from the [keyword map](../channels/keyword-research.md#5-clustering-and-mapping).
- ChatGPT judges candidate pages by title, URL and ~202 characters from the H1, so the title also works as the assistant's first filter ([AI assistants](../how-it-works/ai-assistants.md#1-the-opening-of-the-page-carries-it)).
- **Not adopted: appending Search Console keywords to titles.** A conference talk (Michael King, relayed) reported that clicks rose when queries from Search Console were appended to titles; no data was shown. It runs against the 50–60-character guidance above, so treat it as a hypothesis for an A/B test on a page group, not as a rule. *Practitioner, no data, relayed.*[^lr-seoweek]

## 2. Meta descriptions
- Google rewrote meta descriptions 62.78 % of the time (head terms 59.65 %, long tail 65.62 %). Length barely mattered: 61.46 % of too-long descriptions were rewritten vs 63.69 % of those within limits. 25.02 % of top-ranking pages had none. *Measured, vendor data, dated 2020 (20,000 keywords, 192,656 pages).*[^ah-meta]
- **Do:** write descriptions for pages that earn organic traffic or get shared on social, and always for category and home pages; let the rest be generated.[^ah-meta][^nz-meta] (Until 2026-10-28 this rule covered only pages with traffic or sharing.)
- **Gemini's grounding uses meta descriptions.** Through the Gemini API with Search grounding (115 prompts in EN-US and ES-ES, 3 runs each, 2,580 excerpts), Google passed Gemini one excerpt per result; 7.6 % of excerpts were the meta description, and in 83 % of those it was the only text (median ~24 words vs 105 for body excerpts). Pages represented only by their meta were cited 22 % of the time vs 72 % for body excerpts (same page and prompt: 22 % vs 63 %). The meta share was 43 % on homepages, 23 % on category pages and 3.8 % on articles; category pages were cited 6 % of the time with the meta vs 58 % with body text. *Measured, observational, Gemini API only — not AI Overviews or AI Mode.*[^nz-meta]
- **Read it as a symptom.** The analyst reads a meta excerpt as a sign that the body doesn't match the query: the best body paragraph covered 56 % of query terms on pages served by meta vs 71 % otherwise. That better metas raise citations is untested.[^nz-meta] **Do:** give category and home pages visible body copy that answers their head queries, and write their metas as if they were the only text read — brands, ranges, prices, selection criteria ([category pages](../page-types/category-pages.md), [homepage and brand](../page-types/homepage-and-brand.md)).

  > **Conflict:** Google rewrites most metas and ChatGPT ignores them, yet Gemini's grounding uses them as the only text for some home and category pages — [details](../reference/conflicts.md#do-meta-descriptions-still-matter).
- ChatGPT ignores meta descriptions ([AI assistants](../how-it-works/ai-assistants.md#1-the-opening-of-the-page-carries-it)). For shopping results Google writes its own AI summaries of a listing ("pros, cons", "what to know"), so the product facts on the page and in the feed decide what is said ([product pages](../page-types/product-pages.md)).

## 3. Length
- Across ~900M pages, referring domains rose with length up to ~1,000 words and then fell; organic traffic rose moderately and turned negative above ~2,000 words. *Measured correlation, vendor data, dated 2020.*[^ah-length] Mueller (2019): word count isn't a ranking factor. *Official statement, relayed, dated 2019.*[^ah-length]
- **Do:** no length targets; cover what the top-ranking pages have in common, briefly.[^ah-length] The short-vs-long debate: [conflicts](../reference/conflicts.md#short-or-long-pages).

## 4. Answer-first openings
- Lead with the answer: a definition on informational pages, a recommendation on commercial pages, then detail in inverted-pyramid order; add information gain such as original data. *Practitioner.*[^ah-onpage] This matches what assistants extract from the top of a page ([AI assistants](../how-it-works/ai-assistants.md#1-the-opening-of-the-page-carries-it), [category pages](../page-types/category-pages.md)).
- **Not adopted:** the same checklist suggests FAQ/HowTo schema "might help" AI. FAQ rich results were dropped on 2026-05-07 and adding schema did not raise AI citations ([comparison and guides](../page-types/comparison-and-guides.md#6-faq-content-after-the-rich-result), [third-party presence](../channels/third-party-presence.md#2-most-citations-are-third-party)).[^ah-onpage]

## 5. Headings that stand alone
- Google's Vertex AI Search (Discovery Engine) documentation caps chunks at 500 tokens and can prepend ancestor headings to a chunk; ranking fuses base rank, embeddings, a relevance model, BM25, predicted conversion and freshness, with an "ignore low relevant content" gate. An AI-visibility vendor's analyst (Peec AI) extrapolates this to AI Mode. *Official docs for Vertex AI Search; the link to AI Mode is unconfirmed — Inference.*[^mt-aimode]
- **Do:** write descriptive H2/H3 headings that still make sense when prepended to a chunk on their own ("Sizes and dimensions of <product line>", not "Details"). It helps readers too. *Inference.*

## 6. Tables plus a prose conclusion
- In OpenAI's `o200k_base` tokenizer, markdown tables average 2.7 characters per token vs 5.9 for prose (~2.2× more tokens for the same text); Spanish and French take 1.25–1.29× the tokens of English (German not measured). *From code; the effect on retrieval is untested.*[^mt-token]
- **Do:** keep comparison and spec tables — they serve readers and lexical matching — and repeat the key conclusion in a prose sentence next to the table ("<A> is the lighter option; <B> holds more"). *Inference.*

## 7. The first ~500 words carry grounding
- Across 7,060 queries, 2,275 pages and 883,262 snippets, Google's grounding worked with a fixed budget per query — median 1,929 words (p95 2,798) — split by rank: #1 got 531 words (28 %), #5 got 266 (13 %); the median source got 377 words. Selection levelled off at ~540 words (~3,500 characters), so coverage fell with page length (61 % of pages under 1,000 words vs 13 % of pages over 3,000). It is extractive: sentences are scored against the query, non-adjacent ones joined with "…", with a strong lead bias; the average chunk was 15.5 words. *Measured, private data, directional.*[^dj-chunks]
- **Do:** put the answer, key specs and differentiators in the first ~500 words of product, category and guide pages ([section 4](#4-answer-first-openings), [product pages](../page-types/product-pages.md)).

  > **Conflict:** sources measure different units — ChatGPT's ~202-character search card, OpenAI's 100–200-word windows, Gemini's short cited passages, Google's 15.5-word chunks and ~377 words per source — [details](../reference/conflicts.md#how-much-of-a-page-do-ai-engines-read).

## 8. What counts as a content update
- A Google patent on historical data scores content changes: changes to boilerplate, navigation, ads, scripts, comments and date tags count little; changes to the title and main content count more; for some queries, pages that haven't changed rank better. *Patent, likely expired; the leak supports the concept (several date attributes, a "last significant update").*[^sbs-freshness]
- **Do:** refresh the main content substantively when you update a page (new specs, ranges, prices, sections) and adjust the title when the content changed; don't bump dates without a real change; don't force freshness on evergreen queries ([comparison and guides](../page-types/comparison-and-guides.md)). *Inference.*

## 9. Headlines on guides and editorial pages
*Practitioner, news publishing; transfer to shop guides is inference.*[^gn-article]
- The on-page headline (the H1 and the article's `headline`) can run up to ~110 characters; the `<title>` is a separate element and keeps the ~50–60-character guidance ([section 1](#1-titles)). The first 8 words carry most of the weight.
- Put a one-sentence summary right after the H1, use question-style subheads where readers ask questions, and link consistently to the matching topic hub (for a shop: the category page).
- **Do:** on buying guides and magazine pages, write a descriptive H1 headline with the topic in its first 8 words, a summary sentence under it, and a link to the category hub ([comparison and guides](../page-types/comparison-and-guides.md), [section 4](#4-answer-first-openings)). For Discover, use large images ([Google Discover](../channels/google-discover.md)).

Related: [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md), [comparison and guides](../page-types/comparison-and-guides.md), [keyword research](../channels/keyword-research.md), [internal linking](internal-linking.md), [Search Console](../measure/search-console.md), [conflicts](../reference/conflicts.md#short-or-long-pages).

[^ah-titles]: Ahrefs, updated 2024-11-06: Site Audit data from 1M+ sites, shares at site level (68.54 % rewritten, 63.19 % too long, 32.76 % too short, 5.55 % missing, 3.04 % multiple); ~600 px truncation; Mueller 2021 quote.
[^ah-overopt]: Ahrefs, updated 2024-03-28: prioritise title and meta rewrites by organic traffic.
[^ah-meta]: Ahrefs, 2020: 20,000 keywords, 192,656 pages; rewrite rate 62.78 % (head 59.65 %, long tail 65.62 %); 61.46 % vs 63.69 % by length; 25.02 % without a description.
[^ah-length]: Ahrefs, 2020-07-14: ~900M pages, correlation of word count with referring domains and organic traffic; relays Mueller 2019 on word count.
[^ah-onpage]: Ahrefs, updated 2026-03-05: answer-first openings, inverted pyramid, information gain; its FAQ/HowTo schema suggestion is not adopted here.
[^nz-meta]: Natzir Turrado, 2026-10-22: Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts; meta share 7.6 %, only text in 83 % of those (median ~24 vs 105 words); cited 22 % vs 72 % (same page and prompt 22 % vs 63 %); by page type 43 / 23 / 3.8 %; category pages 6 % vs 58 %; query-term coverage 56 % vs 71 %. Observational; not AI Overviews or AI Mode; the advice is his.
[^sbs-freshness]: SEO by the Sea (Bill Slawski), 2008-09-17: patent US 7,346,839 (likely expired), weighting of content changes by page area; leak attributes (lastSignificantUpdate, several date fields) support the concept. Patent analysis; blog inactive since 2022.
[^mt-token]: Metehan Yeşilyurt, 2026-02-13: `o200k_base` analysis (tables 2.7 vs prose 5.9 characters per token; Spanish/French 1.25–1.29× English). Author works at Peec AI; retrieval effect untested.
[^mt-aimode]: Metehan Yeşilyurt, 2025-11-26: Vertex AI Search / Discovery Engine docs (500-token chunks, ancestor headings, fused ranking signals, low-relevance gate), extrapolated to AI Mode without confirmation. Author works at Peec AI.
[^dj-chunks]: DEJAN, 2025-12-20, restated 2026-06-21: 7,060 queries, 2,275 pages, 883,262 snippets; budget median 1,929 words (p95 2,798), #1 531 words (28 %), #5 266 (13 %), median 377 per source, plateau ~540 words, coverage 61 % (< 1,000 words) vs 13 % (> 3,000), average chunk 15.5 words. Private data, not reproducible.
[^gn-article]: Barry Adams, 2025-02-10: the "perfectly optimised" news article — headline up to 110 characters for the on-page/article headline (not the `<title>`), first 8 words carry most weight, summary sentence after the H1, question subheads, consistent links to topic hubs, large Discover images. Publisher-focused practitioner advice.
[^lr-seoweek]: Lily Ray, 2025-05-08, her summary of SEO Week 2025 talks; this item is Michael King's statement that clicks rose when Search Console keywords were appended to titles. No data given.
