<div align="center">

# SEO Website Builder Skill

**A multi-engine SEO operating system for AI coding agents.**

Build, audit, and improve websites for **Google**, **Bing**, **Yandex**, **Pinterest**, and modern **AI-search / answer surfaces**.

[![Skill](https://img.shields.io/badge/Agent%20Skill-seo--website--builder-0ea5e9?style=flat-square)](./SKILL.md)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](./LICENSE)
[![SEO](https://img.shields.io/badge/SEO-Google_|_Bing_|_Yandex_|_Pinterest-f97316?style=flat-square)](#what-it-covers)
[![Maintainer](https://img.shields.io/badge/Maintainer-Ongki%20Pro-111827?style=flat-square)](https://ongki.pro)

*Curated by [Ongki Pro](https://ongki.pro) · [@ongkipro](https://github.com/ongkipro)*

</div>

---

## What this is

`seo-website-builder` is an Agent Skill for AI coding agents that need to plan, build, audit, or maintain SEO-ready websites.

It is designed as a practical SEO operating system, not a bundle of random tips.

The skill helps agents produce:

- technical SEO audits
- website SEO architecture
- metadata patterns
- schema / JSON-LD plans
- sitemap and robots rules
- canonical / noindex decisions
- internal linking strategy
- Shopify SEO recommendations
- Astro/static SEO recommendations
- local business SEO setup
- ecommerce/programmatic SEO quality controls
- algorithm update review workflow

## What it covers

| Area | Coverage |
| --- | --- |
| Google Search | crawl/index, canonical, helpful content, structured data, AI Features readiness |
| Bing / Copilot | XML sitemap, true `lastmod`, IndexNow, Bing Webmaster Tools |
| Yandex | site quality, security, mobile usability, region, Webmaster/Metrica diagnostics |
| Pinterest | visual discovery, claimed domain, Pin metadata, creative quality, landing-page match |
| AI Search | indexed/snippet-eligible pages, passage clarity, entity clarity, trust, freshness |
| Astro/static | static-first SEO, metadata, sitemap, robots, schema, Core Web Vitals |
| Shopify/ecommerce | product/collection SEO, Product schema, image ALT, listing safety, feed hygiene |
| Local business | NAP, GBP alignment, LocalBusiness/Service schema, location-page quality |

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

## How to use

Copy this folder into your Agent Skills directory, for example:

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.agents/skills
ln -s "$PWD/seo-website-builder-skill" ~/.agents/skills/seo-website-builder
```

For Pi.dev, Claude Code, Codex, Gemini, or other Agent Skills-compatible tools, place or symlink the folder where your tool discovers skills.

Then ask your agent for tasks like:

```txt
Use seo-website-builder to audit this Astro website before launch.
```

```txt
Use seo-website-builder to optimise this Shopify product listing safely.
```

```txt
Use seo-website-builder to create LocalBusiness schema, sitemap, robots, and metadata for this service business.
```

## Skill behaviour

The skill is intentionally compact at the top level.

Default load order:

1. `references/COMPACT_SKILL_REFERENCES.md`
2. `references/PLAYBOOK.md`
3. one task-specific playbook, such as Astro, Shopify, Local Business, or Algorithm Intelligence

This keeps agent context light while still allowing deep references when needed.

## Output contract

For substantial SEO work, the skill expects agents to produce:

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

## Safety and evidence rules

This skill is intentionally conservative:

- do not claim secret algorithm knowledge
- prefer official search engine/platform sources
- label speculative claims clearly
- do not invent business facts, reviews, prices, coordinates, product specs, or credentials
- do not add schema for invisible/fake content
- do not index thin doorway/location/facet pages
- do not fake sitemap `lastmod`
- do not bulk-edit Shopify listings without pilot approval

## Source philosophy

The skill prioritises official or platform-owned documentation, including:

- Google Search Central
- Google ranking systems guide
- Google AI Features and Your Website
- Bing Webmaster Blog / IndexNow
- Yandex Webmaster docs
- Pinterest Business / Help / Policy docs

Industry SEO sources may be useful for examples and tactics, but not as claims of secret ranking weights.

## Public credentials

**Maintainer:** [Ongki Pro](https://ongki.pro)  
**GitHub:** [@ongkipro](https://github.com/ongkipro)  
**Email:** [get@ongki.pro](mailto:get@ongki.pro)

> Public credentials here mean authorship/contact credentials only. This repository intentionally contains no private tokens, API keys, sessions, or client secrets.

## License

MIT — see [LICENSE](./LICENSE).

---

<div align="center">

**Built for practical SEO implementation, not SEO theatre.**

</div>
