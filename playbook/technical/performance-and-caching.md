---
type: Checklist
title: Performance and caching
description: Cache-Control templates per page type (never for cart, checkout or account), the back/forward cache, CDN caching notes, web font loading, speculation rules abused by third parties and the Sec-Purpose header, and multi-page templates with View Transitions and prerendering instead of a single-page app.
tags: [technical-seo, performance, caching, cache-control, cdn, bfcache, fonts, speculation-rules, prerender, view-transitions, spa, core-web-vitals, ecommerce]
status: stable
generated: { by: claude-code/claude-opus-5-5, at: 2026-10-28T12:00:00Z }
verified: { by: human:martin-aberastegue, at: 2026-10-28T13:03:00Z }
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
---

# Performance and caching

Which caching headers, font setup and navigation model make a shop fast for people and cheap to crawl, and where third parties can turn browser features against you. Everything here comes from one practitioner's technical guides — sound web-platform practice, but no measured ranking effect; confidence labels follow the [scale](../reference/sources-and-confidence.md). The Core Web Vitals thresholds themselves are in [technical foundations](technical-foundations.md#9-core-web-vitals); edge caching for AI bots and their timeouts in [AI-bot reliability in server logs](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs).

## Rules
- **Set Cache-Control per page type from a template, and never cache cart, checkout or account pages** in a shared cache. *Practitioner* — [evidence](#1-cache-control-templates-per-page-type)
- **Don't send `no-store` on public HTML**, or pages lose the back/forward cache; check bfcache eligibility for category and product templates. *Practitioner* — [evidence](#2-back-forward-cache)
- **On the CDN, cache HTML deliberately**: bypass on a session cookie, strip tracking parameters from the cache key, purge by tag on publish, and avoid `Vary: *` and `Vary: Cookie`. *Practitioner* — [evidence](#3-cdn-notes)
- **Self-host WOFF2 fonts with `font-display: swap`, preload only the above-the-fold faces, and keep to ≤ 3 weights.** *Practitioner* — [evidence](#4-web-fonts)
- **Log the `Sec-Purpose` header, serve speculative hits on search and cart URLs cheaply, and keep them out of demand counts.** *Practitioner argument, no measurements* — [evidence](#5-speculation-rules-used-against-you)
- **Prefer server-rendered multi-page templates with View Transitions and your own prerender rules over a single-page app** for category and product pages. *Practitioner, illustrative numbers* — [evidence](#6-multi-page-templates-instead-of-a-single-page-app)

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
- `stale-if-error` keeps serving the last good page during an origin outage, which also keeps crawlers from seeing 5xx errors that lower the crawl rate ([crawl budget](technical-foundations.md#6-crawl-budget)). *Inference.*

## 2. Back-forward cache
- `no-store` on HTML generally blocks the back/forward cache (bfcache), so a shopper going back from a product to the category reloads the whole page instead of restoring it.[^ja-cache]
- Single-page-app routing also breaks bfcache, scroll restoration and focus ([section 6](#6-multi-page-templates-instead-of-a-single-page-app)).[^ja-spa]
- **Do:** keep `no-store` for pages with personal data only; check bfcache eligibility for category and product templates in the browser's developer tools. *Practitioner.*

## 3. CDN notes
*Practitioner, written for Cloudflare; the principles apply to other CDNs.*[^ja-cache]
- Cloudflare doesn't cache HTML by default; you opt in with rules.
- Bypass the cache when a session cookie is present, so logged-in and cart states are never served from the shared cache.
- Strip tracking parameters (`utm_*`, click IDs) from the cache key, or every campaign click becomes a cache miss.
- Use cache tags to purge exactly the pages a publish or price change affects; check the `cf-cache-status` response header to see whether a page was served from the cache.
- Avoid `Vary: *` and `Vary: Cookie`, which make responses effectively uncacheable.

## 4. Web fonts
*Practitioner, technical guide.*[^ja-fonts]
- Self-host fonts as WOFF2.
- `font-display: swap` as the default; `block` hides text for up to ~3 s; `optional` for decorative faces.
- Preload only the critical above-the-fold faces, with `as="font"`, `type`, `crossorigin` and exactly the same URL as in the `@font-face` rule — a mismatch downloads the font twice.
- No `@import` for fonts; subset them and use `unicode-range`.
- At most 3 weights, ≤ 200 KB per font compressed.
- Set fallback metric overrides (`size-adjust`, `ascent-override`, `descent-override`, `line-gap-override`) so the swap doesn't shift the layout (CLS), and `font-synthesis: none` to stop fake bold and italic.
- Cache fonts for a year with versioned file names ([section 1](#1-cache-control-templates-per-page-type)).

## 5. Speculation rules used against you
*Practitioner argument, no measurements.*[^ja-specevil]
- Third-party pages can inject speculation rules that prefetch or prerender your uncached URLs — site search (`/search?q=*`) or add-to-cart links (`/cart?add-to-cart=*`) — creating real-browser load on your origin.
- These requests carry `Sec-Purpose: prefetch` and often no referrer. There is no cross-site opt-out yet.
- **Do:** log the `Sec-Purpose` header; serve speculative hits on search and cart URLs a cheap response or rate-limit them; exclude them from demand counts (site-search reports, add-to-cart events) so they don't read as shopper interest ([analytics](../measure/analytics.md)).

## 6. Multi-page templates instead of a single-page app
*Practitioner, technical guide with illustrative numbers.*[^ja-spa]
- A multi-page site with cross-document View Transitions (`@view-transition { navigation: auto; }`, Chromium), its own speculation-rules prerendering of likely next pages and a working bfcache covers most reasons teams give for a single-page app.
- Single-page-app routing breaks bfcache, scroll restoration and focus handling, and puts links and content behind JavaScript that AI fetchers don't run ([JavaScript](technical-foundations.md#7-javascript)).
- **Do:** build category and product templates as server-rendered pages; add View Transitions and prerender rules for the next likely page (product from category, next pagination page) instead of client-side routing; check bfcache eligibility ([section 2](#2-back-forward-cache)). Prerender only cheap, cacheable pages — not search, cart or checkout ([section 5](#5-speculation-rules-used-against-you)). *Practitioner; the page choices are inference.*

Related: [technical foundations](technical-foundations.md), [AI crawlers and controls](ai-crawlers-and-controls.md), [diagnostic tests](../measure/diagnostic-tests.md#12-ai-bot-reliability-in-server-logs), [category pages](../page-types/category-pages.md), [product pages](../page-types/product-pages.md), [seasonal peaks](../situations/seasonal-peaks.md), [migration](../situations/migration.md).

[^ja-cache]: Jono Alderson, 2025-08-29: HTTP caching guide — Cache-Control templates per resource type (values quoted in section 1), ETag and purge on publish, `no-store` blocks bfcache, Cloudflare notes (no HTML caching by default, bypass on session cookie, strip tracking parameters, cache tags, `cf-cache-status`), avoid `Vary: *` and `Vary: Cookie`, never cache cart/checkout/account. Technical guide, no measurements.
[^ja-fonts]: Jono Alderson, 2025-08-21: font loading guide — WOFF2 self-hosting, `font-display` choices (`block` hides text up to ~3 s), preload attributes and identical URL, no `@import`, subsetting and `unicode-range`, ≤ 3 weights, ≤ 200 KB per font, fallback metric overrides, `font-synthesis: none`, year-long cache with versioned names.
[^ja-specevil]: Jono Alderson, 2026-04-14: third-party speculation rules pointing at uncached URLs (`/search?q=*`, `/cart?add-to-cart=*`); `Sec-Purpose: prefetch`, often no referrer; no cross-site opt-out. Argument, no measurements.
[^ja-spa]: Jono Alderson, 2025-07-24: MPA with cross-document View Transitions (`@view-transition { navigation: auto; }`, Chromium), speculation-rules prerender and bfcache vs SPA; SPA routing breaks bfcache, scroll and focus. Illustrative numbers only.
