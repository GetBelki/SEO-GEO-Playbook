---
type: Reference
title: AI crawlers and controls
description: Official per-vendor reference for AI crawlers and user agents (OpenAI, Anthropic, Perplexity, Google, Apple, Microsoft) — what each bot does, what blocking it costs, robots.txt behaviour, IP lists — plus Google's AI-feature eligibility and snippet controls, Google-Extended and Knowledge Graph facts, sitemap discovery and bot verification, WebMCP and WAFs blocking agents, hallucinated brand hostnames and invented URL paths, Bing's AI Performance report, IndexNow, whether anyone reads llms.txt or Markdown copies, user-triggered fetchers and robots.txt, and status codes per bot in server logs.
tags: [geo, crawling, robots-txt, llms-txt, markdown, openai, anthropic, perplexity, google, bing, apple, google-extended, knowledge-graph, webmcp, waf, sitemaps, server-logs, status-codes, reference]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-01-28T00:00:00Z
sources:
  - id: openai-bots
    resource: "https://developers.openai.com/api/docs/bots"
    title: "OpenAI, Overview of OpenAI crawlers (read 2026-10-27; platform.openai.com/docs/bots redirects here)"
  - id: anthropic-bots
    resource: "https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler"
    title: "Anthropic, Does Anthropic crawl data from the web, and how can site owners block the crawler? (read 2026-10-27)"
  - id: perplexity-bots
    resource: "https://docs.perplexity.ai/guides/bots"
    title: "Perplexity, Perplexity crawlers (read 2026-10-27)"
  - id: google-ai-features
    resource: "https://developers.google.com/search/docs/appearance/ai-features"
    title: "Google Search Central, AI features and your website (updated 2025-12-10)"
  - id: google-crawlers
    resource: "https://developers.google.com/search/docs/crawling-indexing/google-common-crawlers"
    title: "Google Search Central, Google's common crawlers (read 2026-10-27)"
  - id: google-ai-guide
    resource: "https://developers.google.com/search/docs/fundamentals/ai-optimization-guide"
    title: "Google Search Central, optimizing for generative AI search (updated 2026-07-10; announced 2026-05-15)"
  - id: apple-bot
    resource: "https://support.apple.com/en-us/119829"
    title: "Apple, About Applebot (read 2026-10-27)"
  - id: bing-ai-perf
    resource: "https://blogs.bing.com/webmaster/February-2026/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview"
    title: "Bing Webmaster Blog, Introducing AI Performance in Bing Webmaster Tools (public preview, 2026-02-10)"
  - id: indexnow
    resource: "https://www.indexnow.org/documentation"
    title: "IndexNow protocol documentation (read 2026-10-27)"
  - id: learningaisearch
    resource: "https://learningaisearch.com/"
    title: "LearningAISearch.com (Aleyda Solis, version 4, 2026-03-20), curated AI-search roadmap — used as a gap checklist"
  - id: ah-llmstxt
    resource: "https://ahrefs.com/blog/llmstxt-study/"
    title: "Ahrefs, llms.txt study (2026-06-15; 137,210 domains)"
  - id: nz-sdkg
    resource: "https://natzir.com/en/seo/structured-data-kg-google-ai/"
    title: "Natzir Turrado, How structured data reaches AI Overviews and AI Mode (2026-10-27; intern CV, Google Earth WASM strings, 2024 leak, DOJ exhibits; small AI Mode tests)"
  - id: dj-kg-bio
    resource: "https://dejan.ai/blog/knowledge-graph-biography-ai-mode/"
    title: "DEJAN (Dan Petrovic), Knowledge Graph facts reach AI Mode as uncited Biography results (2026-10-28; Google Earth wasm proto schemas + probing, 2 sessions)"
  - id: nz-chromeai
    resource: "https://natzir.com/en/seo/chrome-ai-gemini-nano-webmcp-decisions-api/"
    title: "Natzir Turrado, Gemini Nano, WebMCP and the Decisions API (2026-10-08; Chromium/Canary tests)"
  - id: dj-crawlers
    resource: "https://dejan.ai/blog/crawler-census-robots-llms-okf/"
    title: "DEJAN, Crawler census: robots.txt 1,150 fetches, llms.txt 4 (2026-08-15; one site's logs, 20 days)"
  - id: mt-gptbot
    resource: "https://metehan.ai/blog/i-built-a-60-000-page-ai-website-for-10-gptbot-crawled-it-30-000-times-in-12-hours/"
    title: "Metehan Yeşilyurt, A 60,000-page site crawled 30,000 times by GPTBot (2026-03-04; server logs, one site)"
  - id: mt-sitehack
    resource: "https://metehan.ai/blog/want-real-short-term-ai-visibility-hack-bad-actors-hands/"
    title: "Metehan Yeşilyurt, Hallucinated hostnames in ChatGPT site: fan-outs (2026-08-28; Peec logs, >2M site: queries, 134,922 hostnames, DNS/WHOIS)"
  - id: lr-techseo
    resource: "https://lilyray.nyc/tech-seo-connect-2025-summary-takeaways/"
    title: "Lily Ray, Tech SEO Connect 2025 takeaways (2025-12-05; talk summaries, speakers named per item)"
  - id: ja-cloak
    resource: "https://www.jonoalderson.com/conjecture/cloaking-is-dead-long-live-cloaking/"
    title: "Jono Alderson, Cloaking is dead, long live cloaking (2026-10-26; argument + relayed Mueller 2017, Dave Smart 2026-07 test)"
  - id: ja-words
    resource: "https://www.jonoalderson.com/conjecture/more-than-words/"
    title: "Jono Alderson, A page is more than a container for words (2026-02-03; argument)"
  - id: seer-robots
    resource: "https://www.seerinteractive.com/insights/do-llms-respect-robotstxt"
    title: "Seer Interactive, Do LLMs respect robots.txt? (2026-08-07; practitioner, 1 client audit)"
  - id: cc-kpis
    resource: "https://www.wix.com/studio/ai-search-lab/ai-search-visibility-kpis"
    title: "Crystal Carter, AI search visibility KPIs (2025-07-29, updated 2025-08-03; Wix AI Search Lab; framework)"
---

# AI crawlers and controls

Every row below comes from the vendor's own documentation, read on 2026-10-27.[^learningaisearch] Vendors add bots every few months, so this page goes stale sooner than the others. The key rule: **training bots, search bots and user-triggered fetchers are separate decisions.** Blocking a training bot doesn't remove you from that vendor's search answers. Blocking a search bot or user fetcher does.

## Rules
- **Decide training bots, search bots and user-triggered fetchers separately**: blocking a training bot doesn't remove you from that vendor's answers, blocking a search bot or fetcher does. *Official* — [evidence](#whos-who)
- **Allow all search bots and user fetchers by default**; blocking training bots is a business decision — for Google-Extended, weigh it against Knowledge Graph facts reaching Gemini. *Official (costs); the default and the KG cost are inference* — [evidence](#default-policy-for-most-sites), [Google-Extended](#google-extended-and-knowledge-graph-facts)
- **Write the robots.txt policy down and check robots.txt against it daily**, and again after any CDN change. *Inference* — [evidence](#whos-who), [policy](#default-policy-for-most-sites)
- **Verify bots by the vendors' published IP lists or reverse DNS, not user agents**, re-fetch the lists for firewall rules, and check the WAF doesn't block user-triggered fetchers and agents. *Official; Measured, one site; Practitioner tests* — [evidence](#whos-who), [verification](#sitemaps-and-bot-verification), [agents](#agents-in-the-browser-webmcp-and-wafs)
- **Register and redirect obvious hostname variants of your own brand** (hyphenated, other TLDs) — ChatGPT sometimes searches inside invented ones — and 301 invented URL paths on your own domain that AI traffic keeps hitting. *Measured, vendor data; Practitioner* — [evidence](#hallucinated-brand-hostnames), [invented paths](#invented-url-paths-on-your-own-domain)
- **Add nothing special for Google's AI features**: indexing and snippet eligibility are the requirement, and snippet controls limit AI features too. *Official* — [evidence](#google-ai-features-need-nothing-extra)
- **Read Bing's AI Performance report for page-level citations and push changed URLs with IndexNow.** *Official* — [evidence](#bing-and-copilot)
- **Don't expect an llms.txt file or Markdown copies to be read or to help**: Google ignores llms.txt, almost no files get requested, and Markdown copies showed no retrieval gain while an indexed Markdown-only page risks cloaking. Judge new AI protocols by what they cost to adopt. *Official (Google); measured, vendor data; Practitioner* — [evidence](#llmstxt-almost-nobody-reads-it)
- **Don't rely on robots.txt to keep user-triggered fetchers out, and noindex paid landing pages**; block at the server if you must. *Official (vendor docs); Practitioner, one audit* — [evidence](#user-triggered-fetchers-and-robotstxt)
- **Report HTTP status codes per verified bot from server logs and alert on any 4xx**; Search Console's Crawl Stats can miss a block. *Practitioner, one case* — [evidence](#status-codes-per-bot-in-server-logs)

## Who's who

| Vendor | User agent | Job | Cost of blocking it | robots.txt |
|---|---|---|---|---|
| OpenAI | **OAI-SearchBot** | "used to surface websites in search results in ChatGPT's search features" | Not "shown in ChatGPT search answers, though can still appear as navigational links" | Honoured; changes take "~24 hours" |
| OpenAI | **GPTBot** | Training | Content "should not be used in training generative AI foundation models" | Honoured |
| OpenAI | **ChatGPT-User** | "certain user actions in ChatGPT and Custom GPTs"; "not used for crawling the web in an automatic fashion" | Pages users ask about can't be read | "rules may not apply" |
| OpenAI | **OAI-AdsBot** | "validate the safety of web pages submitted as ads on ChatGPT"; "only visits pages submitted as ads" | Ads can't be validated | — |
| Anthropic | **ClaudeBot** | Training | Excluded "from our AI model training datasets" | Honoured; supports Crawl-delay |
| Anthropic | **Claude-User** | Fetches pages when a user asks Claude | "may reduce your site's visibility for user-directed web search" | Per subdomain |
| Anthropic | **Claude-SearchBot** | Improves Claude's search results | "may reduce your site's visibility and accuracy in user search results" | Per subdomain |
| Perplexity | **PerplexityBot** | "surface and link websites in search results on Perplexity"; not used for training | Out of Perplexity's results | Honoured; up to 24 h |
| Perplexity | **Perplexity-User** | User-requested fetches | — | "generally ignores robots.txt rules" |
| Google | **Google-Extended** (robots token only, no own user agent) | Training of Gemini Apps and Vertex AI models, and grounding | "does not impact a site's inclusion in Google Search nor is it used as a ranking signal" | Token in robots.txt |
| Google | **Googlebot** | Search, including AI Overviews and AI Mode | Out of Search and its AI features | Honoured |
| Apple | **Applebot** | Search in Spotlight, Siri and Safari | Out of those | Follows Googlebot rules if Applebot isn't named; ignores crawl-delay |
| Apple | **Applebot-Extended** | "does not crawl webpages"; controls use of Applebot data for training | Pages "can still be included in search results" | Token in robots.txt |

Sources: OpenAI,[^openai-bots] Anthropic,[^anthropic-bots] Perplexity,[^perplexity-bots] Google,[^google-crawlers] Apple.[^apple-bot]

**Verification and firewalls.** OpenAI and Perplexity publish IP lists per bot (e.g. `openai.com/searchbot.json`, `perplexity.com/perplexitybot.json`); Perplexity advises re-fetching them regularly for WAF rules.[^openai-bots][^perplexity-bots] Apple supports reverse DNS (`*.applebot.apple.com`).[^apple-bot] Anthropic warns that IP blocking may not work reliably, because it stops its bots from reading robots.txt.[^anthropic-bots]

**Watch for CDN defaults.** A CDN's "manage AI bots" setting can add blocks for these agents above your own rules ([example](../how-it-works/ai-assistants.md)). Check robots.txt against this table after any CDN change.

## Google: AI features need nothing extra
- "There are no additional technical requirements." A page "must be indexed and eligible to be shown in Google Search with a snippet"; there is "no special schema.org structured data that you need to add".[^google-ai-features]
- **Controls:** `nosnippet`, `data-nosnippet`, `max-snippet` and `noindex` limit how content appears in AI features. "More restrictive permissions will limit how your content is featured."[^google-ai-features]
- AI-feature traffic is "included in the overall search traffic in Search Console" (Performance report, Web search type).[^google-ai-features]
- Google's 2026 guide: you "don't need to create new machine readable files, AI text files, markup, or Markdown"; Google Search ignores llms.txt; "no requirement to break your content into tiny pieces"; you "don't need to write in a specific way just for generative AI search" — optimising for it "is ... still SEO". Merchant Center and Business Profile help in "both AI responses and other Google Search results".[^google-ai-guide] How this squares with assistant-specific findings: [conflicts](../reference/conflicts.md#googles-guidance-vs-assistant-findings).

## Bing and Copilot
- **AI Performance report** (Bing Webmaster Tools, public preview since February 2026): total citations shown as sources in Copilot, Bing AI summaries and "select partner integrations"; average cited pages per day; a sample of grounding queries; page-level citations; trends. It doesn't show where in an answer you appear, and data is aggregated across surfaces.[^bing-ai-perf] Unlike Google's Search Console AI report (impressions only), it reports citations per page.
- **IndexNow** pushes changed URLs to Bing and every other participating engine: "up to 10,000 URLs per post", a UTF-8 `{key}.txt` at the site root. Responses: 200 submitted, 202 key validation pending, 400 bad format, 403 invalid key, 422 URL/host mismatch, 429 "Too Many Requests (potential Spam)".[^indexnow] Copilot answers come from Bing's index, so fast indexing there matters for it.

## llms.txt: almost nobody reads it
- Google Search ignores llms.txt ([above](#google-ai-features-need-nothing-extra)).[^google-ai-guide]
- Across 137,210 domains (May 2026), 28 % published an llms.txt (an upper bound); 97 % of those files got zero requests. Of the requests that did come, AI assistants made 2.5 % and AI retrieval bots 1.1 %; GPTBot was the most frequent named AI fetcher at 4.51 %. *Measured, vendor data.*[^ah-llmstxt]
- On one site over 20 days, robots.txt was fetched 1,150 times (ClaudeBot 445, OAI-SearchBot 295, Googlebot ~243) and llms.txt 4 times (OpenAI 0). *Measured, one site.*[^dj-crawlers] Bots read robots.txt constantly, so a wrong rule there acts fast.
- **Markdown copies and llms.txt didn't help retrieval.** Conference talks (Alex Halliday, Rachel Anderson, relayed) reported no retrieval improvement from Markdown copies or llms.txt and no evidence that major AI agents reliably crawl llms.txt; a Markdown-only page that gets indexed would be cloaking. *Practitioner, relayed.*[^lr-techseo]
- **Machine-only versions drift.** Separate Markdown versions for machines tend to drift toward "cleaner and more persuasive" than the human page, which creates a which-version-is-true problem; llms.txt is at most "occasionally useful as hints". Judge new AI protocols by adoption cost: a six-hour job needs little justification, a six-month project needs evidence. *Practitioner argument.*[^ja-words][^ja-cloak]
- **Do:** treat llms.txt as optional and low priority; don't publish separate Markdown versions of product or category pages; put the effort into crawlable HTML and the bot policy above.

## Default policy for most sites
- Allow all search bots and user fetchers (OAI-SearchBot, ChatGPT-User, Claude-SearchBot, Claude-User, PerplexityBot, Perplexity-User, Googlebot, Bingbot, Applebot).
- Training bots (GPTBot, ClaudeBot, Google-Extended, Applebot-Extended) are a business decision; blocking them doesn't remove you from search answers, but may reduce how well models know your brand over time (*inference*, see [known sources win](../channels/third-party-presence.md#1-assistants-prefer-sources-they-already-know)).
- Write the policy down and check robots.txt against it daily.

## Google-Extended and Knowledge Graph facts
- Officially, Google-Extended covers Gemini training and grounding, not Search ([table](#whos-who)).[^google-crawlers]
- Knowledge Graph facts reach Gemini and AI Mode as textualised sentences without URLs; DEJAN found them delivered to AI Mode as uncited "Biography" results. The schemas carry provenance values (`THIRD_PARTY`, `CURATION`, `PARTNER_FEED`, `EXTRACTION`) and restriction flags including `SEARCH_GROUNDING` and `GOOGLE_EXTENDED_OPT_OUT`; Natzir's test found Knowledge Graph data in 10 of 10 quoted queries vs 0 of 10 unquoted. *From code (schemas); usage from probing, 2 sessions.*[^dj-kg-bio][^nz-sdkg]
- Whether a Google-Extended opt-out strips Knowledge Graph facts from Gemini answers is unconfirmed — the flag's name suggests it might. *Inference.*[^nz-sdkg] **Do:** if you block Google-Extended, weigh that against your entity's coverage, and audit and correct the brand's Knowledge Graph entity either way ([third-party presence](../channels/third-party-presence.md#11-knowledge-graph-facts-need-corroboration-from-other-domains)).

## Sitemaps and bot verification
- On one new 60,000-page site with no links, GPTBot found the site through its XML sitemap within minutes and made 29,000+ requests in 12 hours, ~470× Googlebot; in a 3-hour snapshot OAI-SearchBot made 94 requests and ChatGPT-User 1. A client-side tracker saw zero bots. *Measured, one site; the author works at an AI-visibility vendor (Peec AI).*[^mt-gptbot]
- **Do:** read bot activity from server logs, not analytics tags, and verify bots against the vendors' published IP ranges, because user agents get spoofed ([verification](#whos-who)).

  > **Conflict:** another study saw GPTBot never fetch sitemap-only URLs — [details](../reference/conflicts.md#do-ai-crawlers-use-sitemaps).

## Agents in the browser: WebMCP and WAFs
- WebMCP (`document.modelContext`) has been in an origin trial since Chrome 149: sites can expose search, filter and add-to-cart as tools an agent calls directly; early tests report "89 % fewer tokens". *From code and practitioner tests.*[^nz-chromeai]
- In the same tests, the most common agent failure was the site's own WAF blocking the agent.[^nz-chromeai] **Do:** check that your WAF and bot-management rules let verified user-triggered fetchers and agents through; watch WebMCP, don't build on it yet.

## Hallucinated brand hostnames
- In ChatGPT's `site:` fan-out searches (> 2M queries, 134,922 hostnames), ChatGPT sometimes invented official-looking hostnames — hyphenated or other-TLD variants of a brand; the citations still pointed to the real domain. 4 unregistered domains appeared 100+ times and ~104 appeared 10–99 times. *Measured, vendor log data (Peec AI), case-level DNS/WHOIS checks.*[^mt-sitehack]
- **Do:** register the obvious variants of your own brand's domain and redirect them to the real site. Never register other brands' variants.

## Invented URL paths on your own domain
- AI bots and assistants also send traffic to URL paths on your real domain that don't exist — paths the model made up. *Practitioner, framework, no measured sample.*[^cc-kpis]
- **Do:** monthly, filter server logs for AI user agents and AI referrers that hit 404s; 301 the paths that recur to the closest real page, and leave one-off misses as 404 ([removed pages](technical-foundations.md#13-removed-pages-404-410-or-301)). *Practitioner.*[^cc-kpis]

## User-triggered fetchers and robots.txt
- User-initiated fetchers (ChatGPT-User, Perplexity-User) don't reliably obey robots.txt; the vendors' own docs say robots rules "may not apply" or are "generally" ignored for them ([table](#whos-who)). OpenAI removed its robots.txt compliance wording for ChatGPT-User in December 2025. *Practitioner, relaying vendor doc changes.*[^seer-robots]
- In one client audit, ~559 paid-landing pages were indexed because they carried no noindex. *Practitioner, one audit.*[^seer-robots]
- **Do:** put noindex on paid landing pages and other pages that shouldn't appear in search or answers; if a page must stay out of user-triggered fetches too, block at the server (authentication or a server rule), not in robots.txt. For most shops the default stays: allow user fetchers ([default policy](#default-policy-for-most-sites)). *Practitioner; the default is inference.*

## Status codes per bot in server logs
- A first-party log dashboard (Rachel Anderson, relayed) found a security tool returning HTTP 406 to Googlebot and every AI bot; Search Console's Crawl Stats didn't show it, and the speaker called Crawl Stats unreliable for large domains. *Practitioner, one case, relayed.*[^lr-techseo]
- **Do:** report status codes per verified bot (Googlebot, Bingbot, OAI-SearchBot, ChatGPT-User, Claude-User, PerplexityBot and the others in the [table](#whos-who)) from server or CDN logs, and alert on any 4xx or 5xx to a verified bot; recheck after every security-tool or WAF change ([AI-bot reliability in logs](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs)).

Related: [AI assistants](../how-it-works/ai-assistants.md), [Google AI features](../how-it-works/google-ai-features.md), [technical foundations](technical-foundations.md), [performance and caching](performance-and-caching.md), [fetch test](../measure/diagnostic-tests.md#4-fetch-a-page-the-way-an-ai-assistant-does), [AI visibility tracking](../measure/ai-visibility-tracking.md).

[^learningaisearch]: LearningAISearch.com, read 2026-10-27: section map used as a gap checklist; it links OpenAI's, Perplexity's, Google's and Microsoft's docs but nothing from Anthropic or Apple, which were read directly.
[^openai-bots]: OpenAI crawler doc, read 2026-10-27: four bots, UA tokens (OAI-SearchBot/1.4, GPTBot/1.4, ChatGPT-User/1.0, OAI-AdsBot/1.0), IP JSON per bot, ~24 h robots propagation.
[^anthropic-bots]: Anthropic help article, read 2026-10-27: three bots, per-subdomain rules, Crawl-delay, IP-blocking caveat. Per-bot robots behaviour not stated separately.
[^perplexity-bots]: Perplexity docs, read 2026-10-27: two bots, UA strings, IP JSON, up to 24 h propagation.
[^google-ai-features]: Google AI features doc (updated 2025-12-10) and the May 2025 "succeeding in AI search" post: eligibility, controls, Search Console reporting.
[^google-crawlers]: Google common crawlers page, read 2026-10-27: Google-Extended scope; also Google-CloudVertexBot and GoogleOther. Doesn't mention AI Overviews.
[^google-ai-guide]: Google's generative-AI optimization guide, updated 2026-07-10.
[^apple-bot]: Apple support doc 119829, read 2026-10-27.
[^bing-ai-perf]: Bing Webmaster Blog, 2026-02-10.
[^indexnow]: IndexNow documentation, read 2026-10-27.
[^ah-llmstxt]: Ahrefs, 2026-06-15: 137,210 domains, May 2026; 28 % with an llms.txt (upper bound); 97 % of files never requested; request shares AI assistants 2.5 %, AI retrieval bots 1.1 %, GPTBot 4.51 % (top named AI fetcher).
[^nz-sdkg]: Natzir Turrado, 2026-10-27: Knowledge Graph facts as textualised data without URLs; `LLM_RESTRICTION_*` flags incl. `GOOGLE_EXTENDED_OPT_OUT`; evidence from the 2024 leak, public WASM strings (meaning inferred) and an unverified intern CV; Google-Extended officially covers Gemini training and grounding, effect of opting out on KG facts unconfirmed.
[^dj-kg-bio]: DEJAN, 2026-10-28: Google Earth wasm proto schemas and probing (2 sessions); KG facts as uncited "Person/Organization Biography" results in AI Mode; provenance and restriction flags; relays Natzir's 10/10 quoted vs 0/10 unquoted test.
[^nz-chromeai]: Natzir Turrado, 2026-10-08: WebMCP origin trial since Chrome 149; agent tools; "89 % fewer tokens" from early tests; WAF blocking as the most common agent failure in his tests.
[^dj-crawlers]: DEJAN, 2026-08-15: one site's logs over 20 days; robots.txt 1,150 fetches (ClaudeBot 445, OAI-SearchBot 295, Googlebot ~243); llms.txt 4 (OpenAI 0).
[^mt-gptbot]: Metehan Yeşilyurt, 2026-03-04: server logs of one new 60,000-page site; GPTBot via sitemap within minutes, 29,000+ requests in 12 h (~470× Googlebot); 3-h snapshot OAI-SearchBot 94, ChatGPT-User 1; client-side tracker saw no bots. Author works at Peec AI.
[^mt-sitehack]: Metehan Yeşilyurt, 2026-08-28: Peec AI logs, > 2M `site:` queries, 134,922 hostnames, DNS/WHOIS checks; 4 unregistered hallucinated domains 100+ times, ~104 at 10–99 times. Author works at Peec AI.
[^lr-techseo]: Lily Ray, 2025-12-05, her summary of Tech SEO Connect 2025: Rachel Anderson (log dashboard found a security tool returning 406 to Googlebot and every AI bot; Crawl Stats missed it); Alex Halliday and Rachel Anderson (Markdown copies and llms.txt showed no retrieval improvement; indexed Markdown-only page = cloaking; no evidence major AI agents reliably crawl llms.txt). Not checked against the slides.
[^ja-words]: Jono Alderson, 2026-02-03: argument that machine-only Markdown versions drift toward "cleaner and more persuasive" content and split the truth between versions. No measurements.
[^ja-cloak]: Jono Alderson, 2026-10-26: llms.txt "occasionally useful as hints"; judge new AI protocols by adoption cost (six hours vs six months). Argument.
[^seer-robots]: Seer Interactive, 2026-08-07: user-initiated fetchers (ChatGPT-User, Perplexity-User) don't reliably obey robots.txt; OpenAI removed its compliance wording for ChatGPT-User in December 2025; one client audit with ~559 paid-landing pages indexed without noindex. Agency practitioner post.
[^cc-kpis]: Crystal Carter, 2025-07-29 (updated 2025-08-03), Wix AI Search Lab: AI bots and assistants send traffic to invented URL paths; monthly log filter for AI user agents/referrers hitting 404s, 301 the recurring ones. Framework, no measured sample.
