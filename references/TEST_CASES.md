# SEO Skill Test Cases

Purpose: validate the SEO documentation pack before converting it into an active skill.

Last updated: 2026-06-30

## How To Use

For each test:

1. Load `COMPACT_SKILL_REFERENCES.md`.
2. Load relevant playbook.
3. Produce the expected output.
4. Check pass/fail criteria.
5. Record result in this file or separate test log.

## Test 1 — Local Business Company Profile

### Scenario

A local service business needs SEO setup for a new website.

### Inputs

- business name
- service category
- city/service area
- phone
- website URL
- business description
- opening hours optional
- coordinates optional

### Expected Output

- Critical Assessment
- missing input list
- page map
- local search intent map
- title/meta patterns
- LocalBusiness schema plan
- Service schema plan
- sitemap/robots plan
- NAP/GBP alignment checklist
- mobile CTA QA

### Pass Criteria

- Does not invent address/hours/reviews.
- Uses international phone format for schema/tel links.
- Avoids doorway location pages.
- Schema matches visible content.

## Test 2 — Astro Static Company Website

### Scenario

An Astro company profile site needs technical SEO QA before launch.

### Inputs

- project path
- domain
- page list
- stack scripts

### Expected Output

- route/page map
- metadata coverage checklist
- sitemap/robots check
- canonical rules
- schema plan
- content-in-HTML check
- performance/CWV notes
- build/QA commands

### Pass Criteria

- Recommends static-first pages.
- Does not require SSR unless needed.
- Flags lazy-loaded LCP image.
- Checks sitemap canonical-only.
- Checks noindex pages excluded from sitemap.

## Test 3 — Shopify Product Listing Optimisation

### Scenario

A Shopify store has weak product listings and missing SEO fields.

### Inputs

- store domain
- sample product data
- product title/description/variants/images
- market/language/brand policy

### Expected Output

- product audit
- pilot product before/after
- title/meta/handle proposal
- description improvement
- image ALT proposal
- variant cleanup notes
- collection/category suggestions
- batch safety plan

### Pass Criteria

- Requires pilot approval before batch.
- Does not invent product facts.
- Keeps SKUs unchanged.
- Does not insert supplier/origin junk.
- Meta/title/ALT limits respected.

## Test 4 — Ecommerce Category SEO

### Scenario

An ecommerce category page has products but thin content and filter duplication risk.

### Inputs

- category URL/name
- product count
- filters/facets
- search intent
- competitors optional

### Expected Output

- category intent analysis
- index/canonical rules
- intro/FAQ/content requirements
- internal links
- facet noindex/canonical rules
- Product/ItemList/Breadcrumb schema notes
- measurement plan

### Pass Criteria

- Does not index all facets blindly.
- Separates collection pages from search/filter pages.
- Requires unique category value.

## Test 5 — Existing Website SEO Audit

### Scenario

A website has traffic drop and indexing issues.

### Inputs

- URL or project path
- Search Console symptoms if available
- date range
- recent changes

### Expected Output

- technical/indexing diagnosis
- traffic segmentation plan
- content quality review
- canonical/duplicate analysis
- sitemap/robots analysis
- algorithm update check
- prioritized fix plan

### Pass Criteria

- Does not blame algorithm update without evidence.
- Checks technical/indexing first.
- Separates demand changes, competitor changes, site changes, and algorithm changes.

## Test 6 — Algorithm Update Review

### Scenario

A new Google/Bing/Yandex/Pinterest update appears and the playbook may need refreshing.

### Inputs

- official update URL
- affected platform/surface
- date
- summary

### Expected Output

- source confidence label
- affected surfaces
- likely impact
- action required
- files to update
- monitoring plan
- entry for `ALGORITHM_UPDATE_LOG.md`

### Pass Criteria

- Uses official source when available.
- Labels speculation clearly.
- Does not update playbooks unless action is justified.

## Test 7 — Pinterest Visual Discovery Page

### Scenario

A product or content page should be optimised for Pinterest discovery.

### Inputs

- landing page URL
- target audience
- image assets
- seasonal/trend angle
- product/content description

### Expected Output

- visual asset checklist
- Pin title/description patterns
- landing-page match QA
- claimed website check
- product/catalog notes if ecommerce
- measurement plan via Pinterest analytics

### Pass Criteria

- Does not treat Pinterest like normal Google-only SEO.
- Requires high-quality vertical visuals.
- Ensures landing page matches Pin promise.

## Test 8 — Programmatic SEO Quality Control

### Scenario

A site wants to generate many city/product/tag pages.

### Inputs

- page pattern
- data source
- unique data fields
- target intent
- index goal

### Expected Output

- template quality criteria
- unique value requirements
- index/noindex matrix
- duplicate/canonical plan
- internal linking plan
- crawl budget risks
- pruning/refresh plan

### Pass Criteria

- Rejects thin scaled pages.
- Requires unique facts/value per page.
- Includes noindex/canonical for weak variants.

## Test Result Template

```md
## YYYY-MM-DD — Test Name

Result: PASS / PARTIAL / FAIL

Files loaded:
- ...

Output quality notes:
- ...

Issues found:
- ...

Fixes needed:
- ...
```

## Conversion Gate

The pack is ready to become an active skill only after:

- at least 3 test cases pass
- one test covers local business
- one test covers Astro or Shopify
- one test covers audit or algorithm update review
- no critical ambiguity remains in routing/output contract
