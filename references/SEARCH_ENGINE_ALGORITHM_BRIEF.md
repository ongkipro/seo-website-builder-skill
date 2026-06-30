# Search Engine Algorithm Brief

Last reviewed: 2026-06-30
Scope: Google, Bing, Yandex, Pinterest, plus cross-engine discovery surfaces.

This document is a practical, evidence-first brief. It does **not** claim secret algorithm knowledge. It converts official guidance and trusted public signals into operational SEO rules.

## Executive Summary

Modern SEO is no longer only “rank page for keyword”. It is multi-surface discoverability:

```txt
Crawlable
-> Indexable
-> Entity-understandable
-> Intent-matched
-> Helpful/trustworthy
-> Fresh when needed
-> Visually/media-ready
-> AI-answer eligible
-> Conversion-measurable
```

The strongest durable pattern across engines:

1. clean technical access
2. accurate sitemap + lastmod
3. unique helpful content
4. clear information architecture
5. structured data matching visible content
6. strong internal linking
7. trust/reputation signals
8. fast mobile experience
9. freshness for pages where freshness matters
10. no spam/manipulative behavior

## Evidence Confidence Labels

| Label | Meaning |
| --- | --- |
| Official | Source directly from search engine/platform documentation/blog |
| Strong public evidence | Repeatedly observed by reputable SEO industry sources |
| Speculative / monitor | Plausible but not confirmed; track only, do not hard-code |

## Google Search: Current Working Model

### Official ranking systems and implications

Google states its ranking systems use many factors and signals at page and site level. Notable systems include:

- BERT / neural matching / RankBrain for language and intent understanding
- passage ranking for section-level relevance
- link analysis and PageRank for link graph understanding
- freshness systems for query-deserves-freshness cases
- original content systems
- reliable information systems
- reviews system
- site diversity system
- spam detection systems including SpamBrain
- deduplication systems

Operational rules:

- Do not over-optimise only exact keywords; cover concepts, entities, and user intent.
- Make each page uniquely useful; duplicate/similar pages may be deduplicated.
- Use canonical rules intentionally.
- Build topical depth but avoid thin programmatic pages.
- Treat helpful content as part of core ranking, not a separate trick.
- Reviews/comparison content must show real analysis, evidence, and first-hand insight.

### Google AI Features / AI Overviews / AI Mode

Google says AI Overviews and AI Mode rely on the same foundational Search eligibility:

- page must be indexed
- page must be eligible for snippets
- no extra technical requirement beyond Search fundamentals
- content should be crawlable, internally linked, textually available, useful, and supported by high-quality media
- structured data must match visible content
- Merchant Center and Business Profile data should be current where relevant

Google AI features may use query fan-out: multiple related searches across subtopics and data sources.

Operational rules:

- Build pages that answer subquestions, not just one keyword.
- Add clear sections and passage-level headings.
- Include concise definitions, comparison tables, FAQs, and evidence where useful.
- Keep important content in HTML text.
- Use image/video support for visual topics.
- Track performance in Search Console Web search type; AI features are folded into Search Console reporting.

### Google spam/current risk notes

Known risk themes:

- scaled low-value content
- expired domain abuse
- site reputation abuse
- misleading UX/spam behavior
- back-button hijacking and malicious practices
- fake reviews / fake authority
- schema abuse

Operational rule: if a tactic exists only to manipulate ranking and not help users, reject it.

## Bing / Microsoft Search / Copilot

Bing has emphasised discoverability for AI-powered search and Copilot-era retrieval.

Current high-confidence Bing themes:

- XML sitemaps remain foundational.
- `lastmod` matters when accurate.
- ISO 8601 timestamp is recommended for lastmod.
- Do not set lastmod to sitemap generation time unless page content changed.
- `changefreq` and `priority` are ignored by Bing.
- IndexNow is valuable for real-time URL update notification.
- Sitemap in robots.txt + Bing Webmaster Tools submission improves discovery coverage.

Operational rules:

- Generate XML sitemap with only canonical-indexable URLs.
- Set true page modification time in `lastmod`.
- Use full date-time ISO 8601 for frequently updated sites.
- Add sitemap URL to robots.txt.
- Submit sitemap in Bing Webmaster Tools.
- Use IndexNow for add/update/delete events, especially ecommerce/news/programmatic sites.

## Yandex

Yandex official webmaster guidance emphasises:

- site quality
- security and violations
- convenience / mobile compatibility
- site region
- usefulness and user behavior diagnostics via Yandex Metrica
- correct page status and index inclusion
- monitoring important pages
- ranking fluctuations from algorithm updates, database updates, competitor changes, user demand, URL/content/site changes, anti-spam/anti-fraud updates

Operational rules:

- If Yandex matters, set site region in Yandex Webmaster.
- Monitor security and violations.
- Use Yandex Metrica to find weak pages and behavior problems.
- Track important URLs.
- Treat traffic drops as a multi-factor diagnosis: demand, competitors, index status, security, content, URL changes.
- Fix duplicate pages and migration/redirect issues carefully.

## Pinterest Search / Discovery

Pinterest is both search engine and visual discovery platform. Official/public Pinterest business guidance emphasises:

- relevance to query/interests
- image/creative quality
- audience engagement
- consistency of publishing
- claimed website/domain trust
- fresh, useful, inspirational content
- descriptive titles/descriptions
- trend alignment

Operational rules:

- Claim website/domain.
- Use high-quality vertical images.
- Use descriptive Pin titles and descriptions.
- Align with seasonal/trend planning.
- Create fresh Pins for key evergreen pages.
- Use product pins/catalogs where relevant.
- Ensure landing page matches Pin promise.
- Optimise images for visual search and saveability, not just web search.

## Cross-Engine Ranking/Discovery Factors

| Factor | Google | Bing | Yandex | Pinterest | Notes |
| --- | --- | --- | --- | --- | --- |
| Crawlability | Critical | Critical | Critical | Medium | foundational |
| XML sitemap | Important | Very important | Important | Low/indirect | Bing emphasizes lastmod strongly |
| Accurate lastmod | Useful | Very important | Useful | N/A | do not fake timestamps |
| Internal links | Critical | Critical | Important | Low | discovery + context |
| Helpful content | Critical | Critical | Critical | Important | platform-specific form differs |
| Structured data | Important | Important | Useful | Product/catalog dependent | must match visible content |
| Mobile UX | Important | Important | Important | Important | especially local/Pinterest |
| Page speed/CWV | Important | Important | Useful | Landing-page quality | not a magic bullet |
| Links/authority | Important | Important | Important | Domain trust/engagement | avoid link spam |
| Freshness | Query-dependent | Strong for AI/indexing | Query/demand dependent | Trend-driven | strongest where intent changes |
| User behavior | Indirect/complex | likely helpful | explicitly useful in Metrica guidance | engagement core | don't fake engagement |
| Entity/trust | Important | Important | Important | domain/account trust | local/business/profile data matter |
| Visual quality | Google Images/Discover | Images/search | useful | Critical | Pinterest is visual-first |

## Multi-Surface SEO Rules

### For every website

- Keep important content crawlable in HTML.
- Maintain sitemap and robots.
- Use canonical and noindex deliberately.
- Avoid duplicated/thin pages.
- Make internal links crawlable `<a href>`.
- Add structured data only for visible real content.
- Track search engines separately where relevant.

### For ecommerce

- Product schema + Merchant data must be accurate.
- Availability/price must match page/feed.
- Handle out-of-stock with alternatives.
- Use IndexNow/Bing for frequently changing catalog.
- Use image ALT and clean filenames.
- Avoid supplier duplicate descriptions.

### For local business

- Keep Business Profile/GBP aligned.
- Keep NAP consistent.
- Use LocalBusiness/Service schema.
- Avoid fake location doorway pages.
- Use Yandex/Bing local equivalents if those markets matter.

### For content/affiliate/review sites

- Show first-hand experience.
- Add original photos, testing, comparisons, methodology.
- Do not publish scaled generic content.
- Update review content when product facts change.
- Disclose affiliate/commercial relationships.

### For Pinterest-led traffic

- Create visual assets intentionally.
- Make landing page match Pin promise.
- Use seasonal planning and trend calendars.
- Product/collection pages should have pinnable images.

## What Not To Do

- Do not chase one search engine at the expense of user value.
- Do not fake freshness via lastmod.
- Do not mass-produce location/facet/tag pages without unique value.
- Do not add schema for invisible/fake content.
- Do not use AI content without editing, fact checking, and adding unique value.
- Do not use misleading UX such as back-button hijacking.
- Do not treat traffic drops as purely “algorithm update” without checking demand, competitors, index, security, and site changes.

## Operational Algorithm Response Framework

When an algorithm update happens:

1. Confirm source: official dashboard/blog first.
2. Identify affected surfaces: web, local, images, shopping, Discover, AI features.
3. Compare Search Console by page type and query intent.
4. Segment pages: winners, losers, unchanged.
5. Check technical/indexing before content rewrites.
6. Check SERP changes and competitor changes.
7. Update playbooks only when evidence is strong.
8. Record update in `ALGORITHM_UPDATE_LOG.md`.

## Current Practical Priority

If building or improving sites now, prioritise:

1. clean IA and URL structure
2. unique page purpose
3. helpful, experience-backed content
4. accurate schema/feed/business data
5. sitemap with true lastmod
6. IndexNow for frequently changing catalogs/content
7. mobile performance and UX
8. visual assets for image/Pinterest discovery
9. Search Console + Bing Webmaster + platform analytics
10. ongoing pruning/refresh workflow
