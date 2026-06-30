# Local Business SEO Playbook

Purpose: SEO implementation and audit rules for local businesses, service businesses, schools, clinics, restaurants, physical stores, and organisations serving a defined area.

## Goal

A local business website must help users and search engines understand:

- who the business is
- what services/products it offers
- where it operates
- why it can be trusted
- how to contact it
- whether it is active and real

## Required inputs

Do not guess business data. Extract it from the existing website, Google Business Profile, official documents, or ask the user.

| Required | Optional / recommended |
| --- | --- |
| Business name | legal name / ABN / NIB / NPWP where relevant |
| Primary service/category | opening hours |
| City/suburb/service area | social profile URLs |
| Phone number | price range |
| Website URL | GPS coordinates |
| Business description | logo / OG image |
| Address or service-area model | accepted payment methods |
| Main CTA | founding date |

## Core local ranking model

Based on Google Business guidance, local visibility is strongly related to:

1. relevance — how well the business matches the query
2. distance — proximity to the searcher or target area
3. prominence — reputation, reviews, citations, authority, and entity strength

A website does not replace a Google Business Profile, but it strengthens relevance and prominence.

## Minimum site structure

```txt
/
/about/
/services/
/services/[service-name]/
/service-areas/
/service-areas/[city-or-suburb]/
/testimonials/
/contact/
/blog/ or /guides/
```

For small businesses, do not create hundreds of thin city pages. Create only location pages that have unique value.

## Homepage checklist

Must include:

- clear H1: business + main service + location
- service summary
- service area
- NAP details
- phone/WhatsApp/form CTA
- trust proof: reviews, licenses, experience, case studies, portfolio
- internal links to primary services
- LocalBusiness/Organization schema

## Service page checklist

Create one page per primary service when there is search demand.

Minimum content:

- what the service is
- who it is for
- problem it solves
- process
- price/range if appropriate
- service area
- FAQ
- relevant proof/testimonials
- clear CTA

## Location / service-area pages

A location page is index-worthy only if it has unique value:

- specific area context
- real project/case in that area
- local photos or proof
- local testimonial
- route/location context
- services available in that area

Do not create copy-paste city pages that only swap the city name.

## NAP consistency

Keep consistent across website, Google Business Profile, citations, and social profiles:

- Name
- Address
- Phone
- Website
- Opening hours

Use correct international phone format in schema and `tel:` links.

## Head tags template

```html
<title>{{PAGE_TITLE}} | {{BUSINESS_NAME}}</title>
<meta name="description" content="{{META_DESCRIPTION}}">
<link rel="canonical" href="{{CANONICAL_URL}}">
<meta property="og:type" content="website">
<meta property="og:url" content="{{CANONICAL_URL}}">
<meta property="og:title" content="{{PAGE_TITLE}} | {{BUSINESS_NAME}}">
<meta property="og:description" content="{{META_DESCRIPTION}}">
<meta property="og:image" content="{{OG_IMAGE_URL}}">
<meta name="twitter:card" content="summary_large_image">
```

Optional geo tags if coordinates are accurate:

```html
<meta name="geo.region" content="{{COUNTRY_REGION}}">
<meta name="geo.placename" content="{{CITY}}">
<meta name="geo.position" content="{{LATITUDE}};{{LONGITUDE}}">
<meta name="ICBM" content="{{LATITUDE}}, {{LONGITUDE}}">
```

Title patterns:

| Page | Pattern |
| --- | --- |
| Homepage | `Brand - Primary Service in Location` |
| Service | `Service in Location | Brand` |
| About | `About Brand | Location` |
| Contact | `Contact Brand | Location` |
| Location | `Service in City/Suburb | Brand` |

Meta description patterns:

| Page | Pattern |
| --- | --- |
| Homepage | `[USP]. [Service] in [Location/Area]. [Trust signal]. Call/WhatsApp [phone].` |
| Service | `Professional [service] in [location]. [Benefit]. [Proof/trust]. Get a quote today.` |
| Location | `[Service] for [city/suburb]. [Local proof/coverage]. Contact [brand].` |
| Contact | `Contact [brand] for [service] in [location]. [Hours]. Call or message today.` |

## Schema

Choose the most accurate schema:

- LocalBusiness
- ProfessionalService
- Store
- Restaurant
- MedicalBusiness
- EducationalOrganization
- Organization
- BreadcrumbList
- FAQPage if FAQ is visible
- Service for service pages

Useful subtypes:

| Subtype | Use case |
| --- | --- |
| Plumber | plumbing |
| Electrician | electrical |
| RoofingContractor | roofing |
| HVACBusiness | HVAC/AC |
| AutoRepair | mechanic |
| BeautySalon | salon/beauty |
| Dentist | dental |
| LegalService | lawyer |
| AccountingService | accountant |
| Restaurant | restaurant/cafe |
| Store | retail |
| EducationalOrganization | school/boarding school/training organisation |
| ProfessionalService | generic service |

LocalBusiness minimal example:

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Business Name",
  "url": "https://example.com/",
  "telephone": "+6281234567890",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Street address",
    "addressLocality": "City",
    "addressRegion": "Region",
    "postalCode": "Postal code",
    "addressCountry": "ID"
  }
}
```

## Service schema template

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "{{SERVICE_NAME}}",
  "description": "{{SERVICE_DESCRIPTION}}",
  "provider": { "@id": "{{SITE_URL}}/#organization" },
  "areaServed": { "@type": "City", "name": "{{CITY}}" },
  "serviceType": "{{SERVICE_TYPE}}"
}
```

## FAQ schema rules

Use `FAQPage` only when the questions and answers are visible on the page.

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "{{QUESTION}}",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "{{ANSWER_VISIBLE_ON_PAGE}}"
      }
    }
  ]
}
```

## Phone / region formatting

| Region | Display | Link / Schema |
| --- | --- | --- |
| Indonesia mobile | `0812-3456-7890` | `+6281234567890` |
| Indonesia landline | `(0341) 123456` | `+62341123456` |
| Australia landline | `(02) 4900 1234` | `+61249001234` |
| Australia mobile | `0412 345 678` | `+61412345678` |

For Australian businesses, include ABN as `taxID` when available.

## Google Business Profile alignment

The website should align with GBP:

- same business name
- matching business category
- correct landing page URL
- same phone number
- same address/opening hours
- fresh photos and services
- reviews answered naturally

## Content plan

Strong local content includes:

- primary service pages
- FAQs based on real customer questions
- pricing/process/preparation guides
- local case studies
- before/after examples where relevant
- educational articles that link to service pages

## Internal linking

- homepage → primary services
- service pages → contact + service area pages
- service area pages → relevant services
- blog/guides → money pages
- footer → NAP + contact + location
- breadcrumbs active on hierarchical pages

## Anti-patterns

- copy-paste city pages
- fake address or misleading virtual office
- fake reviews
- schema for reviews not visible on the page
- unclear NAP
- icon-only CTAs without accessible labels
- poor mobile usability
- contact page without address/phone/hours when relevant

## QA

Check:

- NAP consistency
- GBP alignment
- LocalBusiness schema valid
- Service schema valid if used
- FAQ schema only for visible FAQs
- mobile CTA works
- map/route correct
- `tel:` link correct
- WhatsApp link correct
- contact page indexable if important
- privacy/legal page present when forms/tracking are used
- `robots.txt` exists
- `sitemap.xml` contains canonical-indexable URLs only

Common validation errors:

- missing `@context`
- missing stable `@id`
- phone is not international format
- empty `areaServed`
- review/rating schema without visible reviews
- business address differs from GBP without a clear reason

## Final gate

A local site is not SEO-ready until:

- homepage explains service + location within 5 seconds
- every primary service has a clear landing page
- NAP is consistent
- GBP is aligned
- schema is valid
- trust proof is real
- mobile CTA is easy to use
- there are no doorway location pages
