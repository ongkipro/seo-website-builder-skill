# Local Business SEO Playbook

Untuk company profile, jasa lokal, trades, klinik, toko fisik, pesantren/sekolah, restoran, dan bisnis yang melayani area tertentu. Disusun dari SEO OS + `~/Documents/seo-research-google/local-business-seo-playbook.md`.

## Target

Website local business harus membantu Google dan user memahami:

- siapa bisnisnya
- jasa/produk apa yang ditawarkan
- lokasi/area layanan
- bukti kepercayaan
- cara kontak
- apakah bisnis aktif dan nyata

## Input yang Harus Dikumpulkan

Jangan menebak data bisnis. Ambil dari website existing, Google Business Profile, dokumen user, atau tanya user.

| Required | Optional / Recommended |
| --- | --- |
| Business name | legal name / ABN / NIB / NPWP jika relevan |
| Primary service/category | opening hours |
| City/suburb/service area | social profile URLs |
| Phone number | price range |
| Website URL | GPS coordinates |
| Business description | logo / OG image |
| Address atau service-area model | accepted payment |
| Main CTA | founding date |

## Core Local Ranking Factors

Berdasarkan Google Business guidance, fokus utama local visibility:

1. relevance — cocok dengan query
2. distance — kedekatan dengan pencari/area
3. prominence — reputasi, review, citations, authority

Website tidak menggantikan Google Business Profile, tapi memperkuat relevance dan prominence.

## Struktur Website Minimum

```txt
/
/tentang/
/layanan/
/layanan/[nama-layanan]/
/area-layanan/
/area-layanan/[kota-atau-suburb]/
/testimoni/
/kontak/
/blog/ atau panduan/
```

Untuk bisnis kecil, jangan bikin ratusan halaman lokasi tipis. Buat hanya area yang punya unique value.

## Homepage Checklist

Wajib ada:

- H1 jelas: bisnis + layanan utama + lokasi
- ringkasan layanan
- area layanan
- alamat/NAP
- CTA telepon/WhatsApp/form
- bukti trust: review, lisensi, pengalaman, portfolio
- internal link ke layanan utama
- LocalBusiness/Organization schema

## Service Page Checklist

Setiap layanan utama harus punya halaman sendiri jika ada search demand.

Isi minimal:

- apa jasanya
- untuk siapa
- masalah yang diselesaikan
- proses kerja
- harga/mulai dari jika memungkinkan
- area layanan
- FAQ
- bukti hasil/testimoni relevan
- CTA jelas

## Location / Service Area Pages

Halaman lokasi boleh index jika punya unique value:

- alamat/area spesifik
- contoh project/case di area tersebut
- foto lokal/project nyata
- testimonial lokal
- rute/konteks wilayah
- layanan yang tersedia di area itu

Jangan buat halaman lokasi template copy-paste hanya ganti nama kota.

## NAP Consistency

Pastikan konsisten di website, GBP, citation, dan social:

- Name
- Address
- Phone
- Website
- Opening hours

Gunakan format telepon lokal benar, misalnya Indonesia `+62...`, Australia `+61...`.

## Head Tags Template

Pattern aman untuk local pages:

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

Optional geo tags jika punya koordinat valid:

```html
<meta name="geo.region" content="{{COUNTRY_REGION}}">
<meta name="geo.placename" content="{{CITY}}">
<meta name="geo.position" content="{{LATITUDE}};{{LONGITUDE}}">
<meta name="ICBM" content="{{LATITUDE}}, {{LONGITUDE}}">
```

Title pattern:

| Page | Pattern |
| --- | --- |
| Homepage | `Brand - Primary Service in Location` |
| Service | `Service in Location | Brand` |
| About | `About Brand | Location` |
| Contact | `Contact Brand | Location` |
| Location | `Service in City/Suburb | Brand` |

Meta description pattern:

| Page | Pattern |
| --- | --- |
| Homepage | `[USP]. [Service] in [Location/Area]. [Trust signal]. Call/WhatsApp [phone].` |
| Service | `Professional [service] in [location]. [Benefit]. [Proof/trust]. Get a quote today.` |
| Location | `[Service] for [city/suburb]. [Local proof/coverage]. Contact [brand].` |
| Contact | `Contact [brand] for [service] in [location]. [Hours]. Call or message today.` |

## Schema

Pilih schema sesuai bisnis:

- LocalBusiness
- ProfessionalService
- Store
- Restaurant
- MedicalBusiness
- EducationalOrganization
- Organization
- BreadcrumbList
- FAQPage jika FAQ terlihat
- Service untuk halaman layanan

Gunakan subtype lebih spesifik jika tepat:

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
| EducationalOrganization | school/pesantren/training |
| ProfessionalService | generic service |

LocalBusiness minimal:

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "...",
  "url": "...",
  "telephone": "...",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "...",
    "addressLocality": "...",
    "addressRegion": "...",
    "postalCode": "...",
    "addressCountry": "..."
  },
  "openingHoursSpecification": []
}
```

## Service Schema Template

Untuk halaman layanan:

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

## FAQ Schema Rules

Hanya pakai `FAQPage` bila pertanyaan dan jawaban terlihat di halaman.

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

## Phone / Region Formatting

| Region | Display | Link / Schema |
| --- | --- | --- |
| Indonesia mobile | `0812-3456-7890` | `+6281234567890` |
| Indonesia landline | `(0341) 123456` | `+62341123456` |
| Australia landline | `(02) 4900 1234` | `+61249001234` |
| Australia mobile | `0412 345 678` | `+61412345678` |

For Australian businesses, include ABN as `taxID` if available.

## Google Business Profile Alignment

Website harus selaras dengan GBP:

- nama bisnis sama
- kategori bisnis cocok
- URL landing benar
- nomor telepon sama
- alamat/jam buka sama
- foto dan layanan diperbarui
- review dibalas secara natural

## Content Plan

Konten local business terbaik:

- halaman jasa utama
- FAQ berdasarkan pertanyaan calon customer
- panduan biaya / proses / persiapan
- studi kasus lokal
- sebelum-sesudah jika relevan
- artikel edukasi yang mengarah ke service page

## Internal Linking

- homepage → layanan utama
- layanan → kontak + area layanan
- area layanan → layanan relevan
- blog → layanan uang
- footer → NAP + kontak + lokasi
- breadcrumbs aktif

## Anti-pattern Local SEO

- halaman kota copy-paste
- alamat palsu / virtual office misleading
- review palsu
- schema menandai review yang tidak terlihat
- tidak ada NAP jelas
- CTA hanya icon tanpa label
- website tidak mobile-friendly
- halaman kontak tanpa alamat/telepon/jam operasional

## QA

Cek:

- NAP konsisten
- GBP match
- LocalBusiness schema valid
- Service schema valid bila dipakai
- FAQ schema hanya untuk FAQ terlihat
- mobile CTA bisa diklik
- map/rute benar
- phone link pakai `tel:`
- WhatsApp link benar
- contact page indexable jika penting
- privacy/legal page tersedia bila form tracking ada
- `robots.txt` ada
- `sitemap.xml` berisi URL canonical-indexable saja

Common validation errors:

- missing `@context`
- missing stable `@id`
- phone bukan format internasional
- `areaServed` kosong
- schema review/rating tanpa review terlihat
- business address berbeda dengan GBP tanpa alasan jelas

## Final Gate

Local site belum SEO-ready sampai:

- homepage menjelaskan layanan + lokasi dalam 5 detik
- setiap layanan utama punya landing page jelas
- NAP konsisten
- GBP selaras
- schema valid
- trust proof nyata
- CTA mudah di mobile
- tidak ada location doorway pages
