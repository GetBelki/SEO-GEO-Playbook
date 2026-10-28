---
type: Guide
title: Keyword research
description: How far to trust search volume, valuing topics by the traffic of the page that ranks, long-tail and zero-volume keywords, multi-facet intent, clustering and keyword-to-URL mapping, secondary keywords, customer vocabulary and complementary sub-needs, seeding AI prompts from Search Console, how reliable AI classification is, and support-type volume as a bug report.
tags: [seo, keyword-research, search-volume, long-tail, intent, clustering, keyword-mapping, cannibalisation, synonyms, fan-out, embeddings, classification, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: ah-volume
    resource: "https://ahrefs.com/blog/keyword-search-volume/"
    title: "Ahrefs, Keyword search volume (2021-12-01)"
  - id: ah-secondary
    resource: "https://ahrefs.com/blog/secondary-keywords/"
    title: "Ahrefs, Secondary keywords (2026-03-06)"
  - id: ah-longtail
    resource: "https://ahrefs.com/blog/long-tail-keywords/"
    title: "Ahrefs, Long-tail keywords (updated 2026-05-27; US database 2.3B keywords)"
  - id: ah-zero-volume
    resource: "https://ahrefs.com/blog/zero-volume-keywords/"
    title: "Ahrefs, Zero-volume keywords (2022-10-21; small own-blog test)"
  - id: ah-clustering
    resource: "https://ahrefs.com/blog/keyword-clustering/"
    title: "Ahrefs, Keyword clustering (2023-10-31) and keyword mapping (2023-11-30)"
  - id: ah-topics
    resource: "https://ahrefs.com/blog/topics-not-keywords/"
    title: "Ahrefs, Topics not keywords (2026-03-04)"
  - id: ah-ai-keywords
    resource: "https://ahrefs.com/blog/ai-keyword-research/"
    title: "Ahrefs, Keyword research with AI (2026-04-30)"
  - id: ah-intent
    resource: "https://ahrefs.com/blog/keyword-intent/"
    title: "Ahrefs, Keyword intent (2026-03-13) and buyer-intent keywords (2024-07-30)"
  - id: ah-aio-triggers
    resource: "https://ahrefs.com/blog/ai-overview-triggers/"
    title: "Ahrefs, What triggers AI Overviews (2025-11-10; 146,122,391 US desktop SERPs, Sept 2025)"
  - id: sbs-rewrite
    resource: "https://www.seobythesea.com/2013/12/rewrite-search-terms/"
    title: "SEO by the Sea, How Google may rewrite queries (2013-12-08; patent US 8,600,973, filed 2012-01-03)"
  - id: dj-fanout2
    resource: "https://dejan.ai/blog/fanout2/"
    title: "DEJAN, Fanout V2: complementary query sets (2026-09-16; summary of Google Research arXiv 2603.06397)"
  - id: mt-gscprompts
    resource: "https://metehan.ai/blog/stop-guessing-which-prompts-to-track/"
    title: "Metehan Yeşilyurt, Choosing prompts to track from Search Console (2025-12-12; method)"
  - id: ls-semkw
    resource: "https://lazarinastoy.com/semantic-keyword-research-ai-era/"
    title: "Lazarina Stoy, AI-powered semantic keyword research (2026-10-25; talk, framework)"
  - id: ls-mlday
    resource: "https://lazarinastoy.com/how-to-incorporate-machine-learning-in-your-seo-day-to-day/"
    title: "Lazarina Stoy, ML in your SEO day-to-day (2026-10-25; cites arXiv 2406.08660, 2408.04667)"
  - id: ls-audit
    resource: "https://lazarinastoy.com/automate-content-audit-machine-learning/"
    title: "Lazarina Stoy, Automate your content audit with ML (2026-10-25; workflow)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: ja-bugreport
    resource: "https://www.jonoalderson.com/conjecture/search-volume-bug-report/"
    title: "Jono Alderson, Sometimes search volume is a bug report (2026-10-17; argument)"
---

# Keyword research

How far to trust keyword data, how to value and group keywords, and how to map them to URLs on an ecommerce site. Confidence labels follow the [scale](../reference/sources-and-confidence.md). Sections 1–7 rest mainly on Ahrefs, a tool vendor with an interest in its own metrics, plus practitioner and relayed academic work on classification; section 8 adds a Google patent and a Google Research paper; section 9 is an argument without data.

## Rules
- **Treat Keyword Planner volume as a rough, merged, annual estimate.** Check it against Search Console impressions where you already rank 1–3, and read the monthly series, not the yearly average. *Measured, vendor data, sample not stated* — [evidence](#1-search-volume-is-an-estimate)
- **Value a topic by the organic traffic its current top page earns**, or the clicks of your own equivalent page, not by the volume of one keyword. *Practitioner, vendor data* — [evidence](#2-value-topics-by-traffic-not-volume)
- **Put supporting long-tail keywords on the parent page; give a long-tail keyword its own page only when the SERP shows its own topic.** Target zero-volume keywords only if they are a distinct topic, high-value commercial, or emerging. *Practitioner; zero-volume test dated 2022* — [evidence](#3-long-tail-and-zero-volume-keywords)
- **Tag every mapped keyword with an intent checked against the SERP, one intent per page**, labelled by its dominant intent; add facets (format, knowledge level, persona, context) where they change the page. Keywords that show Shopping ads are category or product targets. *Practitioner* — [evidence](#4-intent)
- **Keep a keyword → URL map with one primary cluster per URL**, and check `site:` and Search Console before creating a page, so you don't build a second page for what Google already ranks one page for. *Practitioner, dated 2023* — [evidence](#5-clustering-and-mapping)
- **On categories: primary term in title and H1, the main facet variants in H2s**; 3–5 secondary keywords placed deliberately. *Practitioner* — [evidence](#6-secondary-keywords)
- **Use AI for ideation and deduplication, fed with Search Console, Ads and tool exports, never for volumes or difficulty; cluster with embeddings and a fixed algorithm and let an LLM only name the clusters.** Check any LLM classifier against ~100 hand-labelled pages first. *Practitioner; arXiv studies relayed* — [evidence](#7-ai-assisted-research)
- **Use the customers' own words for categories and filters, and cluster by complementary sub-need, not only by synonym**: cover the accessory and companion categories a buyer needs alongside the head term. *Patent; Google Research paper, production use unconfirmed* — [evidence](#8-customer-vocabulary-and-complementary-sub-needs)
- **Tag support-type clusters (returns, delivery, order tracking, contact) and route them to their owners**; don't report their decline as an SEO loss. *Practitioner argument; the shop examples are inference* — [evidence](#9-support-type-volume-is-a-bug-report)

## 1. Search volume is an estimate
- Keyword Planner volume was "roughly accurate" in only 45 % of cases when compared with the Search Console impressions of pages ranking #1. *Measured, vendor data, sample not stated, dated 2021.*[^ah-volume]
- It merges variants: six phrasings of one query can share one number. Treat grouped numbers as cluster figures, not per-keyword figures.[^ah-volume]
- Annual averages hide seasonality, and volume counts searches, not people.[^ah-volume] Read monthly series before planning seasonal pages ([seasonal peaks](../situations/seasonal-peaks.md)).
- **Do:** validate volumes with Search Console impressions for keywords where you already hold positions 1–3 ([Search Console](../measure/search-console.md)).

## 2. Value topics by traffic, not volume
- The average #1 page also ranks for ~1,000 other keywords (an earlier Ahrefs study), so one keyword's volume understates what a topic is worth. In one case, a query with 27× the volume sent about half the traffic of another. *Vendor data, single example.*[^ah-volume][^ah-secondary]
- **Do:** value a topic by the organic traffic of the URL that ranks first for it today, or by the Search Console clicks of an equivalent page you already have. *Practitioner.*
- **Topics, not keywords.** One B2B uniforms brand covered ~2,500 keywords with 114 ecommerce pages and held topic leadership for ~2 years, until a redesign launched without SEO review. One ~1,000-word article ranked for 2,500 keywords, 473 AI Overview queries and 279 ChatGPT prompts, while another site's 60+ thin pages on the topic totalled 266 keywords. *Practitioner cases, vendor data.*[^ah-topics] One strong page per sub-topic beats many thin ones — see also how Google scores sections ([Google ranking](../how-it-works/google-ranking.md#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)).

## 3. Long tail and zero-volume keywords
- ~93 % of the 2.3B keywords in Ahrefs' US database have fewer than 10 monthly searches; 17,730 exceed 100k. ~15 % of daily Google searches are new (Google, reconfirmed 2025). More than 95 % of conversational long-tail queries have no measurable volume (Seer, relayed). *Vendor data; the Google and Seer figures relayed.*[^ah-longtail] A conference talk (Michael King) gave the same figure for AI fan-out queries: 95 % have no monthly search volume. *Practitioner, relayed; confirms the Seer figure.*[^lr-techseo]
- **Two kinds of long tail.** A *supporting* long-tail keyword shares its parent topic and belongs on the parent page; a *topical* long-tail keyword is its own topic and gets its own page. The SERP tells you which: if the same pages rank for parent and long tail, it's supporting.[^ah-longtail]
- **Zero-volume keywords.** In a small test on Ahrefs' own blog, keywords ranking in the top 5 with an estimate of ≤ 10 averaged 11.3 impressions; fewer than 1 % drove more than 100. *Measured, small sample, dated 2022.*[^ah-zero-volume] Target them only if they are a distinct topic, high-value commercial, or emerging.
- **Prompts have no search volume.** AI-assistant prompts are long and conversational and show up in no keyword tool; build the prompt set from customer questions and Search Console queries instead ([AI visibility tracking](../measure/ai-visibility-tracking.md#7-how-to-track)). *Inference from the Seer figure above.*
- **Seed prompts from Search Console.** Take queries with ≥ 1,000 impressions and rewrite them as conversational prompts. Search Console can also show bursts of bot-like LLM queries — one post got ~125k impressions and no clicks from long natural-language queries; flag such zero-click bursts as probable machine traffic, not demand. *Practitioner, single example; the author works at an AI-visibility vendor (Peec AI).*[^mt-gscprompts]

## 4. Intent
- Classify every keyword as informational, commercial, transactional or navigational, plus local and branded flags; validate against the live SERP, not the wording alone.[^ah-intent]
- **Mixed intent:** serve one intent per page, or split into two pages when the SERP shows both.[^ah-intent]
- **Multi-facet intent.** Beyond the four classes, tag the facets that change what the page must offer: main category, desired format, knowledge level, persona, implicit struggle and context. Classify in three passes — rules first, then ML or zero-shot classification, then a human-checked sample — and keep only the dominant intent as the label. *Practitioner.*[^ls-semkw]
- **Buyer signals:** modifiers (buy, price, best, review, alternatives, near me), Shopping ads on the SERP, high CPC.[^ah-intent] Keywords with Shopping ads are category or product targets ([category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md)).
- **AI Overviews follow intent.** They showed on 21.4 % of informational SERPs, 4.3 % commercial, 2.1 % transactional and 0.9 % navigational (the article's body text says "0.09%"; its table says 0.9 %). *Measured, vendor data, Sept 2025.*[^ah-aio-triggers] Full trigger data: [Google AI features](../how-it-works/google-ai-features.md).

## 5. Clustering and mapping
- **Cluster by SERP overlap or shared parent topic**, not by wording. Building separate pages for keywords Google already ranks the same pages for is "a waste of time".[^ah-clustering] *Practitioner, plus one tool comparison on 4,703 keywords, dated 2023.*
- **One URL per intent.** Each URL owns one primary cluster; for each topic decide Create, Optimize or No action.[^ah-clustering]
- **Cannibalisation check.** The source gives no process. *Inference:* before creating a page, search `site:` for the topic and check Search Console for queries where two of your URLs swap impressions; if one exists, optimise it instead.
- **Exclude brand names and years** when clustering, so seasonal and branded variants fold into the evergreen topic.[^ah-topics]
- **Cross-check with Search Console query groups.** Search Console Insights added AI-driven query groups in late October 2025, and fan-out queries carry no volume to cluster by; compare the query groups with your own clusters and look at where they split differently. *Practitioner.*[^ls-semkw]

## 6. Secondary keywords
- Place 3–5 secondary keywords deliberately: in H2/H3 headings, section openers and accurate image alt text, and at most 1–2 in the meta description. The title keeps the primary keyword.[^ah-secondary]
- **On categories:** primary term in title and H1, the main facet variants (material, size, use) as H2s. *Practitioner, applied to categories.*[^ah-secondary] Title rules: [titles and snippets](../technical/titles-and-snippets.md).

## 7. AI-assisted research
- Without live data, LLMs fabricate volume, keyword difficulty and trends.[^ah-ai-keywords]
- Use AI for ideation, deduplication, clustering and intent sorting; humans decide fit and cuts. Feed it Search Console, Ads and keyword-tool exports rather than asking it for numbers. *Practitioner.*[^ah-ai-keywords] Until 2026-10-28 the rule above let an LLM do clustering and intent sorting itself; the reliability findings below narrow it to naming clusters and checked classification.
- **LLM classification is not reliable on its own.** Smaller fine-tuned models beat zero-shot ChatGPT and Claude on every text-classification task tested (arXiv 2406.08660); LLM accuracy varied "by up to 15%" between identical "deterministic" runs (arXiv 2408.04667). Structured outputs guarantee the format, not correctness. *arXiv studies, relayed by a practitioner.*[^ls-mlday]
- **Do:** cluster with embeddings and a fixed algorithm, and let an LLM only name the clusters. Before using an LLM on a custom taxonomy (intent classes, page types), check it against ~100 hand-labelled pages; set confidence thresholds (e.g. 70 %, 85 %) and review everything below them by hand; save the model version and the labelled check set so the check can be rerun. *Practitioner.*[^ls-mlday][^ls-audit]

## 8. Customer vocabulary and complementary sub-needs
- **Synonyms have to be used to survive.** A Google patent describes query-rewrite rules that substitute synonyms, and prunes a rule when the substituted term rarely appears in the returned pages or the rewritten results get no clicks. *Patent; use in today's systems unknown.*[^sbs-rewrite] **Do:** use the customers' vocabulary variants (trade term, everyday term, regional term) in category copy and filter labels, so the pages carry the words people actually search.
- **Fan-out favours complementary, not paraphrased, sub-queries.** A Google Research paper trains query generation that penalises paraphrase collapse and rewards diversity, groundedness and alignment with the root query; the resulting sub-queries become complementary product categories (for a camping kit: shelter, sleep, cooking, lighting). *Google Research paper, summarised by DEJAN; production use unconfirmed.*[^dj-fanout2]
- **Do:** when clustering, group by distinct sub-need and adjacent category as well as by SERP overlap ([section 5](#5-clustering-and-mapping)); from category hubs, cover and link the accessory and companion categories a buyer needs ([internal linking](../technical/internal-linking.md), [category pages](../page-types/category-pages.md)). *Inference.*

## 9. Support-type volume is a bug report
- Some query volume is caused by the business itself: hidden contact details, unclear cancellation, pricing or compatibility information. A "double the volume" test — would you want twice as many of these searches? — separates demand from friction. Fixing the cause can lower traffic. *Practitioner argument, no data.*[^ja-bugreport]
- **Do:** tag support-type clusters (for a shop: returns, delivery, order tracking — *inference*), route them to the team that owns the cause, and don't report their decline as an SEO loss ([analytics](../measure/analytics.md)). *Inference.*

Related: [category pages](../page-types/category-pages.md), [comparison and guides](../page-types/comparison-and-guides.md), [titles and snippets](../technical/titles-and-snippets.md), [internal linking](../technical/internal-linking.md), [Google AI features](../how-it-works/google-ai-features.md), [AI visibility tracking](../measure/ai-visibility-tracking.md), [new market](../situations/new-market.md).

[^ah-volume]: Ahrefs, 2021-12-01: Keyword Planner vs GSC impressions of #1 pages ("roughly accurate" 45 %, sample not stated); variant merging; seasonality; 27× volume vs ~half the traffic example. Vendor interest in its own volume metric.
[^ah-secondary]: Ahrefs, 2026-03-06: secondary-keyword placement (3–5, H2/H3, openers, alt text, ≤ 1–2 in meta description); traffic potential over volume.
[^ah-longtail]: Ahrefs, updated 2026-05-27: US database of 2.3B keywords (~93 % under 10 searches, 17,730 over 100k); relays Google's ~15 % new queries and Seer's > 95 % no-volume conversational queries; supporting vs topical long tail.
[^ah-zero-volume]: Ahrefs, 2022-10-21: small test on its own blog; top-5 keywords with estimate ≤ 10 averaged 11.3 impressions, < 1 % drove > 100.
[^ah-clustering]: Ahrefs, 2023-10-31 and 2023-11-30: clustering by SERP overlap / parent topic, one tool comparison on 4,703 keywords; keyword mapping with Create / Optimize / No action; no cannibalisation process.
[^ah-topics]: Ahrefs, 2026-03-04: B2B uniforms case (~2,500 keywords, 114 pages, ~2 years, lost after an unreviewed redesign); one article vs 60+ thin pages (2,500 vs 266 keywords; 473 AIO queries, 279 ChatGPT prompts); exclude brands and years.
[^ah-ai-keywords]: Ahrefs, 2026-04-30: LLMs invent volume, KD and trends without live data; AI for ideation, dedup, clustering, intent. Promotes Ahrefs' AI features.
[^ah-intent]: Ahrefs, 2026-03-13 and 2024-07-30: four intents plus local and branded; SERP validation; buyer modifiers, Shopping ads, CPC as signals.
[^ah-aio-triggers]: Ahrefs, 2025-11-10: 146,122,391 US desktop SERPs, Sept 2025; AIO on 20.5 % overall, by intent 21.4 / 4.3 / 2.1 / 0.9 % (text says 0.09 % for navigational).
[^sbs-rewrite]: SEO by the Sea (Bill Slawski), 2013-12-08: patent US 8,600,973 (filed 2012-01-03) on synonym substitution rules, pruned when the substitute rarely appears in results or rewritten results get no clicks. Patent analysis; blog inactive since 2022.
[^dj-fanout2]: DEJAN, 2026-09-16: summary of Google Research arXiv 2603.06397 (R4T; penalises paraphrase collapse, rewards diversity (Vendi), groundedness, root alignment; camping-kit example; diffusion retriever 12–20× faster with 128-dim Matryoshka embeddings). Research, not confirmed in production.
[^mt-gscprompts]: Metehan Yeşilyurt, 2025-12-12: method for seeding prompt sets from Search Console queries (≥ 1,000 impressions, rewritten conversationally); one post with ~125k impressions and no clicks from bot-like LLM queries. Author works at Peec AI.
[^ls-semkw]: Lazarina Stoy, 2026-10-25 (republished talk): multi-facet intent (main category, format, knowledge level, persona, implicit struggle, context), rules → ML/zero-shot → human-checked sample, dominant intent only; fan-out queries have no volume; Search Console Insights AI-driven query groups since late October 2025. Links to her paid courses.
[^ls-mlday]: Lazarina Stoy, 2026-10-25: relays arXiv 2406.08660 (smaller fine-tuned models beat zero-shot ChatGPT and Claude on every classification task tested) and arXiv 2408.04667 (accuracy varied "by up to 15%" across identical runs); structured outputs ≠ correctness; check against ~100 hand-labelled pages. Primary papers not read here.
[^ls-audit]: Lazarina Stoy, 2026-10-25: content-audit workflow with confidence thresholds (e.g. 70 %, 85 %) and manual review below them; save the model version and a labelled check set.
[^lr-techseo]: Lily Ray, 2025-12-05, her summary of Tech SEO Connect 2025 talks; this item is Michael King's statement that 95 % of fan-out queries have no monthly search volume. Not checked against the slides.
[^ja-bugreport]: Jono Alderson, 2026-10-17: argument that some search volume signals product or service friction (contact, cancellation, pricing, compatibility); "double the volume" test; fixing the cause can lower traffic. No data.
