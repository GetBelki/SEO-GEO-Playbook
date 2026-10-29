---
type: Playbook
title: Core update recovery
description: What to do after losing visibility in a Google core update — confirm the dates and wait out mid-rollout tremors, compare clicks in clean windows, find the loss by directory and page type, compare with what winners and losers share (including intrusive ads and sister sites), treat indexing as a quality signal, tell spam and manual actions from core (feed-generated templates, site reputation abuse), avoid rewrites that only win briefly, watch brand demand and unlinked mentions, and expect the loss to carry into AI answers.
tags: [seo, core-update, spam-update, recovery, quality, google, diagnosis, brand, pruning, manual-actions, ai-overviews, chatgpt, discover]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T09:15:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T09:22:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: chuleta-timelines
    resource: "https://newsletter.chuletaseo.com/p/google-admite-que-el-seo-se-nota"
    title: "Chuleta SEO (Emilio Rodríguez García), Google admite que el SEO se nota (2026-10-22; Spanish newsletter relaying Gary Illyes at Search Central Live Barcelona)"
  - id: status
    resource: "https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history"
    title: "Google Search Status Dashboard, Ranking history (42 entries since Nov 2021) and the per-incident pages, read 2026-10-27"
  - id: mh-spam
    resource: "https://www.mariehaynes.com/august-2025-spam-update/"
    title: "Marie Haynes, August 2025 spam update (2025-10-20)"
  - id: brodie-num100
    resource: "https://brodieclark.com/the-great-decoupling-num100/"
    title: "Brodie Clark, The Great Decoupling and num=100 (updated 2025-09-26; cites LOCOMOTIVE, ThotSEO, JetOctopus samples)"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6: how Google Search works (Oct 2024)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026; trial testimony, 2024 leak, author's schema compilation)"
  - id: mh-satisfaction
    resource: "https://www.mariehaynes.com/what-if-user-satisfaction-is-the-most-important-factor-in-seo/"
    title: "Marie Haynes, What if user satisfaction is the most important factor in SEO (2026-01-26)"
  - id: mh-june2025
    resource: "https://www.mariehaynes.com/analyzing-pages-that-improved-following-the-june-2025-core-update/"
    title: "Marie Haynes, Pages that improved after the June 2025 core update (2025-07-18; 5 cases)"
  - id: mh-dec2025
    resource: "https://www.mariehaynes.com/the-december-2025-core-update-observations-on-4-sites-that-did-well/"
    title: "Marie Haynes, December 2025 core update: 4 sites that did well (2026-02-20)"
  - id: aleyda-may2026
    resource: "https://www.aleydasolis.com/en/ai-search/google-may-2026-core-update-analysis-intent-market-fit-and-source-type-drove-the-biggest-visibility-shifts/"
    title: "Aleyda Solis, May 2026 core update analysis (Sistrix, US+UK; search extracts)"
  - id: aleyda-mar2026
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/google-march-core-update-2026/"
    title: "Aleyda Solis, March 2026 core update (Sistrix, US; search extracts)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays third-party studies)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: mh-cni
    resource: "https://www.mariehaynes.com/crawled-currently-not-indexed/"
    title: "Marie Haynes, Crawled – currently not indexed (2026-07-16) and migration issues may be site quality (2026-10-13)"
  - id: mh-vector
    resource: "https://www.mariehaynes.com/could-optimizing-for-vector-search-do-more-harm-than-good/"
    title: "Marie Haynes, Could optimizing for vector search do more harm than good (2025-06-26)"
  - id: g-spam
    resource: "https://developers.google.com/search/docs/essentials/spam-policies"
    title: "Google Search Central, Spam policies for Google web search (updated 2026-08-28)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: sbs-sitequality
    resource: "https://www.seobythesea.com/2015/05/google-site-quality-scores/"
    title: "SEO by the Sea (Bill Slawski), How Google may calculate a site quality score (2015-05-12; patent US 9,031,929, filed 2012-06-27)"
  - id: sbs-panda
    resource: "https://www.seobythesea.com/2014/03/googles-panda-granted-patent-on-ranking-search-results/"
    title: "SEO by the Sea, Google's Panda granted a patent on ranking search results (2014-03-25; patent US 8,682,892, filed 2012-09-28)"
  - id: bc-low-activity
    resource: "https://www.bruceclay.com/blog/remove-keep-low-activity-webpages/"
    title: "Bruce Clay, Remove or keep low-activity pages (2025-05-27; qualitative client anecdote)"
  - id: gg-mtai
    resource: "https://www.gsqi.com/marketing-blog/when-mt-ai-crumbles-chatgpt-follows/"
    title: "Glenn Gabe, When 'Mt. AI' crumbles, ChatGPT can follow (2026-04-20; 1 case)"
  - id: gg-spam
    resource: "https://www.gsqi.com/marketing-blog/august-2026-google-spam-update-case-studies/"
    title: "Glenn Gabe, August 2026 spam update case studies (2026-08-31; 4 cases)"
  - id: gg-may2026
    resource: "https://www.gsqi.com/marketing-blog/core-roars-back-google-may-2026-core-update-analysis/"
    title: "Glenn Gabe, May 2026 core update analysis (2026-06-10; cases)"
  - id: gg-dec2025
    resource: "https://www.gsqi.com/marketing-blog/google-december-2025-broad-core-update-analysis-findings/"
    title: "Glenn Gabe, December 2025 core update (2026-01-07; 3,000+ tracked sites, qualitative)"
  - id: lr-gsc-meetup
    resource: "https://lilyray.nyc/what-i-learned-at-the-2025-google-search-central-meetup-in-nyc/"
    title: "Lily Ray, 2025 Google Search Central meetup NYC (2025-03-24; her account of Google staff statements)"
  - id: sp-5-features
    resource: "https://sparktoro.com/blog/5-strategic-features-that-predict-survival-in-the-zero-click-era/"
    title: "SparkToro, 5 strategic features that predict survival in the zero-click era (2026-04-20; relays Zyppy, 400+ sites)"
  - id: srp-commodity-content
    resource: "https://serprecon.com/blog/what-is-commodity-content"
    title: "SERPrecon, What is commodity content? (2026-10-15; Google guide and statements relayed, vendor scoring method)"
  - id: mlseo-content-audit
    resource: "https://www.mlforseo.com/machine-learning-implementation-guides/content-audit/content-audit-template/"
    title: "ML for SEO, Content audit template (2026-10-24; rules plus synthetic 24-URL site)"
---

# Core update recovery

Use this page once [traffic drop](traffic-drop.md) has ruled out measurement breaks and the loss lines up with a core update's rollout.

## Rules
- **Confirm the update's dates and compare full weeks before the start with full weeks after the end**, leaving the rollout out — mid-rollout tremors still move rankings, so don't judge before it ends ([step 1](#1-confirm-and-measure-cleanly)). *Official dates; practitioner method and cases.*
- **Compare clicks only**, never impressions or average position across the num=100 and impression-inflation breaks ([step 1](#1-confirm-and-measure-cleanly)). *Practitioner; measured breaks.*
- **Find where the loss sits — by directory, then by page type** ([step 2](#2-locate-the-loss)). *From the leak; trial / leak.*
- **Compare your lost pages with what winners share** — follow-ups, first-hand testing, trust and customer service, brand identity, intent and market fit — and check what losers share: intrusive ads, sister sites on one setup ([step 3](#3-what-winners-share)). *Practitioner cases; measured visibility.*
- **Treat falling indexed counts as part of the same quality problem**, and before pruning check whether the pages feed internal links to the category ([step 4](#4-indexing-is-part-of-the-verdict)). *Case observations plus statements; Practitioner, qualitative.*
- **Google's own rough timeline** for core-update recovery is 3–6 months, up to a year, and 1–3 months for a site migration. *Official statement, relayed.*[^chuleta-timelines]
- **Plan for months, not weeks:** recovery often comes only with a later core update ([step 5](#5-recovery-time-spam-vs-core-and-what-not-to-do)). *Practitioner, four cases.*
- **Don't rewrite pages for embeddings or mass-rewrite and judge on first gains** ([step 5](#5-recovery-time-spam-vs-core-and-what-not-to-do)). *Statement plus anecdotes.*
- **Track branded and navigational demand and unlinked mentions per section, not only links** ([step 6](#6-brand-demand-and-mentions)). *Patent.*
- **If a spam update overlaps, check the Manual actions report and any feed-generated or programmatic templates first** — site reputation abuse is handled by manual actions, and the August 2026 spam update hit feed-built category and product pages ([step 5](#5-recovery-time-spam-vs-core-and-what-not-to-do)). *Google staff, relayed; practitioner, 4 cases.*
- **Expect a Google loss to show up in AI answers too**, and fix the affected section rather than chasing AI visibility separately ([step 7](#7-losses-carry-into-ai-answers)). *Practitioner cases.*
- **Check lost sections for commodity content and run fixed audit rules** (decay = clicks down 30 % or more) instead of rewriting everything ([step 8](#8-commodity-content-and-audit-rules)). *Official, relayed; Practitioner.*

## Steps
1. **Dates:** look up start and end in the [timeline](../reference/google-updates-timeline.md#updates); note overlapping updates ([patterns](../reference/google-updates-timeline.md#patterns)).
2. **Windows:** equal full-week windows either side of the rollout; same weeks last year if seasonal.
3. **Clicks by directory** ([test 3](../measure/diagnostic-tests.md#3-loss-by-directory)); sort pages by loss.
4. **Satisfaction per page type** on the losing sections, by device ([test 2](../measure/diagnostic-tests.md#2-satisfaction-per-page-type)).
5. **Lost queries:** who took them, and what kind of source they are ([test 1](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries)).
6. **Indexing by page type** ([test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type)).
7. **Spam or core?** If a spam update overlapped, check the spam policies first, the Manual actions report and any feed-generated templates ([step 5](#5-recovery-time-spam-vs-core-and-what-not-to-do)).
8. **Fix** the losing sections against the winner traits, after checking them for commodity content and running the audit rules ([step 8](#8-commodity-content-and-audit-rules)): consolidate thin URL sets, improve the pages people use, fix trust signals ([product pages](../page-types/product-pages.md), [category pages](../page-types/category-pages.md)).
9. **Track** monthly against a control section, and re-check after each later core update — including the share of branded and navigational queries per section and unlinked brand mentions ([step 6](#6-brand-demand-and-mentions)), and AI Overview, AI Mode and ChatGPT visibility for the affected section ([step 7](#7-losses-carry-into-ai-answers)).

## 1. Confirm and measure cleanly
- Core rollouts take about 12–19 days (median ~16); March 2024 took 45. Several overlapped with spam updates or bugs, and announcements can be backdated.[^status] A loss inside overlapping windows can't be pinned on one update from dates alone.
- Compare clicks only, in equal windows either side of the rollout, sort pages by loss and look for shared directories.[^mh-spam] Impressions and average position broke from ~10 Sep 2025 with the num=100 change.[^brodie-num100]
- **Tremors.** The May 2026 core update was visible about 48 hours in, with "tremors" during the rollout, and some sites lost Discover only at the final tremor; the December 2025 update had a tremor on 20 December. *Practitioner, cases.*[^gg-may2026][^gg-dec2025] Don't judge before the rollout ends. Google says Discover has "minimal overlap with Search ranking", yet many sites were hit in both.[^gg-may2026]

> **Conflict:** does Discover follow Search rankings? — [details](../reference/conflicts.md#does-discover-follow-search-rankings)

## 2. Locate the loss
- **Directories.** The leak names quality scores at site, section and page level; new pages inherit the section average; low-quality pages are crawled less. *From the leak.*[^leak-6] Sections moving as blocks point at thin or off-topic URL sets.
- **Satisfaction.** NavBoost keeps ~13 months of click history per query and page, by country and device; compare short visits within a page type.[^navboost] AI rerankers reorder only the top 20–30 results from classic ranking. *Trial testimony.*[^mh-satisfaction] A page that satisfies better than its type but still lost rankings has a different problem.[^field-notes]

## 3. What winners share
*Practitioner case observations and visibility measurements; small samples.*
- **Follow-ups and first-hand evidence.** Pages that rose answered the follow-up questions, showed first-hand testing and original photos, and were easy to scan.[^mh-june2025]
- **Trust.** Shops that recovered fixed customer service, navigation and checkout, and off-site reputation; the rater guidelines call reliable customer service vital for online stores.[^mh-dec2025]
- **Brand identity.** In March 2026, brands with product identity gained (Hermès +99.8 %) while retailers competing on broad category demand lost (Wayfair −37.4 %).[^aleyda-mar2026] A risk for multi-brand shops on generic queries.
- **Intent and market fit.** In May 2026 the source type that fits the query and market won; UK local marketplaces gained about 21–23 % while their US .com versions fell about 54 %.[^aleyda-may2026]
- **Assets.** Across 400 sites, proprietary assets (+92 %), task completion (+83 %) and a product offering (+70 %) predicted organic gains. *Relayed.*[^ignite-news] As relayed by SparkToro (which sells audience research), sites with none of five traits (product, task completion, proprietary assets, tight topical focus, strong brand) gained in 13.5 % of cases, with four traits 68.1 % and with five 69.7 %. *Measured, relayed.*[^sp-5-features]
- **What losers share.** Sites with aggressive ads (content-blocking video pop-ups) lost; sister sites on shared technical, ad or affiliate setups moved together. *Practitioner, cases.*[^gg-may2026][^gg-dec2025] **Do:** include intrusive-ad UX in the quality check, and if you run several sites on one setup, check them together.

## 4. Indexing is part of the verdict
From 27 May 2025 Google dropped pages users rarely engaged with — product pages without original content, thin category pages — on ~40 reviewed sites; one shop went from 27,000 to 15,000 indexed pages.[^mh-deindex] "Crawled – currently not indexed" usually means quality; rule out blocked CSS/JS and rendering first.[^mh-cni] 301 dropped pages that have backlinks; improve or consolidate the rest.

Pruning inside a category can hurt its head terms: clients who deleted low-performing pages inside a section lost head-term rankings, because those pages fed internal links and anchors to the category. *Practitioner, qualitative, no figures.*[^bc-low-activity] Update or merge before you remove ([scaling content and templates](scaling-content-and-templates.md)).

## 5. Recovery time, spam vs core, and what not to do
- **Months.** One shop hit in August 2024 recovered only in the December 2025 core update.[^mh-dec2025] Core updates come 3–4 times a year.[^status] Sites hit by an unconfirmed update in January 2026 hadn't recovered by May. *Practitioner, cases.*[^gg-may2026] Losses can come from updates that aren't on the [timeline](../reference/google-updates-timeline.md).
- **Spam is a different question.** Spam updates are short (three of four in 2026 finished within 3 days) and global since December 2024.[^status] The policies define link spam, scaled content abuse, site reputation abuse and expired domain abuse.[^g-spam] If the loss sits in a spam window, check those first; core losses are about quality. *Official definitions; triage is inference.*
- **Spam update case: feed-generated templates.** The August 2026 spam update targeted content, not links: a thin affiliate site with category and product pages built programmatically from a marketplace feed (some without images, footer text 97 %+ likely AI-written) lost 14K+ queries; a 1.5M-URL product-information site, ~85 % programmatic, took a site-wide, core-like hit; recovery takes months. *Practitioner, 4 cases.*[^gg-spam] Audit such templates before the next spam window ([category pages](../page-types/category-pages.md), [scaling content and templates](scaling-content-and-templates.md)).
- **Site reputation abuse is a manual action.** Google staff said at a March 2025 meetup that site reputation abuse is handled by manual actions, not algorithmically, and applies only when content is third-party *and* abuses the host's signals; using freelancers isn't a violation. *Google staff statements, as recounted by an attendee; check against the current policy.*[^lr-gsc-meetup][^g-spam] **Do:** look in Search Console's Manual actions report before blaming an algorithm.
- **Not for embeddings.** Google's John Mueller called optimising for embeddings "literally keywords stuffing"; pages restructured into micro-intent sections gained first and then lost much of it.[^mh-vector] Judge any rewrite by whether rankings hold over weeks.
  > **Conflict:** passage tuning for retrieval vs Google's "no special writing" — [details](../reference/conflicts.md#writing-for-embeddings-and-chunking)

## 6. Brand demand and mentions
*Patents: they show Google may compute this, not that it does now.*
- **Brand and navigational queries in a site-quality ratio.** One patent scores site quality as the ratio of unique queries that refer to the site (`site:`, brand or name, navigational) to unique queries where users merely clicked one of its results; a "site" can be a subdomain or subdirectory. *Patent (in force to ~2032); the 2024 leak supports it only indirectly.*[^sbs-sitequality]
- **Unlinked mentions count as links.** Another patent divides independent links — express links and implied ones, i.e. unlinked citations — by reference queries per site or subdomain, and applies the result as a modification factor to every page in the group. *Patent.*[^sbs-panda]
- **Do:** in Search Console, track the branded and navigational share of clicked queries per section; in recovery, compare growth in unlinked brand mentions and brand queries, not only links ([Search Console](../measure/search-console.md), [links and digital PR](../channels/links-and-digital-pr.md)). Background: [Google ranking](../how-it-works/google-ranking.md).

## 7. Losses carry into AI answers
- After a scaled-content manual action removed an 850K-URL AI-generated directory, its ChatGPT citations mostly disappeared and its AI Overview and AI Mode visibility fell; the rest of the site was unaffected. Spam-update losers also dropped in AI Overviews and AI Mode. *Practitioner cases.*[^gg-mtai][^gg-spam]
- **Do:** expect a Google loss to show up in AI answers for the same section; fix the section in Google rather than chasing AI visibility separately, and track AI visibility for the affected section alongside clicks ([AI visibility tracking](../measure/ai-visibility-tracking.md), [Google AI features](../how-it-works/google-ai-features.md), [AI assistants](../how-it-works/ai-assistants.md)).

## 8. Commodity content and audit rules
- **Commodity content.** Google's guide for generative-AI search has a section on creating "non-commodity content"; Danny Sullivan said commodity content isn't necessarily your strength, and John Mueller (2019) framed the test as whether the site would be the objectively best result. Google hasn't said commodity content is penalised or that a commodity score exists. *Official, relayed.*[^srp-commodity-content] (SERPrecon sells a commodity-scoring tool.) How to de-commoditise a page: [product pages](../page-types/product-pages.md#4-answer-will-it-fit).
- **Replaceable models.** SparkToro's Rand Fishkin argues that tactical SEO can't save a site whose business model a search engine or AI can replace; survival needs products, tools or data. *Practitioner.*[^sp-5-features]
- **Audit with fixed rules.** Flag decay (clicks down 30 % or more between two consecutive 3-month periods, for pages with at least 20 clicks before), striking distance and thin pages with demand, then decide redirect, merge, update or prune in a fixed order. *Practitioner.*[^mlseo-content-audit] (ML for SEO sells courses.) Rules and the pruning order: [scaling content and templates](scaling-content-and-templates.md#11-content-audit-rules).
- **Do:** for each lost section, ask what it offers that competitors don't; if the answer is nothing, add own data, tests or tools before rewriting text.

Related: [Google ranking](../how-it-works/google-ranking.md), [traffic drop](traffic-drop.md), [seasonal peaks](seasonal-peaks.md), [diagnostic tests](../measure/diagnostic-tests.md).

[^status]: Google Search Status Dashboard, Ranking history and incident pages (`https://status.search.google.com/incidents/<id>`), read 2026-10-27. Durations are rounded to whole days except under one day. End of the Oct 2023 spam update is logged 19 Oct 22:15 PT; its note says complete as of 20 Oct.
[^mh-spam]: Marie Haynes, 2025-10-20: click-only comparison, pages sorted by loss, shared directories.
[^brodie-num100]: Brodie Clark, updated 2025-09-26, and notes #sep-2025: impressions down from 10 Sep, desktop-heavy; Google quote; third-party samples (LOCOMOTIVE 319 sites, ThotSEO 1,334, JetOctopus 1,000); bot-impression reading is his inference. Marie Haynes dates the change "around September 11".
[^leak-6]: Resoneo, leak part 6, 2024-10-31: index tiers, crawl skipping, siteFocusScore/siteRadius, new pages inherit the sitechunk average.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: click-signal families, 13-month history per query and page by country and device, Glue for SERP blocks, compare short visits per page type. No measured ranking effects shown.
[^mh-satisfaction]: Marie Haynes, 2026-01-26: rerankers on the top 20–30, rater frozen-vs-retrained comparisons (Douglas Oard testimony).
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^mh-june2025]: Marie Haynes, 2025-07-18: 5 pages that improved after the June 2025 core update.
[^mh-dec2025]: Marie Haynes, 2026-02-20: 4 sites incl. two ecommerce; rater-guideline counts are her own.
[^aleyda-mar2026]: Aleyda Solis, March 2026 core update, Sistrix 26 Mar – 11 Apr 2026, via search extracts.
[^aleyda-may2026]: Aleyda Solis, May 2026 core update, Sistrix 26 May – 2 Jun 2026, via search extracts.
[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: Ahrefs AIO citations (week of 2026-03-01), Pillarbase scroll-to-text (2026-07-25), Zyppy 400 sites (2026-04-11); secondary reporting, primary studies not checked.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^mh-cni]: Marie Haynes, 2026-07-16 and 2026-10-13: Search Central Toronto quote, Search Console help text, robots.txt CSS/JS case, one migration case.
[^mh-vector]: Marie Haynes, 2025-06-26: Mueller quote; anecdotal case screenshots.
[^g-spam]: Google, spam policies, read 2026-10-27.
[^sbs-sitequality]: SEO by the Sea, 2015-05-12: patent US 9,031,929 (filed 2012-06-27, in force to ~2032); site quality from referring vs associated queries; site can be a subdomain or subdirectory.
[^sbs-panda]: SEO by the Sea, 2014-03-25: patent US 8,682,892 (filed 2012-09-28); independent links (express and implied) per reference queries, group-wide modification factor.
[^bc-low-activity]: Bruce Clay, 2025-05-27: pruning order and a client anecdote (head-term losses after deleting pages inside a section); qualitative, no figures.
[^gg-mtai]: Glenn Gabe, 2026-04-20: one case; scaled-content manual action removed an 850K-URL AI-generated directory; ChatGPT citations mostly gone, AIO/AI Mode visibility down; rest of the site unaffected.
[^gg-spam]: Glenn Gabe, 2026-08-31: 4 August 2026 spam update cases; content, not links; feed-built affiliate site (some pages without images, footer text 97 %+ likely AI-written) lost 14K+ queries; 1.5M-URL product-information site ~85 % programmatic, site-wide hit; losers also dropped in AIO/AI Mode; recovery takes months.
[^gg-may2026]: Glenn Gabe, 2026-06-10: May 2026 core update visible ~48 h in, mid-rollout tremors, Discover losses at the final tremor; unconfirmed January 2026 update not recovered by May; sister sites moved together; aggressive ads lost; quotes Google on Discover's "minimal overlap with Search ranking".
[^gg-dec2025]: Glenn Gabe, 2026-01-07: December 2025 core update, tremor on 20 December; 3,000+ tracked sites, qualitative.
[^lr-gsc-meetup]: Lily Ray, 2025-03-24: her account of Google staff statements at the Search Central meetup NYC, March 2025 — site reputation abuse via manual actions, only third-party content abusing host signals, freelancers not a violation.
[^sp-5-features]: SparkToro (Rand Fishkin), 2026-04-20: relays Cyrus Shepard/Zyppy, 400+ sites, 2024–2026 YoY Google traffic; win rate 13.5 % with 0 traits, ~15 % with 1, 68.1 % with 4, 69.7 % with 5; Fishkin's view that tactical SEO can't save a replaceable business model. Video transcript; figures approximate.
[^srp-commodity-content]: SERPrecon, 2026-10-15: relays Google's generative-AI guide ("non-commodity content"), Danny Sullivan via Search Engine Journal and John Mueller (2019); Google hasn't said commodity content is penalised or that a commodity score exists; de-commoditising procedure. Vendor sells a commodity-scoring tool; no validation data.
[^mlseo-content-audit]: ML for SEO, 2026-10-24: rule order, first match wins; decay = clicks −30 % or more between two consecutive 3-month Search Console periods (≥20 clicks earlier); striking distance = position 4–20 with ≥200 impressions; thin = <300 words with demand; prune if <10 clicks, <200 impressions, <20 sessions and no key events. Demonstrated on a synthetic 24-URL site.
[^chuleta-timelines]: Chuleta SEO, 2026-10-22, Spanish, read in full; claims translated. Paraphrases Gary Illyes at Search Central Live Barcelona (no direct quote or recording given): new page discovered in ~20 hours, existing page re-crawled ~30 days, link signals processed in minutes to 3 weeks, title updates 1–2 days, site migration 1–3 months, core-update recovery 3–6 months (up to a year); the author notes the steps add up. Also relays a Cloudflare–OpenAI discovery pilot ("hundreds of millions" of pages, no method) and Bing's Topics Portfolio beta.
