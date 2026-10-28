---
type: Playbook
title: Scaling content and templates
description: Programmatic and AI-assisted pages at scale — Google's scaled content abuse policy, what AI-written content data shows, indexation as the quality gate, template inventory and ownership, tickets with money impact, per-template sample crawls, soft 404 rules for out-of-stock products and thin listings, repeated template phrasing and the strip-the-logo test, the pruning order, why not to atomise topics into micro-pages, the August 2026 spam update's feed-generated templates, and programmatic guardrails (minimum data per page, generation from database fields, fact checks, scheduled pruning).
tags: [seo, programmatic, ai-content, templates, governance, indexing, soft-404, ecommerce, pruning, consolidation, spam-update, fact-checking]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: g-spam
    resource: "https://developers.google.com/search/docs/essentials/spam-policies"
    title: "Google Search Central, Spam policies for Google web search (updated 2026-08-28)"
  - id: ah-ai-content
    resource: "https://ahrefs.com/blog/google-doesnt-punish-ai-content/"
    title: "Ahrefs, Google doesn't punish AI content (2026-07-27; 1M top-10 pages, own AI detector)"
  - id: ah-topics
    resource: "https://ahrefs.com/blog/topics-not-keywords/"
    title: "Ahrefs, Topics not keywords (2026-03-04)"
  - id: mh-deindex
    resource: "https://www.mariehaynes.com/an-interesting-look-at-which-pages-google-started-deindexing-in-late-may-2025/"
    title: "Marie Haynes, Which pages Google started deindexing in late May 2025 (2025-06-05; ~40 sites reviewed)"
  - id: ah-enterprise-gov
    resource: "https://ahrefs.com/blog/enterprise-seo-challenges/"
    title: "Ahrefs, Enterprise SEO challenges (2024-07-30)"
  - id: ah-enterprise-tech
    resource: "https://ahrefs.com/blog/enterprise-technical-seo/"
    title: "Ahrefs, Enterprise technical SEO (2024-06-28)"
  - id: bp-soft404
    resource: "https://botpresso.com/what-is-a-soft-404-issue-how-to-fix-it/"
    title: "Botpresso, Soft 404 issues and fixes (≈2026-07)"
  - id: sbs-ngram
    resource: "https://www.seobythesea.com/2017/09/site-quality-scores/"
    title: "SEO by the Sea, Using n-gram phrase models to generate site quality scores (2017-09-21; patent US 9,767,157, filed 2013-03-15)"
  - id: bc-low-activity
    resource: "https://www.bruceclay.com/blog/remove-keep-low-activity-webpages/"
    title: "Bruce Clay, Remove or keep low-activity pages (2025-05-27; qualitative client anecdote)"
  - id: nz-chunk
    resource: "https://natzir.com/en/seo/chunking-content-bad-seo-ai/"
    title: "Natzir Turrado, Why chunking your content is bad for SEO and AI (2025-12-20; review)"
  - id: ls-pseo
    resource: "https://lazarinastoy.com/programmatic-seo-guide/"
    title: "Lazarina Stoy, Programmatic SEO guide (2026-10-22 update; practitioner)"
  - id: gg-spam
    resource: "https://www.gsqi.com/marketing-blog/august-2026-google-spam-update-case-studies/"
    title: "Glenn Gabe, August 2026 spam update case studies (2026-08-31; 4 cases)"
  - id: brief-distinct
    resource: "https://seobrief.substack.com/p/when-the-logo-comes-off-is-it-still"
    title: "Jes Scholz, SEO Brief: distinctiveness (2026-06-18; essay + one client case)"
---

# Scaling content and templates

Use this page before you generate pages at scale — programmatic category or filter pages, AI-assisted product or category text, location or comparison pages from one template — and when you run a site whose SEO lives in a handful of templates.

## Rules
- **Scale only pages that exist for users, not to manipulate rankings** — that is the line Google's scaled content abuse policy draws, regardless of how the text was written; the August 2026 spam update hit feed-generated category and product templates ([section 1](#1-the-policy-line)). *Official*; spam update *Practitioner, 4 cases.*
- **AI-written isn't penalised as such, but heavily AI-written pages index and rank less often** — every scaled page needs unique data: specs, stock, tests, own photos ([section 2](#2-what-ai-written-content-data-shows)). *Measured, vendor data, correlation.*
- **Treat indexation rate per template as the quality gate** — scale only templates whose indexation holds ([section 3](#3-indexation-is-the-quality-gate)). *Case observations plus statements; inference for the gate.*
- **Keep a template inventory with an owner per template**, and file fixes as tickets with acceptance criteria, evidence and money impact ([section 4](#4-governance-templates-owners-tickets)). *Practitioner.*
- **Change URL structures once** — design the pattern before you scale, not after ([section 4](#4-governance-templates-owners-tickets)). *Practitioner.*
- **Crawl a fixed URL sample per template daily after launches, and a smaller sample after every production push** ([section 5](#5-per-template-sample-crawls)). *Practitioner.*
- **Write down soft 404 rules for inventory** — when a product gets 410, when a thin listing is noindexed — and keep temporarily out-of-stock products indexable by default ([section 6](#6-soft-404s-on-inventory)). *Practitioner; Google's docs give no rule.*
- **Audit repeated template phrases before rolling copy out across thousands of pages** — boilerplate that reads like low-quality sites can drag the whole set ([section 7](#7-template-phrasing-propagates)). *Patent.*
- **Prune in order: update, merge, 301, remove last** — and check what a page feeds before removing it ([section 8](#8-pruning-order)). *Practitioner, qualitative.*
- **Don't atomise a topic into micro-pages**; split only when the search results differ ([section 9](#9-dont-atomise-into-micro-pages)). *Official statements, relayed; practitioner test.*
- **Set a minimum number of unique data fields per template page, generate text only from database fields, and fact-check the output against the source** — titles, metadata and alt text included ([section 10](#10-programmatic-guardrails)). *Practitioner.*

## Steps
1. **Inventory templates:** list every template (product, category, filter, brand, location, comparison, editorial…), its URL pattern, page count and owning team.
2. **Check the policy line:** for each planned page set, name what a user gets on page *n* that they don't get on page *n−1*; if the answer is only a swapped keyword, don't build it ([section 1](#1-the-policy-line)). Strip the logo from a sample page: if it could belong to any site, it adds nothing ([section 7](#7-template-phrasing-propagates)).
3. **Define the unique data per template:** which fields (specs, stock, prices, reviews, own photos, test results) make each page different; AI text only around that data ([section 2](#2-what-ai-written-content-data-shows)). Set the minimum number of unique fields a page needs to exist; skip or merge combinations below it ([section 10](#10-programmatic-guardrails)). Count the phrases that repeat across the sample and rewrite the generic ones ([section 7](#7-template-phrasing-propagates)).
4. **Pilot:** launch a sample, then watch its indexation rate in Search Console by page type ([test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type), [test 17](../measure/diagnostic-tests.md#17-daily-index-status-per-url)) before scaling the rest.
5. **Fix URL patterns now:** trailing slash, parameters, hierarchy — a later change means a [migration](migration.md).
6. **Set up monitoring:** a fixed sample of URLs per template, crawled daily after launch and after each push ([section 5](#5-per-template-sample-crawls)).
7. **Write the inventory rules:** discontinued, temporarily out of stock, empty or near-empty listings ([section 6](#6-soft-404s-on-inventory)); watch the Soft 404 count by page type.
8. **File issues by template** with an owner, acceptance criteria and money impact ([section 4](#4-governance-templates-owners-tickets)).
9. **Prune** weak pages in order — update, merge, 301, remove — after checking what links and anchors they feed ([section 8](#8-pruning-order)); schedule a regular review of unindexed and unvisited pages per template ([section 10](#10-programmatic-guardrails)).

## 1. The policy line
- Google's spam policies define **scaled content abuse**: "many pages are generated for the primary purpose of manipulating search rankings". The policy targets the purpose, not the production method.[^g-spam] See [links and spam policies](../technical/technical-foundations.md#11-links-and-spam-policies).
- City-swap pages, keyword-variant category pages without their own assortment, and near-duplicate comparison pages are where ecommerce sites cross it. *Inference.*
- **Spam update case.** The August 2026 spam update targeted content, not links: a thin affiliate site whose category and product pages were built programmatically from a marketplace feed (some without images, footer text 97 %+ likely AI-written) lost 14K+ queries; a 1.5M-URL product-information site, ~85 % programmatic, took a site-wide, core-like hit; recovery takes months. *Practitioner, 4 cases.*[^gg-spam] **Do:** audit feed-generated templates before a spam-update window ([core update recovery](core-update-recovery.md), [category pages](../page-types/category-pages.md)).
- Thin page sets also lose on their own: one ~1,000-word article ranked for 2,500 keywords, 473 AIO queries and 279 ChatGPT prompts, while 60+ thin pages of another site totalled 266 keywords. *Practitioner case, vendor data.*[^ah-topics] One strong page per sub-topic beats many thin ones ([keyword research](../channels/keyword-research.md)).

## 2. What AI-written content data shows
- In 1M top-10 pages from 100,000 SERPs (~150K scorable, June 2026), 82.2 % of top-3 pages were under 50 % AI-written and 5.3 % were 100 % AI. *Measured, vendor data, own AI detector, correlation.*[^ah-ai-content]
- Indexation: low-AI pages 49.28 % vs very-high-AI pages 40.35 % (1M pages, ~100K scorable); low- and moderate-AI pages got 2–3× the impressions. *Measured, vendor data, correlation.*[^ah-ai-content]
- **Reading:** Google doesn't punish AI text as such, but pages that are mostly AI tend to carry less that's unique. **Do:** programmatic or AI-assisted product and category text needs unique data (specs, stock, tests, photos); scale only templates whose indexation rate holds. *Inference from the data.*[^ah-ai-content]

## 3. Indexation is the quality gate
- Google drops pages users don't engage with from the index — product pages without original content and thin category or list pages among them — and "Crawled – currently not indexed" usually means quality ([indexing is a quality decision](../how-it-works/google-ranking.md#5-indexing-is-a-quality-decision)). *Case observations plus statements.*[^mh-deindex]
- So the indexation rate of a pilot is the cheapest read of whether a template is good enough to scale. A template whose indexed share falls as you add pages is diluting its section ([section-level quality](../how-it-works/google-ranking.md#1-quality-is-scored-per-section-and-new-urls-start-from-its-average)). *Inference.*

## 4. Governance: templates, owners, tickets
- **Segment audit issues by CMS or template** so each one has an owning team. *Practitioner.*[^ah-enterprise-gov]
- **Tickets carry acceptance criteria, evidence and money impact**; let the dev team adjust the effort estimate rather than fixing it for them. *Practitioner.*[^ah-enterprise-gov]
- **Propose stalled fixes as A/B tests** — a test is easier to approve than a change. *Practitioner.*[^ah-enterprise-gov]
- **Fund shared SEO work centrally** (templates, navigation, sitemaps) instead of per business unit. *Practitioner.*[^ah-enterprise-gov]
- **Change URL structures once only.** *Practitioner.*[^ah-enterprise-tech] Every later change is a [migration](migration.md).
- **Do:** a template inventory with an owner per template and a fixed sample crawl per template ([section 5](#5-per-template-sample-crawls)). *Practitioner.*[^ah-enterprise-gov][^ah-enterprise-tech]

## 5. Per-template sample crawls
- Crawl staging behind HTTP auth before launch; after launch, crawl a daily sample of URLs that covers every template, plus a smaller crawl after each production push; review redirect chains longer than 5 hops. *Practitioner.*[^ah-enterprise-tech]
- No source gives a monitoring length; keep the daily crawl at least until indexation and clicks per template have settled, then fall back to the push-triggered crawl. *Inference; gap open.*
- Pair it with daily index status for the URLs that earn clicks ([test 17](../measure/diagnostic-tests.md#17-daily-index-status-per-url)) and a raw vs rendered link check per template ([test 16](../measure/diagnostic-tests.md#16-raw-vs-rendered-internal-links)).

## 6. Soft 404s on inventory
- Out-of-stock product pages get flagged Soft 404 even when they show related products; listings slip into Soft 404 near zero inventory, and so do JS product grids that fail to render. *Practitioner.*[^bp-soft404]
- The same source recommends 410 for discontinued products, a conditional noindex for temporary stockouts, and noindex for listings below an item threshold (no value given).[^bp-soft404] Google's product markup defines out-of-stock and discontinued availability values but gives no rule on indexing such pages; common practice keeps temporary stockouts indexable with the right availability value (*inference*) — keep that as the default; use noindex only for long stockouts, 410 (or a 301 to the successor) for discontinued products. *Official default; practitioner rules.*
  > **Conflict:** noindex temporarily out-of-stock pages vs keep them indexed — [details](../reference/conflicts.md#out-of-stock-pages-noindex-or-keep-indexed)
- **Do:** write the rules down (when 410, at what item count a category is noindexed) and watch the Soft 404 count by page type in Search Console ([Search Console](../measure/search-console.md)). *Practitioner.*[^bp-soft404] Removed pages return real 404 or 410 ([crawl budget](../technical/technical-foundations.md#6-crawl-budget)).

## 7. Template phrasing propagates
- A Google patent predicts quality for new or unscored sites from the frequencies of 2–5-word phrases, mapped against sites already scored; templated boilerplate that resembles low-quality sites carries that resemblance with it. *Patent.*[^sbs-ngram]
- **Do:** before rolling generated copy out across thousands of pages, list the phrases that repeat across the sample and replace the generic ones with page-specific facts ([section 2](#2-what-ai-written-content-data-shows)).
- **Strip-the-logo test.** Content that could belong to anyone builds the category, not the brand. *Essay.*[^brief-distinct] **Do:** remove the logo from a sample page of each template; if nothing on it tells a reader whose page it is, add own data, photos or tests before scaling ([comparison pages and guides](../page-types/comparison-and-guides.md)).

## 8. Pruning order
- Update first, then merge, then 301, and remove last. Clients who deleted low-performing pages inside a topic section lost head-term rankings, because those pages fed internal links and anchors to the category. *Practitioner, qualitative anecdote, no figures.*[^bc-low-activity]
- **Do:** before pruning, check whether the pages link to the category with useful anchors; keep or merge those. Removed pages return real 404 or 410 ([section 6](#6-soft-404s-on-inventory)); recovery context: [core-update recovery](core-update-recovery.md).

## 9. Don't atomise into micro-pages
- Google's Danny Sullivan (Jan 2026) advised against bite-sized chunks; Bing (Dec 2025) said near-duplicates blur signals. *Official statements, relayed.*[^nz-chunk]
- **SERP-overlap test:** if two planned pages share most of their search results, consolidate them; if the results differ, keep them separate. *Practitioner.*[^nz-chunk] Consolidated guides get anchors and a table of contents ([comparison pages and guides](../page-types/comparison-and-guides.md)).

## 10. Programmatic guardrails
*Practitioner.*[^ls-pseo]
- **Minimum-data rule.** Skip or merge combinations with too few unique data points; set a minimum number of unique fields per template.
- **Generate only from database fields**, and run automated fact checks of the output against the source; give titles, metadata and alt text the same scrutiny as body copy.
- **Scheduled pruning.** Review unindexed and unvisited pages per template on a fixed schedule, then apply the pruning order ([section 8](#8-pruning-order)).
- **Not a shortcut: the Indexing API.** The same author withdrew her 2024 advice to push programmatic pages through the Indexing API, which covers only JobPosting and BroadcastEvent pages ([migration](migration.md#6-pre-launch-checks)).

Related: [migration](migration.md), [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md), [technical foundations](../technical/technical-foundations.md), [internal linking](../technical/internal-linking.md), [core-update recovery](core-update-recovery.md), [diagnostic tests](../measure/diagnostic-tests.md).

[^g-spam]: Google, spam policies, read 2026-10-27: scaled content abuse, site reputation abuse, expired domain abuse definitions.
[^ah-ai-content]: Ahrefs, 2026-07-27: 1M top-10 pages from 100,000 SERPs, ~150K scorable for the top-3 split, ~100K scorable for indexation; Ahrefs' own AI detector; correlation only; vendor data, not independently replicated.
[^ah-topics]: Ahrefs, 2026-03-04: case comparison, keyword counts from Ahrefs' own tools; vendor data.
[^mh-deindex]: Marie Haynes, 2025-06-05: indexed pages falling from 27 May 2025 on ~40 sites; 27,000 → 15,000 case; Mueller and Splitt statements.
[^ah-enterprise-gov]: Ahrefs, Enterprise SEO challenges, 2024-07-30: issue segmentation by team, ticket contents, effort estimates, A/B tests for stalled fixes, central funding; practitioner advice.
[^ah-enterprise-tech]: Ahrefs, Enterprise technical SEO, 2024-06-28: staging behind HTTP auth, daily per-template sample crawls, crawls after each push, redirect chains > 5 hops, change URL structures once; no monitoring length given.
[^bp-soft404]: Botpresso, soft 404 guide, ≈2026-07 (no publish date shown): practitioner advice from an agency promoting its own tools; the noindex recommendations partly contradict Google's ecommerce guidance.
[^sbs-ngram]: SEO by the Sea, 2017-09-21: patent US 9,767,157 (filed 2013-03-15); site quality predicted from 2–5-word n-gram frequency models of scored sites.
[^bc-low-activity]: Bruce Clay, 2025-05-27: pruning order and a client anecdote (head-term losses after deleting pages inside a section); qualitative, no figures.
[^nz-chunk]: Natzir Turrado, 2025-12-20: review; relays Bing (Dec 2025) and Danny Sullivan (Jan 2026); SERP-overlap test.
[^ls-pseo]: Lazarina Stoy, programmatic SEO guide, 2026-10-22 update: minimum-data rule, generation only from database fields, automated fact checks, same scrutiny for metadata and alt text, scheduled pruning of unindexed/unvisited pages; withdrew her 2024 Indexing API advice. Practitioner.
[^gg-spam]: Glenn Gabe, 2026-08-31: 4 August 2026 spam update cases; content, not links; feed-built affiliate site (some pages without images, footer text 97 %+ likely AI-written) lost 14K+ queries; 1.5M-URL product-information site ~85 % programmatic, site-wide hit; recovery takes months.
[^brief-distinct]: Jes Scholz, 2026-06-18: essay; strip-the-logo test (relays NN/g and System1, primaries not read, their figures not used here).
