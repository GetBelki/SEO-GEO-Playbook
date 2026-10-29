---
type: Playbook
title: Homepage and brand pages
description: What to do on the homepage and brand-intent pages — verifiable proof points as text, one page per branded intent, brand queries that no longer guarantee a click, the merchant knowledge panel fed by Merchant Center and Business Profile, clicks without citations, brand identity in core updates, third-party listings that match the site, AI Overviews on branded queries, entity hygiene and Knowledge Graph facts, AI referrals landing on the homepage, brand-verification queries, homepage body copy and "need → brand" statements, short stable brand URLs, hallucinated variants of your hostname, brand display in results (favicon, site name, logo, OG image), and a brand canon of checkable facts with accuracy tracking, early facts for obscure questions, per-language anchor pages and the training cut-off.
tags: [seo, geo, homepage, brand, knowledge-panel, merchant-center, third-party, ecommerce, ai-overviews, entity, knowledge-graph, chatgpt, meta-description, gemini, favicon, site-name, brand-accuracy, multilingual]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: siege-credibility
    resource: "https://www.siegemedia.com/research/credibility-statements"
    title: "Siege Media, Credibility statements and AI visibility (2026-10-26; 585 brands, 63 categories, Peec AI)"
  - id: d2c
    resource: "https://searchind.com/the-complete-d2c-ecommerce-seo-guide-strategies-for-sustainable-growth/"
    title: "Searchind, The Complete D2C Ecommerce SEO Guide (Dec 2025)"
  - id: gm-intents
    resource: "https://www.growth-memo.com/p/traditional-intents-can-no-longer"
    title: "Growth Memo, Traditional intents can no longer… (2026-06-01; ~846,000 US sessions; recommendations partly paywalled)"
  - id: brodie-notes
    resource: "https://brodieclark.com/notes/"
    title: "Brodie Clark, Notes (dated SERP-test sightings with screenshots, Jun 2025 – Oct 2026; month anchors)"
  - id: brodie-loyalty
    resource: "https://brodieclark.com/loyalty-program-promotion-gmc/"
    title: "Brodie Clark, Loyalty programme and promotions in Merchant Center (2025-08-13)"
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10; announced 2026-05-15)"
  - id: aleyda-traffic
    resource: "https://www.aleydasolis.com/en/ai-search/ai-traffic-citations-research/"
    title: "Aleyda Solis, AI traffic vs citations research (~Apr–May 2026; 40 US sites, Semrush + Similarweb; search extracts)"
  - id: siege-bofu
    resource: "https://www.siegemedia.com/research/ai-buying-advice"
    title: "Siege Media, AI buying advice (2026-03-24; ~1,000 bottom-funnel prompts, 57,095 citations, Peec AI)"
  - id: gm-owners
    resource: "https://www.growth-memo.com/p/does-topical-authority-matter-in"
    title: "Growth Memo, Does topical authority matter in ChatGPT (2026-07-20; 1,094 US categories × 5 prompts, Jan–Jun 2026, Semrush data)"
  - id: leak-2
    resource: "https://www.resoneo.com/google-leak-part-2-understanding-the-twiddler-framework/"
    title: "Resoneo, Google leak part 2: twiddlers (Oct 2024)"
  - id: aleyda-mar2026
    resource: "https://www.aleydasolis.com/en/search-engine-optimization/google-march-core-update-2026/"
    title: "Aleyda Solis, March 2026 core update (Sistrix, US; search extracts)"
  - id: mh-dec2025
    resource: "https://www.mariehaynes.com/the-december-2025-core-update-observations-on-4-sites-that-did-well/"
    title: "Marie Haynes, December 2025 core update: 4 sites that did well (2026-02-20)"
  - id: aleyda-citations
    resource: "https://www.aleydasolis.com/en/ai-search/ai-search-citations/"
    title: "Aleyda Solis, AI search citations by source type (2026-08-02; read from search extracts, site returned 403)"
  - id: siege-leader
    resource: "https://www.siegemedia.com/strategy/category-leader-trap"
    title: "Siege Media, The category leader trap (2026-09-25; same prompt set)"
  - id: ipr-local
    resource: "https://ipullrank.com/local-ai-search-data"
    title: "iPullRank (Francine Monahan), Local AI search data (2025-12-16; Yext, 1.6M questions, 6.9M citations)"
  - id: ah-brand-corr
    resource: "https://ahrefs.com/blog/ai-brand-visibility-correlations/"
    title: "Ahrefs, AI brand visibility correlations (2025-12-12; 75,000 brands with DR > 40, Spearman)"
  - id: ah-aio-branded
    resource: "https://ahrefs.com/blog/ai-overviews-on-branded-searches/"
    title: "Ahrefs, AI Overviews on branded searches (2026-10-02; 232.8M US desktop crawls Jul–Sep 2026; 100-brand panel)"
  - id: ah-kg
    resource: "https://ahrefs.com/blog/google-knowledge-graph/"
    title: "Ahrefs, Google Knowledge Graph (2026-05-14)"
  - id: bp-chatgpt-links
    resource: "https://botpresso.com/chatgpt-may-links-update-traffic-impact-study/"
    title: "Botpresso, ChatGPT May links update traffic study (≈2026-07; 52 client sites, GA4)"
  - id: bp-brand-verify
    resource: "https://botpresso.com/how-do-users-verify-a-brand/"
    title: "Botpresso, How users verify a brand (≈2026-10)"
  - id: bp-seo-vs-ai
    resource: "https://botpresso.com/why-winning-seo-doesnt-guarantee-ai-visibility/"
    title: "Botpresso, Why winning SEO doesn't guarantee AI visibility (Apr 2026; two-brand Semrush comparison)"
  - id: field-notes
    resource: "field notes"
    title: "Anonymised observations from one German-market ecommerce shop, 2025–2026"
  - id: nz-meta
    resource: "https://natzir.com/en/seo/meta-descriptions-impact-gemini-ai/"
    title: "Natzir Turrado, Are meta descriptions back? Impact on Gemini (2026-10-22; Gemini API with Search grounding, 115 prompts EN-US/ES-ES × 3 runs, 2,580 excerpts)"
  - id: bc-brand
    resource: "https://www.bruceclay.com/blog/google-explains-why-having-a-differentiating-brand-is-important-to-search-visibility/"
    title: "Bruce Clay, Google on why a differentiating brand matters (2025-05-15; Danny Sullivan, Search Central Live NYC, March 2025)"
  - id: dj-parametric
    resource: "https://dejan.ai/blog/parametric-memory-impacts-brands/"
    title: "DEJAN, AI models encode brand data but fail to recall a third of it (2026-08-17; summary of a Google Research study, 13 LLMs, 2,150 facts)"
  - id: dj-kg-bio
    resource: "https://dejan.ai/blog/knowledge-graph-biography-ai-mode/"
    title: "DEJAN (Dan Petrovic), Knowledge Graph facts reach AI Mode as uncited Biography results (2026-10-28; Google Earth wasm proto schemas + probing, 2 sessions)"
  - id: sbs-kgrecon
    resource: "https://www.seobythesea.com/2019/08/google-knowledge-graph-reconciliation/"
    title: "SEO by the Sea, Google Knowledge Graph reconciliation (2019-08-05; patent US 10,331,706, filed 2017-10-04)"
  - id: nz-sdkg
    resource: "https://natzir.com/en/seo/structured-data-kg-google-ai/"
    title: "Natzir Turrado, How structured data reaches AI Overviews and AI Mode (2026-10-27; intern CV, Google Earth WASM strings, 2024 leak, DOJ exhibits; small AI Mode tests)"
  - id: sbs-navqueries
    resource: "https://www.seobythesea.com/2012/12/navigational-queries-resources/"
    title: "SEO by the Sea, How Google may identify navigational queries and resources (2012-12-09; patent US 8,326,826, filed 2009-01-15)"
  - id: mt-sitehack
    resource: "https://metehan.ai/blog/want-real-short-term-ai-visibility-hack-bad-actors-hands/"
    title: "Metehan Yeşilyurt, Hallucinated hostnames in ChatGPT site: fan-outs (2026-08-28; Peec logs, >2M site: queries, 134,922 hostnames, DNS/WHOIS)"
  - id: brief-distinct
    resource: "https://seobrief.substack.com/p/when-the-logo-comes-off-is-it-still"
    title: "Jes Scholz, SEO Brief: distinctiveness (2026-06-18; essay + one client case)"
  - id: seer-brand-accuracy
    resource: "https://www.seerinteractive.com/insights/ai-brand-accuracy-study"
    title: "Seer Interactive, AI declined to answer prompts about our brand 31 % of the time (2026-08-27; 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, May 1 – Jun 9 2026, own brand)"
  - id: lr-gullible
    resource: "https://lilyray.nyc/which-ai-search-tools-llms-are-the-most-gullible/"
    title: "Lily Ray, Which AI search tools are the most gullible? (2025-06-17; one planted page, 5 questions, 6 engines, one run)"
  - id: lr-gsc-meetup
    resource: "https://lilyray.nyc/what-i-learned-at-the-2025-google-search-central-meetup-in-nyc/"
    title: "Lily Ray, 2025 Google Search Central meetup NYC (2025-03-24; her account of Google staff statements)"
  - id: ja-multiling
    resource: "https://www.jonoalderson.com/conjecture/localisation-without-borders/"
    title: "Jono Alderson, Shaping visibility in a multilingual internet (2025-08-08; opinion)"
  - id: cc-entity
    resource: "https://www.crystalcarter.ai/post/managing-your-brand-entity-for-generative-search"
    title: "Crystal Carter, Managing your brand entity for generative search (≈2026-03; practitioner)"
---

# Homepage and brand pages

For anyone responsible for the homepage, the pages that answer branded searches, and how the brand is described across Google, assistants and third-party sites.

## Rules
- **State five or more verifiable proof points as text on the homepage** — review score with count, years trading, assortment size, awards, each with a source or figure — in visible body copy that says what you sell; write the meta description as if it were the only text read. *Measured, observational* ([§1](#1-proof-points-as-text), [§11](#11-say-what-you-are-in-text)).
- **Give every branded intent its own page** — discount code, student discount, prices, reviews, alternatives, "vs", and the brand-verification intents: returns, delivery, "legit" — at short, shallow, stable URLs. *Practitioner*; URL shape *Patent* ([§2](#2-one-page-per-branded-intent), [§10](#10-brand-verification-queries), [§12](#12-brand-urls-and-hostname-variants)).
- **Don't treat brand queries as a sure click**: own the results around the brand, not only position 1. *Measured* ([§3](#3-the-branded-results-page)).
- **Fill Merchant Center and Business Profile completely** — promotions, loyalty, policies — because they build the merchant knowledge panel. *Official* + *Practitioner* ([§3](#3-the-branded-results-page)).
- **Expect the homepage to receive AI clicks but few citations**; earn citations on comparison and guide pages. *Measured, panel estimates* ([§4](#4-clicked-not-cited)).
- **Build a clear brand and product identity** rather than competing only on generic category demand and other brands' names, and publish "need → brand" statements (what problem or category you are the answer for). *Measured visibility* / *From the leak* / *Official statement, relayed* ([§5](#5-brand-identity-in-core-updates), [§11](#11-say-what-you-are-in-text)).
- **Keep third-party listings consistent with the site and feed**, and check which ones are cited before dropping any. *Measured, vendor data* ([§6](#6-third-party-listings-match-the-site)).
- **Check every month what the AI Overview and the assistants say about your brand against a brand canon of checkable facts**, track accurate, wrong and no-answer rates, publish correct facts early for poorly covered questions, and keep the facts on Wikipedia/Wikidata, YouTube and LinkedIn current — they write the summary; a recent launch missing from answers may be the training cut-off, not a content gap. *Measured, vendor data; one-brand study; one-run test; practitioner* ([§7](#7-what-the-ai-overview-says-about-your-brand), [§14](#14-brand-canon-and-answer-accuracy)).
- **Keep the brand entity and its display clean**: Organization markup with `sameAs` and `@id` on the homepage, a Wikidata item if notable, a claimed Knowledge Panel, a site name that is the official brand name, a current favicon, and identical facts on your site, Wikidata, marketplaces, press and a few anchor pages in each language you sell in; audit the Knowledge Graph entity yearly. *Practitioner*; *Patent*; *From code + probing, n=2*; favicon *one case* ([§8](#8-entity-hygiene), [§13](#13-brand-display-in-the-results), [§14](#14-brand-canon-and-answer-accuracy)).
- **Put bestsellers and category entry points above the fold on the homepage**, because AI referrals increasingly land there. *Measured, observational, 52 sites* ([§9](#9-ai-referrals-land-on-the-homepage)).
- **Register and redirect obvious hallucinated variants of your own hostname** (hyphenated or other-TLD); never anyone else's. *Measured, vendor log data, case-level* ([§12](#12-brand-urls-and-hostname-variants)).

## Checklist
- [ ] Homepage text (not badge images) names the review score with count, years trading, assortment size and awards, each with a source.
- [ ] Search Console split into brand and non-brand.
- [ ] Each branded query with volume ("[brand] discount code", "[brand] student discount", "[brand] reviews", "[brand] vs …") lands on a page that answers it.
- [ ] Merchant Center has promotions, loyalty, return and support data; Business Profile identity (name, address, hours, primary category) is correct.
- [ ] Ask several assistants what you sell, what it costs and your return policy; fix wrong answers at the source.
- [ ] Marketplaces, review sites and roundups cited for your category show the same price range, assortment, returns and delivery as the site.
- [ ] Seasonal hubs live at evergreen URLs ([seasonal peaks](../situations/seasonal-peaks.md)).
- [ ] Monthly: the AI Overview for the bare brand name read and its claims checked; wrong facts traced to Wikipedia, YouTube, LinkedIn or another cited source.
- [ ] Homepage carries Organization markup (name, logo, url, `sameAs`, `@id`); every `sameAs` points to your own profiles; Wikidata and Knowledge Panel checked yearly.
- [ ] Homepage shows bestsellers and category entry points above the fold; AI referrals split by page type in analytics.
- [ ] Quarterly: brand-verification queries (reviews, legit, scam, returns, delivery…) checked in Search Console and each lands on a page that answers it.
- [ ] Homepage body copy says in plain text what you sell, for whom, and which needs or categories you are the answer for; the meta description works as a stand-alone summary.
- [ ] Founding date, address, assortment and other single-answer facts are identical on the site, Wikidata, marketplaces and press pages; the Knowledge Graph entity checked yearly.
- [ ] Brand and core category URLs are short and shallow and haven't changed.
- [ ] Obvious hyphenated or other-TLD variants of your own hostname are registered and redirect to the main domain.
- [ ] Site name in results = official brand name; favicon is a crisp, current SVG; Organization logo exists in square and horizontal versions; OG images are 1200×675 px.
- [ ] A brand canon lists checkable facts (locations, what you sell and don't sell, delivery, returns); assistants' answers scored accurate / wrong / no answer each month.
- [ ] Obscure brand and product attributes (materials, origin, policies) answered on your own pages and included in the monthly checks.
- [ ] Each language you sell in has a few accurate anchor pages (About, flagship products).

## 1. Proof points as text
- Mid-authority brands with 5+ verifiable proof points on the homepage had "62% more AI visibility" than peers with none; most of the gain came from the first two, none for high-authority brands.[^siege-credibility] Write them as text with a source, not only as badge images.
- Shops that recovered in a core update fixed trust: customer service, navigation and checkout, off-site reputation (4 cases).[^mh-dec2025]

## 2. One page per branded intent
- A "[brand] discount code" page stating the voucher policy captures searches even for small brands; split Search Console into brand and non-brand and expect the non-brand share to grow with brand age.[^d2c]
- **Example.** "[brand] discount code" searches (~3,000 impressions a year, position 1–2) landed on the newsletter sign-up page; "[brand] student discount" on a store page. The searcher wanted a policy and got a form.[^field-notes]

## 3. The branded results page
- With an AI Overview, 45.8 % of navigational searchers were still on the results page after 21 s (12 % without), looking at results around the brand.[^gm-intents]
- Merchant knowledge panels now show deals, loyalty benefits, an AI "Ask" assistant and business information from Merchant Center and the business profile.[^brodie-notes] Merchant Center data "takes precedence over structured data"; long-running promotions (maximum 6 months) help. *Practitioner how-to.*[^brodie-loyalty]
- Google: Merchant Center and Business Profile help in "both AI responses and other Google Search results". *Official.*[^google-ai-guide] Setup: [feeds and Merchant Center](../channels/feeds-and-merchant-center.md), [local](../channels/local.md).

## 4. Clicked, not cited
- Homepages and brand-entry pages took about 57.7 % of AI traffic but 3.0 % of citations across 40 US sites.[^aleyda-traffic] Homepages were cited at single-digit rates for bottom-funnel prompts.[^siege-bofu]
- The most-cited domain was the most-mentioned brand only 20.8 % of the time. *Measured, correlational, ChatGPT only.*[^gm-owners] Track citations and brand mentions separately ([AI visibility tracking](../measure/ai-visibility-tracking.md)).

## 5. Brand identity in core updates
- OfficialPageTwiddler puts the official page first for exact-name queries; brand owners tend to win bare brand-name queries, resellers win on modifiers. *From the leak.*[^leak-2]
- March 2026 core update (Sistrix US): brands with product identity gained (e.g. +90.2 %, +99.8 %); retailers competing on broad category demand and other brands' names lost (−11 % to −37 %).[^aleyda-mar2026] A risk for multi-brand shops on generic category queries ([core update recovery](../situations/core-update-recovery.md)).

## 6. Third-party listings match the site
- For ecommerce, owned sites made up 30.4 % of AI citations, external sources 69.6 %.[^aleyda-citations] 52.5 % of the 40 most-cited domains for bottom-funnel prompts were affiliate or sponsorship sites.[^siege-leader]
- In local answers the business's own website led, and listings acted as verification.[^ipr-local] AI visibility correlated with branded web mentions (AI Overviews 0.656, AI Mode 0.709, ChatGPT 0.664) and YouTube mentions (~0.737) more than with Domain Rating (0.266–0.326); backlinks were "very weak". *Measured, vendor data, 75,000 brands, skewed to big brands.*[^ah-brand-corr] Audit: [third-party presence](../channels/third-party-presence.md).
- **Branded demand vs ranking breadth.** In one two-brand comparison, the brand with fewer keywords, pages and backlinks but more branded visits (767,000 vs 336,000) had the higher AI visibility score (77 vs 52). *Practitioner, method undisclosed, approximate figures — weak evidence.*[^bp-seo-vs-ai] Details: [third-party presence](../channels/third-party-presence.md#9-ranking-well-is-not-ai-visibility).

## 7. What the AI Overview says about your brand
- **Branded searches now get AI Overviews.** In Sept 2026, AI Overviews showed on 73.3 % of branded keywords on average (83 % on 29 Sep) vs 78.3 % of non-branded ones — up from 13.1 % of branded keywords in the Nov 2025 study. *Measured, vendor data, US desktop.*[^ah-aio-branded]
- **The summary sits on top and is written from third parties.** Of 100 bare brand names, 63 showed an AI Overview, 76.2 % of those at position 1. Its citations came from Wikipedia (71.9 %), YouTube (38.6 %) and LinkedIn (22.8 %) (n=57); 3.4 % mentioned competitors. *Measured, vendor data.*[^ah-aio-branded]
- **Do:** read the AI Overview for your bare brand name every month; fix wrong facts where they come from — Wikipedia and Wikidata, your YouTube channel, your LinkedIn page. *Inference from the citation shares.* How AI Overviews work: [Google AI features](../how-it-works/google-ai-features.md).

## 8. Entity hygiene
*Practitioner.*[^ah-kg]
- **Organization markup on the homepage** with `name`, `logo`, `url`, `sameAs` (social profiles, the Wikidata Q-ID) and an `@id`.
- **A Wikidata item** if the brand is notable; the same name, address and phone everywhere.
- **Claim the Knowledge Panel.**
- **Check every `sameAs`.** A wrong `sameAs` can attach another entity to your brand. The source reports (unverified) that Google removed more than 3 billion Knowledge Graph entities in one week in June 2025.
- **Knowledge Graph facts reach AI Mode without a link.** Code schemas and probing show AI Mode receiving Knowledge Graph facts as uncited "Organization/Person Biography" results, with provenance values (third party, curation, partner feed, extraction) and restriction flags including `SEARCH_GROUNDING` and `GOOGLE_EXTENDED_OPT_OUT`. *From code; usage from probing, n=2.*[^dj-kg-bio] Wrong entity facts are repeated without a source you could fix on the page.
- **Only corroborated facts get merged.** A Google patent merges extracted facts into the Knowledge Graph only when corroborated, discards conflicting values for single-answer facts (founding date and the like), and may not accept several sources from one domain as enough. *Patent.*[^sbs-kgrecon] **Do:** keep brand and product facts identical across your site, Wikidata, marketplaces and press.
- **Google-Extended trade-off.** Google-Extended officially covers Gemini training and grounding, not Search; whether opting out also strips Knowledge Graph facts from Gemini is unconfirmed. *Official + inference.*[^nz-sdkg] Weigh any block against entity coverage ([AI crawlers and controls](../technical/ai-crawlers-and-controls.md)).
- **Do:** audit `sameAs` and the Wikidata item once a year. Markup rules: [structured data policies](../technical/technical-foundations.md#8-structured-data-policies).

## 9. AI referrals land on the homepage
- **A ChatGPT link change moved traffic to homepages.** From 7 May 2026 (not announced by OpenAI), ChatGPT referrals to 52 client sites rose from 183,497 to 363,089 sessions (+97.9 %, median site +54 %), comparing 26 Mar – 6 May with 7 May – 17 Jun 2026. Homepage sessions rose +1,316 % (7,990 → 113,183) and their share from 4.4 % to 31.2 %; landing pages grew +60 % but fell from 71 % to 57 % of sessions; blogs −28 %. *Measured, observational, GA4.*[^bp-chatgpt-links]
- **The gain was concentrated.** The top site took 64 % of the net gain and the top 5 took 91 %; the other 47 sites grew +10 % combined. 12 of 17 ecommerce stores grew, and 16 of the 17 sites that lost product-page traffic gained homepage traffic.[^bp-chatgpt-links]
- **Do:** split AI referrals by page type ([analytics](../measure/analytics.md)); put bestsellers and category entry points above the fold, so a visitor sent to the homepage reaches a product in one click. *Practitioner.* This fits [§4](#4-clicked-not-cited): the homepage is clicked, not cited.

## 10. Brand-verification queries
- **Shoppers check a shop before buying.** Search Console queries that combine the brand with reviews, legit, scam, fake, returns, refunds, delivery, trustpilot, reddit, amazon, "worth it" or "real or fake" show what they want verified. *Practitioner.*[^bp-brand-verify]
- **Do:** each quarter, filter Search Console queries with a regex for those words, open each landing page and list its queries; build or extend the returns, delivery and reviews pages that answer them. Same logic as [§2](#2-one-page-per-branded-intent). Query filters: [Search Console](../measure/search-console.md).

## 11. Say what you are, in text
- **Google wants a recognisable brand.** Google's Danny Sullivan (Search Central Live NYC, March 2025): "if you are recognized as a brand in your field, big, small, whatever, just a brand, then that's important"; make clear what the site is about as soon as people arrive. *Official statement, relayed by an agency blog.*[^bc-brand] At a 2025 Search Central meetup, Google staff said their systems don't judge a brand by size, but recognisable brands "often have signals that perform well". *Google staff statements, as recounted by an attendee.*[^lr-gsc-meetup]
- **The homepage meta is often all Gemini reads.** When Gemini grounds on Google Search, the meta description was the excerpt for 43 % of homepage results (categories 23 %, articles 3.8 %), and a meta-only excerpt was cited far less often (22 % vs 72 % for body excerpts across page types). *Measured, observational, Gemini API only.*[^nz-meta] **Do:** visible body copy that says what you sell and for whom, and a meta description that stands on its own.

> **Conflict:** does the meta description still matter? — [details](../reference/conflicts.md#do-meta-descriptions-still-matter)

- **Models recall "brand → feature" better than "need → brand".** A Google Research study summarised by DEJAN: models encode 95–98 % of facts but fail to recall 26–34 %; long-tail recall falls by 20–35 points, and reverse queries (feature → brand) are weaker than brand → feature. *Research summary, 13 LLMs.*[^dj-parametric] **Do:** publish and earn statements that tie the need or category to the brand ("for X, [brand] …"), on your site and in third-party coverage ([third-party presence](../channels/third-party-presence.md)).

## 12. Brand URLs and hostname variants
- **Short, shallow, stable.** A Google patent identifies navigational resources from session patterns and long clicks and prefers shorter URLs at shallower depth; the patent has likely expired, but session-based click signals survive per trial testimony. *Patent.*[^sbs-navqueries] **Do:** keep brand, about and core category URLs short, shallow and unchanged ([migration](../situations/migration.md)).
- **Assistants invent hostnames.** For `site:` searches ChatGPT sometimes invents official-looking hostnames — hyphenated or other-TLD variants of a brand; citations still point to the real domain. 4 unregistered domains appeared 100+ times and ~104 appeared 10–99 times in the logs. *Measured, vendor log data (author works at an AI-visibility vendor), case-level DNS/WHOIS checks.*[^mt-sitehack] **Do:** register and redirect the obvious variants of your own brand's hostname; never register anyone else's. How assistants search inside sites: [AI assistants](../how-it-works/ai-assistants.md).

## 13. Brand display in the results
- **A missing favicon cost branded clicks.** In one case, branded clicks fell sharply while impressions and average position stayed flat; a developer had removed the favicon by accident, and the fix took minutes. *One case.*[^brief-distinct]
- **Display checklist:** site name = the official brand name; Knowledge Graph entity under the official name; a crisp, current SVG favicon; an Organization logo in square and horizontal versions; OG images at 1200×675 px. *Practitioner.*[^brief-distinct]
- **Do:** when branded CTR falls while impressions and position hold, check favicon and site-name display before anything else ([traffic drop](../situations/traffic-drop.md#3-segment-then-name-the-surface)); entity setup: [§8](#8-entity-hygiene).

## 14. Brand canon and answer accuracy
- **Assistants skip more than they get wrong.** In one B2B brand's own study (28,123 answers from 6 AI surfaces, 87 attributes, May – June 2026), answers were accurate 95.9 % of the time when given, but 31.2 % of prompts got no answer and 2.8 % were wrong. Claude declined most (46.3 %), AI Mode least (24.1 %); comparative prompts were accurate only 18.8 % of the time because 80.3 % went unanswered. The brand's own domain was ~35 % of 219,349 citations, and wrong answers traced back to stale profiles (location, headcount, services). *Measured, one brand, agency's own data.*[^seer-brand-accuracy]
- **Assistants repeat the first page that answers.** A page with made-up claims on questions nobody covered was indexed "within 12 hours" and repeated "within 24 hours": AI Mode used it for 4 of 5 questions, AI Overviews, Gemini, ChatGPT and Perplexity for 2 each (Perplexity once without caveat), Claude for none; engines that sought agreement across sources resisted more. *Measured, one planted page, one run.*[^lr-gullible] On a poorly covered question, the first page that answers wins — make it yours, and make it correct.
- **The training cut-off can explain a gap.** A recent launch can be missing from answers that rely on training data simply because of the model's cut-off; recheck after the next model update before treating it as a content gap. *Practitioner.*[^cc-entity]
- **Other languages.** With no local-language footprint, models borrow from other languages or from similar companies. *Opinion, no data.*[^ja-multiling] Publish a few accurate anchor pages per language (About, flagship products) and clean up mistranslated mentions ([new market](../situations/new-market.md)).
- **Do:** keep a brand canon — checkable facts on locations, what you sell and don't sell, delivery and returns; score answers monthly as accurate, wrong or no answer; fix wrong facts on your own site and profiles first; answer obscure brand and product questions on your own pages early, and include them in the checks ([AI visibility tracking](../measure/ai-visibility-tracking.md), [third-party presence](../channels/third-party-presence.md)).

Related: [comparison pages and guides](comparison-and-guides.md), [category pages](category-pages.md), [Google AI features](../how-it-works/google-ai-features.md), [third-party presence](../channels/third-party-presence.md), [analytics](../measure/analytics.md).

[^siege-credibility]: Siege Media, 2026-10-26: 585 brands, Peec mention share 20 Sep – 19 Oct 2026, controlled for DR and organic traffic; AI-assisted scoring (inter-rater 0.90); correlational.
[^d2c]: Searchind, D2C guide, read 2026-10-27: branded intent pages incl. discount codes; brand / non-brand split.
[^gm-intents]: Growth Memo, 2026-06-01: share still active at 21 s by intent with and without AIO; schema recommendations are opinion, no test shown.
[^brodie-notes]: Brodie Clark notes (month anchors #jul-2025, #aug-2025, #oct-2025, #dec-2025, #feb-2026, #jul-2026): AI snippet summaries, merchant knowledge panel tests, buying-guide and documentation carousels.
[^brodie-loyalty]: Brodie Clark, 2025-08-13: promotions add-on, 6-month maximum, promotions rejection rate, loyalty markets, Merchant Center over structured data, no organic loyalty reporting.
[^google-ai-guide]: Google's generative-AI optimization guide, updated 2026-07-10.
[^aleyda-traffic]: Aleyda Solis, ~Apr–May 2026, via search extracts: 4 verticals × 10 US sites, Semrush and Similarweb estimates; some AI traffic may be agents.
[^siege-bofu]: Siege Media, 2026-03-24: ~1,000 BOFU prompts in Peec across ChatGPT, Perplexity, Gemini, AIO/AI Mode, 57,095 citations, 29 Jan – 4 Feb 2026; Siege sells GEO and digital PR.
[^gm-owners]: Growth Memo, 2026-07-20: 15.2 % owned / 53.7 % open categories; owners first in 90.4 %; citation–mention correlation −0.229; most-cited = most-mentioned 20.8 %. Semrush-sponsored data.
[^leak-2]: Resoneo, leak part 2, 2024-10-31: OfficialPageTwiddler, host diversity caps.
[^aleyda-mar2026]: Aleyda Solis, March 2026 core update, Sistrix 26 Mar – 11 Apr 2026, via search extracts.
[^mh-dec2025]: Marie Haynes, 2026-02-20: 4 sites incl. two ecommerce; rater-guideline counts are her own.
[^aleyda-citations]: Aleyda Solis, 2026-08-02, via search extracts (direct fetch blocked): owned/earned/shared split by vertical; sample sizes not visible. Re-check on the page.
[^siege-leader]: Siege Media, 2026-09-25 (and 2026-07-14): 52.5 % affiliate/sponsorship among the top 40 domains; visibility benchmarks from its book, data unpublished.
[^ipr-local]: iPullRank, 2025-12-16: Yext study; Google doesn't cite Business Profiles.
[^field-notes]: Anonymised shop: seasonal URL status and 16 months of Search Console impressions, checked 2026-10-27; brand voucher queries × landing page, Oct 2025 – Oct 2026.
[^ah-brand-corr]: Ahrefs, 2025-12-12: 75,000 brands with DR > 40, Spearman; YouTube mentions ~0.737; branded web mentions AIO 0.656, AI Mode 0.709, ChatGPT 0.664; DR 0.266–0.326; branded search volume 0.352–0.466; backlinks "very weak". Skews to big brands; factors not independent. Replaces the rounded figures (0.7 / 0.3) relayed by Growth Memo that this page cited until 2026-10-28.
[^ah-aio-branded]: Ahrefs, 2026-10-02: 232.8M US desktop crawls, Jul–Sep 2026; Sept 2026 monthly average 73.3 % branded vs 78.3 % non-branded, 83 % branded on 29 Sep; earlier study (Nov 2025) 13.1 % branded; 100-brand panel: 63 with AIO, 76.2 % at position 1, citations Wikipedia 71.9 %, YouTube 38.6 %, LinkedIn 22.8 % (n=57), 3.4 % mentioned competitors. Ahrefs' own data.
[^ah-kg]: Ahrefs, Google Knowledge Graph, 2026-05-14: Organization markup fields, Wikidata, consistent NAP, claiming the Knowledge Panel, wrong `sameAs` risk; the June 2025 removal of > 3B entities is reported, not verified.
[^bp-chatgpt-links]: Botpresso, ≈2026-07: 52 client sites (43 B2C, 9 B2B), GA4 ChatGPT referrals, 26 Mar – 6 May vs 7 May – 17 Jun 2026; observational, no control; OpenAI didn't announce the change. Agency client base.
[^bp-brand-verify]: Botpresso, ≈2026-10: Search Console query regex for brand-verification terms; practitioner method, no measured results.
[^bp-seo-vs-ai]: Botpresso, Apr 2026: two beauty D2C brands compared in Semrush (DA 57 each; keywords, indexed pages, backlinks, branded visits, AI visibility score); method undisclosed, figures approximate.
[^nz-meta]: Natzir Turrado, 2026-10-22: Gemini API with Search grounding, 115 prompts (EN-US, ES-ES) × 3 runs, 2,580 excerpts; meta share by page type (home 43 %, category 23 %, article 3.8 %); meta-only pages cited 22 % vs 72 % for body excerpts. Observational; not AI Overviews or AI Mode.
[^bc-brand]: Bruce Clay, 2025-05-15: relays Danny Sullivan at Search Central Live NYC, March 2025 (official statement via Search Engine Journal).
[^dj-parametric]: DEJAN, 2026-08-17: summary of a Google Research study (13 LLMs, 2,150 facts): 95–98 % encoded, 26–34 % not recalled, long tail −20 to −35 points, reverse queries weaker, thinking modes recover 40–65 % of missed facts.
[^dj-kg-bio]: DEJAN, 2026-10-28: Google Earth wasm proto schemas plus AI Mode probing (2 sessions); Biography results without URL; provenance and restriction flags. Confirms Natzir's reading of the same strings.
[^sbs-kgrecon]: SEO by the Sea, 2019-08-05: patent US 10,331,706 on Knowledge Graph reconciliation; corroboration, single-answer predicates.
[^nz-sdkg]: Natzir Turrado, 2026-10-27: Google-Extended scope from Google's docs; effect on Knowledge Graph facts in Gemini unconfirmed.
[^sbs-navqueries]: SEO by the Sea, 2012-12-09: patent US 8,326,826 (filed 2009-01-15, likely expired); navigational resources, shorter URLs and shallower depth favoured.
[^mt-sitehack]: Metehan Yeşilyurt, 2026-08-28: Peec logs, > 2M ChatGPT `site:` queries, 134,922 hostnames, DNS/WHOIS checks; not reproducible outside Peec; author works at Peec AI.
[^brief-distinct]: Jes Scholz, 2026-06-18: one client case (branded clicks down, impressions and position flat; favicon removed by accident) and a brand-display checklist (site name, Knowledge Graph name, SVG favicon, square and horizontal logo, OG images 1200×675 px); essay.
[^seer-brand-accuracy]: Seer Interactive, 2026-08-27: own B2B brand, 1,562 prompts daily × 6 AI surfaces, 28,123 responses, 87 attributes, 1 May – 9 Jun 2026; accurate 95.9 % when answered, no answer 31.2 %, wrong 2.8 %; Claude 46.3 % vs AI Mode 24.1 % declined; comparative 18.8 % accurate, 80.3 % unanswered; own domain ~35 % of 219,349 citations.
[^lr-gullible]: Lily Ray, 2025-06-17: one planted page with made-up claims, 5 questions, 6 engines, one run; indexed within 12 hours, repeated within 24 hours; AI Mode 4/5, AIO 2, Gemini 2, ChatGPT 2, Perplexity 2, Claude 0.
[^lr-gsc-meetup]: Lily Ray, 2025-03-24: her account of Google staff statements at the Search Central meetup NYC, March 2025 (brand size not judged; recognisable brands "often have signals that perform well").
[^ja-multiling]: Jono Alderson, 2025-08-08: opinion, no data; LLMs borrow from other languages or similar companies; anchor pages per language.
[^cc-entity]: Crystal Carter, ≈2026-03: practitioner; training cut-off can explain a missing launch; recheck after the next model update.
