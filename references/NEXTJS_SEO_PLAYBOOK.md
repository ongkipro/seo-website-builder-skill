# Next.js SEO Playbook

Purpose: SEO implementation and audit rules for Next.js frontend projects using App Router or Pages Router.

Last updated: 2026-06-30

## Core principle

Next.js can be excellent for SEO when public pages render meaningful HTML, metadata is route-specific, and client components do not hide primary content from crawlers.

Default SEO rule:

```txt
Public SEO pages should be static or server-rendered with complete metadata and crawlable content in the initial HTML.
```

## Rendering strategy

| Page type | Recommended strategy | Notes |
| --- | --- | --- |
| Homepage | SSG / server component | Should render complete content and links. |
| Marketing/service page | SSG | Best for stable public pages. |
| Blog/article | SSG or ISR | Use ISR if content updates periodically. |
| Product/category | SSG/ISR or SSR | ISR for catalog freshness; SSR if pricing/availability must be request-time. |
| Search/internal filters | noindex, often client/SSR | Usually not indexable unless curated and unique. |
| Dashboard/account/cart/checkout | noindex/private | Exclude from sitemap. |

Rules:

- Use static generation for stable public SEO pages.
- Use ISR for content/catalog pages that change but do not require per-request personalization.
- Use SSR only when request-time data is needed.
- Avoid client-only rendering for primary content.
- Client Components are fine for interactive UI, not for the main indexable content.

## App Router SEO

For Next.js App Router, prefer built-in Metadata API.

### Static metadata

```tsx
export const metadata = {
  title: 'Service in Location | Brand',
  description: 'Professional service description written for humans.',
  alternates: {
    canonical: 'https://example.com/service/',
  },
  openGraph: {
    type: 'website',
    url: 'https://example.com/service/',
    title: 'Service in Location | Brand',
    description: 'Professional service description written for humans.',
    images: ['https://example.com/og/service.jpg'],
  },
  twitter: {
    card: 'summary_large_image',
    title: 'Service in Location | Brand',
    description: 'Professional service description written for humans.',
    images: ['https://example.com/og/service.jpg'],
  },
}
```

### Dynamic metadata

Use `generateMetadata()` for dynamic routes:

```tsx
export async function generateMetadata({ params }) {
  const page = await getPage(params.slug)

  return {
    title: page.seoTitle,
    description: page.seoDescription,
    alternates: {
      canonical: `https://example.com/${page.slug}/`,
    },
    openGraph: {
      title: page.seoTitle,
      description: page.seoDescription,
      url: `https://example.com/${page.slug}/`,
      images: [page.ogImageAbsoluteUrl],
    },
  }
}
```

Rules:

- Metadata must be unique per indexable route.
- Canonical URLs must be absolute.
- OG/Twitter images should be absolute URLs.
- Do not set every route canonical to homepage.
- Do not rely only on client-side metadata changes.

## Pages Router SEO

For Pages Router, use `next/head` carefully:

```tsx
import Head from 'next/head'

export default function Page() {
  return (
    <>
      <Head>
        <title>Service in Location | Brand</title>
        <meta name="description" content="Professional service description written for humans." />
        <link rel="canonical" href="https://example.com/service/" />
        <meta name="robots" content="index, follow, max-image-preview:large" />
        <meta property="og:type" content="website" />
        <meta property="og:title" content="Service in Location | Brand" />
        <meta property="og:description" content="Professional service description written for humans." />
        <meta property="og:url" content="https://example.com/service/" />
        <meta property="og:image" content="https://example.com/og/service.jpg" />
        <meta name="twitter:card" content="summary_large_image" />
      </Head>
      <main>...</main>
    </>
  )
}
```

Rules:

- Avoid duplicate Head tags from nested components.
- Keep canonical and robots consistent.
- Ensure dynamic pages receive server-side/static SEO values.

## Sitemap and robots

### App Router files

Use route handlers or metadata files:

- `app/sitemap.ts`
- `app/robots.ts`

Example sitemap:

```ts
import type { MetadataRoute } from 'next'

export default function sitemap(): MetadataRoute.Sitemap {
  return [
    {
      url: 'https://example.com/',
      lastModified: new Date('2026-06-30'),
    },
    {
      url: 'https://example.com/services/',
      lastModified: new Date('2026-06-30'),
    },
  ]
}
```

Example robots:

```ts
import type { MetadataRoute } from 'next'

export default function robots(): MetadataRoute.Robots {
  return {
    rules: {
      userAgent: '*',
      allow: '/',
      disallow: ['/dashboard/', '/checkout/', '/account/'],
    },
    sitemap: 'https://example.com/sitemap.xml',
  }
}
```

Rules:

- Sitemap should include canonical-indexable URLs only.
- Exclude noindex/private/search/filter pages.
- Use true `lastModified`, not generation time, when possible.
- Reference sitemap in robots.

## Structured data in Next.js

Use JSON-LD script in server-rendered output:

```tsx
export function JsonLd({ data }: { data: object }) {
  return (
    <script
      type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify(data) }}
    />
  )
}
```

Rules:

- Schema must match visible content.
- Do not inject fake reviews/ratings.
- Use stable `@id` for Organization/LocalBusiness entities.
- Use BreadcrumbList on hierarchical pages.
- Use Product/Offer only when price/availability are visible and accurate.

## next/image SEO and performance

Rules:

- Every meaningful image needs `alt`.
- Decorative images can use `alt=""`.
- LCP/hero image should use priority/preload where appropriate.
- Do not lazy-load LCP image.
- Set stable dimensions to avoid CLS.
- Use descriptive filenames where practical.

Example:

```tsx
import Image from 'next/image'

<Image
  src="/images/service-hero.webp"
  alt="Team providing professional service in Newcastle"
  width={1200}
  height={630}
  priority
/>
```

## Link and navigation rules

Use `next/link` for internal links:

```tsx
import Link from 'next/link'

<Link href="/services/hot-water-repairs/">Hot water repairs</Link>
```

Rules:

- Internal navigation must remain crawlable.
- Avoid buttons/divs for page navigation.
- Use descriptive anchor text.
- Add breadcrumbs for hierarchical sites.
- Avoid orphan pages.

## Client Components and SEO

Client Components are fine for:

- menus
- filters
- accordions/tabs
- calculators
- forms
- interactive widgets

Avoid using Client Components for:

- primary body content
- critical product/service descriptions
- main internal links
- route metadata
- JSON-LD that must be available in initial HTML

If content is fetched client-side only, crawlers and AI retrieval systems may not see it reliably or quickly.

## Common anti-patterns

- same metadata on every route
- canonical pointing to homepage for all pages
- `noindex` accidentally inherited by public pages
- dynamic route metadata missing/fallback generic
- important content loaded only after client fetch
- JSON-LD injected only after hydration
- sitemap includes noindex/private URLs
- `lastModified` equals build time for all URLs
- OG image uses relative URL
- LCP image lazy-loaded
- internal links implemented as buttons

## Complete Next.js page checklist

| Check | Pass? | Notes |
| --- | --- | --- |
| Route has unique title |  |  |
| Route has unique meta description |  |  |
| Canonical absolute and correct |  |  |
| Robots directive correct |  |  |
| OG/Twitter metadata complete |  |  |
| OG/Twitter images absolute |  |  |
| Main content rendered in initial HTML |  |  |
| One clear H1 |  |  |
| Internal links crawlable |  |  |
| JSON-LD matches visible content |  |  |
| Sitemap includes page only if indexable |  |  |
| Private/search/filter pages excluded |  |  |
| LCP image not lazy-loaded |  |  |
| Images have appropriate ALT |  |  |
| Build passes |  |  |

## Validation commands

Read project scripts first:

```bash
cat package.json
npm run build
npm run lint
```

Inspect rendered output:

- view source / rendered HTML
- check `sitemap.xml`
- check `robots.txt`
- check canonical/meta/JSON-LD per route
- run Lighthouse/PageSpeed where useful
- use Search Console URL Inspection after deploy

## Final rule

Next.js SEO is strong when:

```txt
route metadata + rendered HTML + crawlable links + valid schema + clean sitemap
```

are all correct together.
