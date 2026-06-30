<div align="center">

# SEO Website Builder Skill

### A multi-engine SEO operating system for AI coding agents

Plan, build, audit, and maintain SEO-ready websites for **Google**, **Bing**, **Yandex**, **Pinterest**, and modern **AI-search / answer surfaces**.

<br />

[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-seo--website--builder-0ea5e9?style=for-the-badge)](./SKILL.md)
[![License](https://img.shields.io/badge/License-MIT-16a34a?style=for-the-badge)](./LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-22c55e?style=for-the-badge)](#validation-status)

<br />

[![Google](https://img.shields.io/badge/Google%20Search-4285F4?style=flat-square&logo=google&logoColor=white)](#search-engines--discovery-surfaces)
[![Bing](https://img.shields.io/badge/Bing-008373?style=flat-square&logo=microsoftbing&logoColor=white)](#search-engines--discovery-surfaces)
[![Yandex](https://img.shields.io/badge/Yandex-FF0000?style=flat-square&logo=yandex&logoColor=white)](#search-engines--discovery-surfaces)
[![Pinterest](https://img.shields.io/badge/Pinterest-BD081C?style=flat-square&logo=pinterest&logoColor=white)](#search-engines--discovery-surfaces)
[![Shopify](https://img.shields.io/badge/Shopify-7AB55C?style=flat-square&logo=shopify&logoColor=white)](#website-platforms)
[![Astro](https://img.shields.io/badge/Astro-FF5D01?style=flat-square&logo=astro&logoColor=white)](#website-platforms)

<br />

[![Claude](https://img.shields.io/badge/Claude%20Code-Compatible-111827?style=flat-square)](#compatible-ai-agents)
[![Codex](https://img.shields.io/badge/OpenAI%20Codex-Compatible-111827?style=flat-square&logo=openai&logoColor=white)](#compatible-ai-agents)
[![Gemini](https://img.shields.io/badge/Gemini%20CLI-Compatible-4285F4?style=flat-square&logo=googlegemini&logoColor=white)](#compatible-ai-agents)
[![Pi.dev](https://img.shields.io/badge/Pi.dev-Compatible-f97316?style=flat-square)](#compatible-ai-agents)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Compatible-7c3aed?style=flat-square)](#installation)

<br />

**Curated by [Ongki Pro](https://ongki.pro) · [@ongkipro](https://github.com/ongkipro)**

</div>

---

## Table of contents

- [Overview](#overview)
- [Why this exists](#why-this-exists)
- [Compatible AI agents](#compatible-ai-agents)
- [Coverage](#coverage)
- [Inputs and outputs](#inputs-and-outputs)
- [How the skill works](#how-the-skill-works)
- [Installation](#installation)
- [Example prompts](#example-prompts)
- [Repository structure](#repository-structure)
- [Safety and evidence rules](#safety-and-evidence-rules)
- [Validation status](#validation-status)
- [Public credentials](#public-credentials)

---

## Overview

`seo-website-builder` is an **Agent Skill** for AI coding agents that need to make SEO decisions while working inside real codebases.

It is not a keyword checklist. It is a structured SEO operating system for:

- auditing existing websites
- planning SEO architecture before development
- generating metadata and schema plans
- handling sitemap, robots, canonical, and noindex decisions
- improving Astro/static, Shopify/ecommerce, and local business websites
- controlling programmatic SEO quality
- reviewing algorithm updates from official or trusted sources

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
- Does this algorithm update require changing the SEO playbook?

---

## Compatible AI agents

This skill follows the **Agent Skills** directory pattern: a folder containing `SKILL.md` plus optional references.

It can be used by any agent/runtime that supports Agent Skills-style loading or custom skill directories.

| Agent / CLI | Compatibility | Suggested install path |
| --- | --- | --- |
| **Pi.dev** | Native skill directory support | `~/.pi/agent/skills/seo-website-builder` |
| **Claude Code** | Compatible via skills folder | `~/.claude/skills/seo-website-builder` |
| **OpenAI Codex CLI** | Compatible via skills folder | `~/.codex/skills/seo-website-builder` |
| **Gemini CLI** | Compatible via skills folder | `~/.gemini/skills/seo-website-builder` |
| **Agents / Agent Skills compatible tools** | Compatible | `~/.agents/skills/seo-website-builder` |
| **Other AI coding agents** | Manual import/reference | Copy folder or reference `SKILL.md` |

If your tool does not auto-discover skills, you can still point the agent to `SKILL.md` and the `references/` folder manually.

---

## Coverage

### Search engines & discovery surfaces

| Surface | What the skill handles |
| --- | --- |
| **Google Search** | crawl/index, canonical, helpful content, structured data, Google AI Features readiness |
| **Bing / Copilot** | XML sitemap, true `lastmod`, IndexNow, Bing Webmaster Tools |
| **Yandex** | site quality, security, mobile usability, regional targeting, Yandex Webmaster/Metrica diagnostics |
| **Pinterest** | visual discovery, claimed domain, Pin metadata, creative quality, landing-page match |
| **AI Search / answer engines** | indexed/snippet-eligible pages, passage clarity, entity clarity, trust, freshness |

### Website platforms

| Platform / site type | What the skill handles |
| --- | --- |
| **Astro/static sites** | static-first SEO, metadata, sitemap, robots, schema, Core Web Vitals |
| **Shopify/ecommerce** | product/collection SEO, Product schema, image ALT, listing safety, feed hygiene |
| **Local business** | NAP consistency, GBP alignment, LocalBusiness/Service schema, location-page quality |
| **Programmatic SEO** | page quality gates, duplicate control, crawl budget, pruning, refresh workflows |
| **Content/affiliate/review sites** | helpful content, original value, disclosure, internal linking, update workflows |

---

## Inputs and outputs

### Typical inputs

The agent may ask for or inspect:

| Input | Examples |
| --- | --- |
| Website/project | URL, local project path, framework/CMS |
| Business context | business model, target audience, location/market |
| Conversion goal | sales, leads, calls, bookings, signups, traffic, authority |
| Page inventory | homepage, services, products, collections, blog, location pages |
| Existing data | title/meta, sitemap, robots, schema, Search Console notes |
| Platform data | Shopify products, Astro routes, local business NAP, GBP details |
| Update context | official algorithm update URL, affected search surface, date |

The skill explicitly tells agents **not to invent** facts such as business addresses, reviews, prices, opening hours, coordinates, product specs, or credentials.

### Standard output contract

For substantial SEO work, agents should produce:

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

### Example output shape

```md
## Critical Assessment
- Main issue:
- Biggest SEO risk:
- Highest-impact opportunity:

## Index + Canonical Rules
| Page type | Index rule | Canonical rule | Notes |
| --- | --- | --- | --- |

## Schema Plan
| Page type | Schema | Eligible? | Notes |
| --- | --- | --- | --- |

## QA Checklist
- [ ] sitemap contains canonical-indexable URLs only
- [ ] robots.txt does not block important assets
- [ ] schema matches visible content
- [ ] title/meta are unique
- [ ] key CTAs work on mobile
```

---

## How the skill works

The skill is intentionally compact at the top level and uses references progressively.

```txt
User request
   ↓
Load SKILL.md
   ↓
Read COMPACT_SKILL_REFERENCES.md
   ↓
Classify task mode
   ↓
Load one specific playbook
   ↓
Inspect project/site facts
   ↓
Produce structured SEO output
   ↓
Validate with QA checklist
```

### Default load order

1. `references/COMPACT_SKILL_REFERENCES.md`
2. `references/PLAYBOOK.md`
3. one task-specific reference:
   - `ASTRO_SEO_PLAYBOOK.md`
   - `SHOPIFY_SEO_PLAYBOOK.md`
   - `LOCAL_BUSINESS_SEO_PLAYBOOK.md`
   - `SEARCH_ENGINE_ALGORITHM_BRIEF.md`

This keeps agent context light while still allowing deeper references when needed.

---

## Installation

### Option 1 — Generic Agent Skills directory

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.agents/skills
ln -s "$PWD/seo-website-builder-skill" ~/.agents/skills/seo-website-builder
```

### Option 2 — Pi.dev

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.pi/agent/skills
ln -s "$PWD/seo-website-builder-skill" ~/.pi/agent/skills/seo-website-builder
```

### Option 3 — Claude Code

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.claude/skills
ln -s "$PWD/seo-website-builder-skill" ~/.claude/skills/seo-website-builder
```

### Option 4 — OpenAI Codex CLI

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.codex/skills
ln -s "$PWD/seo-website-builder-skill" ~/.codex/skills/seo-website-builder
```

### Option 5 — Gemini CLI

```bash
git clone https://github.com/ongkipro/seo-website-builder-skill.git
mkdir -p ~/.gemini/skills
ln -s "$PWD/seo-website-builder-skill" ~/.gemini/skills/seo-website-builder
```

> If your agent does not auto-load skills, manually provide the path to `SKILL.md` and the `references/` folder.

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

### Plan programmatic SEO safely

```txt
Use seo-website-builder to review this programmatic SEO plan.
Reject thin pages, define index/noindex rules, canonical rules, internal links, and pruning criteria.
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
| `VALIDATION_REPORT.md` | Documentation validation report |
| `CHANGELOG.md` | Change history |

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

## Validation status

This repository was validated before publication:

| Check | Status |
| --- | --- |
| `SKILL.md` present | Passed |
| References present | Passed |
| Local markdown links | Passed |
| Secret/token scan | Passed |
| Dry-run SEO test cases | Passed |
| Public README | Passed |

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
