# Shopify SEO Implementation Playbook

Untuk Shopify theme, product listing, collection, Liquid, dan Merchant SEO. Disusun dari SEO OS + `~/Documents/seo-research-google/shopify-seo-playbook.md`.

## Target

Shopify harus punya:

- product pages yang unik dan conversion-aware
- collection pages yang index-worthy
- variant/facet control
- schema Product/Offer valid
- image ALT dan filename SEO-friendly
- Merchant Center/feed hygiene
- internal linking kuat dari collection, related products, dan blog

## Safe Workflow Untuk Editing Listing

Untuk bulk listing/customer-facing changes, jangan langsung batch besar.

1. Scan produk: title, descriptionHtml, variants, options, SEO fields, tags, category, media ALT.
2. Pilih 1 produk pilot.
3. Buat before/after.
4. Minta approval style dan aturan brand/market.
5. Baru batch dengan script resume-safe.
6. Log produk yang sukses/gagal.
7. Verifikasi hasil akhir.

Hard rule: jangan invent fakta produk. Ambil hanya dari data lama, gambar, spesifikasi valid, atau input user.

## Page Types

| Page | Default SEO Rule |
| --- | --- |
| Homepage | index, brand + category gateway |
| Product | index jika unik dan tersedia |
| Collection | index jika punya demand dan unique copy |
| Blog | index jika helpful dan mendukung topical authority |
| Search results | noindex |
| Cart/checkout/account | noindex |
| Tag/filter tipis | noindex/canonical |
| Sold out product | keep index jika demand tinggi + alternatif |

## Product Page Checklist

Wajib:

- title produk jelas dan natural
- meta title unik
- meta description benefit + intent
- H1 sama/selaras dengan product title
- deskripsi produk tidak copy-paste supplier
- bullets: benefit, spec, use case, compatibility
- variant jelas
- price dan availability jelas
- review/UGC valid jika ada
- related products
- breadcrumbs
- Product schema valid

Listing data limits yang disarankan:

| Field | Rule |
| --- | --- |
| Product title | ≤70 chars, natural, no keyword spam |
| SEO title | ≤60 chars, keyword-first, no forced store suffix unless requested |
| Meta description | ≤155 chars, benefit + differentiator, no CTA spam |
| Handle | ≤6 keyword words, unique, stable |
| Image ALT | ≤125 chars, descriptive view/feature label |
| Tags | clean taxonomy, no junk supplier/origin tags |

For catalog cleanup:

- remove country/Ships From variants unless operationally needed
- keep SKUs unchanged for kept variants
- relabel option values from codes to human-readable names only when verified
- remove `Brand Name: NONE`, origin junk, and supplier residue from customer-facing copy

## Product Schema

Minimal:

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "...",
  "image": ["..."],
  "description": "...",
  "brand": {"@type":"Brand","name":"..."},
  "offers": {
    "@type":"Offer",
    "priceCurrency": "...",
    "price": "...",
    "availability": "https://schema.org/InStock",
    "url": "..."
  }
}
```

Tambahkan `aggregateRating` hanya jika review nyata terlihat di halaman.

## Collection Page Checklist

Collection yang layak index harus punya:

- demand search jelas
- intro copy unik
- produk cukup
- filter berguna tapi terkendali
- internal links ke subcollection/guide
- FAQ jika membantu intent
- canonical sendiri

Jangan index collection kosong/tipis.

## Image SEO

Untuk setiap image penting:

- ALT menjelaskan produk, bukan keyword stuffing
- filename deskriptif bila bisa
- compress WebP/JPG sesuai kebutuhan
- dimensi stabil
- hero product image tidak lazy-load jika LCP

ALT pattern:

```txt
[Product Title] - [view/angle/feature]
```

View label examples:

- front view
- side angle view
- feature close-up view
- lifestyle in-use shot
- size reference view
- packaging view
- material close-up view

Fix generic ALT seperti:

- `main product image`
- `product image 1`
- filename acak/supplier code

## Shopify Liquid Technical Points

Cek theme:

- `theme.liquid` punya dynamic title/meta/canonical
- canonical tidak salah untuk variant/filter
- JSON-LD tidak duplikat berlebihan
- heading hierarchy masuk akal
- product availability sinkron dengan data Shopify
- pagination collection crawlable
- breadcrumb link pakai `<a href>`

## Merchant / Feed Hygiene

Wajib rapikan:

- product title feed
- description
- image
- price
- availability
- GTIN/MPN/brand bila ada
- product category
- variant attributes

## Internal Linking

Minimal:

- homepage → top collections
- collection → product + subcollection + guide
- product → collection + related products
- blog → collection/product terkait
- footer → policy/trust/contact

## Anti-pattern Shopify

- duplikasi deskripsi supplier
- collection semua auto-index walau tipis
- filter URL terbuka semua ke index
- review palsu
- schema rating tanpa review terlihat
- product title spam keyword
- sold-out product langsung dihapus tanpa redirect/alternatif
- canonical semua variant salah arah
- brand names dimasukkan tanpa izin/user policy
- CTA seperti buy/shop/add to cart di meta description secara berlebihan
- origin/supplier noise seperti `Mainland China` tampil di copy
- batch mutation tanpa pilot dan tanpa rollback/log

## QA

Theme/code QA:

```bash
shopify theme check
```

Listing QA target:

- 0 product missing SEO title/meta description
- 0 product missing product category/type when required
- 0 important image missing ALT
- 0 junk supplier text in customer-facing copy
- 0 leftover country/Ships From option unless explicitly needed
- 0 duplicate handles
- 0 schema rating without visible reviews

Manual check:

- view-source product
- view-source collection
- Rich Results Test Product schema
- Search Console coverage
- Merchant Center diagnostics
- PageSpeed product page

## Final Gate

Shopify store belum SEO-ready sampai:

- product/collection punya title/meta unik
- schema Product valid
- collection tipis noindex/canonical
- image ALT bagus
- feed Merchant sehat
- internal linking jelas
- checkout/cart/search tidak index
