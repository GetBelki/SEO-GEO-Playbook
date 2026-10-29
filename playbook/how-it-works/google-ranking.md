---
type: Guide
title: How Google ranks
description: Section-level quality scores, new URLs inheriting their section's average, click memory per query and page (NavBoost, RankEmbed, rerankers), exact-term scoring, host caps, indexing as a quality decision, what core-update winners share, and what patents say about site quality, navigational queries, click thresholds and freshness, plus manual actions for site reputation abuse, brand size, spam losses carrying over to AI answers, and Preferred Sources.
tags: [seo, google, google-leak, navboost, quality, indexing, core-updates, patents, freshness, spam, manual-actions, preferred-sources]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: rs-intent
    resource: "https://think.resoneo.com/search-intent/"
    title: "Resoneo, How Google matches pages to search intent (Oct 2026; internal schemas, a 2011 patent, SERP captures for 8 queries in the US and France)"
  - id: rs-kscorer
    resource: "https://think.resoneo.com/kscorer/"
    title: "Resoneo, KScorer: how Google decides what a search means (Oct 2026; 15 internal schema types, 287 fields, 56 signals; provenance not stated)"
  - id: aleyda-may2026
    resource: "https://www.aleydasolis.com/en/ai-search/google-may-2026-core-update-analysis-intent-market-fit-and-source-type-drove-the-biggest-visibility-shifts/"
    title: "Aleyda Solis, May 2026 core update analysis (Sistrix, US+UK; search extracts)"
  - id: aleyda-mar2026
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/google-march-core-update-2026/"
    title: "Aleyda Solis, March 2026 core update (Sistrix, US; search extracts)"
  - id: ignite-news
    resource: "https://ignitevisibility.com/digital-marketing-news/"
    title: "Ignite Visibility, weekly digital marketing news recap (Jan – Oct 2026; relays third-party studies)"
  - id: mh-trial
    resource: "https://www.mariehaynes.com/what-googles-trial-docs-reveal-about-clicks-links-and-other-ranking-signals/"
    title: "Marie Haynes, What Google's trial docs reveal about clicks, links and other ranking signals (2025-09-04) and User data in Google ranking systems (2026-01-22)"
  - id: mh-navboost
    resource: "https://www.mariehaynes.com/navboost/"
    title: "Marie Haynes, NavBoost (2024-06-25, updated 2025-01-10)"
  - id: mh-satisfaction
    resource: "https://www.mariehaynes.com/what-if-user-satisfaction-is-the-most-important-factor-in-seo/"
    title: "Marie Haynes, What if user satisfaction is the most important factor in SEO (2026-01-26)"
  - id: mh-vector
    resource: "https://www.mariehaynes.com/could-optimizing-for-vector-search-do-more-harm-than-good/"
    title: "Marie Haynes, Could optimizing for vector search do more harm than good (2025-06-26)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: mh-cni
    resource: "https://www.mariehaynes.com/crawled-currently-not-indexed/"
    title: "Marie Haynes, Crawled – currently not indexed (2026-07-16) and migration issues may be site quality (2026-10-13)"
  - id: mh-dec2025
    resource: "https://www.mariehaynes.com/the-december-2025-core-update-observations-on-4-sites-that-did-well/"
    title: "Marie Haynes, December 2025 core update: 4 sites that did well (2026-02-20)"
  - id: mh-june2025
    resource: "https://www.mariehaynes.com/analyzing-pages-that-improved-following-the-june-2025-core-update/"
    title: "Marie Haynes, Pages that improved after the June 2025 core update (2025-07-18; 5 cases)"
  - id: leak-2
    resource: "https://www.resoneo.com/google-leak-part-2-understanding-the-twiddler-framework/"
    title: "Resoneo, Google leak part 2: twiddlers (Oct 2024)"
  - id: leak-3
    resource: "https://www.resoneo.com/google-leak-part-3-from-words-to-meaning-googles-advanced-lexical-and-semantic-systems/"
    title: "Resoneo, Google leak part 3: lexical and semantic systems (Oct 2024)"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6: how Google Search works (Oct 2024)"
  - id: qus
    resource: "https://www.resoneo.com/qus-query-expansion-google-and-mysterious-scoring/"
    title: "Resoneo, QUS query expansion and term scoring (Jul 2025; few US examples)"
  - id: navboost
    resource: "https://think.resoneo.com/navboost-glue/"
    title: "Resoneo, NavBoost & Glue (Oct 2026; trial testimony, 2024 leak, author's schema compilation)"
  - id: preferred-sources
    resource: "https://think.resoneo.com/google-preferred-sources/"
    title: "Resoneo, Google Preferred Sources ranking (May 2026)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2025–2026"
  - id: nz-qt
    resource: "https://natzir.com/en/seo/google-quality-topicality-ranking/"
    title: "Natzir Turrado, How Google defines quality (Q) and topicality (T) (2025-05-13; DOJ testimony)"
  - id: sbs-sitequality
    resource: "https://www.seobythesea.com/2015/05/google-site-quality-scores/"
    title: "SEO by the Sea (Bill Slawski), How Google may calculate a site quality score (2015-05-12; patent US 9,031,929, filed 2012-06-27)"
  - id: sbs-panda
    resource: "https://www.seobythesea.com/2014/03/googles-panda-granted-patent-on-ranking-search-results/"
    title: "SEO by the Sea, Google's Panda granted a patent on ranking search results (2014-03-25; patent US 8,682,892, filed 2012-09-28)"
  - id: sbs-catquality
    resource: "https://www.seobythesea.com/2019/06/categorical-quality/"
    title: "SEO by the Sea, Ranking results based on categorical quality (2019-06-10; application US 2019/0155948, filed 2015-03-31; grant status unconfirmed)"
  - id: sbs-navqueries
    resource: "https://www.seobythesea.com/2012/12/navigational-queries-resources/"
    title: "SEO by the Sea, How Google may identify navigational queries and resources (2012-12-09; patent US 8,326,826, filed 2009-01-15)"
  - id: sbs-freshness
    resource: "https://www.seobythesea.com/2008/09/updating-googles-historical-data-patent-part-2-changing-content/"
    title: "SEO by the Sea, Google's historical data patent, part 2: changing content (2008-09-17; patent US 7,346,839; likely expired)"
  - id: sbs-clicks
    resource: "https://www.seobythesea.com/2015/07/google-click-through-feedback-search-results/"
    title: "SEO by the Sea, Click-through user feedback on search results (2015-07-31; patent US 9,092,510)"
  - id: lr-gsc-meetup
    resource: "https://lilyray.nyc/what-i-learned-at-the-2025-google-search-central-meetup-in-nyc/"
    title: "Lily Ray, 2025 Google Search Central meetup NYC (2025-03-24; her account of Google staff statements)"
  - id: gg-mtai
    resource: "https://www.gsqi.com/marketing-blog/when-mt-ai-crumbles-chatgpt-follows/"
    title: "Glenn Gabe (GSQi), When 'Mt. AI' crumbles, ChatGPT can follow (2026-04-20; 1 case)"
  - id: gg-spam
    resource: "https://www.gsqi.com/marketing-blog/august-2026-google-spam-update-case-studies/"
    title: "Glenn Gabe, August 2026 spam update case studies (2026-08-31; 4 cases)"
  - id: gg-may2026
    resource: "https://www.gsqi.com/marketing-blog/core-roars-back-google-may-2026-core-update-analysis/"
    title: "Glenn Gabe, May 2026 core update analysis (2026-06-10; cases)"
  - id: gn-loyalty
    resource: "https://www.seoforgooglenews.com/p/google-audience-loyalty-ecosystem"
    title: "Barry Adams, Google's audience loyalty ecosystem (2026-06-10; Google announcements)"
  - id: srp-search-engine-works
    resource: "https://serprecon.com/blog/how-a-search-engine-works"
    title: "SERPrecon, How a search engine works (2026-05-12; explainer from leaks, DOJ testimony and patents; no tests)"
  - id: srp-semantic-seo
    resource: "https://serprecon.com/blog/what-is-semantic-seo"
    title: "SERPrecon, What is semantic SEO? (2025-09-25; explainer, no data)"
  - id: srp-commodity-content
    resource: "https://serprecon.com/blog/what-is-commodity-content"
    title: "SERPrecon, What is commodity content? (2026-10-15; Google guide and statements relayed, patents, vendor scoring method)"
  - id: mlseo-info-gain
    resource: "https://www.mlforseo.com/ml-fundamentals/what-is-information-gain-in-seo/"
    title: "MLforSEO, What is information gain in SEO? (2026-05-11, upd. 2026-10-24; patent explainer)"
---

# How Google ranks

This page answers what is known about how Google's classic ranking scores sites, sections and pages, and what that means for a site's structure.

**In short.** Google scores sites and site sections, not only pages; it remembers per query and page whether searchers were satisfied; exact words still matter in the first scoring step; one host gets limited slots; and indexing itself is a quality decision. The names below are real; their current weights are unknown ([confidence scale](../reference/sources-and-confidence.md)). AI Overviews and AI Mode pick sources differently: see [Google AI features](google-ai-features.md).

## Rules

- Prune or consolidate thin and bloated URL sets, because they weigh on the whole section's quality, not only on themselves. *From the leak* [why](#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)
- After a core update, analyse losses by directory before looking at single pages. *Inference* [why](#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)
- Compare short visits within a page type and per device, never against one site-wide threshold. *Trial / leak* [why](#2-click-memory-per-query-and-page-navboost)
- Add a missing exact term where a real intent lacks it, but don't engineer pages around term or vector matching. *Practitioner* [why](#3-exact-terms-still-count-in-the-first-scoring-step)
- Keep one indexable URL per intent and consolidate variants with canonicals. *From the leak* [why](#4-one-host-gets-limited-slots)
- Track indexed pages by page type, and treat "Crawled – currently not indexed" as a quality signal once the technical causes are ruled out. *Practitioner* [why](#5-indexing-is-a-quality-decision)
- Win core updates with first-hand content, trust signals and a clear identity that fits the query's intent, not with raw authority. *Practitioner* [why](#6-what-core-update-winners-share)
- Refresh pages by changing the main content, not the date, navigation or boilerplate, and don't force freshness on evergreen queries. *Patent, supported by the leak* [why](#8-what-counts-as-a-content-change)
- Treat a manual action or spam-update loss as a loss in AI Overviews, AI Mode and ChatGPT too, and fix the cause rather than chasing AI visibility separately. *Practitioner, cases* [why](#9-spam-handling-brand-size-and-preferred-sources)
- Add what the ranking pages lack (first-hand tests, own data, a clear position) and keep the shared basics short; Google hasn't announced a commodity penalty, but the leak stores an originality score. *Official, relayed; from the leak; patent* [why](#13-commodity-content-and-information-gain)

## 1. Quality is scored per section, and new URLs start from its average
- The 2024 leak names quality scores at site, "chunk" (section) and page level (NSR, fed by site2vec), plus siteFocusScore and siteRadius, which measure how far a page sits from the site's main topic. A new, unevaluated page inherits its section's average. *From the leak.*[^leak-3][^leak-6]
- Google's Preferred Sources suggestions carry a site-level `uvSitechunk` field. *From code; link to NSR is inference.*[^preferred-sources]
- Pages predicted to be low quality or duplicate are crawled less, low index tiers are rarely re-crawled, and most anchors to them are dropped. *From the leak.*[^leak-6]
- **What it means:**
  - Thin or bloated URL sets (sitemaps with hundreds of thousands of filter or variant URLs) are a quality problem for the whole section, not housekeeping.
  - A topic far from the site's core (siteRadius) needs a coherent hub with its own internal links.
  - In a URL migration, redirect every old URL in one hop, switch internal links and sitemaps the same day, and keep an unchanged control set to measure against ([site moves](../technical/technical-foundations.md#3-site-moves-and-url-renames), [migration](../situations/migration.md)).
  - After a core update, analyse losses **by directory**: whole sections moving together fits section-level scoring ([test](../measure/diagnostic-tests.md#3-loss-by-directory)).

## 2. Click memory per query and page (NavBoost)
- NavBoost's existence and its ~13-month memory come from US DOJ trial testimony; click-signal field names (long, short, last-longest click) come from the leak. Resoneo's article adds per-country and per-device counters and Glue, which decides SERP blocks (sitelinks, packs) from the same click data. *Trial / leak; the extra detail is the author's compilation and not verifiable.*[^navboost]
- The model: a long last click is good; a quick return to the results is bad. Leaked attributes include goodClicks, badClicks, lastLongestClicks; before 2017 the memory was 18 months. *Trial / leak.*[^mh-navboost]
- **A second user-trained system.** Trial exhibits describe RankEmbed BERT, trained on "70 days of search logs" plus rater scores, and a Glue log of query, language, location, device, results shown, clicks, hovers and time on the results page. Popularity draws on "Chrome visit data" and anchor counts. *Trial exhibits, as reported by Marie Haynes.*[^mh-trial]
- **Quality and topicality.** Natzir Turrado reads the same testimony as RankEmbed trained on **one month** of data; topicality T* = "ABC" (anchors, body, clicks); quality Q* mostly static and site-level. *Trial testimony, his reading.*[^nz-qt]

  > **Conflict:** 70 days of logs (Marie Haynes) vs one month (Natzir Turrado) for RankEmbed's training data — [details](../reference/conflicts.md#how-long-is-rankembeds-training-window)
- **Click feedback needs volume.** A Google patent applies implicit click feedback only once a result passes a selection threshold (the example is ~100 clicks), within a time window and against background click trends. *Patent (granted; status not checked); the trial's rolling click memory supports the windowed idea.*[^sbs-clicks][^mh-navboost] **Do:** judge title and snippet tests on long-tail pages only after enough impressions and clicks.
- **Categorical reranking.** A patent application describes reranking the top 20–30 results for broad category queries by a query-independent "categorical quality" score (traffic, being the navigational destination for related queries, authority, selection rates), applied once enough results pass a popularity test (example: 70 %). *Patent application, grant unconfirmed; the trial supports clicks and popularity as inputs.*[^sbs-catquality] **Do:** strengthen category pages that already attract direct and navigational traffic; don't spin up thin hubs ([category pages](../page-types/category-pages.md)).
- **Navigational queries.** An older patent identifies navigational queries and their destination pages from how sessions revise queries and from long clicks; quality favours shorter URLs and shallower depth, and the navigational destination gets a first-page slot. *Patent, reported as likely expired; the mechanism survives in session and NavBoost data per trial testimony.*[^sbs-navqueries] **Do:** keep brand and core category URLs short, shallow and stable.
- **Two stages.** AI rerankers reorder only the top 20–30 results that classic ranking returns, tuned by raters comparing "frozen" and "retrained" results and by live experiments. *Trial testimony.*[^mh-satisfaction] So page quality and classic signals get a page into the candidate set; satisfaction patterns reorder it. Click-through rate isn't a direct factor; satisfaction feeds model training. *Inference.*
- **What it means:** compare short visits **within a page type** (category vs category, product vs product), never against one site-wide threshold, and split by device — the memory is per device ([test](../measure/diagnostic-tests.md#2-satisfaction-per-page-type)).
- **Example.** One shop category's pages lost clicks year on year, but their Google visitors bounced less than the category median (12.5 % vs 20.8 %); the loss was ranking and vanished sitelink impressions, not disappointed visitors. The weak spot was elsewhere: a product configurator converted 7.8 % of mobile visitors to cart vs 37.7 % on desktop.[^field-notes]
- **Example.** A bug froze a configurator for a week; every searcher clicking a preset link met a broken page. The page's ranking slide began in the same weeks — timing matches, cause not proven.[^field-notes]

## 3. Exact terms still count in the first scoring step
- Query understanding gives each query term a score per URL from 0 to ~10; a term in the title adds ~3.5 on average; named entities score highest; stop words and **numbers score 0**; some terms must match exactly, others allow derived forms. *Observed output, few US examples.*[^qus]
- OfficialPageTwiddler puts the official page first for exact-name queries; brand owners tend to win bare brand-name queries, resellers win on modifiers. *From the leak.*[^leak-2]
- **Example.** Of seven lost queries, six already had their exact phrase in title and H1, so the lexical explanation failed. The one exception — a compound noun no page carried in title, H1 or slug — was also the sharpest drop. Test before renaming slugs ([test](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries)).[^field-notes]
- **Don't write for similarity scores.** Google's John Mueller: optimising for embeddings "is literally keywords stuffing". Pages restructured into micro-intent sections gained first and then lost much of it. *Statement plus anecdotes.*[^mh-vector] Add the missing term where a real intent lacks it; don't engineer pages around term or vector matching. Judge any rewrite by whether rankings hold over weeks.

> **Conflict:** Google says you don't need to write or chunk content for AI, while practitioners argue that self-contained passages retrieve better — [details](../reference/conflicts.md#writing-for-embeddings-and-chunking)

## 4. One host gets limited slots
Twiddlers cap how many results one host gets. Near-identical variant URLs compete with each other instead of adding slots. *From the leak.*[^leak-2] **Do:** one indexable URL per intent; consolidate variants with canonicals.
- **Example.** A product page and its category page split one query's impressions about half and half every month, at positions ~4 and ~9.[^field-notes]

## 5. Indexing is a quality decision
- From 27 May 2025 Google dropped many pages from the index on ~40 reviewed sites: product pages without original content, thin category or list pages, old posts, paraphrased content. One shop went from 27,000 to 15,000 indexed pages; clicks mostly didn't fall. Google's Martin Splitt said users rarely engaged with those pages. *Case observations plus statements.*[^mh-deindex]
- "Crawled – currently not indexed" usually means quality, not technology. Google, April 2026: "we looked at it and found it not to be good"; Search Console help: page quality "must be high enough to warrant indexing". Rule out the technical cases first: robots.txt blocking CSS or JS, pages that don't render. *Statements; the migration-triggers-review theory is one case.*[^mh-cni]
- **Do:** track indexed pages by page type over time ([test](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type)); 301 dropped pages that have backlinks; improve or consolidate the rest.

## 6. What core-update winners share
*Practitioner case observations, small samples:*
- Pages that rose answered the follow-up questions, showed first-hand testing and original photos, and were easy to scan (headings, lists, tables of contents, troubleshooting sections, FAQs). Five cases.[^mh-june2025]
- Shops that recovered fixed trust: customer service, navigation and checkout, off-site reputation. One medical shop hit in August 2024 recovered only in the December 2025 core update — recovery takes many months. Four cases.[^mh-dec2025] The rater guidelines call reliable customer service vital for online stores.[^mh-dec2025]
- **Intent and market fit beat raw authority** (May 2026 core update, Sistrix US+UK): the source type that fits the query's intent and market won; in the UK, local marketplaces gained about 21–23 % while their US .com versions fell about 54 %; Reddit, Quora and StackExchange declined; general publishers fell. *Measured visibility, search extracts.*[^aleyda-may2026]
- **Generic resellers lost to brands with clear identity** (March 2026 core update, Sistrix US): brands with product identity gained (Coach +90.2 %, Hermès +99.8 %, ASOS +24.4 %); retailers competing on broad category demand and other brands' names lost (Wayfair −37.4 %, Walmart −14.8 %, Best Buy −11.4 %, Etsy −11.3 %). *Measured visibility, search extracts.*[^aleyda-mar2026] A risk for multi-brand shops on generic category queries.
- **Five traits predicting organic gains** across 400 sites: proprietary assets (+92 %), task completion (+83 %), tight topical focus, a product or service offering (+70 %), strong brand (+32 %). *Measured, Zyppy, relayed.*[^ignite-news]
- Dates of every update are in the [Google updates timeline](../reference/google-updates-timeline.md); the recovery procedure is in [core-update recovery](../situations/core-update-recovery.md).

## 7. What patents say about site-level quality
Patents show what Google has built, not what it uses today. Names are reliable; use and weight are unknown ([confidence scale](../reference/sources-and-confidence.md)).
- **Brand and navigational demand as quality.** One patent scores a site by the ratio of unique queries that *refer* to it (`site:` searches, its name or brand, navigational queries) to unique queries where users merely clicked one of its results. A "site" can be a subdomain or subdirectory. *Patent (US 9,031,929, filed 2012; expiry estimated ~2032 from filing + 20 years, not verified); the 2024 leak supports it only indirectly.*[^sbs-sitequality] **Do:** track the share of branded and navigational queries among clicked queries per section in Search Console ([Search Console](../measure/search-console.md)).
- **Links and mentions per group.** The "Panda" patent computes, per site or subdomain, the ratio of independent links (express links plus implied links, i.e. unlinked citations) to reference queries, and applies the result as a modification factor to every page in the group. *Patent (US 8,682,892, filed 2012; status not verified).*[^sbs-panda] It fits the section-level scoring in [section 1](#1-quality-is-scored-per-section-and-new-urls-start-from-its-average). **Do:** in a recovery, compare unlinked mentions and brand-query growth, not only links ([core-update recovery](../situations/core-update-recovery.md), [links and digital PR](../channels/links-and-digital-pr.md)).

## 8. What counts as a content change
- Google's historical-data patent weighs changes by where they happen: edits to boilerplate, navigation, ads, scripts, comments and date tags count little; changes to the title and main content count more; and for some queries, pages that haven't changed rank better. *Patent (US 7,346,839, likely expired); the 2024 leak's `lastSignificantUpdate` and its several date attributes support the concept.*[^sbs-freshness]
- **Do:** refresh the main content substantively when facts change; don't bump dates or swap boilerplate to look fresh; don't force freshness on evergreen queries. Assistants show a similar recency preference: see [AI assistants](ai-assistants.md#8-assistants-cite-fresher-content-than-search).

## 9. Spam handling, brand size and Preferred Sources
- **Site reputation abuse is a manual action.** By Lily Ray's account of Google staff at a March 2025 meetup, site reputation abuse was handled by manual actions, not algorithmically; it applies only when content is third-party **and** abuses the host site's signals; using freelancers is not a violation. *Relayed (her account of Google staff statements, March 2025); check against the current spam policy before relying on it.*[^lr-gsc-meetup]
- **Brand size isn't judged.** At the same meetup, Google staff said its systems don't judge a brand by its size, but recognisable brands "often have signals that perform well". *Relayed.*[^lr-gsc-meetup] It fits the brand and navigational-demand patent in [section 7](#7-what-patents-say-about-site-level-quality).
- **Google losses carry over to AI answers.** After a scaled-content manual action removed an 850K-URL AI-generated directory from one site, that directory's ChatGPT citations mostly disappeared and its AI Overview and AI Mode visibility fell; the rest of the site was unaffected. Sites that lost in the August 2026 spam update and the May 2026 core update also dropped in AI Overviews and AI Mode. *Practitioner, cases (1 manual-action case, 4 spam-update cases).*[^gg-mtai][^gg-spam][^gg-may2026] ChatGPT's cascade fits its use of Google results for paid "thinking" searches ([AI assistants](ai-assistants.md#4-fewer-sources-known-sources-english-queries)). **Do:** in a recovery, fix the Google problem first ([core-update recovery](../situations/core-update-recovery.md)).
- **Preferred Sources reach AI answers.** Google announced Preferred Sources in August 2025 and rolled it out globally in April 2026; since May 2026 a user's preferred sources also influence AI Overviews and AI Mode, not only Top Stories. *Official announcements, relayed.*[^gn-loyalty] It mostly benefits timely editorial content; for a shop it matters for a magazine or guide section ([Google Discover](../channels/google-discover.md)). Its site-level field: [section 1](#1-quality-is-scored-per-section-and-new-urls-start-from-its-average).

## 10. Intent decides the kind of page, per market
- **Two systems pick the kind of result.** Intent Brain gives each query a probability across 20 broad intents per language and country; seven of them trigger a tab or format (Images, Videos, Maps, Apps, Shopping, News, short videos). Orbit sorts pages into 86 categories scored 0–100. Together they answer what kind of result, from what kind of source. *From the leak (internal schemas, provenance not stated).*[^rs-intent]
- **The same word means different things by market.** "Mercury" read 82 % as a fintech brand on google.com; "mercure" read 50 % planet on google.fr, with hotels in the mix. *Measured, 8 queries in two markets.*[^rs-intent]
- **Commerce has five page roles:** merchant product page, review, comparison, buying guide and top-N list. A query wanting one role is hard to win with another. *From the leak.*[^rs-intent]
- **Freshness, forums and listicles are labelled.** Satisfaction is split by the snippet date's age (1, 3, 30, 90 and 365 days). Authenticity and forum discussion have been counted since mid-2023. Listicles carry their own label and are measured, not filtered; self-promotional rankings were the format that declined in early 2026. *From the leak; the decline is practitioner-reported.*[^rs-intent]
- **Do:** before writing, read each market's results and pick the page role and format they show (product data, reviews, comparison, buying guide, list, forum-style first-hand answers). Back any "best" list with stated criteria and testing. See [keyword research](../channels/keyword-research.md#4-intent).

## 11. Choosing the query's meaning (KScorer)
- **Google scores each interpretation of a query and drops the weak ones.** 56 signals in 12 families vote in three stages: 11 before results, 41 while the results page is assembled, and 6 on whether an answer card appears. *From the leak (internal schemas, provenance not stated).*[^rs-kscorer]
- **Top results count most.** With equal support, the first result weighs ten times the tenth (weight 1/rank). *From the leak.*[^rs-kscorer]
- **Clicks need volume to count.** Confidence from clicks is N/(20+N): about 50 % at 20 impressions, 83 % at 100, 98 % at 1,000. *From the leak.*[^rs-kscorer]
- **One unclear entity drags the reading down.** Entity scores are combined by harmonic mean, so entities recognised at 0.9 and 0.2 give about 0.33, not 0.55. *From the leak.*[^rs-kscorer]
- **Local intent checks local quality.** The mean quality of the top three local results is itself a signal. *From the leak.*[^rs-kscorer]
- **Do:** name brands, product lines and models exactly as the Knowledge Graph does, consistently across site and listings, so the interpretation your page serves isn't the weak one. See [homepage and brand](../page-types/homepage-and-brand.md).

## 12. A vendor's model of the ranking pipeline
SERPrecon, which sells an SEO content-scoring tool, compiled the leaks, DOJ testimony and patents into one model of how Google ranks. It is the vendor's reading, not a Google description, and contains no tests.
- **Two retrievals run side by side.** Lexical candidates come from an inverted index scored with BM25, semantic candidates from cosine similarity of query, document and passage embeddings; the two lists are merged and deduplicated. *Inference, relayed (leaks, DOJ testimony).*[^srp-search-engine-works]
- **The index is tiered before any query.** Tiers are likened to RAM, SSD and slow storage; placement is "more than likely" influenced by clicks, user data and search frequency, and retrieval drops to the next tier only when a tier lacks enough high-scoring documents. *Inference, relayed (DOJ testimony).*[^srp-search-engine-works] It fits the index tiers in [section 1](#1-quality-is-scored-per-section-and-new-urls-start-from-its-average).
- **Cheap scoring first, expensive reranking second.** A first pass combines BM25, cosine similarity, index-time quality signals and NavBoost click data into hundreds to thousands of documents; heavier rerankers (BERT, RankEmbed) then read the page text against the query; Glue blends verticals including Shopping; twiddlers apply diversity, manual actions, DMCA, freshness and official-site boosts. *Inference, relayed (DOJ testimony, leak).*[^srp-search-engine-works] Same two-stage shape as [section 2](#2-click-memory-per-query-and-page-navboost).
- **Quality is computed at index time, independent of the query:** PageRank and links, SpamBrain (which can keep a page out of the index, showing as "crawled, not indexed"), helpful-content classifiers, Core Web Vitals and site-authority metrics. *Inference, relayed (leak).*[^srp-search-engine-works] See [section 5](#5-indexing-is-a-quality-decision).
- **The query is rewritten before retrieval:** spellcheck, intent classification, named-entity recognition, synonym expansion, freshness detection (QDF), SafeSearch and location detection. *Inference.*[^srp-search-engine-works]
- **BM25, not keyword density.** BM25 weights term frequency with diminishing returns, rarity (IDF) and length normalisation; the author says no engine uses keyword density, H2 counts or tool TF-IDF scores. *Practitioner.*[^srp-semantic-seo] It agrees with [section 3](#3-exact-terms-still-count-in-the-first-scoring-step): a missing term matters, repetition doesn't.

## 13. Commodity content and information gain
- **Google has not announced a commodity penalty.** Danny Sullivan said commodity content isn't necessarily your strength and to emphasise what is original; John Mueller's 2019 test is whether the site would be the objectively best result. Google has not said commodity content is penalised or that a "commodity score" exists. *Official, relayed (Search Engine Journal).*[^srp-commodity-content] Google's AI guidance on the same point: [Google AI features](google-ai-features.md#15-google-asks-for-non-commodity-content).
- **An originality field exists.** The 2024 leak has `OriginalContentScore`, stored 0–127 and present only on low-content pages; its weight is unknown. *From the leak.*[^srp-commodity-content]
- **Information-gain patents.** US11354342B2 scores how much new information a document adds relative to documents the user has already seen;[^srp-commodity-content] US20200349181A1 describes the same novelty idea, and its explainer stresses that the patent does not confirm use in Search and that no numeric thresholds exist. *Patent.*[^mlseo-info-gain] Near-duplicate detection by simhash is published research (2007). *Patent; use unconfirmed.*[^srp-commodity-content]
- **Do:** before writing, list what the top 10–20 pages already cover (entities, facts, formats) and plan what the page adds: first-hand tests, own data, a clear position. Cover the shared basics briefly. *Practitioner.*[^mlseo-info-gain][^srp-commodity-content] Fits the core-update winners in [section 6](#6-what-core-update-winners-share).

Related: [Google AI features](google-ai-features.md), [AI assistants](ai-assistants.md), [Google Discover](../channels/google-discover.md), [traffic drop](../situations/traffic-drop.md), [category pages](../page-types/category-pages.md), [technical foundations](../technical/technical-foundations.md), [diagnostic tests](../measure/diagnostic-tests.md).

[^leak-2]: Resoneo, leak part 2, 2024-10-31: OfficialPageTwiddler, host diversity caps.
[^leak-3]: Resoneo, leak part 3, 2024-10-31: NSR at site, chunk and article level; site2vec.
[^leak-6]: Resoneo, leak part 6, 2024-10-31: index tiers, crawl skipping, siteFocusScore/siteRadius, new pages inherit the sitechunk average.
[^qus]: Resoneo, QUS, 2025-07-22: per-term scores 0–~10, title +3.5, numbers 0, exact vs derived match.
[^navboost]: Resoneo, "NavBoost & Glue", read 2026-10-27: click-signal families, 13-month history per query and page by country and device, Glue for SERP blocks, compare short visits per page type. No measured ranking effects shown.
[^preferred-sources]: Resoneo, Preferred Sources, May 2026: `uvSitechunk` field.
[^aleyda-may2026]: Aleyda Solis, May 2026 core update, Sistrix 26 May – 2 Jun 2026, via search extracts.
[^aleyda-mar2026]: Aleyda Solis, March 2026 core update, Sistrix 26 Mar – 11 Apr 2026, via search extracts.
[^ignite-news]: Ignite Visibility weekly recap, read 2026-10-27: Ahrefs AIO citations (week of 2026-03-01), Pillarbase scroll-to-text (2026-07-25), Zyppy 400 sites (2026-04-11); secondary reporting, primary studies not checked.
[^mh-trial]: Marie Haynes, 2025-09-04 and 2026-01-22: trial exhibits on "learning from this user feedback", Glue log fields, RankEmbed BERT on 70 days of logs, PageRank as distance from a known good source, Chrome visit data. Exhibit images; numbers not always given.
[^mh-navboost]: Marie Haynes, NavBoost (updated 2025-01-10): 13-month memory (18 months before 2017), leaked click attributes, device and location slices.
[^mh-satisfaction]: Marie Haynes, 2026-01-26: rerankers on the top 20–30, rater frozen-vs-retrained comparisons (Douglas Oard testimony).
[^mh-vector]: Marie Haynes, 2025-06-26: Mueller quote; anecdotal case screenshots.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^mh-cni]: Marie Haynes, 2026-07-16 and 2026-10-13: Search Central Toronto quote, Search Console help text, robots.txt CSS/JS case, one migration case.
[^mh-june2025]: Marie Haynes, 2025-07-18: 5 pages that improved after the June 2025 core update.
[^mh-dec2025]: Marie Haynes, 2026-02-20: 4 sites incl. two ecommerce; rater-guideline counts are her own.
[^field-notes]: Anonymised shop: GA4 google / organic landing pages vs page-type medians, 34 days in Sep–Oct 2026; Search Console query × page, same 5 weeks 2025 vs 2026; live title/H1/slug check.
[^nz-qt]: Natzir Turrado, 2025-05-13: his reading of DOJ testimony — RankEmbed on one month of data, T* = ABC (anchors, body, clicks), Q* largely static and site-level.
[^sbs-sitequality]: SEO by the Sea (Bill Slawski), 2015-05-12: patent US 9,031,929, filed 2012-06-27; ratio of referring queries (site:, brand/name, navigational) to associated (clicked) queries; site may be a subdomain or subdirectory. Blog inactive since 2022.
[^sbs-panda]: SEO by the Sea, 2014-03-25: patent US 8,682,892, filed 2012-09-28; independent links (express and implied) vs reference queries per group; group-wide modification factor.
[^sbs-catquality]: SEO by the Sea, 2019-06-10: application US 2019/0155948, filed 2015-03-31, grant status unconfirmed; top 20–30 reranked by categorical quality after a popularity test (example 70 %).
[^sbs-navqueries]: SEO by the Sea, 2012-12-09: patent US 8,326,826, filed 2009-01-15, reported as likely expired (not verified); session revisions, long clicks, URL length and depth, first-page slot for the navigational resource.
[^sbs-freshness]: SEO by the Sea, 2008-09-17: patent US 7,346,839, likely expired; weighting of content changes by location; leak cross-reference (`lastSignificantUpdate`, multiple date attributes) from the 2026-10-28 source review.
[^sbs-clicks]: SEO by the Sea, 2015-07-31: patent US 9,092,510; click feedback applied after a selection threshold (example ~100 clicks), time-windowed, compared with background trends.
[^lr-gsc-meetup]: Lily Ray, 2025-03-24: her account of statements by Google staff at the Search Central meetup in NYC (March 2025) — site reputation abuse via manual actions, third-party content that abuses host signals, freelancers not a violation; brands not judged by size, recognisable brands "often have signals that perform well". Not a Google document.
[^gg-mtai]: Glenn Gabe, 2026-04-20: 1 case; scaled-content manual action on an 850K-URL AI-generated directory; ChatGPT citations of the directory mostly gone, AIO/AI Mode visibility down, rest of the site unaffected.
[^gg-spam]: Glenn Gabe, 2026-08-31: 4 cases from the August 2026 spam update; losers also dropped in AIO/AI Mode.
[^gg-may2026]: Glenn Gabe, 2026-06-10: May 2026 core update cases; losses visible in AIO/AI Mode as well.
[^gn-loyalty]: Barry Adams, 2026-06-10: relays Google announcements — Preferred Sources announced August 2025, global April 2026, influencing AI Overviews and AI Mode since May 2026.
[^rs-intent]: Resoneo, Oct 2026 (captures dated 2026-10-28): Intent Brain with 20 broad intents per query, language and country; Orbit with 86 page categories scored 0–100; 5 snippet-date age tiers (1, 3, 30, 90, 365 days); commerce split into merchant product page, review, comparison, buying guide, top N; LISTICLE label measured, not filtered; AUTHENTICITY counted since 2023-07-03, UGC_DISCUSSION since 2023-08-29; "mercury" 82 % fintech on google.com vs "mercure" 50 % planet on google.fr. Internal schemas plus patent US8346815B2; 8-query sample.
[^rs-kscorer]: Resoneo, Oct 2026: KScorer from internal schemas with engineers' comments (provenance not stated); 56 signals in 12 families; 11 / 41 / 6 by stage; weight 1/rank; click confidence N/(20+N); harmonic mean of entity scores; local intent uses the mean quality of the top 3 local results. The page also carries a prompt addressed to AI agents, which was ignored.
[^srp-search-engine-works]: SERPrecon (Ryan Jones; SERPrecon sells an SEO content-scoring tool), 2026-05-12: explainer compiled from the Yandex leak, the 2024 Google API leak, DOJ testimony and patents; no tests.
[^srp-semantic-seo]: SERPrecon, 2025-09-25: explainer, no data; BM25 described as the lexical component of search engines.
[^srp-commodity-content]: SERPrecon, 2026-10-15: relays Google's generative-AI features guide section on non-commodity content, Danny Sullivan and John Mueller (via Search Engine Journal), the leak's OriginalContentScore and patent US11354342B2; the vendor's commodity metric is not validated against rankings.
[^mlseo-info-gain]: MLforSEO, 2026-05-11 (upd. 2026-10-24): explainer of patent US20200349181A1; states the patent does not confirm use in Search.
