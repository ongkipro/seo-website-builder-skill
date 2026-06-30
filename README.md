<div align="center">

# SEO Website Builder Skill

### A multi-engine SEO operating system for AI coding agents

Plan, build, audit, and maintain SEO-ready websites for **Google**, **Bing**, **Yandex**, **Pinterest**, and modern **AI-search / answer surfaces**.

<br />

[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-seo--website--builder-0ea5e9?style=for-the-badge)](./SKILL.md)
[![License](https://img.shields.io/badge/License-MIT-16a34a?style=for-the-badge)](./LICENSE)
[![SEO](https://img.shields.io/badge/Multi--Engine%20SEO-Google%20%7C%20Bing%20%7C%20Yandex%20%7C%20Pinterest-f97316?style=for-the-badge)](#coverage)

[![Astro](https://img.shields.io/badge/Astro-Static%20SEO-ff5d01?style=flat-square&logo=astro&logoColor=white)](#coverage)
[![Shopify](https://img.shields.io/badge/Shopify-Ecommerce%20SEO-7ab55c?style=flat-square&logo=shopify&logoColor=white)](#coverage)
[![Local SEO](https://img.shields.io/badge/Local%20SEO-GBP%20%7C%20NAP%20%7C%20Schema-2563eb?style=flat-square)](#coverage)
[![AI Search](https://img.shields.io/badge/AI%20Search-Answer%20Readiness-7c3aed?style=flat-square)](#coverage)

<br />

**Curated by [Ongki Pro](https://ongki.pro) · [@ongkipro](https://github.com/ongkipro)**

</div>

---

## Overview

`seo-website-builder` is an **Agent Skill** for AI coding agents that need to make SEO decisions while working inside real codebases.

It is not a keyword checklist. It is a structured operating system for:

- auditing existing websites
- planning SEO architecture before development
- generating implementation-ready metadata and schema plans
- handling sitemap, robots, canonical, and noindex decisions
- improving Astro/static, Shopify/ecommerce, and local business websites
- responding to algorithm changes using official or trusted public sources

The goal is simple: help agents produce websites that are **crawlable, indexable, useful, trustworthy, measurable, and commercially meaningful**.

---

## Why this exists

Most AI agents can write meta tags. Fewer can reason through SEO as a system.

This skill gives agents a repeatable framework for decisions like:

- Should this page exist?
- Should this page be indexed?
- What is the canonical target?
- Which schema is eligible and safe?
- What should be in the sitemap?
- Does this Shopify listing need a pilot before batch edits?
- Is this local landing page useful or just a doorway page?
- Does this update require changing the SEO playbook?

---

## Coverage

| Area | What the skill handles |
| --- | --- |
| **Google Search** | crawl/index, canonical, helpful content, structured data, AI Features readiness |
| **Bing / Copilot** | XML sitemap, true `lastmod`, IndexNow, Bing Webmaster Tools |
| **Yandex** | site quality, security, mobile usability, region, Webmaster/Metrica diagnostics |
| **Pinterest** | visual discovery, claimed domain, Pin metadata, creative quality, landing-page match |
| **AI Search** | indexed/snippet-eligible pages, passage clarity, entity clarity, trust, freshness |
| **Astro/static sites** | static-first SEO, metadata, sitemap, robots, schema, Core Web Vitals |
| **Shopify/ecommerce** | product/collection SEO, Product schema, image ALT, listing safety, feed hygiene |
| **Local business** | NAP consistency, GBP alignment, LocalBusiness/Service schema, location-page quality |
| **Programmatic SEO** | page quality gates, duplicate control, crawl budget, pruning, refresh workflows |

---

## What agents produce

For substantial SEO tasks, the skill expects the agent to produce this output contract:

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

---

## Repository structure

```txt
seo-website-builder-skill/
├── SKILL.md
├── LICENSE
├── README.md
└── references/
    ├── COMPACT_SKILL_REFERENCES.md
    ├── PLAYBOOK.md
    ├── ASTRO_SEO_PLAYBOOK.md
    ├── SHOPIFY_SEO_PLAYBOOK.md
    ├── LOCAL_BUSINESS_SEO_PLAYBOOK.md
    ├── SEARCH_ENGINE_ALGORITHM_BRIEF.md
    ├── SEARCH_ENGINE_SOURCE_INDEX.md
    ├── ALGORITHM_UPDATE_LOG.md
    ├── OUTPUT_TEMPLATES.md
    ├── TEST_CASES.md
    ├── REFERENCE_MANIFEST.md
    ├── VALIDATION_REPORT.md
    └── CHANGELOG.md
```

---

## Quick start

Clone the repository:

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
```

Symlink it into an Agent Skills directory:

```bash
mkdir -p ~/.agents/skills
ln -s "$PWD/seo-website-builder-skill" ~/.agents/skills/seo-website-builder
```

For Pi.dev, Claude Code, Codex, Gemini, or other Agent Skills-compatible tools, place or symlink this folder into the skill discovery directory for that tool.

---

## Example prompts

### Audit an Astro website

```txt
Use seo-website-builder to audit this Astro website before launch.
Check metadata, sitemap, robots, canonical, schema, internal links, and Core Web Vitals risks.
```

### Optimise Shopify listings safely

```txt
Use seo-website-builder to optimise these Shopify product listings.
Start with one pilot product, do not invent facts, preserve SKUs, and produce before/after copy.
```

### Build local business SEO setup

```txt
Use seo-website-builder to create LocalBusiness schema, Service schema, metadata patterns, sitemap, robots, and local SEO QA for this service business.
```

### Review an algorithm update

```txt
Use seo-website-builder to review this Google/Bing/Yandex/Pinterest update.
Label evidence confidence, summarise impact, and update the algorithm log only if action is justified.
```

---

## Skill behaviour

The skill is intentionally compact at the top level.

Default load order:

1. `references/COMPACT_SKILL_REFERENCES.md`
2. `references/PLAYBOOK.md`
3. one task-specific reference:
   - `ASTRO_SEO_PLAYBOOK.md`
   - `SHOPIFY_SEO_PLAYBOOK.md`
   - `LOCAL_BUSINESS_SEO_PLAYBOOK.md`
   - `SEARCH_ENGINE_ALGORITHM_BRIEF.md`

This keeps agent context light while still allowing deeper references when needed.

---

## Reference files

| File | Purpose |
| --- | --- |
| `COMPACT_SKILL_REFERENCES.md` | Fast default reference for agents |
| `PLAYBOOK.md` | Daily SEO operating workflow |
| `ASTRO_SEO_PLAYBOOK.md` | Astro/static SEO implementation rules |
| `SHOPIFY_SEO_PLAYBOOK.md` | Shopify product, collection, listing, and feed SEO |
| `LOCAL_BUSINESS_SEO_PLAYBOOK.md` | Local business SEO, NAP, GBP, LocalBusiness schema |
| `SEARCH_ENGINE_ALGORITHM_BRIEF.md` | Multi-engine algorithm/discovery model |
| `SEARCH_ENGINE_SOURCE_INDEX.md` | Official/trusted source index |
| `ALGORITHM_UPDATE_LOG.md` | Algorithm update tracking workflow |
| `OUTPUT_TEMPLATES.md` | Audit, build plan, schema QA, and metadata templates |
| `TEST_CASES.md` | Dry-run scenarios for validating the skill |
| `REFERENCE_MANIFEST.md` | Reference map and load profiles |

---

## Safety and evidence rules

This skill is intentionally conservative.

Agents should:

- prefer official search engine/platform sources
- label speculative claims clearly
- avoid claiming secret algorithm knowledge
- inspect project/site facts before advising
- ask for missing business-critical data
- keep important content crawlable in HTML
- use schema only when it matches visible real content

Agents should not:

- invent business facts, reviews, prices, coordinates, hours, product specs, or credentials
- add schema for invisible or fake content
- index thin doorway/location/facet/search pages without unique value
- fake sitemap `lastmod`
- bulk-edit Shopify listings without a pilot approval step
- treat algorithm volatility as proof without source and diagnosis

---

## Source philosophy

This skill prioritises official or platform-owned documentation, including:

- Google Search Central
- Google ranking systems guide
- Google AI Features and Your Website
- Bing Webmaster Blog / IndexNow
- Yandex Webmaster documentation
- Pinterest Business / Help / Policy documentation

Industry SEO sources can be useful for examples, workflows, and tactical context, but should not be treated as disclosure of secret ranking weights.

---

## Public credentials

**Maintainer:** [Ongki Pro](https://ongki.pro)  
**GitHub:** [@ongkipro](https://github.com/ongkipro)  
**Email:** [get@ongki.pro](mailto:get@ongki.pro)

> Public credentials here mean authorship and contact credentials only. This repository intentionally contains no private tokens, API keys, auth sessions, client secrets, or private customer data.

---

## License

MIT — see [LICENSE](./LICENSE).

---

<div align="center">

**Built for practical SEO implementation, not SEO theatre.**

</div>
