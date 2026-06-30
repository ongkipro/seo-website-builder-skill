# Astro SEO Implementation Playbook

Untuk project Astro/static/Cloudflare site. Disusun dari SEO OS + referensi Google-first di `~/Documents/seo-research-google/astro-static-seo-playbook.md`.

## Target

Astro harus menghasilkan halaman yang:

- konten utama sudah ada di HTML awal
- metadata unik per halaman
- sitemap canonical-only
- robots benar
- Core Web Vitals ringan
- schema valid dan sesuai konten terlihat

## Project Classification

Sebelum implementasi, klasifikasikan project:

| Lane | Pattern |
| --- | --- |
| Content site | static pages, blog, docs, company profile |
| Hybrid site | mostly static + forms/API/auth/dashboard kecil |
| App-like site | banyak state/dynamic UI; Astro mungkin bukan pilihan utama |

SEO default: pilih static HTML dulu. Tambahkan server/API/islands hanya jika benar-benar perlu.

## Rendering Strategy

Urutan default:

1. static generation untuk public SEO pages
2. selective server/API routes untuk form atau data dinamis
3. framework islands hanya untuk interaksi kecil
4. full server rendering hanya jika halaman butuh request-time data

Rules:

- jangan jadikan semua route SSR hanya karena ada satu form
- jangan render konten utama via client JS
- hydrate hanya island terkecil yang butuh interaksi
- navigation dan internal links harus tetap crawlable `<a href>`

## Checklist Setup

### 1. Base layout SEO

Setiap layout harus menerima props:

```ts
title
metaDescription
canonical
ogImage
noindex
breadcrumbs
schema
```

Output wajib:

```html
<title>...</title>
<meta name="description" content="...">
<link rel="canonical" href="...">
<meta property="og:title" content="...">
<meta property="og:description" content="...">
<meta property="og:url" content="...">
<meta property="og:image" content="...">
<meta name="twitter:card" content="summary_large_image">
```

Jika `noindex=true`:

```html
<meta name="robots" content="noindex,follow">
```

### 2. Sitemap

Sitemap harus:

- hanya memasukkan URL canonical
- tidak memasukkan checkout, thanks, search, filter tipis, policy low-value jika memang noindex
- memakai absolute URL
- include `lastmod` jika valid

Pattern aman:

```txt
/
/tentang/
/kontak/
/layanan/
/layanan/[slug]/
/blog/[slug]/
```

### 3. Robots

Robots minimal:

```txt
User-agent: *
Allow: /
Sitemap: https://domain.com/sitemap.xml
```

Blokir hanya jika benar-benar perlu. Jangan blokir file JS/CSS penting.

### 4. Content collections

Untuk blog/content:

Frontmatter wajib:

```yaml
title:
description:
publishedDate:
updatedDate:
author:
slug:
canonical:
noindex: false
```

Validasi:

- title unik
- description unik
- slug stabil
- date akurat
- author jelas

### 5. Performance SEO

Astro advantage harus dipertahankan:

- minimalkan client islands
- jangan lazy-load hero/LCP image
- preload LCP image bila perlu
- pakai WebP/AVIF
- width/height image selalu ada
- font display strategy aman
- CSS critical tidak bloat
- hindari global client JS besar
- gunakan components `.astro` untuk UI statis

Island boleh untuk:

- mobile menu
- tabs/accordion ringan
- forms dengan client validation
- search/filter widgets
- charts/rich interaction

Jika bukan interaktif, jangan jadikan React/Vue/Svelte island.

### 6. Schema Astro

Schema umum:

- Organization / LocalBusiness site-wide
- BreadcrumbList per halaman hierarchy
- Article untuk blog
- Product untuk ecommerce
- FAQPage hanya jika FAQ terlihat

Inject JSON-LD sebagai raw script dan validasi di Rich Results Test.

### 7. QA Commands

```bash
npm run build
npm run check
```

Lalu cek output:

```bash
rg '<title>|canonical|description|robots' dist -n
rg 'application/ld\+json' dist -n
```

Cek manual:

- `/sitemap.xml`
- `/robots.txt`
- 404 page
- canonical host
- mobile layout
- Lighthouse/PageSpeed

## Anti-pattern Astro

- semua konten dirender client-side
- meta tag statis sama di semua halaman
- sitemap memasukkan noindex URL
- canonical mengarah ke homepage semua
- lazy-load hero image
- internal link pakai button tanpa href
- slug berubah saat build
- semua halaman dibuat SSR tanpa kebutuhan
- framework island dipakai untuk UI statis
- content collection tanpa validasi frontmatter
- 404 statis tapi deployment mengembalikan 200

## Final Gate

Sebuah Astro site belum SEO-ready sampai:

- build sukses
- sitemap valid
- robots valid
- setiap indexable page punya title/meta/canonical unik
- schema valid
- no broken internal links
- HTML awal berisi konten utama
- Search Console siap setelah deploy
