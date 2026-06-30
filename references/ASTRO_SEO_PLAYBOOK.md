# Astro SEO Playbook

Purpose: SEO implementation and audit rules for Astro, static HTML, and Cloudflare-hosted content sites.

## Goal

Astro should produce pages where:

- primary content exists in the initial HTML
- metadata is unique per page
- sitemap contains canonical-indexable URLs only
- robots rules are correct
- Core Web Vitals remain lightweight
- schema is valid and matches visible content

## Project classification

Before implementation, classify the project:

| Lane | Pattern |
| --- | --- |
| Content site | static pages, blog, docs, company profile |
| Hybrid site | mostly static plus forms, API routes, auth, or a small dashboard |
| App-like site | many dynamic stateful UI screens; Astro may not be the best fit |

SEO default: choose static HTML first. Add server behavior or islands only when needed.

## Rendering strategy

Default order:

1. static generation for public SEO pages
2. selective server/API routes for forms or dynamic data
3. framework islands only for small interactive pieces
4. full server rendering only when request-time data is required

Rules:

- do not make every route SSR just because the site has one form
- do not render primary content exclusively with client-side JavaScript
- hydrate only the smallest interactive island
- navigation and internal links must remain crawlable `<a href>` links

## Setup checklist

### 1. Base SEO layout

Every layout should accept:

```ts
title
metaDescription
canonical
ogImage
noindex
breadcrumbs
schema
```

Required output:

```html
<title>...</title>
<meta name="description" content="...">
<link rel="canonical" href="...">
<meta property="og:title" content="...">
<meta property="og:description" content="...">
<meta property="og:url" content="...">
<meta property="og:image" content="...">
<meta name="twitter:card" content="summary_large_image">
```

If `noindex=true`:

```html
<meta name="robots" content="noindex,follow">
```

### 2. Sitemap

The sitemap should:

- include only canonical URLs
- exclude checkout, thank-you, internal search, thin filters, and noindex policy pages
- use absolute URLs
- include `lastmod` only when accurate

Safe pattern:

```txt
/
/about/
/contact/
/services/
/services/[slug]/
/blog/[slug]/
```

### 3. Robots

Minimum robots file:

```txt
User-agent: *
Allow: /
Sitemap: https://domain.com/sitemap.xml
```

Block only when necessary. Do not block important JS/CSS/image assets.

### 4. Content collections

For blog/content sites, required frontmatter:

```yaml
title:
description:
publishedDate:
updatedDate:
author:
slug:
canonical:
noindex: false
```

Validate:

- title is unique
- description is unique
- slug is stable
- dates are accurate
- author/entity is clear

### 5. Performance SEO

Preserve Astro's advantage:

- minimise client islands
- do not lazy-load hero/LCP image
- preload LCP image when useful
- use WebP/AVIF where appropriate
- always set image width/height or stable dimensions
- keep font loading safe
- avoid global heavy client JavaScript
- use `.astro` components for static UI

Islands are appropriate for:

- mobile menus
- tabs/accordions
- forms with client validation
- search/filter widgets
- charts/rich interactions

If it is not interactive, do not make it a React/Vue/Svelte island.

### 6. Schema

Common schema:

- Organization / LocalBusiness site-wide
- BreadcrumbList for hierarchical pages
- Article for blog posts
- Product for ecommerce pages
- FAQPage only if FAQ is visible

Inject JSON-LD as a script and validate with rich result/schema tools.

## QA commands

```bash
npm run build
npm run check
```

Inspect output:

```bash
rg '<title>|canonical|description|robots' dist -n
rg 'application/ld\+json' dist -n
```

Manual checks:

- `/sitemap.xml`
- `/robots.txt`
- 404 page and status
- canonical host
- mobile layout
- Lighthouse/PageSpeed

## Anti-patterns

- all content rendered client-side
- same meta tags on every page
- sitemap includes noindex URLs
- every canonical points to homepage
- hero/LCP image lazy-loaded
- internal navigation uses buttons without `href`
- slugs change between builds
- all pages are SSR without need
- framework islands used for static UI
- content collections lack frontmatter validation
- 404 page returns 200 in deployment

## Final gate

An Astro site is not SEO-ready until:

- build passes
- sitemap is valid
- robots is valid
- every indexable page has unique title/meta/canonical
- schema validates
- internal links are not broken
- primary content exists in initial HTML
- Search Console is ready after deployment
