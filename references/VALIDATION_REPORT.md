# SEO Skill Validation Report

Date: 2026-06-30
Scope: public `seo-website-builder` Agent Skill repository.

## Files validated

- `SKILL.md`
- `README.md`
- `LICENSE`
- `COMPACT_SKILL_REFERENCES.md`
- `PLAYBOOK.md`
- `PAGE_COMPLETENESS_FORMULA.md`
- `ASTRO_SEO_PLAYBOOK.md`
- `NEXTJS_SEO_PLAYBOOK.md`
- `SHOPIFY_SEO_PLAYBOOK.md`
- `LOCAL_BUSINESS_SEO_PLAYBOOK.md`
- `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
- `SEARCH_ENGINE_SOURCE_INDEX.md`
- `ALGORITHM_UPDATE_LOG.md`
- `OUTPUT_TEMPLATES.md`
- `TEST_CASES.md`
- `REFERENCE_MANIFEST.md`
- `CHANGELOG.md`

## Existing skill patterns integrated

### Local business SEO

Integrated patterns:

- required/optional business info matrix
- local head tag template
- LocalBusiness subtype mapping
- LocalBusiness required/recommended fields
- Service schema
- FAQ schema rules
- validation errors
- phone formatting patterns

Applied to:

- `LOCAL_BUSINESS_SEO_PLAYBOOK.md`
- `SKILL.md`

### Shopify listing SEO

Integrated patterns:

- scan → pilot → approval → batch workflow
- listing limits for title/meta/handle/ALT
- hard rules against invented facts/supplier junk
- variant cleanup rules
- image ALT patterns
- final QA target

Applied to:

- `SHOPIFY_SEO_PLAYBOOK.md`
- `SKILL.md`

### Astro development SEO

Integrated patterns:

- project classification
- static-first rendering strategy
- smallest island principle
- content in initial HTML
- Astro-native SEO defaults

Applied to:

- `ASTRO_SEO_PLAYBOOK.md`
- `SKILL.md`

### Next.js frontend SEO

Integrated patterns:

- App Router Metadata API
- `generateMetadata()` for dynamic routes
- Pages Router `next/head`
- `app/sitemap.ts` and `app/robots.ts`
- SSG/SSR/ISR rendering decisions
- Client Component SEO boundaries
- JSON-LD in rendered HTML
- `next/image` ALT/LCP handling
- crawlable `next/link` navigation

Applied to:

- `NEXTJS_SEO_PLAYBOOK.md`
- `SKILL.md`

## Validation checks

| Check | Status |
| --- | --- |
| `SKILL.md` exists | PASS |
| required frontmatter exists | PASS |
| references folder exists | PASS |
| core references exist | PASS |
| local markdown links | PASS |
| obvious secret/token scan | PASS |
| dry-run test cases | PASS |
| public README | PASS |
| English public docs | PASS |

## Dry-run coverage

The skill has dry-run scenarios for:

- local business company profile
- Astro static website
- Next.js frontend SEO
- Shopify product listing optimisation
- ecommerce category SEO
- existing website SEO audit
- algorithm update review
- Pinterest visual discovery page
- programmatic SEO quality control

## Public safety statement

The public skill repository intentionally contains no private credentials, API keys, auth sessions, client secrets, or private customer data.

## Final verdict

Status: **production-ready public Agent Skill**

The skill is suitable for AI coding agents that support Agent Skills-style workflows or manual skill loading.
