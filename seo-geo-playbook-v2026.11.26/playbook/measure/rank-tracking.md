---
type: Checklist
title: Rank tracking
description: Why rank trackers drift from Search Console — personalisation, generated and "poisoned" result pages, shallower depth after num=100, AI Overviews that change every ~2 days, AIO citations drifting away from the organic top 10 and cited vs ranking domains across keywords — and how to use them as a trend, not a truth.
tags: [measurement, rank-tracking, search-console, ai-overviews, ai-mode, caveats]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: intent-engine
    resource: "https://think.resoneo.com/google-intent-engine/"
    title: "Resoneo, What Google is building (Jun 2026; decompiled Google app)"
  - id: ipr-generative
    resource: "https://ipullrank.com/generative-serps"
    title: "iPullRank, Generative SERPs (2026-10-15; Google Research paper; Nozzle, 27.5M results)"
  - id: brodie-num100
    resource: "https://brodieclark.com/the-great-decoupling-num100/"
    title: "Brodie Clark, The Great Decoupling and num=100 (updated 2025-09-26; cites LOCOMOTIVE, ThotSEO, JetOctopus samples)"
  - id: ah-aio-change
    resource: "https://ahrefs.com/blog/ai-overview-change/"
    title: "Ahrefs, How often AI Overviews change (2025-11-11; 43,000+ keywords)"
  - id: ls-serp
    resource: "https://lazarinastoy.com/how-to-incorporate-machine-learning-into-your-serp-analysis/"
    title: "Lazarina Stoy, ML in SERP analysis (2026-10-25; one-keyword time series)"
  - id: mlseo-aio-tracker
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/ai-search-optimisation/track-ai-overviews-python/"
    title: "MLforSEO, How to track AI Overviews for your keywords (2026-10-24; 29-keyword run, US desktop)"
  - id: mlseo-kw-clustering
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/keyword-research/keyword-clustering-serp-vs-semantic/"
    title: "MLforSEO, Keyword clustering: SERP-based vs semantic (2026-10-24; synthetic 160 keywords plus 29 real keywords)"
  - id: sp-track-ai-visibility
    resource: "https://sparktoro.com/blog/office-hours-can-you-actually-track-ai-visibility/"
    title: "SparkToro, Office Hours: Can you actually track AI visibility? (2026-05-07; SparkToro x Gumshoe.ai, ~600 volunteers, 142 prompts, 994 runs)"
---

# Rank tracking

What a rank tracker's position still means when no single results page exists, and how to use trackers without being misled.

## Rules
- **Keep Search Console as the source of truth for position** and use trackers as a trend. *From code* — [section 1](#1-no-single-reference-results-page), [section 4](#4-how-to-use-trackers)
- **Take several captures a day and drop outliers** before reading a tracker's movement. *Measured* — [section 2](#2-generated-result-pages-and-poisoned-captures)
- **If Search Console holds while the tracker drops, question the tracker** before the page. *Measured* — [section 2](#2-generated-result-pages-and-poisoned-captures)
- **Don't read tracker gains or losses beyond the top 30 across Sept 2025;** the depth changed. *Measured, relayed* — [section 3](#3-tracker-depth-after-num100)
- **Track organic position, AI Overview citation and AI Mode citation as separate series** for important pages; the overlap between AIO citations and the organic top 10 drifts. *Inference; one-keyword anecdote* — [section 4](#4-how-to-use-trackers), [section 6](#6-aio-citations-drift-from-the-organic-top-10)
- **Never read AI Overview presence or citation from one capture;** sample every 2–3 days and report share across many keywords. *Measured, vendor data* — [section 5](#5-ai-overviews-change-every-2-days)

## 1. No single reference results page
- Personalisation (57 on-device signals, LLM rerankers) means there is no single reference results page. Rank trackers drift further from Search Console's average position. *From code.*[^intent-engine] How the surfaces differ: [Google ranking](../how-it-works/google-ranking.md) and [Google AI features](../how-it-works/google-ai-features.md).

## 2. Generated result pages and poisoned captures
- **Generated result pages.** A Google Research paper reports generated results pages preferred over the top result 90 % of the time on LMArena prompts (73.5 % on information-seeking prompts).[^ipr-generative]
- **Rank trackers can be fed bad pages.** One vendor's anomalous ("poisoned") captures rose from 0.17 % to 8.0 % of results pages after 13 Sep 2026; on those, only 20.7 % of organic results matched a normal capture (88.5 % otherwise), while Shopping units held at 92.2 %. That Google degrades what suspected scrapers see is an inference.[^ipr-generative]
- Take several captures a day, drop outliers, and check trackers against Search Console: if Search Console holds while the tracker drops, question the tracker.

## 3. Tracker depth after num=100
- After Google stopped supporting `&num=100` (from ~10 Sept 2025), rank trackers cut their depth to about the top 30.[^brodie-num100] What the change did to Search Console impressions and position: [Search Console](search-console.md#2-num100-from-10-sept-2025).

## 4. How to use trackers
- Several captures a day; drop outliers; validate against Search Console ([section 2](#2-generated-result-pages-and-poisoned-captures)).
- **Do:** for important guides, track organic position, AIO citation and AI Mode citation separately. Keep Search Console as the source of truth; use trackers as a trend.
- Tracking AI assistants instead of Google results is prompt tracking: [test 9](diagnostic-tests.md#9-prompt-tracking-per-engine). AI trackers that query an API don't see what app users see (fewer sources, different citations), the same way a SERP scraper doesn't see a personalised results page: [AI-visibility tracking](ai-visibility-tracking.md#10-what-prompt-trackers-dont-tell-you).

## 5. AI Overviews change every ~2 days
- Across 43,000+ keywords observed at least 16 times each (~1 month), AI Overview text changed in 70 % of consecutive observations, with an average persistence of 2.15 days; consecutive answers shared only 54.5 % of their cited URLs, though their meaning stayed close (semantic similarity 0.95). *Measured, vendor data.*[^ah-aio-change]
- **Do:** treat a single AIO capture as anecdote. Sample every 2–3 days, report AIO presence and citation as a share across many keywords over a period, and don't attribute one lost citation to a page change ([Google AI features](../how-it-works/google-ai-features.md#9-ai-overviews-change-every-few-days)).

## 6. AIO citations drift from the organic top 10
- For one keyword tracked on 5 dates in 2026, 2–4 of the URLs cited in the AI Overview were also in the organic top 10 from January to August; on 22 October none of the 8 cited URLs were. *Anecdote, one keyword.*[^ls-serp]
- **Do:** keep AIO citations as their own series next to organic position, and track the overlap between the two over time instead of assuming a top-10 ranking implies an AIO citation ([Google AI features](../how-it-works/google-ai-features.md)).

## 7. Cited vs ranking domains across keywords
- On 29 keywords (US desktop, 2026-10-25) the median overlap between domains cited in the AI Overview and domains in the organic top 10 was 22 %, and 0 % for seven keywords. The organic top 10 also held only 7–9 organic URLs per keyword, because AI Overviews, People Also Ask and video blocks took slots. *Measured, small sample, vendor tool.*[^mlseo-aio-tracker][^mlseo-kw-clustering] MLforSEO sells courses.
- **Do:** keep AIO citation share as its own weekly series on a fixed keyword set ([AI-visibility tracking](ai-visibility-tracking.md#19-ai-overview-citation-tracking)); position in AI answers is close to random, so track presence, not rank.[^sp-track-ai-visibility]

Related: [Search Console](search-console.md), [AI-visibility tracking](ai-visibility-tracking.md), [diagnostic tests](diagnostic-tests.md), [Google AI features](../how-it-works/google-ai-features.md).

[^intent-engine]: Resoneo, "What Google is building", Jun 2026: personalisation signals, rerankers.
[^ipr-generative]: iPullRank, 2026-10-15: Google Research generative-UI paper; Nozzle, 27.5M results, 2026-08-20 – 2026-10-09; "poisoned" is the vendor's term; "scraper degradation" is King's inference.
[^brodie-num100]: Brodie Clark, updated 2025-09-26, and notes #sep-2025: impressions down from 10 Sep, desktop-heavy; Google quote; third-party samples (LOCOMOTIVE 319 sites, ThotSEO 1,334, JetOctopus 1,000); bot-impression reading is his inference. Marie Haynes dates the change "around September 11".
[^ah-aio-change]: Ahrefs, 2025-11-11: 43,000+ keywords, ≥ 16 observations each over ~1 month; 70 % of consecutive observations changed text, persistence 2.15 days, 54.5 % shared URLs, semantic similarity 0.95.
[^ls-serp]: Lazarina Stoy, 2026-10-25: one keyword, 5 capture dates in 2026; 2–4 AIO-cited URLs in the organic top 10 Jan–Aug, 0 of 8 on 22 Oct; anecdote.
[^mlseo-aio-tracker]: MLforSEO (Lazarina Stoy), 2026-10-24: 29 keywords, US desktop, 2026-10-25, DataForSEO; median cited/organic domain overlap 22 %, 0 % for seven keywords.
[^mlseo-kw-clustering]: MLforSEO (Lazarina Stoy), 2026-10-24: organic top 10 yields 7–9 organic URLs per keyword (Google US desktop via DataForSEO, 2026-10-25).
[^sp-track-ai-visibility]: SparkToro (Rand Fishkin), 2026-05-07: SparkToro x Gumshoe.ai study, 994 runs; position in AI output essentially random (paraphrase).
