# Shopify SEO Playbook

Purpose: SEO implementation and audit rules for Shopify themes, product listings, collections, Liquid templates, and Merchant/feed hygiene.

## Goal

A Shopify store should have:

- unique product pages that support search and conversion
- index-worthy collection pages
- controlled variants/facets
- valid Product/Offer schema
- SEO-friendly image ALT and filenames
- clean Merchant Center/feed data
- strong internal linking from collections, products, and blog content

## Safe workflow for listing edits

For customer-facing or bulk changes, never batch blindly.

1. Scan product titles, `descriptionHtml`, variants, options, SEO fields, tags, category, and media ALT.
2. Choose one pilot product.
3. Produce before/after copy.
4. Ask for approval on style, brand policy, market, and language.
5. Batch only after approval.
6. Use resume-safe scripts/logging.
7. Verify final output.

Hard rule: do not invent product facts. Use only existing data, images, verified specifications, or user-provided input.

## Page types

| Page | Default SEO rule |
| --- | --- |
| Homepage | index; brand + category gateway |
| Product | index if unique and available |
| Collection | index if it has demand and unique copy |
| Blog | index if helpful and supports topical authority |
| Search results | noindex |
| Cart/checkout/account | noindex |
| Thin tag/filter pages | noindex/canonical |
| Sold-out product | keep indexed if demand is high and alternatives are shown |

## Product page checklist

Required:

- clear natural product title
- unique SEO title
- meta description with benefit + intent
- H1 aligned with product title
- product description not copied from supplier
- bullets for benefits, specs, use cases, compatibility
- clear variants
- visible price and availability
- valid review/UGC if present
- related products
- breadcrumbs
- valid Product schema

Suggested listing limits:

| Field | Rule |
| --- | --- |
| Product title | ≤70 chars, natural, no keyword stuffing |
| SEO title | ≤60 chars, keyword-first, no forced store suffix unless requested |
| Meta description | ≤155 chars, benefit + differentiator, no CTA spam |
| Handle | ≤6 keyword words, unique, stable |
| Image ALT | ≤125 chars, descriptive view/feature label |
| Tags | clean taxonomy, no supplier/origin junk |

For catalog cleanup:

- remove country/Ships From variants unless operationally required
- keep SKUs unchanged for kept variants
- relabel code-like options only when verified
- remove customer-facing supplier residue such as `Brand Name: NONE` or origin noise

## Product schema

Minimal example:

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Product name",
  "image": ["https://example.com/product.jpg"],
  "description": "Product description",
  "brand": { "@type": "Brand", "name": "Brand" },
  "offers": {
    "@type": "Offer",
    "priceCurrency": "USD",
    "price": "49.00",
    "availability": "https://schema.org/InStock",
    "url": "https://example.com/products/product-name"
  }
}
```

Add `aggregateRating` only when real reviews are visible on the page.

## Collection page checklist

An index-worthy collection should have:

- clear search demand
- unique intro copy
- enough products
- useful but controlled filters
- internal links to subcollections/guides
- FAQ if it helps intent
- self canonical

Do not index empty or thin collections.

## Image SEO

For each important image:

- ALT describes the product, not keywords stuffed together
- filename is descriptive where practical
- image is compressed appropriately
- dimensions are stable
- hero product image is not lazy-loaded if it is LCP

ALT pattern:

```txt
[Product Title] - [view/angle/feature]
```

View labels:

- front view
- side angle view
- feature close-up view
- lifestyle in-use shot
- size reference view
- packaging view
- material close-up view

Fix generic ALT values like:

- `main product image`
- `product image 1`
- random supplier filenames/codes

## Shopify Liquid technical checks

Check theme templates:

- `theme.liquid` has dynamic title/meta/canonical
- canonical is correct for variants/filters
- JSON-LD is not duplicated excessively
- heading hierarchy is logical
- product availability matches Shopify data
- collection pagination is crawlable
- breadcrumb links use `<a href>`

## Merchant / feed hygiene

Clean and verify:

- product title
- description
- image
- price
- availability
- GTIN/MPN/brand if available
- product category
- variant attributes

## Internal linking

Minimum:

- homepage → top collections
- collection → products + subcollections + guides
- product → collection + related products
- blog → relevant collection/product pages
- footer → policy/trust/contact pages

## Anti-patterns

- duplicate supplier descriptions
- auto-indexing every collection even when thin
- all filter URLs open to indexing
- fake reviews
- rating schema without visible reviews
- keyword-stuffed product titles
- deleting sold-out products without redirect/alternatives
- incorrect canonical handling for variants
- brand names used without permission/policy
- excessive CTA language in meta descriptions
- supplier/origin noise in customer-facing copy
- bulk mutation without pilot, rollback, or log

## QA

Theme/code QA:

```bash
shopify theme check
```

Listing QA target:

- 0 products missing SEO title/meta description
- 0 products missing required category/type fields
- 0 important images missing ALT
- 0 supplier junk in customer-facing copy
- 0 leftover country/Ships From option unless explicitly required
- 0 duplicate handles
- 0 schema ratings without visible reviews

Manual checks:

- view source of product page
- view source of collection page
- Rich Results Test for Product schema
- Search Console coverage
- Merchant Center diagnostics
- PageSpeed for product page

## Final gate

A Shopify store is not SEO-ready until:

- product and collection pages have unique title/meta
- Product schema is valid
- thin collections/facets are noindex/canonical-controlled
- important images have good ALT
- Merchant/feed data is healthy
- internal linking is clear
- cart/checkout/search/account pages are not indexed
