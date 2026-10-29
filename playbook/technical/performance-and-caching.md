---
type: Checklist
title: Performance and caching
description: Cache-Control templates per page type (never for cart, checkout or account), the back/forward cache, CDN caching notes, web font loading, speculation rules abused by third parties and the Sec-Purpose header, multi-page templates with View Transitions and prerendering instead of a single-page app, plus No-Vary-Search for tracking parameters, field vs lab Core Web Vitals, TTFB and cache keys, the critical rendering path, resource hints and preload pitfalls, lazy loading and embed facades, consent banners and third-party code, and code splitting.
tags: [technical-seo, performance, caching, cache-control, cdn, bfcache, fonts, speculation-rules, prerender, view-transitions, spa, core-web-vitals, ttfb, no-vary-search, preload, fetchpriority, lazy-loading, consent, third-party, inp, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-29T08:30:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-29T08:47:00Z }
stale_after: 2027-04-28T00:00:00Z
sources:
  - id: ja-cache
    resource: "https://www.jonoalderson.com/performance/http-caching/"
    title: "Jono Alderson, A complete guide to HTTP caching (2025-08-29; technical guide)"
  - id: ja-fonts
    resource: "https://www.jonoalderson.com/performance/youre-loading-fonts-wrong/"
    title: "Jono Alderson, You're loading fonts wrong (2025-08-21; technical guide)"
  - id: ja-specevil
    resource: "https://www.jonoalderson.com/performance/speculation-rules-for-evil/"
    title: "Jono Alderson, Speculation rules for evil (2026-04-14; technical argument, no measurements)"
  - id: ja-spa
    resource: "https://www.jonoalderson.com/conjecture/its-time-for-modern-css-to-kill-the-spa/"
    title: "Jono Alderson, Modern CSS should kill the SPA (2025-07-24; technical guide, illustrative numbers)"
  - id: wd-why-speed
    resource: "https://web.dev/learn/performance/why-speed-matters"
    title: "web.dev (Google Chrome team), Why speed matters (2023-11-01; relayed case studies)"
  - id: wd-html
    resource: "https://web.dev/learn/performance/general-html-performance"
    title: "web.dev, General HTML performance considerations (2023-11-01; guidance)"
  - id: wd-critical-path
    resource: "https://web.dev/learn/performance/understanding-the-critical-path"
    title: "web.dev, Understanding the critical path (2023-11-27; guidance)"
  - id: wd-resource-loading
    resource: "https://web.dev/learn/performance/optimize-resource-loading"
    title: "web.dev, Optimize resource loading (2023-11-01; guidance)"
  - id: wd-resource-hints
    resource: "https://web.dev/learn/performance/resource-hints"
    title: "web.dev, Assist the browser with resource hints (2023-11-01; guidance)"
  - id: wd-video
    resource: "https://web.dev/learn/performance/video-performance"
    title: "web.dev, Video performance (2026-04-02; guidance + HTTP Archive data)"
  - id: wd-fonts
    resource: "https://web.dev/learn/performance/optimize-web-fonts"
    title: "web.dev, Optimize web fonts (2023-11-01; guidance)"
  - id: wd-code-split
    resource: "https://web.dev/learn/performance/code-split-javascript"
    title: "web.dev, Code-split JavaScript (2023-12-04; guidance)"
  - id: wd-lazy
    resource: "https://web.dev/learn/performance/lazy-load-images-and-iframe-elements"
    title: "web.dev, Lazy load images and iframe elements (2023-11-01; guidance)"
  - id: wd-prefetch
    resource: "https://web.dev/learn/performance/prefetching-prerendering-precaching"
    title: "web.dev, Prefetching, prerendering, and service worker precaching (2023-11-01; guidance)"
  - id: wd-workers
    resource: "https://web.dev/learn/performance/web-worker-overview"
    title: "web.dev, An overview of web workers (2023-11-01; guidance)"
  - id: dbb-psi
    resource: "https://www.debugbear.com/blog/pagespeed-insights"
    title: "DebugBear, How To Use PageSpeed Insights (2025-03-09, upd. 2026-10-08; explainer)"
  - id: dbb-ttfb-field
    resource: "https://www.debugbear.com/blog/ttfb-lab-vs-field"
    title: "DebugBear, Why Is Google Field TTFB Worse Than Lighthouse Lab Data? (2025-01-10, upd. 2025-10-19; explainer)"
  - id: dbb-nvs
    resource: "https://www.debugbear.com/blog/no-vary-search"
    title: "DebugBear, Smarter Website Caching With No-Vary-Search (2026-05-26; explainer)"
  - id: dbb-spec-proxy
    resource: "https://www.debugbear.com/blog/google-blocked-website"
    title: "DebugBear, How Google Search Uses Speculation Rules With A Proxy (2025-05-28, upd. 2025-06-22; observation of Google SERP code)"
  - id: dbb-cdn-seo
    resource: "https://www.debugbear.com/blog/cdn-seo"
    title: "DebugBear, Can A Content Delivery Network Boost Website SEO? (2026-05-04; explainer)"
  - id: dbb-cmp-inp
    resource: "https://www.debugbear.com/blog/consent-management-platforms-performance-comparison"
    title: "DebugBear, A Web Performance Analysis Of Consent Management Platforms (2026-02-06, upd. 2026-03-17; lab test, 11 CMPs x 5 sites)"
  - id: dbb-consent-cwv
    resource: "https://www.debugbear.com/blog/cookie-consent-banner-performance"
    title: "DebugBear, Cookie Consent Banners, Page Speed, And Core Web Vitals (2025-03-20; one example test)"
  - id: dbb-3p
    resource: "https://www.debugbear.com/blog/reduce-the-impact-of-third-party-code"
    title: "DebugBear, How To Reduce The Impact Of Third-Party Code (2025-03-06, upd. 2026-01-27; guidance)"
  - id: dbb-shopify
    resource: "https://www.debugbear.com/blog/shopify-speed-optimization"
    title: "DebugBear, Shopify Speed Optimization: Fixing The Real Bottlenecks (2026-04-20; practitioner examples)"
  - id: dbb-fonts
    resource: "https://www.debugbear.com/blog/preload-web-fonts"
    title: "DebugBear, Preload Fonts On Your Website For Better Core Web Vitals (2025-02-07, upd. 2025-11-30; example tests)"
  - id: dbb-lazy
    resource: "https://www.debugbear.com/blog/lazy-loading-performance"
    title: "DebugBear, How to Use Lazy Loading Without Hurting Web Performance (2026-04-10; guidance)"
---

# Performance and caching

Which caching headers, font setup and navigation model make a shop fast for people and cheap to crawl, and where third parties can turn browser features against you. Sections 1–6 come from one practitioner's technical guides; later additions come from web.dev, the Google Chrome team's official performance course, and DebugBear, a vendor that sells performance monitoring (its tests are vendor data). None of it shows a measured ranking effect; confidence labels follow the [scale](../reference/sources-and-confidence.md). The Core Web Vitals thresholds themselves are in [technical foundations](technical-foundations.md#9-core-web-vitals); edge caching for AI bots and their timeouts in [AI-bot reliability in server logs](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs).

## Rules
- **Set Cache-Control per page type from a template, and never cache cart, checkout or account pages** in a shared cache. *Practitioner* — [evidence](#1-cache-control-templates-per-page-type)
- **Don't send `no-store` on public HTML**, or pages lose the back/forward cache; check bfcache eligibility for category and product templates. *Practitioner* — [evidence](#2-back-forward-cache)
- **On the CDN, cache HTML deliberately**: bypass on a session cookie, strip tracking parameters from the cache key, purge by tag on publish, and avoid `Vary: *` and `Vary: Cookie`. *Practitioner* — [evidence](#3-cdn-notes)
- **Self-host WOFF2 fonts with `font-display: swap`, preload only the above-the-fold faces, and keep to ≤ 3 weights.** *Practitioner* — [evidence](#4-web-fonts)
- **Log the `Sec-Purpose` header, serve speculative hits on search and cart URLs cheaply, and keep them out of demand counts.** *Practitioner argument, no measurements* — [evidence](#5-speculation-rules-used-against-you)
- **Prefer server-rendered multi-page templates with View Transitions and your own prerender rules over a single-page app** for category and product pages. *Practitioner, illustrative numbers* — [evidence](#6-multi-page-templates-instead-of-a-single-page-app)
- **Judge Core Web Vitals on field data (CrUX, p75, 28 days), not the Lighthouse score**, and expect a fix to take up to 28 days to show. *Practitioner, vendor data* — [evidence](#7-field-data-vs-lab-scores)
- **Keep field TTFB low on campaign URLs**: no redirect hops in ad click URLs, tracking parameters out of the cache key (No-Vary-Search where supported), short-cached static HTML revalidated with ETag. *Official; Practitioner, vendor data* — [evidence](#8-ttfb-redirects-and-cache-keys), [CDN](#3-cdn-notes)
- **Put the LCP element and critical resources in the server HTML, give the LCP image `fetchpriority="high"`, never lazy-load it, and preload only what the preload scanner can't find (always with `as`).** *Official* — [evidence](#9-critical-rendering-path), [hints](#10-resource-hints-and-preload-pitfalls), [lazy loading](#11-lazy-loading-video-and-embed-facades)
- **Treat the consent banner and every third-party script as an INP and LCP cost**: load them async, put embeds behind click-to-load facades, remove unused tags first. *Measured, vendor data, small sample; Official* — [evidence](#12-consent-banners-and-third-party-code)
- **Split JavaScript so startup code stays small**, and move heavy non-DOM work to a web worker. *Official* — [evidence](#13-javascript-code-splitting-and-workers)

## 1. Cache-Control templates per page type
*Practitioner, technical guide.*[^ja-cache] Values as given in the source:

| Resource | `Cache-Control` | Plus |
|---|---|---|
| Fingerprinted assets (CSS, JS, fonts with a hash in the name) | `public, max-age=31536000, immutable` | — |
| High-change HTML (category pages with stock and prices, homepage) | `public, max-age=60, s-maxage=300, stale-while-revalidate=60, stale-if-error=600` | ETag |
| Low-change HTML (guides, brand and service pages) | `max-age=300, s-maxage=86400, stale-while-revalidate=300, stale-if-error=3600` | purge on publish |
| Logged-in pages | `private, no-cache` | `private, no-store` for personal or financial data |
| APIs | `s-maxage=30, stale-while-revalidate=30, stale-if-error=300` | — |
| Images | `max-age=86400` | — |

- **Never cache cart, checkout or account pages** in a shared cache; they belong in the logged-in row or stricter.[^ja-cache]
- Which page type is "high-change" is a shop decision: product pages with live stock and price usually are. *Inference.*
- **Static HTML in the browser cache:** "Five minutes for static HTML resources is a safe bet"; never cache personalised or logged-in HTML in the browser, and revalidate with `ETag` or `Last-Modified` so repeat views get small 304 responses. *Official.*[^wd-html]
- **Compression:** Brotli is about 15–20 % smaller than gzip (keep gzip as fallback) — compress static assets at build time, HTML on the fly; files under 1 KiB barely shrink. *Official.*[^wd-html]
- `stale-if-error` keeps serving the last good page during an origin outage, which also keeps crawlers from seeing 5xx errors that lower the crawl rate ([crawl budget](technical-foundations.md#6-crawl-budget)). *Inference.*

## 2. Back-forward cache
- `no-store` on HTML generally blocks the back/forward cache (bfcache), so a shopper going back from a product to the category reloads the whole page instead of restoring it.[^ja-cache]
- Single-page-app routing also breaks bfcache, scroll restoration and focus ([section 6](#6-multi-page-templates-instead-of-a-single-page-app)).[^ja-spa]
- The HTTP cache and a service worker's Cache API are separate stores: `Cache-Control` doesn't govern what a service worker precached. Precaching costs bandwidth, storage and CPU, so precache only assets that are likely used. *Official.*[^wd-prefetch]
- **Do:** keep `no-store` for pages with personal data only; check bfcache eligibility for category and product templates in the browser's developer tools. *Practitioner.*

## 3. CDN notes
*Practitioner, written for Cloudflare; the principles apply to other CDNs.*[^ja-cache]
- Cloudflare doesn't cache HTML by default; you opt in with rules.
- Bypass the cache when a session cookie is present, so logged-in and cart states are never served from the shared cache.
- Strip tracking parameters (`utm_*`, click IDs) from the cache key, or every campaign click becomes a cache miss.
- Use cache tags to purge exactly the pages a publish or price change affects; check the `cf-cache-status` response header to see whether a page was served from the cache.
- Avoid `Vary: *` and `Vary: Cookie`, which make responses effectively uncacheable.
- **No-Vary-Search** does the same job in the browser and in supporting caches: a response header listing parameters (e.g. `utm_source`, `utm_campaign`) to ignore, so URLs that differ only in those share one cache entry. Supported in Chrome, Edge and Opera, not Firefox or Safari (experimental as of 2026-05). Never list parameters that change content (`q`, `page`, personalisation). The source doesn't mention `gclid`; listing it too is inference. *Official spec feature, relayed; vendor explainer.*[^dbb-nvs]
- A CDN doesn't directly lift rankings; it lowers TTFB and LCP, absorbs traffic spikes and makes crawling cheaper. Check that HTML is really served from the edge (`cf-cache-status: HIT` on Cloudflare). *Practitioner, vendor data.*[^dbb-cdn-seo]

## 4. Web fonts
*Practitioner, technical guide.*[^ja-fonts]
- Self-host fonts as WOFF2.
- `font-display: swap` as the default; `block` hides text for up to ~3 s; `optional` for decorative faces.
- Preload only the critical above-the-fold faces, with `as="font"`, `type`, `crossorigin` and exactly the same URL as in the `@font-face` rule — a mismatch downloads the font twice.
- No `@import` for fonts; subset them and use `unicode-range`.
- At most 3 weights, ≤ 200 KB per font compressed.
- Set fallback metric overrides (`size-adjust`, `ascent-override`, `descent-override`, `line-gap-override`) so the swap doesn't shift the layout (CLS), and `font-synthesis: none` to stop fake bold and italic.
- Cache fonts for a year with versioned file names ([section 1](#1-cache-control-templates-per-page-type)).
- web.dev confirms the basics: self-hosting is usually faster (no extra connection), WOFF2 is up to 30 % smaller than WOFF; inline the `@font-face` rules in the `<head>` and don't base64-inline font files. `swap` is the most used value but shifts content; `optional` uses the web font only if it arrives within 100 ms; `block` hides text indefinitely in Safari. *Official.*[^wd-fonts]
- Subsetting can cut font size by 40–50 %. *Practitioner.*[^dbb-shopify] In one test, preloading the key font moved LCP from 1.82 s to 1.24 s; on a page with 38 preloaded fonts, removing the preloads let render-blocking CSS finish ~2 s sooner and FCP and LCP improved by more than 2 s. Preloads go stale when fonts change — re-check them after a redesign. *Measured, vendor data, one case each.*[^dbb-fonts]

## 5. Speculation rules used against you
*Practitioner argument, no measurements.*[^ja-specevil]
- Third-party pages can inject speculation rules that prefetch or prerender your uncached URLs — site search (`/search?q=*`) or add-to-cart links (`/cart?add-to-cart=*`) — creating real-browser load on your origin.
- These requests carry `Sec-Purpose: prefetch` and often no referrer. There is no cross-site opt-out yet.
- **Google Search itself prefetches.** It prefetches the HTML of the first two results through a privacy proxy using speculation rules (`anonymous-client-ip-when-cross-origin`), and skips that when the user already has cookies for the domain. The source doesn't cover effects on logs, analytics or an opt-out. *Practitioner observation of Google's SERP code; vendor.*[^dbb-spec-proxy]
- **Do:** log the `Sec-Purpose` header; serve speculative hits on search and cart URLs a cheap response or rate-limit them; exclude them from demand counts (site-search reports, add-to-cart events) so they don't read as shopper interest ([analytics](../measure/analytics.md)).

## 6. Multi-page templates instead of a single-page app
*Practitioner, technical guide with illustrative numbers.*[^ja-spa]
- A multi-page site with cross-document View Transitions (`@view-transition { navigation: auto; }`, Chromium), its own speculation-rules prerendering of likely next pages and a working bfcache covers most reasons teams give for a single-page app.
- Single-page-app routing breaks bfcache, scroll restoration and focus handling, and puts links and content behind JavaScript that AI fetchers don't run ([JavaScript](technical-foundations.md#7-javascript)).
- **Speculation rules syntax.** `<script type="speculationrules">` with JSON rules supports `prefetch` and `prerender` (Chromium only). Prerender runs the page's JavaScript, so use it only where navigation is fairly certain; viewport-based prefetching (e.g. Quicklink) matches intent better than prefetching every link. Old `<link rel="prerender">` has only done a NoState Prefetch since Chrome 63 — advice treating it as a full prerender is outdated. *Official.*[^wd-prefetch]
- Don't prefetch personalised or cross-origin documents; prefetch only on fast connections, never with `Save-Data` on, and only for paths analytics show almost everyone takes. *Official.*[^wd-prefetch][^wd-resource-hints]
- A prerendered `/login` doesn't serve `/login?source=sidebar` unless No-Vary-Search ignores that parameter ([section 3](#3-cdn-notes)); `expects_no_vary_search` in the rule lets the browser reuse an in-flight prerender. *Practitioner, vendor explainer.*[^dbb-nvs]
- **Do:** build category and product templates as server-rendered pages; add View Transitions and prerender rules for the next likely page (product from category, next pagination page) instead of client-side routing; check bfcache eligibility ([section 2](#2-back-forward-cache)). Prerender only cheap, cacheable pages — not search, cart or checkout ([section 5](#5-speculation-rules-used-against-you)). *Practitioner; the page choices are inference.*

## 7. Field data vs lab scores
- **Field data counts.** CrUX data in PageSpeed Insights covers the last 28 days and is assessed at the 75th percentile, so a page passes even if a quarter of visits are slower; after a fix, field data can take 28 days to catch up. *Practitioner, vendor data.*[^dbb-psi] Thresholds: [technical foundations](technical-foundations.md#9-core-web-vitals).
- The Lighthouse Performance score doesn't feed rankings; the real-user CWV assessment does. Lighthouse weights load metrics ~45 % (LCP largest), TBT 30 %, CLS 25 %; 90+ is "good". *Practitioner, vendor data.*[^dbb-psi]
- **Business cases Google chose to publish.** Vodafone: 31 % better LCP, 8 % more sales. Rakuten 24: +53.37 % revenue per visitor and +33.13 % conversion rate after Core Web Vitals work. redBus: +7 % sales from better INP. The Economic Times: 43 % better bounce rate after passing the thresholds. BBC: 10 % more users lost per extra second. *Official; relayed, one case each.*[^wd-why-speed]

> **Conflict:** web.dev's speed cases are success stories selected by Google, not controlled studies, and argue for conversion, not rankings; elsewhere Core Web Vitals are treated as a minor ranking factor. Use them to justify speed work for shoppers, not for SEO.

## 8. TTFB, redirects and cache keys
- **Field TTFB is worse than lab TTFB** because real visits include redirects (e.g. ad click URLs), edge cache misses at the specific CDN node, short app-cache lifetimes on low-traffic pages, logged-in or personalised pages, query parameters like `utm_campaign` or `gclid` that create unique cache keys, and long-tail pages that dominate origin-level data. *Practitioner, vendor data.*[^dbb-ttfb-field]
- CrUX TTFB includes redirect and connection time; Lighthouse "server response time" is server processing only, so the two aren't comparable. Mobile Lighthouse simulates 150 ms RTT, so a request takes ≥ 600 ms even with an instant server. *Practitioner, vendor data.*[^dbb-ttfb-field]
- Measure server time with the `Server-Timing` header and field TTFB with Navigation Timing; shared hosting often causes high TTFB, and CDNs cut round-trip time. Each redirect adds a full request. *Official.*[^wd-html]
- **Do:** keep ad and campaign landing URLs free of redirect hops, keep tracking parameters out of the cache key ([section 3](#3-cdn-notes)), and compare field TTFB for landing pages with and without parameters. *Inference.*

## 9. Critical rendering path
*Official.*
- The resources needed for first render are the HTML, render-blocking CSS and scripts in the `<head>`. CSS is render-blocking by default; a non-matching `media` (e.g. `media="print"`) makes a stylesheet non-blocking. Scripts block the parser unless `async` or `defer`.[^wd-critical-path] `async` runs on download in any order, `defer` after parsing in order, and `type="module"` is deferred by default.[^wd-resource-loading]
- The preload scanner can't see CSS background images, injected scripts, dynamic `import()`, client-rendered markup or CSS `@import`. Don't render the LCP element or critical content with client-side JavaScript: it creates request chains and long tasks.[^wd-resource-loading]
- Inline critical CSS for the first viewport and load the rest async; replace `@import` with `<link>`; find unused CSS and JS with DevTools Coverage. Inlined CSS isn't cached separately, so measure.[^wd-resource-loading]

## 10. Resource hints and preload pitfalls
*Official.*[^wd-resource-hints]
- `preconnect` only to the most critical cross-origin hosts (CDN, font host), with `crossorigin` for CORS resources such as fonts, or the connection isn't reused; `dns-prefetch` is the cheaper alternative.
- `preload` is for late-discovered critical resources (fonts, `@import` CSS, a background-image LCP). Without the `as` attribute the file is downloaded twice; too many preloads compete for bandwidth ([fonts](#4-web-fonts) has a measured case).
- Images start at low priority and are raised only after layout. Set `fetchpriority="high"` on the LCP image and lower it for thumbnails; for a responsive LCP image, preload with `imagesrcset` and `fetchpriority="high"`. Per-template choices: [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md).

## 11. Lazy loading, video and embed facades
- Use `loading="lazy"` only below the initial viewport, never on hero or LCP candidates — lazy images wait for layout. `loading` doesn't change fetch priority. *Official.*[^wd-lazy]
- Lazy loading causes CLS without reserved `width`/`height` or `aspect-ratio`, and can move work into scroll interactions (INP). Prefer native `loading="lazy"`; browsers start loading ~500–800 px before the viewport. *Practitioner, vendor data.*[^dbb-lazy]
- **Embeds.** Lazy-loading iframes saves more than 500 KiB for a YouTube embed and more than 200 KiB for a Facebook Like button[^wd-lazy]; YouTube embeds block the main thread for more than 1.7 s at the median, hurting INP.[^wd-video] Use click-to-load facades (e.g. lite-youtube-embed, chat loaders). *Official; HTTP Archive data.*

## 12. Consent banners and third-party code
- **Consent banners cost INP.** In a lab test of 11 consent platforms on 5 sites (desktop, 4× CPU throttle), median INP on clicking "Accept" ranged from 6 ms (Sourcepoint, iframe) to 468 ms (Google Funding Choices); OneTrust 104 ms, Cookiebot 57 ms, Usercentrics 56 ms, Osano 225 ms. Iframe-based banners mostly answered in < 10 ms; slow cases were often scripts firing after consent (e.g. conversion tags), not the banner itself. *Measured, vendor data, small sample.*[^dbb-cmp-inp]
- **And LCP and CLS.** A render-blocking consent script (no `async`/`defer`) keeps the page blank until it loads; the banner can become the LCP element — in one example LCP rose from 1.43 s to 3.61 s when the policy text rendered. Banners inserted into the flow (not overlays) cause CLS. *Measured, vendor data, one case.*[^dbb-consent-cwv]
- **Third-party order of work:** remove providers first (highest impact), delay loading until after main content, review configuration (one example ran 200 concurrent A/B tests), ask the vendor, or move scripts to a web worker (Partytown). Lighthouse "Reduce the impact of third-party code" shows main-thread time per provider. *Practitioner, vendor data.*[^dbb-3p]
- Apps and plugins add weight: one cart-drawer app script was ~540 KB against a ~6 KB native equivalent; apps can inject duplicate libraries, and removed apps can keep loading scripts. *Practitioner, one case.*[^dbb-shopify]
- **Do:** load the consent script async, prefer an overlay or iframe banner, profile the "Accept" click in DevTools, and audit the request waterfall after every app install, tag change or theme update. Testing with and without the banner: [diagnostic tests](../measure/diagnostic-tests.md). *Practitioner.*

## 13. JavaScript: code splitting and workers
*Official.*
- Code-split with dynamic `import()` so startup JavaScript stays small. Total Blocking Time is described as highly correlated with INP; Lighthouse warns at more than 2 s of JavaScript execution and fails above 3.5 s.[^wd-code-split]
- Web workers move work off the main thread, which helps INP, but can't touch the DOM.[^wd-workers]
- Client-side navigation has its own costs: [section 6](#6-multi-page-templates-instead-of-a-single-page-app), [JavaScript](technical-foundations.md#7-javascript).

Related: [technical foundations](technical-foundations.md), [AI crawlers and controls](ai-crawlers-and-controls.md), [diagnostic tests](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs), [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md), [seasonal peaks](../situations/seasonal-peaks.md), [migration](../situations/migration.md).

[^ja-cache]: Jono Alderson, 2025-08-29: HTTP caching guide — Cache-Control templates per resource type (values quoted in section 1), ETag and purge on publish, `no-store` blocks bfcache, Cloudflare notes (no HTML caching by default, bypass on session cookie, strip tracking parameters, cache tags, `cf-cache-status`), avoid `Vary: *` and `Vary: Cookie`, never cache cart/checkout/account. Technical guide, no measurements.
[^ja-fonts]: Jono Alderson, 2025-08-21: font loading guide — WOFF2 self-hosting, `font-display` choices (`block` hides text up to ~3 s), preload attributes and identical URL, no `@import`, subsetting and `unicode-range`, ≤ 3 weights, ≤ 200 KB per font, fallback metric overrides, `font-synthesis: none`, year-long cache with versioned names.
[^ja-specevil]: Jono Alderson, 2026-04-14: third-party speculation rules pointing at uncached URLs (`/search?q=*`, `/cart?add-to-cart=*`); `Sec-Purpose: prefetch`, often no referrer; no cross-site opt-out. Argument, no measurements.
[^ja-spa]: Jono Alderson, 2025-07-24: MPA with cross-document View Transitions (`@view-transition { navigation: auto; }`, Chromium), speculation-rules prerender and bfcache vs SPA; SPA routing breaks bfcache, scroll and focus. Illustrative numbers only.
[^wd-why-speed]: web.dev, 2023-11-01: case studies relayed by Google — Vodafone (31 % LCP, 8 % sales), Rakuten 24 (+53.37 % revenue per visitor, +33.13 % conversion), redBus (+7 % sales via INP), The Economic Times (43 % better bounce rate), Renault (no figures), BBC (10 % users lost per extra second, via Creative Bloq). Selected cases, not controlled studies.
[^wd-html]: web.dev, 2023-11-01: HTML caching (about five minutes for static HTML, no browser caching of personalised HTML, ETag/Last-Modified 304s), Brotli ~15–20 % better than gzip, < 1 KiB barely compresses, Server-Timing and Navigation Timing for TTFB, each redirect adds a request. Guidance.
[^wd-critical-path]: web.dev, 2023-11-27: critical resources, render-blocking CSS, `media` attribute, parser-blocking scripts. Guidance.
[^wd-resource-loading]: web.dev, 2023-11-01: preload scanner blind spots, no client-rendered LCP, critical CSS inlining, `@import`, Coverage, `async`/`defer`/`type="module"`. Guidance.
[^wd-resource-hints]: web.dev, 2023-11-01: `preconnect`/`dns-prefetch`, `preload` with `as` (double download without it), `fetchpriority`, `imagesrcset`, prefetch only for common paths and not with Save-Data. Guidance.
[^wd-video]: web.dev, 2026-04-02: YouTube embeds block the main thread > 1.7 s at the median (HTTP Archive); facades. Guidance plus HTTP Archive data.
[^wd-fonts]: web.dev, 2023-11-01: `font-display` behaviour (`block` up to 3 s in Chromium/Firefox, indefinitely in Safari; `optional` 100 ms), self-hosting, WOFF2 up to 30 % smaller than WOFF, inline `@font-face`, preload with `crossorigin`, no base64. Guidance.
[^wd-code-split]: web.dev, 2023-12-04: dynamic `import()`, TBT correlated with INP, Lighthouse JS execution thresholds (warn > 2 s, fail > 3.5 s). Guidance.
[^wd-lazy]: web.dev, 2023-11-01: `loading="lazy"` only outside the initial viewport, no priority change; iframe savings (> 500 KiB YouTube, > 200 KiB Facebook Like); facades. Guidance.
[^wd-prefetch]: web.dev, 2023-11-01: speculation rules (`prefetch`/`prerender`, Chromium), prerender runs JS, Quicklink, no personalised or cross-origin prefetch, Save-Data, `rel=prerender` only NoState Prefetch since Chrome 63, service worker precaching costs, Cache API vs HTTP cache. Guidance.
[^wd-workers]: web.dev, 2023-11-01: web workers move work off the main thread for INP, no DOM access; demo without figures. Guidance.
[^dbb-psi]: DebugBear, 2025-03-09 (upd. 2026-10-08): CrUX in PSI = 28 days at p75, up to 28 days to update; Lighthouse score not a ranking input, weights (~45 % load, 30 % TBT, 25 % CLS). Explainer, vendor.
[^dbb-ttfb-field]: DebugBear, 2025-01-10 (upd. 2025-10-19): causes of field vs lab TTFB gaps (redirects, edge misses, short app caches, personalisation, `utm_campaign`/`gclid` cache keys, long tail); CrUX TTFB includes redirects and connection; mobile Lighthouse 150 ms RTT. Explainer, vendor.
[^dbb-nvs]: DebugBear, 2026-05-26: No-Vary-Search header (Chrome, Edge, Opera; not Firefox/Safari; experimental as of 2026-05), don't ignore content-changing parameters, prerender reuse with `expects_no_vary_search`. Explainer; `gclid` not mentioned.
[^dbb-spec-proxy]: DebugBear, 2025-05-28 (upd. 2025-06-22): Google SERP prefetches the first two results' HTML via speculation rules and a privacy proxy, skipped when the user has cookies for the domain. Observation of Google's page code.
[^dbb-cdn-seo]: DebugBear, 2026-05-04: a CDN improves TTFB/LCP, reliability and crawl efficiency but doesn't directly boost rankings; `cf-cache-status: HIT`. Explainer, one Shopify example, no before/after data.
[^dbb-cmp-inp]: DebugBear, 2026-02-06 (upd. 2026-03-17): lab test, 11 consent platforms × 5 sites, desktop with 4× CPU throttle, median INP after clicking "Accept"; iframe banners < 10 ms in most cases; slow cases often from post-consent scripts. Vendor data, small sample.
[^dbb-consent-cwv]: DebugBear, 2025-03-20: one example test — render-blocking consent script, banner as LCP element (1.43 s → 3.61 s), inserted banners cause CLS. Vendor data, one case.
[^dbb-3p]: DebugBear, 2025-03-06 (upd. 2026-01-27): order for reducing third-party impact (remove, delay, configure, vendor, Partytown), Lighthouse audit. Guidance, vendor; GTM not covered.
[^dbb-shopify]: DebugBear, 2026-04-20: Shopify examples — cart-drawer app ~540 KB vs ~6 KB native, duplicate libraries, leftover scripts from removed apps; font subsetting 40–50 %. Practitioner examples.
[^dbb-fonts]: DebugBear, 2025-02-07 (upd. 2025-11-30): font preload test (LCP 1.82 s → 1.24 s); page with 38 preloaded fonts improved > 2 s after removing them; preloads go stale. Vendor data, one case each.
[^dbb-lazy]: DebugBear, 2026-04-10: lazy loading harms above-the-fold LCP, causes CLS without reserved space, shifts work into scroll (INP); native lazy loading starts ~500–800 px early. Guidance, vendor.
