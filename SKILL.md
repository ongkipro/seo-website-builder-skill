---
name: seo-website-builder
description: >-
  End-to-end SEO operating system for building, auditing, and improving websites.
  Use for technical SEO, information architecture, metadata, schema/JSON-LD,
  sitemap, robots.txt, canonical/noindex decisions, internal linking, Shopify SEO,
  Astro/static SEO, local business SEO, ecommerce SEO, programmatic SEO, Search
  Console diagnosis, SEO QA, multi-engine algorithm updates, and AI-search readiness.
---

# SEO Website Builder

End-to-end SEO operating system for building, auditing, improving, and maintaining websites across Google, Bing, Yandex, Pinterest, and AI-search surfaces.

## First Rule

Do not guess. Extract available facts from the project/site first. Ask for missing business-critical inputs when needed.

## Evidence Rule

Prefer official search engine/platform documentation and existing project data. Industry sources may guide tactics, but do not claim secret algorithm knowledge.

## Always Read First

1. [Compact Skill References](references/COMPACT_SKILL_REFERENCES.md)
2. [SEO OS Playbook](references/PLAYBOOK.md)

## Then Load by Task

| Task | Read |
| --- | --- |
| Astro/static/Cloudflare site | [Astro SEO Playbook](references/ASTRO_SEO_PLAYBOOK.md) |
| Shopify product/collection/listing/feed | [Shopify SEO Playbook](references/SHOPIFY_SEO_PLAYBOOK.md) |
| Local/service business | [Local Business SEO Playbook](references/LOCAL_BUSINESS_SEO_PLAYBOOK.md) |
| Algorithm/update review | [Search Engine Algorithm Brief](references/SEARCH_ENGINE_ALGORITHM_BRIEF.md), [Source Index](references/SEARCH_ENGINE_SOURCE_INDEX.md), [Algorithm Update Log](references/ALGORITHM_UPDATE_LOG.md) |
| Complete page audit / title-description-schema checklist | [Page Completeness Formula](references/PAGE_COMPLETENESS_FORMULA.md) |
| Audit/build/schema templates | [Output Templates](references/OUTPUT_TEMPLATES.md) |
| Deep routing/reference map | [Reference Manifest](references/REFERENCE_MANIFEST.md) |

## Workflow

1. Classify the task: new build, audit, Astro/static, Shopify, local business, ecommerce, programmatic, schema, algorithm update, or launch QA.
2. Gather inputs: website URL/project path, business model, audience, market/location, conversion goal, stack/CMS, main pages/products, current pain.
3. Inspect before advising:
   - local codebase: routes/pages, metadata/layout, sitemap/robots, schema, build scripts
   - live site: source HTML, robots/sitemap, canonical, schema, mobile CTA, page experience
4. For important indexable pages, apply the Page Completeness Formula: purpose, metadata, canonical/robots, social metadata, headings, images, links, schema, sitemap, and measurement.
5. Produce the output contract.
6. Validate using QA checklist.

## Output Contract

For substantial SEO work, return:

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
Multi-Engine Notes (Google/Bing/Yandex/Pinterest where relevant)
Technical Implementation
Complete Page Formula Checks
QA / Validation Checklist
Measurement Plan
Risk Notes
```

## Hard Stops

Stop and ask/flag if:

- business goal unclear
- page map unclear
- index/canonical decision unclear
- requested content would be fake/misleading
- schema would mark invisible content
- location pages would be copy-paste doorway pages
- bulk Shopify changes requested without pilot approval
- project lacks any measurement plan

## Mode Rules

### Local Business

Use `references/LOCAL_BUSINESS_SEO_PLAYBOOK.md`.

Must produce NAP consistency, Google Business/Profile alignment notes, LocalBusiness/Service/FAQ schema if eligible, service/location page rules, and phone/WhatsApp/contact QA.

### Shopify

Use `references/SHOPIFY_SEO_PLAYBOOK.md`.

Must respect pilot-first workflow, no invented product facts, no fake reviews, kept SKUs unchanged, no supplier/origin junk, image ALT limits, title/meta/handle limits.

### Astro / Static

Use `references/ASTRO_SEO_PLAYBOOK.md`.

Must enforce static-first public pages, content in initial HTML, smallest client islands, per-route metadata/canonical, valid sitemap/robots, and non-lazy LCP image.

### Algorithm Intelligence

Use `references/SEARCH_ENGINE_ALGORITHM_BRIEF.md`, `references/SEARCH_ENGINE_SOURCE_INDEX.md`, and `references/ALGORITHM_UPDATE_LOG.md`.

Must label evidence confidence, prefer official sources, avoid secret-algorithm claims, and update recommendations only when action is justified.

## Promotion / Tests

For validating this skill, see [Test Cases](references/TEST_CASES.md). Keep large original SEO OS exports in `/home/fantastico/Documents/SEO`; load them only when deep research is needed via the manifest.
