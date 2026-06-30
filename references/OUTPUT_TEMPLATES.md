# SEO Output Templates

Template siap pakai untuk audit, build plan, dan implementasi SEO.

## 1. Full SEO Audit Template

```md
# SEO Audit: {{SITE_OR_PROJECT}}

## Executive Summary

- Status:
- Biggest risk:
- Biggest opportunity:
- Priority action:

## Critical Assessment

| Area | Status | Notes |
| --- | --- | --- |
| Crawlability | Pass/Warning/Fail | |
| Indexability | Pass/Warning/Fail | |
| Metadata | Pass/Warning/Fail | |
| Canonical | Pass/Warning/Fail | |
| Sitemap/Robots | Pass/Warning/Fail | |
| Schema | Pass/Warning/Fail | |
| Internal Linking | Pass/Warning/Fail | |
| Content Quality | Pass/Warning/Fail | |
| Performance/CWV | Pass/Warning/Fail | |
| Conversion Path | Pass/Warning/Fail | |

## Search Intent Map

| Query/Topic | Intent | Target Page | Existing? | Action |
| --- | --- | --- | --- | --- |

## Page Type Map

| Page | Type | Business Value | Index Rule | Notes |
| --- | --- | --- | --- | --- |

## Technical Findings

### High Priority

1. ...

### Medium Priority

1. ...

### Low Priority

1. ...

## Schema Plan

| Page Type | Schema | Eligible? | Notes |
| --- | --- | --- | --- |

## Internal Linking Plan

- Homepage →
- Category/service pages →
- Product/detail pages →
- Blog/supporting content →
- Footer/trust pages →

## Fix Plan

| Priority | Task | File/Page | Impact | Effort |
| --- | --- | --- | --- | --- |

## QA Checklist

- [ ] sitemap canonical-only
- [ ] robots correct
- [ ] no accidental noindex
- [ ] unique title/meta
- [ ] canonical correct
- [ ] schema valid
- [ ] internal links crawlable
- [ ] mobile CTA works
- [ ] tracking/Search Console ready

## Measurement Plan

- Search Console queries:
- pages to monitor:
- conversions/events:
- review cadence:
```

## 2. New Website SEO Plan Template

```md
# SEO Build Plan: {{PROJECT}}

## Business Context

- Business model:
- Target market:
- Primary audience:
- Conversion goal:
- Main offer:

## Architecture

```txt
/
/about/
/contact/
/services/
/services/[slug]/
/blog/[slug]/
```

## Page Map

| URL | Page Type | Intent | Index? | Primary CTA |
| --- | --- | --- | --- | --- |

## Metadata Pattern

| Page Type | Title Pattern | Meta Description Pattern |
| --- | --- | --- |

## Schema Plan

| Page Type | Schema |
| --- | --- |

## Internal Linking

| Source | Links To | Purpose |
| --- | --- | --- |

## Content Requirements

| Page Type | Required Sections |
| --- | --- |

## Launch QA

- [ ] build passes
- [ ] sitemap generated
- [ ] robots correct
- [ ] canonical correct
- [ ] schema valid
- [ ] no broken links
- [ ] PageSpeed acceptable
- [ ] Search Console ready
```

## 3. Metadata Pattern Template

```md
# Metadata Pattern

## Homepage

Title:
`{{Brand}} - {{Primary Service/Product}} in {{Location/Market}}`

Description:
`{{USP}}. {{Primary offer}} for {{audience}} in {{market}}. {{Trust signal}}. {{CTA}}.`

## Service Page

Title:
`{{Service}} in {{Location}} | {{Brand}}`

Description:
`Professional {{service}} in {{location}}. {{Benefit}}. {{Trust signal}}. Contact {{brand}} today.`

## Product Page

Title:
`{{Product Name}} - {{Primary Attribute}}`

Description:
`{{Product}} with {{key benefit/spec}}. Ideal for {{use case}}. {{Trust/availability note}}.`

## Blog / Guide

Title:
`{{How to / Guide Topic}} | {{Brand}}`

Description:
`Learn {{topic}} with practical tips for {{audience}}. Covers {{key points}}.`
```

## 4. Schema QA Template

```md
# Schema QA

| URL | Schema Type | Valid? | Matches Visible Content? | Notes |
| --- | --- | --- | --- | --- |

Rules:

- No fake reviews.
- No ratings unless visible.
- FAQ schema only if FAQ visible.
- Product schema needs real price/availability.
- LocalBusiness address/phone must match real business data.
- Breadcrumb schema must match visible/internal hierarchy.
```

## 5. SEO Fix Commit Note Template

```md
# SEO Change Log

Date: {{DATE}}
Project: {{PROJECT}}

## Changed

- ...

## Files touched

- ...

## Validation

- build:
- sitemap:
- robots:
- schema:
- links:

## Follow-up

- ...
```
