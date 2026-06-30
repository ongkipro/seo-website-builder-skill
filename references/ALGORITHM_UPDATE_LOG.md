# Algorithm Update Log

Purpose: Track trusted updates from Google, Bing, Yandex, Pinterest, and other discovery systems. Use this to decide when the SEO playbooks need revisions.

## Update Policy

Only record an update as actionable if it comes from:

1. official search engine/platform blog/docs/status page
2. official webmaster tools notification
3. strong multi-source industry confirmation, clearly labelled as non-official

Do not overreact to ranking volatility without evidence.

## Log Format

```md
## YYYY-MM-DD — Platform — Update Name

Source:
- URL:
- Source type: Official / Strong public evidence / Speculative monitor

Summary:
- ...

Affected surfaces:
- Web / Local / Images / Shopping / Discover / AI answers / Pinterest / etc.

Likely impact:
- ...

Action required:
- None / Monitor / Update playbook / Audit sites / Change implementation

Files updated:
- ...

Validation:
- ...
```

## 2026-06-30 — Multi-engine baseline refresh

Source:
- Google AI Features and Your Website: https://developers.google.com/search/docs/appearance/ai-features
- Google Search ranking systems guide: https://developers.google.com/search/docs/appearance/ranking-systems-guide
- Bing sitemap guidance for AI-powered search: https://blogs.bing.com/webmaster/July-2025/Keeping-Content-Discoverable-with-Sitemaps-in-AI-Powered-Search
- Yandex ranking improvement guidance: https://yandex.com/support/webmaster/en/yandex-indexing/rank
- Pinterest Business / Help sources listed in `SEARCH_ENGINE_SOURCE_INDEX.md`

Source type: Official / platform-owned documentation and blogs

Summary:
- Google AI features use the same Search fundamentals; indexed and snippet-eligible pages can appear.
- Google ranking systems remain multi-signal and include language understanding, freshness, link analysis, original content, reliable information, reviews, deduplication, and spam detection.
- Bing emphasises accurate XML sitemaps, true `lastmod`, and IndexNow for AI-powered search discoverability.
- Yandex emphasises quality, security, convenience, region, usefulness, and monitoring via Webmaster/Metrica.
- Pinterest requires visual discovery thinking: domain claim, creative quality, relevance, engagement, consistency, and trend alignment.

Affected surfaces:
- Web search
- AI search features
- Bing Copilot/search discovery
- Yandex web/local regional search
- Pinterest visual search/discovery

Likely impact:
- SEO playbooks should include multi-engine sitemap, AI-feature eligibility, IndexNow, Yandex diagnostics, and Pinterest visual discovery.

Action required:
- Update documentation pack.

Files updated/created:
- `SEARCH_ENGINE_ALGORITHM_BRIEF.md`
- `SEARCH_ENGINE_SOURCE_INDEX.md`
- `ALGORITHM_UPDATE_LOG.md`
- `PLAYBOOK.md`
- `SKILL_DRAFT.md`
- `REFERENCE_MANIFEST.md`

Validation:
- Local markdown link validation should be run after edits.

## Monitoring Queue

Track these going forward:

- Google Search Status Dashboard updates
- Google Search Central Blog core/spam/content updates
- Google AI features documentation changes
- Bing Webmaster Blog updates about Copilot/AI search/IndexNow/sitemaps
- Yandex Webmaster guidance changes
- Pinterest Business and Help updates about organic reach/search/catalogs
- Merchant Center product data changes
- structured data policy changes
- Core Web Vitals metric changes

## Review Cadence

Recommended:

- quick source check: monthly
- full playbook review: quarterly
- immediate review: after major Google/Bing/Yandex/Pinterest official update
- project-specific review: before major site launch or migration
