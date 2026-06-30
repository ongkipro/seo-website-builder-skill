# SEO OS Playbook Harian

Playbook ini adalah versi operasional ringkas dari SEO Knowledge Base. Pakai ini saat membangun, mengaudit, atau memperbaiki website agar tidak tenggelam di 100+ modul referensi.

## Prinsip Utama

SEO yang bagus bukan sekadar keyword. Website harus:

1. bisa dicrawl
2. bisa dirender
3. bisa dipahami
4. layak diindex
5. menjawab search intent
6. membangun trust
7. punya internal linking jelas
8. siap untuk AI-search / answer surfaces
9. terukur performanya
10. menghasilkan outcome bisnis

## Multi-Engine Baseline

Pakai baseline ini untuk Google, Bing, Yandex, Pinterest, dan discovery surfaces lain:

| Surface | Prioritas |
| --- | --- |
| Google | helpful content, crawl/index, canonical, structured data, page experience, AI feature eligibility |
| Bing | XML sitemap, true `lastmod`, IndexNow, Bing Webmaster Tools, crawlability |
| Yandex | quality, security, mobile convenience, site region, Yandex Webmaster/Metrica diagnostics |
| Pinterest | high-quality vertical visuals, claimed website, descriptive Pin text, trend/seasonal relevance, landing-page match |
| AI Search | indexed/snippet-eligible pages, clear passages, entity clarity, source trust, fresh accurate data |

Default rule: optimise for users and technical clarity first, then add platform-specific signals without creating spam.

## Alur Kerja Standar

### 1. Definisikan konteks bisnis

Wajib jawab:

- bisnis apa?
- target user siapa?
- area layanan / market mana?
- tujuan utama: lead, sales, booking, signup, traffic, authority?
- halaman uangnya apa?

### 2. Buat search intent map

Kelompokkan query menjadi:

| Intent | Contoh | Page Type |
| --- | --- | --- |
| Brand | nama brand | Homepage / About |
| Transactional | beli produk X | Product / Service page |
| Commercial investigation | best X, X vs Y | Category / Comparison |
| Local | jasa X dekat saya | Location / Service-area page |
| Informational | cara memilih X | Guide / Blog |
| Trust | review, testimoni, legal | Review / About / Policy |

### 3. Buat page type map

Setiap halaman harus punya alasan eksis:

- traffic
- conversion
- trust
- crawl path
- topical authority
- support page uang

Kalau tidak memenuhi salah satu, pertimbangkan `noindex`, gabungkan, atau jangan dibuat.

### 4. Tentukan URL architecture

Pola aman:

```txt
/
/tentang/
/kontak/
/layanan/
/layanan/nama-layanan/
/produk/
/produk/nama-produk/
/kategori/nama-kategori/
/blog/judul-artikel/
/lokasi/nama-kota/
```

Aturan:

- slug pendek, deskriptif, lowercase
- jangan ganti URL tanpa redirect
- hindari parameter indexable kecuali sengaja
- canonical harus konsisten

### 5. Tentukan index rules

| Page | Default |
| --- | --- |
| Homepage | index |
| Product/service utama | index |
| Category/collection unik | index |
| Blog helpful | index |
| Thank-you page | noindex |
| Cart/checkout/search internal | noindex |
| Filter/facet tipis | noindex/canonical |
| Duplikat lokasi tanpa unique value | noindex/gabung |

### 6. Buat template SEO per halaman

Setiap halaman indexable wajib punya:

- title unik
- meta description unik
- canonical URL
- H1 tunggal dan relevan
- intro yang menjawab intent
- body content yang cukup membantu
- internal links ke halaman terkait
- CTA jelas
- schema bila eligible

### 7. Internal linking plan

Minimal:

- homepage → kategori/layanan utama
- kategori → produk/subkategori/guide
- produk → kategori, related products, FAQ
- artikel → halaman uang + artikel terkait
- footer → halaman trust/legal/kontak
- breadcrumbs → semua halaman dalam hierarchy

### 8. Structured data plan

Gunakan hanya schema yang benar-benar merepresentasikan konten terlihat.

Umum:

- Organization / LocalBusiness
- WebSite
- BreadcrumbList
- Product
- Offer
- AggregateRating / Review jika valid
- Article / BlogPosting
- FAQPage jika FAQ terlihat di halaman

### 9. Technical QA sebelum launch

Checklist minimum:

- halaman penting return 200
- broken links 0
- sitemap hanya URL canonical-indexable
- robots tidak memblokir asset penting
- canonical benar
- title/meta unik
- mobile layout aman
- LCP image tidak lazy-loaded
- 404 benar
- redirect 301 bila URL berubah
- Search Console siap

### 10. Measurement plan

Pasang dan pantau:

- Google Search Console
- Bing Webmaster Tools
- analytics event untuk CTA
- conversion tracking
- top queries
- indexed pages
- crawl/index errors
- CWV
- halaman dengan impressions tinggi CTR rendah
- halaman traffic turun
- Bing sitemap/indexing status
- IndexNow submission result untuk situs yang sering berubah
- Yandex Webmaster/Metrica jika target market relevan
- Pinterest analytics untuk visual/content commerce

## Output Wajib dari AI Agent

Saat diminta SEO, AI harus menghasilkan:

```txt
Critical Assessment
Search Intent Map
Page Type Map
URL Structure
Index/Canonical Rules
Metadata Pattern
Schema Plan
Internal Linking Plan
Content Requirements
Technical QA Checklist
Measurement Plan
```

## Stop Rules

Jangan lanjut build bila:

- tujuan bisnis belum jelas
- page map belum ada
- index/canonical belum jelas
- halaman dibuat hanya demi keyword
- konten generik tanpa pengalaman/kepercayaan
- schema menandai konten yang tidak terlihat
- tidak ada plan Search Console / analytics

## Referensi Resmi Prioritas

Gunakan sumber resmi lebih dulu:

- Google Search Essentials
- Google SEO Starter Guide
- Google ranking systems guide
- Google AI Features and Your Website
- Google structured data docs
- Google crawling/indexing docs
- Google Search Console docs
- web.dev Core Web Vitals
- Bing Webmaster Blog / Bing Webmaster Guidelines / IndexNow
- Yandex Webmaster documentation
- Pinterest Business / Help / Policy docs

Industry sources seperti Ahrefs/Semrush/Moz/Search Engine Land boleh dipakai untuk taktik dan contoh, bukan sebagai klaim bobot algoritma rahasia.

Untuk update algoritma, cek dan catat di:

- `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
- `SEARCH_ENGINE_SOURCE_INDEX.md`
- `ALGORITHM_UPDATE_LOG.md`
