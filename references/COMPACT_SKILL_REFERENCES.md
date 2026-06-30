# Compact Skill References

Purpose: versi ringkas untuk calon skill `seo-website-builder`. File ini dibuat agar skill tidak perlu memuat 100+ dokumen setiap kali dipakai.

Last updated: 2026-06-30

## Default Load Order

1. `COMPACT_SKILL_REFERENCES.md`
2. `PLAYBOOK.md`
3. specific mode file if needed:
   - `ASTRO_SEO_PLAYBOOK.md`
   - `SHOPIFY_SEO_PLAYBOOK.md`
   - `LOCAL_BUSINESS_SEO_PLAYBOOK.md`
   - `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
4. deep modules only when necessary via `REFERENCE_MANIFEST.md`

## Core Operating Principle

SEO is a system, not a checklist.

Every indexable page must earn its place by supporting at least one of:

- search demand
- business conversion
- topical authority
- crawl path/discovery
- trust/entity proof
- user support/objection handling

If a page has no unique value, do not index it.

## Universal Output Contract

Every substantial SEO task should return:

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
QA / Validation Checklist
Measurement Plan
Risk Notes
```

## Mode Routing

| Intent | Primary file | Deep modules |
| --- | --- | --- |
| New website SEO | `PLAYBOOK.md` | 01, 02, 03, 11, 12, 85 |
| Existing audit | `PLAYBOOK.md` | 13, 23, 38, 57, 59, 82, 95 |
| Astro/static | `ASTRO_SEO_PLAYBOOK.md` | 28, 58, 82 |
| Shopify/ecommerce | `SHOPIFY_SEO_PLAYBOOK.md` | 04, 26, 30, 50, 69, 89 |
| Local business | `LOCAL_BUSINESS_SEO_PLAYBOOK.md` | 08, 49, 56 |
| Algorithm update | `SEARCH_ENGINE_ALGORITHM_BRIEF.md` | `SEARCH_ENGINE_SOURCE_INDEX.md`, `ALGORITHM_UPDATE_LOG.md` |
| Complete page audit | `PAGE_COMPLETENESS_FORMULA.md` | 02, 12, 85 |
| Schema | stack playbook | 12, 91 |
| Programmatic SEO | `PLAYBOOK.md` | 10, 42, 57, 59, 71, 72 |

## Hard Rules

- Prefer official sources for hard claims.
- Do not claim secret algorithm knowledge.
- Do not invent facts, reviews, credentials, prices, coordinates, hours, or product specs.
- Do not add schema for invisible content.
- Do not index thin/search/filter/location pages without unique value.
- Do not fake `lastmod` freshness.
- Do not create doorway pages.
- Do not batch-edit Shopify listings without pilot approval.
- Keep important content in crawlable HTML.
- Internal links must use real crawlable `<a href>` links.

## Multi-Engine Baseline

| Engine / Surface | Must handle |
| --- | --- |
| Google | helpful content, indexing, snippets, canonical, structured data, page experience, AI feature eligibility |
| Bing | XML sitemap, true `lastmod`, IndexNow, Bing Webmaster Tools |
| Yandex | quality, security, mobile convenience, site region, Yandex Webmaster/Metrica |
| Pinterest | claimed site, high-quality vertical visuals, Pin title/description, trends, landing-page match |
| AI Search | indexed/snippet-eligible pages, passage clarity, entity clarity, trust, freshness |

## Page Completeness Formula

For every important indexable page, verify:

- clear page purpose and search intent
- unique title, ideally 45–60 characters; warning above ~65 characters
- meta description, ideally 120–160 characters; warning above ~180 characters
- absolute canonical URL
- correct robots directive (`index, follow, max-image-preview:large` for normal indexable pages)
- OG/Twitter metadata for shareable pages
- absolute OG/Twitter image URL
- one clear H1 matching intent
- logical H2/H3 structure
- meaningful ALT on important images
- LCP/hero image not lazy-loaded
- crawlable internal links
- eligible JSON-LD schema matching visible content
- page included in sitemap only if canonical-indexable
- CTA/conversion measurement ready

Use `PAGE_COMPLETENESS_FORMULA.md` for detailed audit rules and examples.

## Technical SEO Minimum

- `robots.txt` exists and does not block critical assets.
- `sitemap.xml` contains only canonical-indexable URLs.
- canonical URLs are absolute and correct.
- index/noindex rules are deliberate.
- 404 returns 404.
- redirects are 301 for permanent moves.
- key pages return 200.
- title/meta are unique on indexable pages.
- schema validates and matches visible content.
- mobile UX and CTA are usable.

## Metadata Rules

- Title: unique, intent-aligned, not spammy; target 45–60 chars when practical.
- Meta description: unique, benefit/trust/intent focused; target 120–160 chars when practical.
- H1: one primary H1 matching page intent.
- OG/Twitter tags: present for shareable pages.
- OG/Twitter image URLs: absolute, crawlable, share-friendly.
- Canonical: self-referential unless duplicate/consolidation is intentional.
- Meta keywords: not used by Google ranking; optional only as internal targeting notes.

## Schema Rules

Use schema only when eligible:

- Organization / LocalBusiness
- WebSite
- BreadcrumbList
- Product / Offer
- Article / BlogPosting
- FAQPage only if FAQ visible
- AggregateRating / Review only if real visible reviews exist
- Service for service pages

Reject schema spam.

## Internal Linking Rules

- Homepage links to primary money/category/service pages.
- Category links to products/subcategories/guides.
- Product links to category, related products, FAQ/trust.
- Blog links to money pages and related content.
- Breadcrumbs reinforce hierarchy.
- Footer links trust/contact/legal pages.

## Stack Rules

### Astro/static

- Static-first for public SEO pages.
- Main content in initial HTML.
- Hydrate smallest possible island only.
- LCP image not lazy-loaded.
- Content collections validate frontmatter.
- Sitemap/robots generated correctly.

### Shopify

- Pilot one product before batch.
- Product title ≤70 chars.
- SEO title ≤60 chars.
- Meta description ≤155 chars.
- Image ALT ≤125 chars.
- Keep SKUs unchanged for kept variants.
- Remove supplier/origin junk.
- Product/Offer/feed data accurate.

### Local business

- NAP consistent.
- GBP aligned.
- LocalBusiness/Service schema valid.
- Phone links use international format.
- Avoid copy-paste location pages.
- Map/route/CTA work on mobile.

## Algorithm Update Workflow

1. Confirm update from official/trusted source.
2. Record in `ALGORITHM_UPDATE_LOG.md`.
3. Identify affected surface.
4. Segment traffic/pages by type and intent.
5. Check technical/indexing before rewriting content.
6. Compare competitors/SERP changes.
7. Update playbooks only when action is justified.

## Promotion Rule

Do not convert into active skill until `TEST_CASES.md` and `PROMOTION_CHECKLIST.md` pass.