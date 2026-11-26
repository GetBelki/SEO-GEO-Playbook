---
type: Guide
title: ML methods for SEO
description: Machine-learning methods for SEO analysis and where they fail — keyword clustering by embeddings vs SERP overlap, intent classification, internal-link and redirect suggestions, entity salience and NLP APIs, simulated fan-out coverage, topic modelling, rule-based content audits, generated metadata and structured data, and test-vs-control measurement.
tags: [measurement, machine-learning, embeddings, clustering, entities, nlp, content-audit, fan-out, python]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-29T00:00:00Z
sources:
  - id: mlseo-kw-clustering
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/keyword-research/keyword-clustering-serp-vs-semantic/"
    title: "MLforSEO, Keyword clustering: SERP-based vs semantic (2026-10-24; synthetic 160 keywords plus 29 real keywords, Google US desktop)"
  - id: mlseo-intent-classification
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/serp-analysis/search-intent-classification-with-machine-learning-approaches/"
    title: "MLforSEO, Search-intent classification with ML (2026-08-01, updated 2026-10-22; methods, no accuracy figures)"
  - id: mlseo-internal-linking
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/internal-link-analysis/automate-internal-linking-ai/"
    title: "MLforSEO, 10 ways to automate internal linking with AI (2026-10-22; one blog, 12-suggestion LLM test, synthetic DiD demo)"
  - id: mlseo-migration
    resource: "https://www.mlforseo.com/machine-learning-tutorials/fuzzy-matching/seo-site-migration-checklist/"
    title: "MLforSEO, The SEO site migration checklist (2026-10-24; procedure, 43 checks)"
  - id: mlseo-entity-salience
    resource: "https://www.mlforseo.com/machine-learning-tutorials/entity-analysis/entity-salience-check/"
    title: "MLforSEO, Entity SEO: is Google reading your page the way you think? (2026-10-24; 6 live pages, Google NL API v1)"
  - id: mlseo-nlp-apis
    resource: "https://www.mlforseo.com/machine-learning-tutorials/entity-analysis/comparing-nlp-apis-for-entity-and-sentiment-analysis/"
    title: "MLforSEO, Comparing NLP APIs for entity and sentiment analysis (2026-08-01, updated 2026-10-24; one 221-word text; relays a 2023 sentiment study)"
  - id: mlseo-fanout
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/query-fan-out-tool/"
    title: "MLforSEO, Query fan-out tool (2026-10-24; runs 2026-10-25, few seeds)"
  - id: mlseo-bertopic
    resource: "https://www.mlforseo.com/machine-learning-tutorials/topic-modeling-clustering/topic-modeling-for-seo-with-bertopic/"
    title: "MLforSEO, Topic modelling for SEO with BERTopic (2026-08-01, updated 2026-10-24; public datasets)"
  - id: mlseo-content-audit
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/content-audit/content-audit-template/"
    title: "MLforSEO, Content audit template (2026-10-24; rules plus synthetic 24-URL site)"
  - id: mlseo-meta-desc
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/onpage-seo/automatically-generate-meta-descriptions-python/"
    title: "MLforSEO, Automatically generate meta descriptions with Python (2026-10-22; 5 sample pages)"
  - id: mlseo-schema-automation
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/structured-data-audit/structured-data-automation-python/"
    title: "MLforSEO, Structured data automation with Python (2026-10-22; method, a handful of real sites, no counts)"
  - id: mlseo-info-gain
    resource: "https://www.mlforseo.com/ml-fundamentals/what-is-information-gain-in-seo/"
    title: "MLforSEO, What is information gain in SEO? (2026-05-11, updated 2026-10-24; patent explainer)"
---

# ML methods for SEO

Which machine-learning methods help with SEO analysis, what their defaults are, and where they fail. Every item comes from MLforSEO, a site that sells ML-for-SEO courses and promotes its own notebooks; most results use small or synthetic samples.

## Rules
- **Map keywords to pages with SERP overlap, not embeddings alone;** on real keywords the two barely agreed. *Measured, small sample, one case* — [section 1](#1-keyword-clustering)
- **Use a multilingual embedding model for non-English keywords;** the common MiniLM default is English-only. *Practitioner* — [section 1](#1-keyword-clustering)
- **Automate the finding, never the deciding:** a person approves every link, redirect, description and markup change before it goes live. *Practitioner* — [section 3](#3-internal-link-suggestions), [section 10](#10-generated-metadata-and-structured-data)
- **Analyse the main content only** — strip navigation and footer before entity analysis, and treat salience as the API's view, not a Google signal. *Measured, one case; practitioner* — [section 5](#5-entity-salience)
- **Use a task-specific NLP API at scale, not a chatbot,** and test it on your own data first. *Measured, one text; relayed study* — [section 6](#6-entity-extraction-and-sentiment-apis)
- **Rerank before trusting cosine similarity,** and run LLM fan-outs 2–3 times with two providers. *Measured, one case; small sample* — [section 7](#7-simulated-fan-out-coverage)
- **Never let an LLM write prices, dates or authors into live markup;** deterministic code builds the JSON-LD. *Practitioner* — [section 10](#10-generated-metadata-and-structured-data)
- **Measure changes against a control group,** and expect the estimate to be rough. *Practitioner, synthetic validation* — [section 11](#11-measuring-a-change)

## 1. Keyword clustering
- **Embeddings and SERP overlap disagree.** On 29 real keywords (Google US desktop, 2026-10-25) the two clusterings barely agreed (adjusted Rand index 0.04): 12 keywords grouped by embeddings split into 10 SERP clusters. On a synthetic 160-keyword set the index was 0.37. *Measured, small sample, one case.*[^mlseo-kw-clustering]
- **Stated defaults:** semantic clustering with all-MiniLM-L6-v2 and agglomerative clustering at distance threshold 0.40; SERP clustering takes the highest-volume head keyword plus members sharing at least 3 top-10 URLs; a hybrid score weights 60 % SERP and 40 % embedding at threshold 0.60. The thresholds were tuned on short English keywords, and MiniLM is English-only. *Practitioner.*[^mlseo-kw-clustering]
- **Fewer organic URLs per SERP.** The organic top 10 yielded only 7–9 organic URLs per keyword, which matters when an overlap threshold assumes 10. HDBSCAN was rejected as a default (2 clusters and 15 noise points on 160 keywords). SERP data costs about $0.002 per keyword (live) or $0.0006 (standard) at October 2026 list prices. *Measured, small sample; vendor pricing.*[^mlseo-kw-clustering]
- Applied to keyword mapping: [keyword research](../channels/keyword-research.md#10-embedding-clusters-and-serp-clusters-disagree).

## 2. Intent classification
- **Four approaches:** regex rules (match whole words: "top" otherwise matches "laptop"), SERP-feature mapping (60+ features; reflects Google's choices, not the user's), zero-shot classification with BART, and entity-based rules (e.g. consumer goods or prices → transactional). About 1,700 keywords ran in under 3 minutes on a GPU with a transformer. *Practitioner.*[^mlseo-intent-classification]
- **No accuracy figures** were reported for any approach, and commercial tools don't disclose how they label intent. Hand-label a sample before trusting any of them. *Practitioner.*[^mlseo-intent-classification]

## 3. Internal-link suggestions
- Paragraph-level embeddings, Search Console striking-distance queries and LLM-written anchors can suggest links; keep only pairs in the top 10 % of the site's own similarity distribution and skip pairs at 0.95 or above (near-duplicates). *Practitioner.*[^mlseo-internal-linking]
- Weak and orphan pages by the definitions used: weak = exactly one contextual inlink; deep = more than 4 clicks from the start; orphans = URLs in the sitemap, Search Console or analytics but not in the crawl. Lower a crawler's semantic-similarity default of 0.95 (meant for duplicates) when looking for link candidates. *Practitioner.*[^mlseo-internal-linking]
- Full method and the LLM-anchor test: [internal linking](../technical/internal-linking.md#13-automating-link-suggestions).

## 4. Redirect mapping
- Fuzzy matching (Levenshtein) on URL, title, H1, H2 and meta description, scored 0–100, with matches below 70 flagged for review; even a 71-score match could be the wrong page. *Practitioner.*[^mlseo-migration] Thresholds and launch checks: [internal linking](../technical/internal-linking.md#14-redirect-mapping-by-fuzzy-matching), [migration](../situations/migration.md).

## 5. Entity salience
- **Most pages weren't read as intended.** With Google's Natural Language API v1 (v2 has no salience field) on 6 live pages (2026-10-25), only 2 scored 3 of 3 on the author's rubric (target entity most salient, linked to the Knowledge Graph, first mention in the first 10 % of text); 4 scored 1 of 3 — e.g. "Google" (0.39) outranked the target (rank 7, 0.05), or the topic split across 24 entity rows. *Measured, small sample, one day.*[^mlseo-entity-salience]
- **Boilerplate distorts it.** On one page, menu entities outranked the page's topic when the whole page was analysed instead of the main text. Extract the main content (e.g. with trafilatura) first. *Measured, one case.*[^mlseo-entity-salience]
- **Limits:** salience is the API's view of the submitted text, not a confirmed Search or LLM signal; extraction can miss tabs, accordions and JavaScript content; the rubric is the author's own, and no after-edit results exist yet. Billing is per 1,000-character unit, first 5,000 a month free. *Practitioner.*[^mlseo-entity-salience]

## 6. Entity extraction and sentiment APIs
- **Entities.** On one 221-word bio (early 2025, one annotator), Google NL found all 13 core entities but 31 of its 59 unique entities were noise; ChatGPT o1 found 13 of 13 in 14 rows; IBM Watson 7 of 13; Gemini declined. Chatbots invented entities and changed their output on re-runs. *Measured, one text.*[^mlseo-nlp-apis]
- **Sentiment.** Against human labels on ~6,000 comments (Bergamaschi 2023, relayed), Amazon Comprehend agreed 71.8 %, Google 70.3 %, IBM 67.1 %; all three agreed with each other and the human label on only 43.3 %. IBM Watson NLU was deprecated on 2026-07-31. *Measured, relayed.*[^mlseo-nlp-apis]
- **Do:** test an API on a hand-labelled sample of your own text (e.g. product reviews) before using it at scale.

## 7. Simulated fan-out coverage
- **Method:** split the page into 40–160-word passages, retrieve the top 5 per sub-query by cosine (multi-qa-MiniLM-L6-cos-v1) and rerank with a cross-encoder (ms-marco-MiniLM-L6-v2). Covered = rerank score ≥ 6 or cosine ≥ 0.75; partial = 3–6 or 0.60–0.75; gap below. The thresholds were set by reading samples. *Practitioner, small sample.*[^mlseo-fanout]
- **Cosine alone misleads.** It rated "is buying a used espresso machine worth it" as covered on a page that never mentions used machines; the reranker caught it. Read 10–15 rows before adjusting thresholds. *Measured, one case.*[^mlseo-fanout]
- **LLM fan-outs vary.** For the same seed, 20 sub-queries each, one provider gave 7 covered / 6 partial / 7 gaps and another 8 / 9 / 3; rule-based sub-queries found no gaps. Google doesn't publish its fan-out queries. *Measured, small sample.*[^mlseo-fanout] Applied: [keyword research](../channels/keyword-research.md#11-checking-a-pages-fan-out-coverage), [test 13](diagnostic-tests.md#13-fan-out-coverage).

## 8. Topic modelling
- **BERTopic on short texts:** on 1,373 titles it found 7 topics with coherence (c_v) 0.41 and 7 % unassigned; NMF also scored 0.41, LDA 0.33. On ~3,400 posts, outlier reduction took unassigned from 8 % to 0 %. A minimum cluster size of 15 merged unrelated topics; 30 worked. It is weak below ~1,000 documents. *Measured, public dataset.*[^mlseo-bertopic]
- **Do:** hand-label 50–100 documents to check the topics, and don't over-read small coherence differences.[^mlseo-bertopic]

## 9. Content audits by rules
- **Rule order, first match wins:** 3xx → redirect; 4xx/5xx → redirect if it has clicks or referring domains, else prune; noindex or canonicalised → keep; merge if it overlaps a stronger page (semantic similarity ≥ 0.9 or ≥ 90 % near-duplicate by MinHash) and has no key events; update if decaying, in striking distance or thin with demand; prune if under 10 clicks, 200 impressions and 20 sessions with no key events; else keep. *Practitioner.*[^mlseo-content-audit]
- Decay and striking-distance definitions: [Search Console](search-console.md#18-decay-and-striking-distance-from-two-periods); joining the data per URL: [analytics](analytics.md#19-joining-crawl-search-console-and-analytics-per-url).
- **Information gain** is a patent concept (US20200349181A1: scoring documents by novelty relative to what the user already saw); the article says the patent doesn't confirm use in Search, and no thresholds exist. The practical check is an entity frequency map of the top 10–20 pages and what your piece adds. *Patent.*[^mlseo-info-gain]

## 10. Generated metadata and structured data
- **Meta descriptions:** check length (70–155 characters), numbers and capitalised names that don't appear in the page text, a missing top query, duplicates across URLs and low similarity to the page, and keep a required human "Approved" column. A small open model exceeded the length on 3 of 5 pages even after re-prompting; checks flag problems but don't prove quality. *Practitioner, small sample.*[^mlseo-meta-desc]
- **Structured data:** never let an LLM generate prices, dates or authors for live pages. Use it only to classify page types or draft column-to-property mappings; deterministic code builds JSON-LD as one `@graph` linked by `@id`. Validate syntax, schema.org vocabulary, Google's required properties, and that names and prices appear in the visible text. *Practitioner.*[^mlseo-schema-automation]

## 11. Measuring a change
- Compare test and control page groups with difference-in-differences, about a week after the change. On synthetic data with a planted 15 % uplift the script reported +11.8 points, so it under-estimated the effect. *Practitioner, synthetic validation.*[^mlseo-internal-linking] Procedure: [test 33](diagnostic-tests.md#33-test-vs-control-for-site-changes).

## Checklist
- [ ] Keyword-to-page mapping uses SERP overlap; embeddings only pre-group.
- [ ] Embedding model fits the language of the keywords.
- [ ] Intent labels checked against a hand-labelled sample.
- [ ] Every suggested link, redirect, description and markup change approved by a person.
- [ ] Entity analysis runs on main content only; salience not reported as a ranking signal.
- [ ] NLP API tested on your own labelled text before scaling.
- [ ] Fan-out coverage uses a reranker; LLM sub-queries run 2–3 times with two providers.
- [ ] Content-audit thresholds written down and seasonality checked before pruning.
- [ ] Changes rolled out with a control group.

Related: [keyword research](../channels/keyword-research.md), [internal linking](../technical/internal-linking.md), [diagnostic tests](diagnostic-tests.md), [Search Console](search-console.md), [analytics](analytics.md), [migration](../situations/migration.md).

[^mlseo-kw-clustering]: MLforSEO (Lazarina Stoy), 2026-10-24: 29 real keywords (Google US desktop via DataForSEO, 2026-10-25), ARI 0.04; synthetic 160-keyword set, ARI 0.37; default models and thresholds; 7–9 organic URLs per top 10; DataForSEO list prices.
[^mlseo-intent-classification]: MLforSEO (Lazarina Stoy), 2026-08-01, updated 2026-10-22: regex, SERP-feature, zero-shot and entity-based intent methods; no accuracy figures; ~1,700 keywords in under 3 minutes on a GPU.
[^mlseo-internal-linking]: MLforSEO (Lazarina Stoy), 2026-10-22: one 68–79-post blog; embedding and Search Console link suggestions; weak, deep and orphan definitions; synthetic difference-in-differences demo (+11.8 points vs a planted 15 %).
[^mlseo-migration]: MLforSEO (Lazarina Stoy), 2026-10-24: fuzzy redirect mapping on URL, title, H1, H2, description; 0–100 scores, review below 70; 71-score wrong match example.
[^mlseo-entity-salience]: MLforSEO (Lazarina Stoy), 2026-10-24: 6 live pages, one day (2026-10-25), Google NL API v1 analyzeEntities; 2 of 6 scored 3/3; navigation distortion on one page; the post's navigation salience values are internally inconsistent.
[^mlseo-nlp-apis]: MLforSEO (Lazarina Stoy), 2026-08-01, updated 2026-10-24: one 221-word text, early 2025, single annotator; relays Bergamaschi 2023 (~6,000 comments) for sentiment accuracy; IBM Watson NLU deprecated 2026-07-31.
[^mlseo-fanout]: MLforSEO (Lazarina Stoy), 2026-10-24: passage retrieval and cross-encoder reranking; thresholds set by reading samples; runs 2026-10-25 on a few seeds, 20 sub-queries per provider.
[^mlseo-bertopic]: MLforSEO (Lazarina Stoy), 2026-08-01, updated 2026-10-24: public datasets, 1,373 titles and ~3,400 posts; c_v 0.41 (BERTopic, NMF) vs 0.33 (LDA); outlier reduction 8 % → 0 %.
[^mlseo-content-audit]: MLforSEO (Lazarina Stoy), 2026-10-24: rule-based audit template on a synthetic 24-URL site; first-match rule order and thresholds.
[^mlseo-meta-desc]: MLforSEO (Lazarina Stoy), 2026-10-22: 5 sample pages; QA checks; open model over length on 3 of 5.
[^mlseo-schema-automation]: MLforSEO (Lazarina Stoy), 2026-10-22: method on "a handful of real sites", no counts; LLM only for classification and mapping; validation layers.
[^mlseo-info-gain]: MLforSEO (Lazarina Stoy), 2026-05-11, updated 2026-10-24: explainer of patent US20200349181A1; no confirmed use in Search; no thresholds.
