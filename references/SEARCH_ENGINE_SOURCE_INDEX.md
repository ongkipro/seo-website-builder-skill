# Search Engine Source Index

Last updated: 2026-06-30

Use this file to keep SEO recommendations tied to trusted public sources. Prefer official sources first.

## Google Official Sources

### Core Search

- Google Search Essentials  
  https://developers.google.com/search/docs/essentials
- SEO Starter Guide  
  https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- Creating helpful, reliable, people-first content  
  https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- Google guidance about AI-generated content  
  https://developers.google.com/search/docs/fundamentals/using-gen-ai-content
- Google Search ranking systems guide  
  https://developers.google.com/search/docs/appearance/ranking-systems-guide
- Google Search status dashboard / ranking updates  
  https://status.search.google.com/products/rGHU1u87FJnkP6W2GwMi/history
- Google Search Central Blog  
  https://developers.google.com/search/blog

### AI Search Features

- AI Features and Your Website  
  https://developers.google.com/search/docs/appearance/ai-features

Key notes:

- AI Overviews and AI Mode use the same Search fundamentals.
- Eligible pages must be indexed and snippet-eligible.
- No extra technical requirement beyond Search fundamentals.
- Query fan-out can surface diverse supporting links.

### Crawling / Indexing / Technical

- Google crawling docs  
  https://developers.google.com/crawling
- Robots.txt guide  
  https://developers.google.com/search/docs/crawling-indexing/robots/intro
- Robots meta tags  
  https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag
- Block indexing with noindex  
  https://developers.google.com/search/docs/crawling-indexing/block-indexing
- Sitemaps overview  
  https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview
- Canonicalization  
  https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
- Crawlable links  
  https://developers.google.com/search/docs/crawling-indexing/links-crawlable
- URL structure  
  https://developers.google.com/search/docs/crawling-indexing/url-structure
- JavaScript SEO basics  
  https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

### Structured Data

- Structured data intro  
  https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data
- Product structured data  
  https://developers.google.com/search/docs/appearance/structured-data/product
- Merchant listing structured data  
  https://developers.google.com/search/docs/appearance/structured-data/merchant-listing
- LocalBusiness structured data  
  https://developers.google.com/search/docs/appearance/structured-data/local-business
- Breadcrumb structured data  
  https://developers.google.com/search/docs/appearance/structured-data/breadcrumb
- Article structured data  
  https://developers.google.com/search/docs/appearance/structured-data/article
- FAQ / structured data policies as relevant  
  https://developers.google.com/search/docs/appearance/structured-data/sd-policies

## Bing / Microsoft Official Sources

- Bing Webmaster Blog  
  https://blogs.bing.com/webmaster
- Keeping Content Discoverable with Sitemaps in AI Powered Search  
  https://blogs.bing.com/webmaster/July-2025/Keeping-Content-Discoverable-with-Sitemaps-in-AI-Powered-Search
- IndexNow  
  https://www.indexnow.org/
- Bing Webmaster Tools  
  https://www.bing.com/webmasters
- Bing Webmaster Guidelines  
  https://www.bing.com/webmasters/help/webmaster-guidelines-30fba23a

Key notes from Bing 2025 sitemap guidance:

- XML sitemap remains preferred.
- Accurate `lastmod` is important for AI-powered indexing.
- Use ISO 8601 date-time for frequently updated pages.
- Do not fake `lastmod` using sitemap generation time.
- `changefreq` and `priority` are ignored by Bing.
- Submit sitemap in robots.txt and Bing Webmaster Tools.
- Use IndexNow for real-time URL updates.

## Yandex Official Sources

- Yandex Webmaster help  
  https://yandex.com/support/webmaster/en/
- How to improve site ranking in search  
  https://yandex.com/support/webmaster/en/yandex-indexing/rank
- Site indexing  
  https://yandex.com/support/webmaster/en/yandex-indexing/site-indexing
- Indexing recommendations  
  https://yandex.com/support/webmaster/en/recommendations/indexing
- Site structure recommendations  
  https://yandex.com/support/webmaster/en/recommendations/site-structure
- Sitemap  
  https://yandex.com/support/webmaster/en/controlling-robot/sitemap
- Site region  
  https://yandex.com/support/webmaster/en/site-geography/site-region
- Yandex Metrica  
  https://metrika.yandex.com/

Key notes:

- Track quality, security, mobile convenience, usefulness, and search representation.
- Site region matters for relevant regional queries.
- Yandex Webmaster and Metrica are important diagnostics.
- Ranking changes can come from algorithms, database updates, competitors, demand shifts, site changes, anti-spam/anti-fraud updates.

## Pinterest Official / Platform Sources

- Pinterest Business  
  https://business.pinterest.com/
- Pinterest Business: build audience organically  
  https://business.pinterest.com/en-gb/blog/how-to-build-audience-pinterest/
- Pinterest help: claim your website  
  https://help.pinterest.com/en/business/article/claim-your-website
- Pinterest Predicts / trend planning  
  https://business.pinterest.com/pinterest-predicts/
- Pinterest policy / merchant and content rules  
  https://policy.pinterest.com/

Key notes:

- Pinterest is visual discovery plus search.
- Domain claiming improves trust/control.
- High-quality creative, relevance, engagement, consistency, and trends matter.
- Landing pages should match Pin promise.

## Other Engines / Discovery Surfaces To Track Later

### DuckDuckGo

Track:

- Bing index dependence and own crawler behavior
- privacy search behavior
- structured data and site quality indirectly through source indexes

### Apple / Spotlight / Siri / Maps

Track:

- Apple Business Connect
- structured data and app/site metadata
- local/business entity consistency

### Baidu / Naver / regional engines

Only add if target market requires it.

## Source Governance Rules

1. Use official engine/platform docs for hard rules.
2. Use reputable SEO industry sources for tactics/examples only.
3. Record date reviewed.
4. Do not treat correlation studies as algorithm disclosure.
5. When algorithm updates happen, add notes to `ALGORITHM_UPDATE_LOG.md`.
6. Update playbooks only when a pattern is confirmed or strategically useful.
