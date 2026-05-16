# Raw Data Manifest — David Chang Hero Study
**Date:** 2026-05-16  
**Branch:** `claude/agent-identity-document-OIVZe`  
**Repo:** yungecon/yungagent  
**Research Agent session:** Boot session — full platform collection  

## Platforms collected this session
| Platform | Status | Files | Tool |
|---|---|---|---|
| YouTube | ✅ | 4 files | yt-dlp 2026.03.17 |
| SERP | ✅ | 8 files | WebSearch (fallback) |
| Press | ✅ | 3 files | WebSearch (fallback) |
| Website | ✅ | 4 files | WebFetch |
| Products | ✅ | 2 files | WebFetch |
| Services | ✅ | 2 files | WebSearch + WebFetch |
| Instagram | ❌ Blocked | — | Apify not available (no APIFY_TOKEN) |
| TikTok | ❌ Blocked | — | Apify not available |
| Twitter | ❌ Blocked | — | Apify not available |
| Backlinks | ❌ Skipped | — | No Ahrefs/Apify available |

## File manifest

| Path | Platform | Scraper/Tool | Timestamp | Size (bytes) | Notes |
|---|---|---|---|---|---|
| `research/heroes/david-chang/00_subject.md` | — | Manual | 2026-05-16 | 3601 | Subject definition |
| `research/heroes/david-chang/01_raw/youtube/channel-metadata_2026-05-16.json` | YouTube | yt-dlp --flat-playlist | 2026-05-16T04:47Z | 598955 | 351 videos from The Dave Chang Show |
| `research/heroes/david-chang/01_raw/youtube/video-index_2026-05-16.json` | YouTube | Python (derived) | 2026-05-16 | 98566 | Sorted index of all 351 videos |
| `research/heroes/david-chang/01_raw/youtube/top-performers-note_2026-05-16.md` | YouTube | Manual analysis | 2026-05-16 | 1709 | Top candidates for Whisper transcription |
| `research/heroes/david-chang/01_raw/youtube/runs.log` | YouTube | — | 2026-05-16 | 285 | Run log |
| `research/heroes/david-chang/01_raw/press/press-summary_2026-05-16.md` | Press | WebSearch | 2026-05-16 | 4906 | 6 major story arcs, YUNG framed |
| `research/heroes/david-chang/01_raw/press/sources-index_2026-05-16.json` | Press | WebSearch | 2026-05-16 | 5971 | 25 sources with URLs |
| `research/heroes/david-chang/01_raw/press/runs.log` | Press | — | 2026-05-16 | 196 | Run log |
| `research/heroes/david-chang/01_raw/serp/serp-query-01_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 864 | Query: "David Chang" |
| `research/heroes/david-chang/01_raw/serp/serp-query-02_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1332 | Query: business revenue |
| `research/heroes/david-chang/01_raw/serp/serp-query-03_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1398 | Query: chili crunch trademark 2024 |
| `research/heroes/david-chang/01_raw/serp/serp-query-04_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1323 | Query: restaurant closures 2023 |
| `research/heroes/david-chang/01_raw/serp/serp-query-05_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1268 | Query: Majordomo Media founding |
| `research/heroes/david-chang/01_raw/serp/serp-query-06_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1148 | Query: social media metrics |
| `research/heroes/david-chang/01_raw/serp/serp-query-07_2026-05-16.json` | SERP | WebSearch | 2026-05-16 | 1251 | Query: Momofuku Goods catalog |
| `research/heroes/david-chang/01_raw/serp/serp-domain-summary_2026-05-16.md` | SERP | Manual analysis | 2026-05-16 | 1892 | Domain landscape summary |
| `research/heroes/david-chang/01_raw/serp/runs.log` | SERP | — | 2026-05-16 | 155 | Run log |
| `research/heroes/david-chang/01_raw/website/pages/momofuku-com-home_2026-05-16.md` | Website | WebFetch | 2026-05-16 | 1378 | momofuku.com homepage |
| `research/heroes/david-chang/01_raw/website/pages/majordomo-com-home_2026-05-16.md` | Website | WebFetch | 2026-05-16 | 1466 | majordomo.com homepage |
| `research/heroes/david-chang/01_raw/website/web-presence-map_2026-05-16.md` | Website | Manual analysis | 2026-05-16 | 2107 | Full owned channel map |
| `research/heroes/david-chang/01_raw/website/runs.log` | Website | — | 2026-05-16 | 225 | Run log |
| `research/heroes/david-chang/01_raw/products/momofuku-goods-catalog_2026-05-16.json` | Products | WebFetch | 2026-05-16 | 2711 | Full Shopify catalog + pricing + retail |
| `research/heroes/david-chang/01_raw/products/runs.log` | Products | — | 2026-05-16 | 175 | Run log |
| `research/heroes/david-chang/01_raw/services/services-overview_2026-05-16.json` | Services | WebSearch + WebFetch | 2026-05-16 | 1876 | Full services map + gap analysis |
| `research/heroes/david-chang/01_raw/services/runs.log` | Services | — | 2026-05-16 | 129 | Run log |

**Total files on disk:** 25  
**Total data size:** ~730KB (YouTube metadata dominates at 598KB)

## Verification (Analyst Agent: spot-check these before proceeding)
```bash
ls -la research/heroes/david-chang/01_raw/youtube/channel-metadata_2026-05-16.json  # 598955 bytes
ls -la research/heroes/david-chang/01_raw/press/sources-index_2026-05-16.json       # 5971 bytes
ls -la research/heroes/david-chang/01_raw/serp/serp-query-01_2026-05-16.json       # 864 bytes
ls -la research/heroes/david-chang/01_raw/products/momofuku-goods-catalog_2026-05-16.json  # 2711 bytes
ls -la research/heroes/david-chang/01_raw/website/web-presence-map_2026-05-16.md   # 2107 bytes
```

## What is NOT here (and why)
- **Instagram raw corpus** — Apify token not present in environment. Skip.
- **TikTok raw corpus** — Same.
- **Twitter raw corpus** — Same.
- **Backlinks** — No Ahrefs or Apify available.
- **Full YouTube transcripts** — Whisper not installed. yt-dlp succeeded at metadata level only. Videos available for download once Whisper is added to environment.
- **Full article text (press)** — WebFetch blocked by 403 on Inc, Fast Company, NYT, Washington Post. Press layer built from search snippets and summaries. Raw full-text not available.

## Claims that trace to this manifest
All intelligence in this session references files above. No claims written to Notion without a source path.
