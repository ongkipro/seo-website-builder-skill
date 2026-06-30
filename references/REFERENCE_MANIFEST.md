# SEO Reference Manifest

This manifest maps the important files in the `seo-website-builder` skill so agents can load the right reference without reading everything.

## Core entry points

| File | Purpose |
| --- | --- |
| `SKILL.md` | Main skill instructions |
| `COMPACT_SKILL_REFERENCES.md` | Compact default reference for fast use |
| `PLAYBOOK.md` | Daily operational SEO workflow |
| `PAGE_COMPLETENESS_FORMULA.md` | Complete page audit formula: title, description, canonical, robots, headings, images, links, schema, sitemap |
| `OUTPUT_TEMPLATES.md` | Audit/build/schema/metadata/change-log templates |
| `SEARCH_ENGINE_ALGORITHM_BRIEF.md` | Multi-engine algorithm/discovery model |
| `SEARCH_ENGINE_SOURCE_INDEX.md` | Official/trusted source index |
| `ALGORITHM_UPDATE_LOG.md` | Algorithm update log and playbook refresh policy |
| `TEST_CASES.md` | Pre-promotion and regression test scenarios |
| `VALIDATION_REPORT.md` | Documentation validation report |
| `CHANGELOG.md` | Change history |

## Stack / use-case playbooks

| File | Use case |
| --- | --- |
| `ASTRO_SEO_PLAYBOOK.md` | Astro/static/Cloudflare site SEO |
| `NEXTJS_SEO_PLAYBOOK.md` | Next.js frontend/App Router/Pages Router SEO |
| `SHOPIFY_SEO_PLAYBOOK.md` | Shopify product, collection, listing, and feed SEO |
| `LOCAL_BUSINESS_SEO_PLAYBOOK.md` | Local/service business, GBP alignment, NAP, LocalBusiness schema |

## Recommended load profiles

### Fast mode

1. `COMPACT_SKILL_REFERENCES.md`
2. `PLAYBOOK.md`
3. `PAGE_COMPLETENESS_FORMULA.md` when auditing one specific page
4. relevant stack/use-case playbook

### Build mode

1. `PLAYBOOK.md`
2. `PAGE_COMPLETENESS_FORMULA.md`
3. stack/use-case playbook (`ASTRO_SEO_PLAYBOOK.md`, `NEXTJS_SEO_PLAYBOOK.md`, `SHOPIFY_SEO_PLAYBOOK.md`, etc.)
4. `OUTPUT_TEMPLATES.md`

### Audit mode

1. `COMPACT_SKILL_REFERENCES.md`
2. `PLAYBOOK.md`
3. `PAGE_COMPLETENESS_FORMULA.md`
4. relevant stack/use-case playbook
5. `OUTPUT_TEMPLATES.md`

### Algorithm refresh mode

1. `SEARCH_ENGINE_SOURCE_INDEX.md`
2. `ALGORITHM_UPDATE_LOG.md`
3. `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
4. relevant stack/use-case playbook

### Skill authoring / maintenance mode

1. `SKILL.md`
2. `COMPACT_SKILL_REFERENCES.md`
3. `REFERENCE_MANIFEST.md`
4. `TEST_CASES.md`
5. `VALIDATION_REPORT.md`
6. `CHANGELOG.md`

## Deep reference note

The original long-form SEO OS archive is intentionally not bundled into this public skill. This repository includes compact, agent-ready references only.

If a local user has a larger private SEO archive, load it only for deep research tasks and keep the public skill compact.

## Canonical duplicate policy

When a duplicated reference exists, keep one canonical file and replace duplicates with redirect stubs or remove them. Do not ship duplicated reference bodies in the public skill.

## Source governance

- Use official search engine/platform sources for hard rules.
- Use industry sources for tactical context only.
- Label speculative claims clearly.
- Do not claim secret algorithm knowledge.
- Record meaningful updates in `ALGORITHM_UPDATE_LOG.md` and `CHANGELOG.md`.
