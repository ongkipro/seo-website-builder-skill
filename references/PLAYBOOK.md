# SEO OS Daily Playbook

This is the operational daily playbook for `seo-website-builder`. Use it when building, auditing, or improving websites without loading the full deep SEO knowledge base.

## Core principle

SEO is not just keywords. A website must be:

1. crawlable
2. renderable
3. understandable
4. index-worthy
5. intent-matched
6. trustworthy
7. internally linked
8. ready for AI-search / answer surfaces
9. measurable
10. commercially useful

## Multi-engine baseline

| Surface | Priority |
| --- | --- |
| Google | helpful content, crawl/index, canonical, structured data, page experience, AI feature eligibility |
| Bing | XML sitemap, accurate `lastmod`, IndexNow, Bing Webmaster Tools, crawlability |
| Yandex | quality, security, mobile convenience, site region, Yandex Webmaster/Metrica diagnostics |
| Pinterest | high-quality vertical visuals, claimed website, descriptive Pin text, seasonal/trend relevance, landing-page match |
| AI Search | indexed/snippet-eligible pages, clear passages, entity clarity, source trust, fresh accurate data |

Default rule: optimise for users and technical clarity first, then add platform-specific signals without creating spam.

## Standard workflow

### 1. Define business context

Answer:

- What is the business?
- Who is the target user?
- What market/location is being served?
- What is the primary goal: leads, sales, bookings, signups, traffic, authority?
- Which pages generate business value?

### 2. Build a search intent map

| Intent | Example | Page type |
| --- | --- | --- |
| Brand | brand name | Homepage / About |
| Transactional | buy product X | Product / Service page |
| Commercial investigation | best X, X vs Y | Category / Comparison |
| Local | service near me | Location / Service-area page |
| Informational | how to choose X | Guide / Blog |
| Trust | reviews, testimonials, policies | Review / About / Policy |

### 3. Build a page type map

Every page must support at least one of:

- traffic
- conversion
- trust
- crawl path
- topical authority
- support for a money page

If not, consider merging it, noindexing it, or not creating it.

### 4. Define URL architecture

Safe patterns:

```txt
/
/about/
/contact/
/services/
/services/service-name/
/products/
/products/product-name/
/categories/category-name/
/blog/article-title/
/locations/city-name/
```

Rules:

- short, descriptive, lowercase slugs
- do not change URLs without redirects
- avoid indexable parameters unless intentional
- canonical rules must be consistent

### 5. Define index rules

| Page | Default |
| --- | --- |
| Homepage | index |
| Primary product/service page | index |
| Unique category/collection | index |
| Helpful blog/guide | index |
| Thank-you page | noindex |
| Cart/checkout/internal search | noindex |
| Thin filter/facet page | noindex/canonical |
| Duplicate location page without unique value | noindex/merge |

### 6. Create per-page SEO templates

Every indexable page needs:

- unique title
- unique meta description
- absolute canonical URL
- one relevant H1
- intro that answers intent
- helpful body content
- internal links
- clear CTA
- eligible schema where appropriate

### 7. Internal linking plan

Minimum:

- homepage → primary categories/services
- category → products/subcategories/guides
- product → category, related products, FAQ/trust
- article → money pages and related content
- footer → trust/legal/contact pages
- breadcrumbs → hierarchical pages

### 8. Structured data plan

Use schema only when it represents visible, real content.

Common types:

- Organization / LocalBusiness
- WebSite
- BreadcrumbList
- Product / Offer
- AggregateRating / Review if real and visible
- Article / BlogPosting
- FAQPage if FAQ is visible on the page
- Service for service pages

### 9. Technical QA before launch

Minimum checks:

- important pages return 200
- broken internal links = 0
- sitemap contains canonical-indexable URLs only
- robots does not block important assets
- canonical URLs are correct
- title/meta are unique
- mobile layout is usable
- LCP image is not lazy-loaded
- 404 page returns 404
- permanent URL changes use 301 redirects
- Search Console and/or platform webmaster tools are ready

### 10. Measurement plan

Track:

- Google Search Console
- Bing Webmaster Tools
- analytics CTA events
- conversion tracking
- top queries
- indexed pages
- crawl/index errors
- Core Web Vitals
- high-impression low-CTR pages
- traffic drops by page type
- Bing sitemap/indexing status
- IndexNow results for frequently changing sites
- Yandex Webmaster/Metrica if relevant
- Pinterest analytics for visual/content commerce

## Required AI output

For substantial SEO tasks, return:

```txt
Critical Assessment
Evidence / Source Confidence
Missing Inputs / Assumptions
Search Intent Map
Page Type Map
URL Structure
Index + Canonical Rules
Metadata Pattern
Schema Plan
Internal Linking Plan
Content Requirements
Multi-Engine Notes
Technical Implementation
Complete Page Formula Checks
QA / Validation Checklist
Measurement Plan
Risk Notes
```

## Stop rules

Stop or ask before continuing if:

- business goal is unclear
- page map is unclear
- index/canonical rules are unclear
- the page exists only for keyword capture
- content would be generic, fake, or misleading
- schema would mark invisible content
- there is no Search Console/analytics plan

## Official source priority

Prefer official sources first:

- Google Search Essentials
- Google SEO Starter Guide
- Google ranking systems guide
- Google AI Features and Your Website
- Google structured data docs
- Google crawling/indexing docs
- Google Search Console docs
- web.dev Core Web Vitals
- Bing Webmaster Blog / Bing Webmaster Guidelines / IndexNow
- Yandex Webmaster documentation
- Pinterest Business / Help / Policy docs

Use industry sources for examples and tactics, not as secret ranking-weight claims.

For algorithm updates, check and record:

- `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
- `SEARCH_ENGINE_SOURCE_INDEX.md`
- `ALGORITHM_UPDATE_LOG.md`
