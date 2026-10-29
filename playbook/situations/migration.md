---
type: Playbook
title: Site migration and URL renames
description: How to rename URLs, move a domain or relaunch a site without losing search, ads or AI visibility — Google's official move rules, same-day internal links and sitemaps, a control set, redirects that keep query strings, feed and ad URLs, pre-launch checks on staging, a separate bucket for parameter and facet URLs, short stable core URLs, daily per-URL and per-template monitoring afterwards, signals derived from one record so sitemaps, hreflang, canonicals and feeds don't drift, and the Removals tool only as a stopgap for a leaked staging or login host.
tags: [seo, migration, redirects, url-renames, site-move, hreflang, google-ads, feeds, staging, monitoring, faceted-navigation, parameters, signal-drift, removals-tool, replatforming]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T09:15:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T09:22:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: chuleta-geo2027
    resource: "https://newsletter.chuletaseo.com/p/geo-2027-la-guia-de-los-expertos"
    title: "Chuleta SEO (Emilio Rodríguez García), GEO 2027: la guía de los expertos (2026-10-29; Spanish newsletter, own projects plus relayed studies)"
  - id: g-indexing-api
    resource: "https://developers.google.com/search/apis/indexing-api/v3/quickstart"
    title: "Google Search Central, Indexing API quickstart (updated 2026-10-16)"
  - id: g-site-move
    resource: "https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes"
    title: "Google Search Central, Site moves with URL changes (updated 2026-08-20)"
  - id: g-canonical
    resource: "https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls"
    title: "Google Search Central, How to specify a canonical URL (updated 2026-07-10)"
  - id: g-crawl-budget
    resource: "https://developers.google.com/search/docs/crawling-indexing/large-site-managing-crawl-budget"
    title: "Google Search Central, Large site owner's guide to managing crawl budget"
  - id: g-hreflang
    resource: "https://developers.google.com/search/docs/specialty/international/localized-versions"
    title: "Google Search Central, Tell Google about localized versions of your page (updated 2026-09-21)"
  - id: leak-6
    resource: "https://www.resoneo.com/google-leak-part-6-how-does-google-search-work-a-deep-dive-into-google-leaks/"
    title: "Resoneo, Google leak part 6: how Google Search works (Oct 2024)"
  - id: qus
    resource: "https://www.resoneo.com/qus-query-expansion-google-and-mysterious-scoring/"
    title: "Resoneo, QUS query expansion and term scoring (Jul 2025; few US examples)"
  - id: chatgpt-retrieval
    resource: "https://think.resoneo.com/chatgpt-retrieval/"
    title: "Resoneo × Oncrawl, What ChatGPT pulls, shows and cites (Jul–Aug 2026)"
  - id: google-ads
    resource: "https://think.resoneo.com/google-ads/"
    title: "Resoneo, Google Ads deep dive (Sep 2026; decompiled app, trial exhibits)"
  - id: gmc-audit
    resource: "https://searchind.com/the-google-merchant-center-audit-i-run-for-every-client/"
    title: "Searchind, The Google Merchant Center Audit I run for every client (Aug 2026, updated Oct 2026)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: mh-cni
    resource: "https://www.mariehaynes.com/crawled-currently-not-indexed/"
    title: "Marie Haynes, Crawled – currently not indexed (2026-07-16) and migration issues may be site quality (2026-10-13)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop's GA4, Search Console and Google Ads data, 2024–2026"
  - id: bp-77k
    resource: "https://botpresso.com/how-did-we-catch-a-77k-url-redirect-on-day-1-with-indexvigil/"
    title: "Botpresso, How we caught a 77K-URL redirect on day 1 (≈2026-10; one enterprise ecommerce case; promotes IndexVigil)"
  - id: bp-migration
    resource: "https://botpresso.com/website-migration-checklist/"
    title: "Botpresso, Website migration checklist (≈2023-11)"
  - id: ah-static
    resource: "https://ahrefs.com/blog/seo-for-static-sites/"
    title: "Ahrefs, SEO for static sites (2026-10-01)"
  - id: ah-enterprise-tech
    resource: "https://ahrefs.com/blog/enterprise-technical-seo/"
    title: "Ahrefs, Enterprise technical SEO (2024-06-28)"
  - id: ah-reclamation
    resource: "https://ahrefs.com/blog/link-reclamation/"
    title: "Ahrefs, Link reclamation (2024-07-31; one domain, 30 days)"
  - id: ah-overopt
    resource: "https://ahrefs.com/blog/over-optimization/"
    title: "Ahrefs, Over-optimization (updated 2024-03-28)"
  - id: ah-topics
    resource: "https://ahrefs.com/blog/topics-not-keywords/"
    title: "Ahrefs, Topics not keywords (2026-03-04)"
  - id: bc-redirects
    resource: "https://www.bruceclay.com/blog/url-redirects-best-practices-during-a-site-migration/"
    title: "Bruce Clay, URL redirects during a site migration (2026-04-28)"
  - id: sbs-navqueries
    resource: "https://www.seobythesea.com/2012/12/navigational-queries-resources/"
    title: "SEO by the Sea, How Google may identify navigational queries and resources (2012-12-09; patent US 8,326,826, filed 2009-01-15)"
  - id: ja-brain
    resource: "https://www.jonoalderson.com/conjecture/your-website-needs-a-brain/"
    title: "Jono Alderson, Your website needs a brain (2026-10-04; worked examples)"
  - id: gg-canonical
    resource: "https://www.gsqi.com/marketing-blog/rel-canonical-hint-cascade-chatgpt/"
    title: "Glenn Gabe, Rel canonical is just a hint — cascade to ChatGPT (2026-02-17; 3 client cases)"
  - id: am-utm-not-working
    resource: "https://www.analyticsmania.com/post/utm-parameters-not-working-in-google-analytics-4/"
    title: "Analytics Mania, UTM parameters not working in GA4 (updated 2026-10-12)"
  - id: am-cross-domain
    resource: "https://www.analyticsmania.com/post/google-analytics-4-cross-domain-tracking-not-working/"
    title: "Analytics Mania, GA4 cross-domain tracking not working (updated 2026-10-12)"
  - id: mlseo-migration
    resource: "https://www.mlforseo.com/machine-learning-tutorials/fuzzy-matching/seo-site-migration-checklist/"
    title: "ML for SEO, The SEO site migration checklist I use (2026-10-24; procedure, 43 checks)"
  - id: wd-html
    resource: "https://web.dev/learn/performance/general-html-performance"
    title: "web.dev, General HTML performance considerations (2023-11-01; guidance)"
  - id: mlseo-404-fuzzy
    resource: "https://www.mlforseo.com/machine-learning-tutorials/fuzzy-matching/404-and-redirect-mapping-with-fuzzy-matching-in-google-colab-python/"
    title: "ML for SEO, 404 and redirect mapping with fuzzy matching (2025-08-09; method, no benchmarks)"
---

# Site migration and URL renames

Use this page before any change that alters URLs: slug renames, category restructures, a new shop system, a domain or subdomain move, or a redesign that touches templates.

## Rules
- **Map every old URL to one new URL and 301 or 308 it in one hop — one hop even when protocol and host change together — for at least a year** ([section 1](#1-googles-official-rules), [section 7](#7-parameter-and-facet-urls-in-the-redirect-map)). *Official; practitioner for combined changes.* Build the map by fuzzy matching and check every partial match by hand ([section 9](#9-fuzzy-matched-redirect-maps)). *Practitioner.*
- **Switch internal links and sitemaps on the same day as the redirects, and on the new platform derive sitemaps, hreflang, canonicals, schema and feeds from one record so they never drift apart** ([section 2](#2-what-the-official-rules-leave-out), [section 8](#8-signal-drift-trace-ordinary-edits-before-replatforming)). *Official for the map; same day is from the leak plus inference; drift is practitioner, worked examples.*
- **Keep an unchanged control set of URLs** so you can tell a migration loss from a market-wide move ([section 2](#2-what-the-official-rules-leave-out)). *Inference.*
- **Every redirect must keep the query string**, or ad clicks lose gclid and UTM ([section 3](#3-ads-feeds-and-ai-crawlers)). *Field notes.*
- **Update feed links and ad final URLs with the site, and re-check ad copy against the new page** ([section 3](#3-ads-feeds-and-ai-crawlers)). *From code; practitioner.*
- **Don't rename slugs for keywords without testing first** — the exact-term theory often fails ([section 4](#4-slugs-and-exact-terms)). *Observed output, few examples; field notes.*
- **Use Change of Address only for domain or subdomain moves**, not HTTP→HTTPS, www or path changes ([section 1](#1-googles-official-rules)). *Official.*
- **Diff staging against production per template and test the redirect map on a separate stage before launch**; launch at low traffic, away from seasonal peaks and core updates; if staging or a login host leaks into the index, pair the Removals tool with a lasting fix ([section 6](#6-pre-launch-checks)). *Practitioner*; Removals *Practitioner case.*
- **Track index status per URL daily after launch, including legacy URL patterns that still earn clicks** — Search Console's reports show the decline, not the cause ([section 5](#5-monitoring-after-launch)). *Practitioner, one case.*
- **Don't relaunch a design without an SEO review** — one redesign ended ~2 years of topic leadership ([section 2](#2-what-the-official-rules-leave-out)). *Practitioner case.*
- **Give parameter, filter and facet URLs their own bucket in the redirect map** — redirect, keep, canonicalise or noindex by purpose, never bulk-redirect them; old URLs with no equivalent return 404 ([section 7](#7-parameter-and-facet-urls-in-the-redirect-map)). *Practitioner.*

## Steps
1. **Inventory:** export every URL with clicks, impressions, backlinks, ad final URLs, sitelinks and feed `link` values — including every legacy URL pattern that still earns clicks ([section 5](#5-monitoring-after-launch)). Crawl production and record per template: status, canonicals, robots, schema, internal links and anchors, Core Web Vitals, top pages ([section 6](#6-pre-launch-checks)). Before replatforming, trace ordinary edits (noindex, delete, price or stock change, new variant) and list every output that reacts ([section 8](#8-signal-drift-trace-ordinary-edits-before-replatforming)).
2. **Map** old → new, one to one where possible, with no chains, no JavaScript redirects and no meta refresh; pages with no successor and no backlinks can return 404 or 410. Score candidates by fuzzy matching and review partials by hand ([section 9](#9-fuzzy-matched-redirect-maps)). Add the most-linked URLs that already return 404 ([section 5](#5-monitoring-after-launch)). Put parameter, filter and facet URLs in a separate bucket and decide per pattern ([section 7](#7-parameter-and-facet-urls-in-the-redirect-map)).
3. **Pick a control set** of URLs that won't change, from the same sections.
4. **Prepare new URLs:** self-canonical, updated hreflang, temporary noindex removed ([technical foundations](../technical/technical-foundations.md#3-site-moves-and-url-renames), [canonicals](../technical/technical-foundations.md#2-canonicals-and-duplicates)).
5. **Check staging:** blocked by robots.txt disallow plus server-side auth; crawled and diffed 1:1 with production; server rendering and mobile/desktop parity on samples; trailing slash, 404 probe and sitemap checks ([section 6](#6-pre-launch-checks)). Get an SEO review of any redesign ([section 2](#2-what-the-official-rules-leave-out)).
6. **Test the redirect map** on a separate stage, not on production ([section 6](#6-pre-launch-checks)).
7. **Pick the launch date:** lowest traffic, away from seasonal peaks and expected core updates ([section 2](#2-what-the-official-rules-leave-out)).
8. **Launch day:** server-side 301/308 in one hop with the query string kept; internal links, navigation and sitemaps switched; feed links and ad final URLs updated; Change of Address only for a domain move.
9. **Same day:** request every redirected URL with a test gclid; confirm the parameter arrives. Test the live site, not only staging ([section 6](#6-pre-launch-checks)).
10. **Submit the new sitemap.** Redirect warnings on the old one can be ignored during the move.
11. **After launch:** list-crawl the old URLs, check the top URLs with a second crawler, track index status per URL daily and crawl a sample per template daily ([section 5](#5-monitoring-after-launch)).
12. **Monitor weekly** for at least the settling period ([section 5](#5-monitoring-after-launch)).

## 1. Google's official rules
- "It's important to map your old site's URLs to the URLs for the new site"; use the map to update internal links and sitemaps.[^g-site-move]
- "Use HTTP permanent redirects if possible, such as 301 and 308" — server-side, no chains — and keep them "for as long as possible, generally at least 1 year".[^g-site-move] Redirects are "a strong signal" for canonicalisation; sitemap inclusion is "a weak signal".[^g-canonical] Avoid redirect chains, which also waste crawl.[^g-crawl-budget]
- New URLs need a self-canonical, updated hreflang, and any temporary noindex removed.[^g-site-move] Hreflang uses fully qualified URLs and must be reciprocal: "If two pages don't both point to each other, the tags will be ignored."[^g-hreflang]
- Change of Address is for domain or subdomain moves only.[^g-site-move]
- Expect "a few weeks or more" for a medium site; larger sites take longer.[^g-site-move]
- Removed pages return 404 or 410; a 404 is "a strong signal not to crawl that URL again".[^g-crawl-budget]

## 2. What the official rules leave out
- **New URLs start from their section's average.** The 2024 leak describes quality scores per section; a new, unevaluated page inherits the section average. *From the leak.*[^leak-6] Moving pages into a weaker section, or mixing thin URL sets into a strong one, changes their starting point.
- **Same-day switch and a control set.** Redirect every old URL in one hop, switch internal links and sitemaps the same day, and keep an unchanged control set to measure against. *Inference from the leak.*
- **Quality can look like a migration bug.** One case suggests a migration can trigger a quality review; "Crawled – currently not indexed" usually means quality, not technology. *One case.*[^mh-cni]
- **Timing.** Don't launch inside a core or spam rollout: rankings move throughout it, and you can't separate the two effects ([update dates](../reference/google-updates-timeline.md#how-to-use-the-dates)). *Inference.* A practitioner checklist adds: launch at the lowest-traffic time, away from seasonal peaks and expected core updates ([seasonal peaks](seasonal-peaks.md)). *Practitioner.*[^bp-migration]
- **Redesigns are migrations too.** A B2B uniforms shop covered ~2,500 keywords with 114 ecommerce pages and held topic leadership for ~2 years, until a redesign launched without SEO review. *Practitioner case, vendor data.*[^ah-topics]

## 3. Ads, feeds and AI crawlers
- **Query strings.** In one shop some old URLs redirected without the query string; ad clicks lost gclid and UTM, and affected campaigns were undercounted for months.[^field-notes]
- **Parameter stripping.** Sites, single-page apps and CDNs that strip or 404 on unknown query parameters kill UTMs and the cross-domain `_gl` linker; whitelist `utm_*` and `_gl` in the new platform's routing and caching rules, and run the [UTM survival check](../measure/diagnostic-tests.md#28-utm-survival-check). *Practitioner*, Analytics Mania (a practitioner who sells GA4/GTM courses).[^am-utm-not-working][^am-cross-domain]
- **Landing page as ad input.** Google Ads builds an LLM summary of each landing page and checks generated assets for faithfulness against it. *From code.*[^google-ads] When a final URL changes, check that headlines and descriptions describe the new page.
- **Feed links are landing URLs.** Free-listing clicks now go straight to the retailer page set in the feed (Shopping tab, Chrome default, AI Mode grids).[^brodie-notes] Check them for redirects, lost parameters and the right variant.
- **Backend renames move slugs.** Change product titles in the feed, not the shop backend: a backend rename can change the URL slug and needs redirects and an ads URL check. *Practitioner.*[^gmc-audit]
- **AI crawlers find pages by links.** GPTBot followed internal links and never fetched sitemap-only URLs.[^chatgpt-retrieval] Stale internal links leave AI crawlers on redirects; a sitemap alone won't introduce the new URLs. See [AI crawlers and controls](../technical/ai-crawlers-and-controls.md).

## 4. Slugs and exact terms
A term in the title adds ~3.5 to its query score on average; some terms must match exactly. *Observed output, few US examples.*[^qus] But in one shop, 6 of 7 lost queries already carried their exact phrase in title and H1; only the seventh, a compound noun missing from title, H1 and slug, fit the lexical explanation.[^field-notes] Run the [exact-term gap test](../measure/diagnostic-tests.md#1-exact-term-gap-on-lost-queries) before a keyword-driven rename; usually title and H1 are enough. Keep years out of slugs ([seasonal peaks](seasonal-peaks.md)).

**Short and stable beats keyword-perfect.** A Google patent on navigational queries favours shorter URLs at shallower depth; the patent has likely expired, but session-based click signals survive per trial testimony. *Patent.*[^sbs-navqueries] Keep brand and core category URLs short, shallow and unchanged — every rename restarts their history ([homepage and brand](../page-types/homepage-and-brand.md)).

## 5. Monitoring after launch
- **Index status per URL, daily.** In one Magento migration a developer's bulk redirect hit a legacy URL template of 77,493 URLs (prior 3 months: 8.23K clicks, 196K impressions, 4.2 % CTR, average position 6.9). Search Console only showed the decline; a daily per-URL check through the URL Inspection API showed each URL move from "Indexed" to "Page with redirect" on a dated crawl. *Practitioner, one case, vendor promoting its tool.*[^bp-77k] **Do:** before a migration or template change, export every indexed URL pattern that earns clicks, legacy ones included; check status, reason and last crawl per URL daily; alert the same day ([test 17](../measure/diagnostic-tests.md#17-daily-index-status-per-url)).
- **Sample crawls per template.** After launch, crawl a daily sample of URLs that covers every template, plus a smaller crawl after each production push. *Practitioner.*[^ah-enterprise-tech] One practitioner checklist sets daily monitoring for 2 weeks after launch and reviews at 3, 6 and 12 months, and keeps redirects permanently rather than for Google's minimum of a year. *Practitioner.*[^mlseo-migration] Keep the daily crawl at least that long, and until clicks and indexation per template have settled. *Inference.* See [scaling content and templates](scaling-content-and-templates.md#5-per-template-sample-crawls).
- **List-crawl the old URLs** after launch (each should 301 in one hop) and check the top URLs with a second crawler. *Practitioner.*[^bp-migration]
- **Redirect chains.** Fix chains at 5+ hops; Google follows up to 10 (Mueller, relayed by Ahrefs). *Practitioner, relayed.*[^ah-overopt][^ah-enterprise-tech] Link internally to the final URL, in its correct trailing-slash form; every redirect adds a request. *Official.*[^wd-html]
- **Reclaim links to 404s.** Monthly, 301 the most-linked URLs that return 404 to the closest live equivalent. One domain lost 6,285 links in 30 days, 594 of which passed a "best links" filter; redirected linking pages are "rarely worth pursuing". *Practitioner, one domain, vendor data.*[^ah-reclamation]
- **Clicks by directory**, migrated vs control set, weekly ([test 3](../measure/diagnostic-tests.md#3-loss-by-directory)); see [Search Console](../measure/search-console.md).
- **Indexed pages by page type** ([test 8](../measure/diagnostic-tests.md#8-indexed-pages-by-page-type)).
- **Ad landing URLs with a test gclid**, weekly ([analytics](../measure/analytics.md)).
- **Conversions after any checkout change:** in one shop, ad conversion tracking stayed broken for 6–8 months after a checkout rebuild.[^field-notes]
- **AI-bot status codes in server logs**, and whether the new URLs get fetched at all ([diagnostic tests](../measure/diagnostic-tests.md)).
- If clicks fall, follow [traffic drop](traffic-drop.md).

## 6. Pre-launch checks
- **Baseline.** Crawl production and record per template: status codes, canonicals, robots directives, schema, internal links and anchors, Core Web Vitals, top pages. *Practitioner.*[^bp-migration]
- **Staging.** Block it with a robots.txt disallow plus server-side authentication; crawl it and diff 1:1 against the production baseline; confirm server-side rendering and mobile/desktop parity on samples. *Practitioner.*[^bp-migration][^ah-enterprise-tech]
- **AI-search baseline.** Before launch, record rich results, AI Overview appearances and citations in ChatGPT, Perplexity and Gemini; keep entity `@id` values stable; diff the new production robots.txt against the old one; submit changed URLs via IndexNow. *Practitioner.*[^mlseo-migration]
- **Redirect map.** 1:1 301s, no chains, no JavaScript redirects, no meta refresh — tested on a separate stage. *Practitioner.*[^bp-migration]
- **If staging or a login host leaks into the index.** Search Console's Removals tool hid a public login subdomain in about 8–10 hours, but it doesn't deindex — the hiding is temporary. Pair it with a lasting fix: 404/410, noindex or authentication; a robots.txt disallow is not a fix. List every subdomain as a property so you see such leaks. *Practitioner case.*[^gg-canonical]
- **Static and JavaScript sites.** One trailing-slash format, set in both framework and host; request URLs you know don't exist and confirm they return 404 (single-page-app fallbacks cause soft 404s); keep noindex pages out of sitemaps; test several pages per template; compare old vs new canonicals, metadata, schema and sitemap rules; test the live site, not only staging. Ahrefs' own migration accidentally nofollowed every internal link. *Practitioner.*[^ah-static] Compare raw and rendered internal links per template ([test 16](../measure/diagnostic-tests.md#16-raw-vs-rendered-internal-links)).
- **Not adopted: submitting top URLs through the Indexing API.** The same checklist recommends submitting the top 200 URLs via the Indexing API.[^bp-migration] Google: it "can only be used to crawl pages with either JobPosting or BroadcastEvent embedded in a VideoObject",[^g-indexing-api] so it isn't a migration tool; rely on redirects, updated internal links and sitemaps ([section 1](#1-googles-official-rules)). *Official scope; practitioner step rejected.*

## 7. Parameter and facet URLs in the redirect map
- Review parameter, filtered and faceted URLs separately: decide per pattern whether to redirect, keep, canonicalise or noindex; "avoid bulk redirecting all parameter URLs without reviewing their purpose". *Practitioner.*[^bc-redirects]
- Old URLs with no equivalent return 404 rather than a redirect to an unrelated page; combined protocol and host changes still go old → final in a single hop; test on staging, then on the live site. *Practitioner, consistent with Google's site-move rules.*[^bc-redirects]
- **Do:** add a facet/parameter bucket to the redirect map, list each pattern with its decision, and check that indexable facet URLs keep Google's facet rules ([faceted navigation](../technical/technical-foundations.md#1-faceted-navigation), [category pages](../page-types/category-pages.md)).

## 8. Signal drift: trace ordinary edits before replatforming
- **Outputs drift when they don't share a source.** Example: a page is noindexed at 09:00 but the sitemap regenerates at midnight — about 15 hours of conflicting signals. Hreflang siblings, canonicals, schema availability and feeds must all derive from one record; output that is valid but wrong passes every validator. *Practitioner, worked examples.*[^ja-brain]
- **Do:** before replatforming, trace a handful of ordinary edits — noindex a page, delete a product, change a price or stock level, add a variant — and list every output that reacts (sitemap, hreflang, canonical, schema, feed, internal links); on the new platform, update sitemaps and hreflang on the event, not on a nightly batch, and test outputs against the intended state, not only against a validator ([technical foundations](../technical/technical-foundations.md), [feeds and Merchant Center](../channels/feeds-and-merchant-center.md)).

## 9. Fuzzy-matched redirect maps
ML for SEO sells courses and promotes its own notebooks; the methods below come without accuracy benchmarks.
- **Score candidates, then review.** Match old to new URLs by fuzzy string matching (Levenshtein, via libraries such as TheFuzz, RapidFuzz or PolyFuzz) on URL, title, H1, H2 and meta description, score 0–100, and count how many algorithms agree; flag every match below 70. Priority URLs are those with at least 100 clicks or 5 referring domains. In the author's example a 71-score partial still pointed at the wrong page, and a 38 led to a 410 rather than a homepage redirect. *Practitioner.*[^mlseo-migration]
- **Thresholds depend on the data.** Use 60–70 for inconsistent datasets and 85–90 for minor URL variations; label Exact = 100, Partial = 50 to under 100, No match = under 50; partials of 70 or more can be pre-built redirects but still need a manual check. No-code tools suffice below about 100–300 URLs; use Python above about 1,000. *Practitioner, no accuracy benchmark.*[^mlseo-404-fuzzy]
- **What a homepage redirect costs.** A rental portal that redirected a whole section to its homepage fell from an estimated 21,645 to 3,065 monthly visits for that section, losing rankings for established commercial terms. *Practitioner, one case, third-party visibility estimate.*[^chuleta-geo2027]
- **Do:** check every priority URL and every partial match by hand; send "no match" URLs to 404 or 410, not to the homepage ([section 1](#1-googles-official-rules)).

Related: [technical foundations](../technical/technical-foundations.md), [new market](new-market.md), [feeds and Merchant Center](../channels/feeds-and-merchant-center.md), [scaling content and templates](scaling-content-and-templates.md), [internal linking](../technical/internal-linking.md), [links and digital PR](../channels/links-and-digital-pr.md).

[^g-site-move]: Google, site moves with URL changes, read 2026-10-27.
[^g-canonical]: Google, canonical URLs, read 2026-10-27.
[^g-crawl-budget]: Google, crawl budget guide, read 2026-10-27.
[^g-hreflang]: Google, localized versions, read 2026-10-27; nothing explicit on IP-based redirects in the extracted text.
[^leak-6]: Resoneo, leak part 6, 2024-10-31: index tiers, crawl skipping, siteFocusScore/siteRadius, new pages inherit the sitechunk average.
[^mh-cni]: Marie Haynes, 2026-07-16 and 2026-10-13: Search Central Toronto quote, Search Console help text, robots.txt CSS/JS case, one migration case.
[^field-notes]: Anonymised shop, 2024–2026: every "Example" on this page. The shop's own caveat list records dates and sizes; they are omitted here so the shop can't be identified.
[^google-ads]: Resoneo, Google Ads deep dive, Sep 2026: LLM_LP_SUMMARY, LP_ASSET_FAITHFULNESS, productFidelityScore, pLQ vs pCTR; AdsBot and robots.txt.
[^brodie-notes]: Brodie Clark notes, Jul 2025 – Sep 2026 (month anchors #jul-2025, #oct-2025, #nov-2025, #mar-2026, #apr-2026, #may-2026, #jun-2026, #jul-2026, #aug-2026, #sep-2026): screenshots, some backed by Google or OpenAI posts and Digiday.
[^gmc-audit]: Searchind, Merchant Center audit, read 2026-10-27: title test design, feed-only changes, material most missing, specific categories, auto-created data sources, disapproval CSV, warehouse transfer.
[^chatgpt-retrieval]: Resoneo × Oncrawl, read 2026-10-27: ~202-character snippet from the H1; sitemap-only URLs not fetched by GPTBot.
[^qus]: Resoneo, QUS, 2025-07-22: per-term scores 0–~10, title +3.5, numbers 0, exact vs derived match.
[^bp-77k]: Botpresso, ≈2026-10 (no publish date shown): one enterprise Magento migration, Search Console figures for the 3 months before; daily URL Inspection API checks; the agency promotes its own monitoring tool.
[^bp-migration]: Botpresso, migration checklist, ≈2023-11: practitioner checklist (baseline crawl, staging block and diff, SSR and parity, 1:1 redirect map tested on a separate stage, launch timing, post-launch list crawl and second crawler). Its "submit top 200 URLs via the Indexing API" step contradicts Google's Indexing API documentation (JobPosting and BroadcastEvent only) and is left out.
[^ah-static]: Ahrefs, SEO for static sites, 2026-10-01: trailing slash, 404 probes, sitemap hygiene, per-template tests, old vs new comparison, live-site test; own migration nofollow incident.
[^ah-enterprise-tech]: Ahrefs, Enterprise technical SEO, 2024-06-28: staging behind HTTP auth, daily per-template sample crawls, crawls after each push, redirect chains > 5 hops; no monitoring length given.
[^ah-reclamation]: Ahrefs, link reclamation, 2024-07-31: own domain, 6,285 lost links in 30 days, 594 after filtering; a third-party case reclaimed 31 of 166 (18.67 %); vendor data.
[^ah-overopt]: Ahrefs, over-optimization, updated 2024-03-28: relays Mueller on fixing redirect chains at 5+ hops and Google following up to 10.
[^ah-topics]: Ahrefs, 2026-03-04: B2B uniforms case (~2,500 keywords, 114 ecommerce pages, ~2 years of leadership until a redesign without SEO review); keyword counts from Ahrefs' own tools.
[^g-indexing-api]: Google Indexing API quickstart, read 2026-10-28: allowed only for JobPosting and BroadcastEvent-in-VideoObject pages.
[^bc-redirects]: Bruce Clay, 2026-04-28: parameter, filtered and faceted URLs reviewed separately; no bulk redirects of parameter URLs; 404 when no equivalent; single hop for combined protocol + host changes; staging then live tests. Practitioner method.
[^sbs-navqueries]: SEO by the Sea, 2012-12-09: patent US 8,326,826 (filed 2009-01-15, likely expired); navigational resources from session patterns and long clicks; shorter URLs and shallower depth favoured.
[^ja-brain]: Jono Alderson, 2026-10-04: worked examples of signal drift (noindex at 09:00, sitemap at midnight → ~15 h conflict); hreflang, canonicals, schema availability and feeds from one record; event-driven updates; valid-but-wrong output.
[^gg-canonical]: Glenn Gabe, 2026-02-17: client cases; Removals tool hid a public login subdomain in ~8–10 hours but doesn't deindex; pair with 404/410, noindex or auth; robots.txt not a fix; list every subdomain in Search Console.
[^am-utm-not-working]: Analytics Mania, updated 2026-10-12: sites, SPAs and CDNs stripping or 404ing on unknown parameters lose UTMs.
[^am-cross-domain]: Analytics Mania, updated 2026-10-12: stripped query strings break the _gl cross-domain linker.
[^mlseo-migration]: ML for SEO, 2026-10-24: 43-check procedure; one hop 301/308 to a 200, daily monitoring for 2 weeks, reviews at 3, 6, 12 months, redirects kept permanently; fuzzy-matched redirect map (URL, title, H1, H2, meta description; flag <70; priority = ≥100 clicks or ≥5 referring domains); AI-search baseline, stable @id, robots.txt diff, IndexNow.
[^wd-html]: web.dev, 2023-11-01: avoid redirects and chains (e.g. HTTP → HTTPS then trailing slash); link to final URLs; each redirect adds a request.
[^mlseo-404-fuzzy]: ML for SEO, 2025-08-09: fuzzy thresholds 60–70 for inconsistent data, 85–90 for minor URL variations; Exact 100 / Partial 50–<100 / No match <50; no-code below ~100–300 URLs, Python above ~1,000. Method, no accuracy benchmark.
[^chuleta-geo2027]: Chuleta SEO (Emilio Rodríguez García), 2026-10-29, Spanish newsletter, read in full; claims translated. Own projects: a section redirected to the homepage (Sistrix estimate 21,645 → 3,065), ~9,340 robots.txt-blocked pages still indexed (Search Console, Aug–Oct 2026). Relays SE Ranking: 82.5 % of US brand searches show an AI Overview, 62 % of cited pages rank outside the organic top 10 (sample and period not stated).
