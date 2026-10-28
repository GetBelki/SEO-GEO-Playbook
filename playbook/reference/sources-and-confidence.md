---
type: Reference
title: Sources and confidence
description: The research sources, what each is good for, the six-level confidence scale, how to read research, and what not to adopt.
tags: [sources, confidence, research, method]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: official-docs
    resource: "https://developers.google.com/search/docs"
    title: "Vendor documentation: Google Search Central, OpenAI, Anthropic, Perplexity, Apple, Bing, IndexNow (read 2026-10-27)"
  - id: siege
    resource: "https://www.siegemedia.com/blog"
    title: "Siege Media blog and research, 2025 – Oct 2026 (14 studies used)"
  - id: aleyda
    resource: "https://www.aleydasolis.com/en/blog/"
    title: "Aleyda Solis blog, 2025 – Oct 2026 (14 posts; read from search extracts, the site returned 403 to direct fetches)"
  - id: learning-sites
    resource: "https://learningaisearch.com/"
    title: "LearningSEO.io and LearningAISearch.com (Aleyda Solis), curated roadmaps used as gap checklists"
  - id: thrive
    resource: "https://thriveagency.com/blog/"
    title: "Thrive Internet Marketing Agency blog, 13 posts Aug 2025 – Oct 2026"
  - id: ignite
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly news recap Jan – Oct 2026 and blog"
  - id: ipullrank
    resource: "https://ipullrank.com/blog"
    title: "iPullRank blog (Mike King and team), Jul 2025 – Oct 2026 (18 posts used)"
  - id: brodie
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes and articles, Jun 2025 – Oct 2026"
  - id: haynes
    resource: "https://www.mariehaynes.com/blog/"
    title: "Marie Haynes, blog, Apr 2025 – Oct 2026 (20 posts read)"
  - id: growth-memo
    resource: "https://www.growth-memo.com/archive"
    title: "Kevin Indig, Growth Memo, 2025 – Oct 2026 (free parts only; most posts older than ~4 weeks are paywalled)"
  - id: status
    resource: "https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history"
    title: "Google Search Status Dashboard, Ranking history"
  - id: resoneo
    resource: "https://think.resoneo.com/"
    title: "Resoneo research hub (think.resoneo.com) and resoneo.com Google leak series, read 2024-10 – 2026-10"
  - id: searchind
    resource: "https://searchind.com/blog/"
    title: "Searchind blog (Simone Parodi), 10 ecommerce SEO articles, Aug 2025 – Sep 2026"
  - id: ahrefs
    resource: "https://ahrefs.com/blog/"
    title: "Ahrefs blog, categories local SEO, keyword research, link building, technical SEO, enterprise SEO, on-page SEO and general SEO (read 2026-10-28; ~45 posts used)"
  - id: botpresso
    resource: "https://botpresso.com/blog/"
    title: "Botpresso blog (read 2026-10-28; 12 posts used, no publish dates on posts)"
  - id: seer
    resource: "https://www.seerinteractive.com/insights"
    title: "Seer Interactive, insights (read 2026-10-28; 12 used)"
  - id: gsqi
    resource: "https://www.gsqi.com/marketing-blog/"
    title: "Glenn Gabe (GSQi), marketing blog (read 2026-10-28; 11 used)"
  - id: stoy
    resource: "https://lazarinastoy.com/blog/"
    title: "Lazarina Stoy, blog (read 2026-10-28; 9 used)"
  - id: lilyray
    resource: "https://lilyray.nyc/blog/"
    title: "Lily Ray, blog (read 2026-10-28; 4 used)"
  - id: adams
    resource: "https://www.seoforgooglenews.com/"
    title: "Barry Adams, SEO for Google News (read 2026-10-28; 10 used)"
  - id: alderson
    resource: "https://www.jonoalderson.com/blog/"
    title: "Jono Alderson, blog (read 2026-10-28; 12 used)"
  - id: scholz
    resource: "https://seobrief.substack.com/"
    title: "Jes Scholz, SEO Brief (read 2026-10-28; 4 used)"
  - id: carter
    resource: "https://www.crystalcarter.ai/resources"
    title: "Crystal Carter, resources (read 2026-10-28; 6 used)"
  - id: natzir
    resource: "https://natzir.com/en/articles/"
    title: "Natzir Turrado, articles (read 2026-10-28; 16 used)"
  - id: dejan
    resource: "https://dejan.ai/blog/"
    title: "DEJAN (Dan Petrovic), blog (read 2026-10-28; 17 used)"
  - id: metehan
    resource: "https://metehan.ai/blog/"
    title: "Metehan Yeşilyurt, blog (read 2026-10-28; 17 used; author works at Peec AI)"
  - id: sbs
    resource: "https://www.seobythesea.com/"
    title: "SEO by the Sea (Bill Slawski), patent analyses (read 2026-10-28; 16 used; inactive since 2022)"
  - id: bruceclay
    resource: "https://www.bruceclay.com/blog/"
    title: "Bruce Clay, blog (read 2026-10-28; 13 used; inactive since June 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's Search Console, GA4, Google Ads and feed data, 2024–2026"
---

# Sources and confidence

Where the playbook's claims come from and how much each can carry. Every claim carries one of seven labels: an *Official* or *Measured* finding can justify a change on its own; an *Inference* needs a test on your own data first ([diagnostic tests](../measure/diagnostic-tests.md)). Where sources disagree, see the [conflicts register](conflicts.md).

## Confidence scale

| Label | Meaning | Typical example |
|---|---|---|
| **Official** | The vendor's own documentation about its own system | Google's canonical and site-move rules; OpenAI's and Anthropic's crawler docs ([technical foundations](../technical/technical-foundations.md), [AI crawlers](../technical/ai-crawlers-and-controls.md))[^official-docs] |
| **Measured** | Large sample, method published, or confirmed in our own data with a control | ChatGPT citation funnel from 1,249 answers and server logs; Gemini citation positions from 222k searches[^resoneo] |
| **From code** | Field, system or signal names read from shipped apps, network traffic or binaries | Google Ads landing-page summary fields; Maps' 72 rank signals; Lens category lists[^resoneo] |
| **From the leak** | 2024 Google API documentation leak or trial exhibits | NSR, site focus, twiddlers, index tiers[^resoneo] |
| **Patent** | A granted patent or published application describing a mechanism. Proves Google *may* do it, not that it does; check status (in force, expired, abandoned) and whether the leak, testimony or measurements support it | Site quality from branded/navigational query ratios; reachability scores[^sbs] |
| **Practitioner** | Experienced consultant's advice, plausible, not measured | Evergreen seasonal URLs, feed title tests, branded-intent pages[^searchind] |
| **Inference** | The author's (or our) reading of the above | "This field probably means section-level quality" |

A claim relayed by a secondary source (an agency blog citing a study) says "relayed" and names the original study.

**Names are reliable, weights are not.** Code and leak sources prove a signal exists; they never say how much it counts today, or whether it is still live.

## The sources

- **Vendor docs.**[^official-docs] Google Search Central, OpenAI, Anthropic, Perplexity, Apple, Bing. The top of the scale for what a vendor does with its own systems — but not proof of what works best, and docs change often.
- **Google Search Status Dashboard.**[^status] The only primary source for update dates ([timeline](google-updates-timeline.md)).
- **Resoneo** (think.resoneo.com, resoneo.com).[^resoneo] French agency that reverse-engineers search and AI products: decompiled apps, captured traffic, large prompt samples, the 2024 leak. Strongest source for *how systems work*. Weak on *what to do*: it rarely tests interventions. Some studies rest on one session, one page or one account; check the sample size on each.
- **Growth Memo** (Kevin Indig).[^growth-memo] Large measured studies: clickstream, usability tests, citation datasets, often with tool vendors' data (Semrush, Similarweb, Omnia). Best source for *how users and engines behave at scale*. Most posts go behind a paywall after about four weeks, so several claims here rest on headlines; they are marked.
- **iPullRank** (Mike King and team).[^ipullrank] Reads patents, the leak and trial material, and aggregates third-party studies (Profound, Nozzle, Datos, SimilarWeb, Yext). Best source for *retrieval mechanics* (fan-out, passage ranking) and for *measurement method* (prompt-tracking statistics). Strong advocacy for "relevance engineering"; its own tests are small and use its own tools. Its method for reading patents is worth adopting: check the priority date and the claims first, remember patents can be defensive, and cross-check leak features against sworn testimony.
- **Marie Haynes** (mariehaynes.com).[^haynes] Reads DOJ trial exhibits, patents, rater guidelines and Google statements, plus client cases. Good for *what Google has said or shown in court*; separate the quoted source from her interpretation. One own measured study (assistant traffic across 100 GA4 properties).
- **Siege Media.**[^siege] Content and digital-PR agency publishing its own studies (GA4 benchmarks across hundreds of properties, AI citation sets from Peec AI). Good for *benchmarks and content-type evidence*; samples lean B2B/SaaS, and it sells the services its studies favour.
- **Aleyda Solis.**[^aleyda] Independent consultant; measured citation and traffic studies (Semrush, Similarweb, Sistrix data), core-update analyses, and practical checklists (12-step AI-search audit, prompt library). Her site blocked direct fetches, so her claims here come from search extracts — re-check on the page before a decision. Her curated roadmaps LearningSEO.io and LearningAISearch.com served as gap checklists and pointed to the official docs.[^learning-sites]
- **Ahrefs.**[^ahrefs] Tool vendor publishing large studies from its own data (Brand Radar AI-citation sets, Keywords Explorer, aggregated Search Console data from its users, its own AI-content detector): AI Overview triggers across 146M results pages, branded AI Overviews, click loss, schema and llms.txt studies, CTR benchmarks. The largest samples in the playbook — but vendor data, not independently replicated, and several posts show text/table number mismatches (quoted as found). Its guides route advice through its own metrics (DR, Traffic Potential); its older on-page and link guides (2020–2023) are marked as dated.
- **Botpresso.**[^botpresso] Technical SEO/GEO agency: a migration case caught by daily per-URL index checks, an assistant schema test, a 52-site study of ChatGPT referrals before and after a May 2026 link change, practical Merchant Center and soft-404 guidance. Posts carry no publish dates (dates approximate), samples are its own clients, and several posts promote its tools.
- **Natzir Turrado** (natzir.com).[^natzir] Technical SEO consultant who reads leaks, trial exhibits and Chromium source, and runs small, well-designed experiments (Gemini grounding excerpts, model-change ablations, HTML extraction). Good for *mechanisms and measurement method*; samples are small and his interpretations are labelled as such.
- **DEJAN** (Dan Petrovic, dejan.ai).[^dejan] Machine-learning research on Google and AI search: grounding budgets, ablation tests, order bias in LLM judges, Chrome model extraction, large fan-out datasets via APIs. Strong method, but much data is private and API results may differ from the consumer apps.
- **Metehan Yeşilyurt** (metehan.ai).[^metehan] Network captures and config dumps of ChatGPT, plus large log datasets from Peec AI, where he works — vendor data that can't be reproduced outside Peec. Some posts are explicitly hypotheses; those are marked. His pages contain instructions aimed at AI agents, which were ignored.
- **SEO by the Sea** (Bill Slawski).[^sbs] Patent analyses, 2005–2022; inactive since the author's death in 2022. Used for mechanisms with a patent status and a note on whether later evidence supports them; one abandoned application is marked as not evidence.
- **Bruce Clay.**[^bruceclay] Agency blog with no first-party data; inactive since June 2026. Used for documented practitioner methods (siloing, pruning order, redirect mapping); third-party studies it cites are attributed to their original authors.
- **Seer Interactive.**[^seer] Agency publishing measured studies: AI brand-accuracy tracking (28,123 answers), ChatGPT model comparisons, content recency vs citations, paid-CTR trends, a shopper panel. Strong method, but samples are mostly its own brand or B2B/lead-gen clients.
- **Glenn Gabe (GSQi).**[^gsqi] Case-based analyses of core and spam updates, canonicalisation, PDFs, and AI search (a JavaScript-rendering retest across assistants). Charts are images, so few aggregate numbers; cases are well documented.
- **Lazarina Stoy.**[^stoy] ML and NLP for SEO: classification reliability, intent facets, fan-out patents, programmatic guardrails; relays iPullRank, Seer and academic studies. Posts were republished in October 2026 as updates of older talks.
- **Lily Ray.**[^lilyray] Her blog holds one AI-gullibility test, conference recaps (each item names the original speaker) and her account of Google staff statements. Her data-led core-update work is published elsewhere (Amsive, her Substack) and wasn't read.
- **Barry Adams** (SEO for Google News).[^adams] Publisher-focused, opinion-heavy; used for what transfers to a shop's editorial content: Discover, semantic HTML, international structure, reading industry decline figures.
- **Jono Alderson.**[^alderson] Technical guides (HTTP caching, fonts, rendering, speculation rules) and well-argued positions (signal drift, machine-only versions); few measurements.
- **Jes Scholz** (SEO Brief).[^scholz] Brand-science essays applied to SEO and GEO; four posts, inactive since July 2026. Pew's primary study, which she cites, was read directly.
- **Crystal Carter.**[^carter] Practitioner frameworks for AI visibility (RAPP audit, KPIs) and entity work; no measured study of her own.
- **Not read:** SparkToro and MobileMoxie were queued in the same batch, but those readers were stopped before reporting. Their figures quoted here come via other sources.
- **Brodie Clark** (brodieclark.com).[^brodie] Dated sightings of Google and ChatGPT SERP tests, nearly all with screenshots, plus a few how-to articles. Best source for *when a surface changed*. No measured data; notes have no permalinks, only month anchors.
- **Searchind** (searchind.com).[^searchind] One consultant's ecommerce SEO blog. Practical checklists (Merchant Center audit, seasonal SEO, D2C, market analysis). Case results are anecdotal, never quantified. Use it for *procedures*, not for evidence.
- **Thrive and Ignite Visibility.**[^thrive][^ignite] Agency blogs with almost no original research. Used only for third-party studies they relay (Ahrefs, Moz, SE Ranking, Adobe…), marked "relayed"; their own case figures have no baseline or method and are not used.
- **Field notes.**[^field-notes] Two years of one shop's data. Used to confirm or reject the outside claims. Every example in this playbook comes from there and is anonymised.

## Reading research well

- Note the date and the model or app version. AI-assistant behaviour shifts with every model release (ChatGPT's source concentration changed with one release in March 2026).[^resoneo]
- Separate US-only rollouts from your market. Many agentic-commerce and Perplexity shopping features are US/CA-first.[^resoneo]
- Check numbers against the original article before they go into a decision; summaries and fetch tools condense.
- When two sources agree, check whether one is citing the other.
- Trace relayed figures to the original. Example: a schema-vs-AI-citation correlation of "−0.04 to +0.04" relayed by an agency blog as Ahrefs data doesn't exist at Ahrefs — its 0.04 is word count vs citation, and its actual schema study found no citation lift.[^ahrefs]
- When they disagree, log it in the [conflicts register](conflicts.md) instead of picking one silently.

## Not to adopt

- **Private blog networks (PBNs).** Recommended in one practitioner article without a risk assessment.[^searchind] They violate Google's spam policies ([technical foundations](../technical/technical-foundations.md#11-links-and-spam-policies)).
- **llms.txt as GEO work.** No engine is shown to use it, and crawlers rarely fetch it;[^resoneo] Google Search ignores it ([AI crawlers and controls](../technical/ai-crawlers-and-controls.md#google-ai-features-need-nothing-extra)). Keeping one costs nothing; counting it as progress is the mistake.
- **Rank tracker positions as truth.** Personalisation and AI surfaces mean there is no single reference results page; use Search Console as the source of truth and trackers as a trend ([rank tracking](../measure/rank-tracking.md)).
- **Writing for embeddings.** Google calls it keyword stuffing; gains from micro-intent rewrites faded ([conflict](conflicts.md#writing-for-embeddings-and-chunking)).
- **Google-Extended as an AI-answers opt-out.** It covers Gemini training and Gemini's grounding, not Search's AI Overviews or AI Mode ([AI crawlers and controls](../technical/ai-crawlers-and-controls.md)).
- **One study as a rule.** A single captured shopping session or one test page shows what *can* happen, not what usually does.

Related: [conflicts register](conflicts.md), [glossary](glossary.md), [Google updates timeline](google-updates-timeline.md).

[^official-docs]: Vendor docs, read 2026-10-27; per-page update dates on [technical foundations](../technical/technical-foundations.md) and [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).
[^seer]: Seer Interactive, read 2026-10-28: 12 posts, Jun – Oct 2026; listing pages 4–17 not opened.
[^gsqi]: GSQi, read 2026-10-28: 11 posts, Dec 2025 – Oct 2026.
[^stoy]: Lazarina Stoy, read 2026-10-28: 9 posts, republished 2026-10-22/25.
[^lilyray]: Lily Ray, read 2026-10-28: 4 of 13 posts used.
[^adams]: SEO for Google News, read 2026-10-28: 10 posts, Feb 2025 – Sep 2026.
[^alderson]: Jono Alderson, read 2026-10-28: 12 posts, Jul 2025 – Oct 2026.
[^scholz]: SEO Brief, read 2026-10-28: 4 posts, Apr – Jul 2026.
[^carter]: Crystal Carter, read 2026-10-28: 6 resources incl. Wix SEO Hub / AI Search Lab articles; her book not read.
[^natzir]: Natzir Turrado, read 2026-10-28: 16 articles, May 2025 – Oct 2026.
[^dejan]: DEJAN, read 2026-10-28: 17 posts, Dec 2025 – Oct 2026; blog index truncated around post 222.
[^metehan]: Metehan Yeşilyurt, read 2026-10-28: 17 posts, Aug 2025 – Oct 2026; author works at Peec AI.
[^sbs]: SEO by the Sea, read 2026-10-28: 16 patent posts, 2008–2020; last post 2022-05-13; patent expiry estimated from filing dates, application status not verified.
[^bruceclay]: Bruce Clay, read 2026-10-28: 13 posts, Apr 2025 – Jun 2026; last post 2026-06-30.
[^ahrefs]: Ahrefs, read 2026-10-28 by category; general-seo pages 2–21 not read; per-study samples on the pages that cite them.
[^botpresso]: Botpresso, read 2026-10-28 via the post sitemap (65 posts); listing pages 2–3 returned page 1.
[^siege]: Siege Media, read 2026-10-27 via its Research category and post sitemap (part of the sitemap not scanned).
[^aleyda]: Aleyda Solis, read 2026-10-27 via search-result extracts only; every direct fetch returned 403. Several dates approximate.
[^learning-sites]: LearningSEO.io and LearningAISearch.com (version 4, 2026-03-20), read 2026-10-27.
[^thrive]: Thrive, read 2026-10-27: index pages 1–2, 13 posts fetched.
[^ignite]: Ignite Visibility, read 2026-10-27: weekly recap page (2 Jan – 23 Oct 2026) and selected posts; client-result PDFs unreadable.
[^ipullrank]: iPullRank, read 2026-10-27 via the post listings (Jul 2025 – Oct 2026); the AI Search Manual e-book was not read.
[^brodie]: Brodie Clark, read 2026-10-27: notes Jun 2025 – Oct 2026 (first ~100k characters of the page) and two linked articles.
[^haynes]: Marie Haynes, read 2026-10-27 via the post sitemap (the blog index paginates by script).
[^growth-memo]: Growth Memo, read 2026-10-27 via the archive API; paywalled bodies not read.
[^status]: Google Search Status Dashboard, read 2026-10-27.
[^resoneo]: Resoneo studies 2024–2026; sample sizes per study as stated in each article. See the per-claim footnotes on the other pages.
[^searchind]: Searchind articles Aug 2025 – Sep 2026; incl. "eCommerce SEO for Google is not enough" (PBN recommendation).
[^field-notes]: Anonymised; no figures here identify the shop.
