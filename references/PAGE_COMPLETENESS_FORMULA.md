# SEO Page Completeness Formula

Purpose: define the minimum complete SEO package for an indexable page. Use this when auditing a page like a homepage, service page, product page, local business page, article, or landing page.

Last updated: 2026-06-30

## Important note about character counts

Character counts are practical QA targets, not guaranteed ranking factors. Search engines may rewrite titles/snippets. The goal is clarity, intent match, and clean presentation.

Recommended working ranges:

| Field | Recommended | Warning zone | Notes |
| --- | ---: | ---: | --- |
| Title tag | 45–60 chars | >65 chars | Keep primary entity + intent visible early. Some tools allow longer, but SERP may truncate. |
| Meta description | 120–160 chars | >180 chars | Google may rewrite snippets. Keep concise, useful, and non-spammy. |
| H1 | 20–70 chars | multiple H1s | One primary H1 matching page intent. |
| Image ALT | 5–125 chars | empty or keyword-stuffed | Describe image context naturally. |
| URL slug | 1–6 words | long/parameter-heavy | Stable, lowercase, descriptive. |

## Complete page formula

Every indexable page should have:

```txt
Purpose + Intent
Metadata
Canonical + Robots
Social metadata
Content hierarchy
Structured data
Images/media metadata
Internal links
External trust links where useful
Sitemap + robots discovery
Measurement readiness
```

## 1. Purpose and intent

Before optimising tags, answer:

- What search intent does this page serve?
- What business outcome does it support?
- Why should this page be indexed?
- What unique value does it provide compared with similar pages?
- What is the next user action?

If these are unclear, the page is not complete.

## 2. Required head fields

Minimum head fields for an indexable page:

```html
<title>{{TITLE}}</title>
<meta name="description" content="{{DESCRIPTION}}">
<link rel="canonical" href="{{ABSOLUTE_CANONICAL_URL}}">
<meta name="robots" content="index, follow, max-image-preview:large">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta charset="UTF-8">
```

Recommended fields:

```html
<meta name="author" content="{{AUTHOR_OR_ORGANIZATION}}">
<meta name="publisher" content="{{PUBLISHER_OR_ORGANIZATION}}">
<meta name="theme-color" content="{{BRAND_COLOR}}">
```

For local business/location pages, optional geo tags if accurate:

```html
<meta name="geo.region" content="{{REGION_CODE}}">
<meta name="geo.placename" content="{{PLACE_NAME}}">
<meta name="geo.position" content="{{LATITUDE}};{{LONGITUDE}}">
<meta name="ICBM" content="{{LATITUDE}}, {{LONGITUDE}}">
```

## 3. Title formula

A strong title usually contains:

```txt
Primary Entity + Primary Intent + Location/Qualifier
```

Examples:

```txt
Ribath Al-Hadi - Girls Quran Memorisation Boarding School in Malang
```

```txt
Emergency Plumbing in Newcastle | ABC Plumbing
```

```txt
Organic Cotton Baby Blanket - Soft Newborn Gift
```

Rules:

- put the most important entity/keyword early
- do not keyword-stuff
- do not repeat the same location/category unnaturally
- title should be unique per page
- avoid changing titles frequently without reason

## 4. Meta description formula

A strong meta description usually contains:

```txt
Entity + offer/service + audience/location + trust/unique value + soft CTA
```

Example:

```txt
Ribath Al-Hadi is a girls Quran memorisation boarding school in Pujon, Malang, offering guided tahfidz, full boarding care, and character formation.
```

Rules:

- write for humans, not keyword density
- avoid long lists of keywords
- avoid claims that are not visible on the page
- keep it concise enough for snippets
- unique per indexable page

## 5. Keywords meta

`meta keywords` is not used by Google for ranking and is usually unnecessary.

However, keyword lists can still be useful internally as:

- editorial targeting notes
- content brief terms
- Search Console query mapping
- page intent vocabulary

If included, keep it clean and not spammy. Do not rely on it for ranking.

## 6. Open Graph and Twitter/X metadata

Required for shareable pages:

```html
<meta property="og:type" content="website">
<meta property="og:site_name" content="{{SITE_NAME}}">
<meta property="og:title" content="{{TITLE}}">
<meta property="og:description" content="{{DESCRIPTION}}">
<meta property="og:url" content="{{ABSOLUTE_CANONICAL_URL}}">
<meta property="og:image" content="{{ABSOLUTE_IMAGE_URL}}">
<meta property="og:locale" content="{{LOCALE}}">

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="{{TITLE}}">
<meta name="twitter:description" content="{{DESCRIPTION}}">
<meta name="twitter:image" content="{{ABSOLUTE_IMAGE_URL}}">
```

Rules:

- use absolute image URLs, not relative paths
- image should be crawlable and share-friendly
- prefer 1200×630 for broad social sharing
- keep OG/Twitter title and description aligned with page intent

## 7. Canonical and robots

Indexable page:

```html
<link rel="canonical" href="https://example.com/page/">
<meta name="robots" content="index, follow, max-image-preview:large">
```

Noindex page:

```html
<meta name="robots" content="noindex, follow">
```

Rules:

- canonical must be absolute
- canonical should usually be self-referential for unique pages
- noindex pages should not be in sitemap
- do not canonical all pages to homepage
- use `max-image-preview:large` for pages where image preview matters

## 8. Heading structure

Minimum:

- exactly one clear H1 for the primary page topic
- H2s for major sections
- H3/H4 for subsections only when useful

Rules:

- heading count is not a score by itself
- hierarchy should match content structure
- avoid decorative headings that confuse topic hierarchy
- headings should help passage-level understanding

## 9. Image completeness

Every important image should have:

- meaningful `alt`
- width/height or stable dimensions
- modern format where possible (WebP/AVIF)
- non-lazy LCP/hero image
- descriptive filename where practical
- title attribute optional; not required for SEO

ALT pattern:

```txt
[Subject] + [context/action/location if useful]
```

Examples:

```txt
Students reading Quran in a guided tahfidz halaqah at Ribath Al-Hadi
```

```txt
Front view of organic cotton baby blanket in cream colour
```

## 10. Link completeness

Internal links:

- use crawlable `<a href>` links
- link to primary money/service/category pages
- add breadcrumbs for hierarchical sites
- use descriptive anchor text
- avoid orphan pages

External links:

- use when they build trust or cite official sources
- use `rel="noopener noreferrer"` for new-window external links
- `title` attributes are optional; useful for clarity but not required

## 11. Structured data completeness

Prefer JSON-LD.

Common schema by page type:

| Page type | Schema |
| --- | --- |
| Homepage | Organization / LocalBusiness / WebSite |
| Local service page | LocalBusiness + Service + BreadcrumbList |
| Product page | Product + Offer + BreadcrumbList |
| Article/blog | Article/BlogPosting + BreadcrumbList |
| FAQ section | FAQPage only if FAQ is visible |
| Review content | Review/AggregateRating only if real reviews are visible |

Rules:

- schema must match visible content
- do not fake ratings/reviews
- use stable `@id` for entities
- validate with schema tools / rich result tools where possible

## 12. Discovery files

A complete site should have:

- `/robots.txt`
- `/sitemap.xml`
- sitemap referenced in robots.txt
- sitemap includes canonical-indexable URLs only
- true `lastmod` when used
- Bing/IndexNow for frequently changing sites

Example robots.txt:

```txt
User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml
```

## 13. Measurement readiness

A complete SEO page should be measurable:

- Google Search Console property verified
- Bing Webmaster Tools property verified where relevant
- analytics events for primary CTA
- conversion tracking if business-critical
- page type and query mapping documented

## 14. Complete page audit checklist

Use this checklist for any important indexable page:

| Check | Pass? | Notes |
| --- | --- | --- |
| Clear page purpose and search intent |  |  |
| Unique title |  |  |
| Meta description |  |  |
| Absolute canonical |  |  |
| Robots directive correct |  |  |
| OG/Twitter tags present |  |  |
| OG/Twitter images absolute |  |  |
| One clear H1 |  |  |
| Logical H2/H3 structure |  |  |
| Important images have ALT |  |  |
| LCP image not lazy-loaded |  |  |
| Internal links crawlable |  |  |
| Schema eligible and valid |  |  |
| Page appears in sitemap if indexable |  |  |
| Noindex pages excluded from sitemap |  |  |
| Robots.txt references sitemap |  |  |
| CTA measurable |  |  |

## 15. Example analysis: Islamic boarding school homepage

Given a page with:

- Title length: 72 chars
- Description length: 217 chars
- Canonical: correct absolute homepage URL
- Robots: `index, follow, max-image-preview:large`
- H1 count: 1
- H2/H3: rich section structure
- Images: all have ALT
- OG/Twitter image: relative path
- Schema.org itemtype: none detected

Assessment:

| Area | Status | Reason |
| --- | --- | --- |
| Title | Warning | Clear but slightly long; may truncate. Consider shortening while preserving entity + intent. |
| Description | Warning | Informative but too long for snippet control. Reduce to ~150–160 chars. |
| Canonical | Pass | Absolute canonical present. |
| Robots | Pass | Index/follow and large image preview present. |
| Headings | Pass | One H1 and rich section hierarchy. Check H2 count for readability, not as a ranking issue. |
| Images | Pass | ALT coverage complete. Image title attributes are optional. |
| Social images | Warning | OG/Twitter image should be absolute URL. |
| Schema | Fail/Gap | Add JSON-LD Organization/LocalBusiness/EducationalOrganization, WebSite, BreadcrumbList, FAQPage if FAQ visible. |
| Links | Pass/Minor | Link title attributes are optional; make sure anchor text is descriptive. |
| Keywords meta | Neutral | Not needed for Google ranking. Keep only as internal targeting if desired. |

Optimised English-style example:

```txt
Title:
Ribath Al-Hadi - Girls Quran Memorisation Boarding School in Malang

Meta description:
Ribath Al-Hadi is a girls Quran memorisation boarding school in Pujon, Malang, offering guided tahfidz, full boarding care, and character formation.

Canonical:
https://rtqalhadi.com/

Robots:
index, follow, max-image-preview:large

OG image:
https://rtqalhadi.com/papan-nama-alhadi.webp
```

Recommended schema types:

- EducationalOrganization or LocalBusiness subtype if appropriate
- WebSite
- BreadcrumbList
- FAQPage only if FAQ is visible

## 16. Final rule

A page is complete when it is understandable by:

- a crawler
- a ranking/retrieval system
- an AI answer system
- a human visitor
- a business owner measuring outcomes
