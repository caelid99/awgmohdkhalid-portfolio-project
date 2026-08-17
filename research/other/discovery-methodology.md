# Discovery Methodology — How the 10 Experts Were Selected

## Process

The 10 experts in `sources.md` were selected through a hybrid approach combining algorithmic discovery (via Apify scrapers) and curated knowledge of the space.

### Phase 1: Apify discovery scrape — Round 1

**Tool used:** `harvestapi/linkedin-post-search` Actor on Apify

**Search parameters:**
- Queries: "AI SEO", "programmatic SEO", "answer engine optimization"
- Posted limit: past month
- Sort by: relevance
- Max posts: 20 per query
- Cost: ~$0.08 USD

**Result:** 39 posts scraped. After review, only ~5 posts came from genuine practitioners worth shortlisting. The rest were recruiters posting job openings, freelancers selling services, hashtag-stuffed engagement bait, or generic thought-leadership pieces with no substance.

**Lesson:** Broad keyword searches on LinkedIn surface engagement-optimized content, not practitioner content. The "first results" trap Alex's brief warned about is real.

### Phase 2: Apify discovery scrape — Round 2

After Round 1's noise problem, I refined the search strategy:

**Search refinements:**
- Added `authorKeywords: "Head of SEO"` filter to surface in-house leaders
- Added `contentType: "documents"` filter to surface long-form carousels (more substantive than text-only posts)
- Tried more specific practitioner phrases ("AI overviews SEO", "AI content production SEO")
- Cost: ~$0.10 USD

**Result:** Found additional strong candidates including Hans van Gent (whose multi-platform GEO experiment analyses became the single strongest pick from any scrape), Puneet Singh, and Rahil Jain.

### Phase 3: Curated additions

Two experts (Kevin Indig and Eli Schwartz) were added based on established reputation in the AI/SEO space:
- Kevin Indig — author of *Growth Memo* newsletter, ex-Shopify/G2 Head of SEO
- Eli Schwartz — author of *Product-Led SEO*, B2B SaaS practitioner

Both were manually verified for active publishing (last 30 days), substantive content with data/evidence, and absence of red flags (no "save + repost" engagement bait, no course-selling-only posts, no surface-level "AI SEO expert" positioning).

## Selection criteria applied to all 10

Every expert was evaluated against:

1. **Recency** — actively publishing in the last 30 days
2. **Practitioner evidence** — real client work, case studies, specific traffic numbers, or named experiments (not just hot takes)
3. **B2B SaaS or transferable relevance** — their work applies to a SaaS context, not purely ecommerce/local/affiliate SEO
4. **AI/SEO intersection** — genuinely engaging with how AI changes content production, not just sprinkling "AI" on stale SEO advice
5. **Distinct perspective** — each expert brings a different angle (in-house leader, founder, data scientist, consultant, established author) so the research base is diverse
6. **Available content** — has either substantial LinkedIn presence OR YouTube/newsletter content to collect

## Why this matters

The 100Hires brief specifically called out: "did you find genuinely strong voices, or just the first Google results?" — the answer is no, we deliberately structured the search to filter past surface noise. The Apify Round 1 result was the proof: even with high-relevance LinkedIn keyword search, the majority of returns were not practitioner-grade.

---

# Phase 4: Video and podcast collection (17 August 2026)

The LinkedIn phase covered what these practitioners *post*. This phase covers what they *say* — longer-form video and podcast material where the reasoning behind a claim is actually visible.

## Tools used

| Actor | Used for | Pricing model |
|---|---|---|
| `starvibe/youtube-video-transcript` | Channel-level discovery — list a channel's most recent uploads with dates, durations and view counts, optionally with transcripts | ~$0.005 per result |
| `johnvc/YoutubeTranscripts` | Per-video transcript pulls from a list of URLs, with full metadata; also has a `list_only` discovery mode that reports available caption tracks without fetching one | ~$0.00001 per video |

Both were called programmatically through the Apify MCP interface rather than the web UI, which is what made the discovery-then-fetch loop below practical.

## Process

**Step 1 — Establish who publishes video at all.** Ten LinkedIn-first experts do not automatically mean ten YouTube channels. Each expert was checked individually for an owned channel and for recent guest appearances. Result: 4 of 10 had usable 2026 video, 6 did not.

**Step 2 — Channel discovery before transcript fetching.** Rather than guessing video URLs from search results, `starvibe` was pointed at each channel URL with a `start_date` filter to list what had actually been published recently. This is what surfaced the strongest material in the entire project — see "The Crawling Mondays find" below.

**Step 3 — Metadata-first, transcript-second.** Every fetch projected only the metadata fields first (`title`, `upload_date`, `duration`, `view_count`) before pulling any transcript text. Publish dates were checked against the recency criterion *before* spending a fetch, which is how four candidate videos were rejected without ever being downloaded.

**Step 4 — Write per video, not per batch.** One markdown file per video, each with metadata header, annotation, extracted key claims, and the full verbatim transcript. Transcripts are reflowed into paragraphs; no wording altered, nothing summarised or truncated.

## What the discovery step caught that a URL guess would have missed

Four videos were found via web search, looked plausible, and were rejected on their real publish dates once metadata came back:

| Video | Apparent fit | Actual publish date | Verdict |
|---|---|---|---|
| Aleyda Solis — "The AI Search Optimization Roadmap" | Strong | 9 September 2025 | Rejected, ~11 months stale |
| Aleyda Solis — SEOPRESSO Ep.215 | Strong | 3 September 2025 | Rejected, ~11 months stale |
| Kevin Indig — Ahrefs Podcast | Strong | 26 August 2025 | Rejected, ~12 months stale |
| Eli Schwartz — Lenny's Podcast | Very strong (89k views) | 19 September 2024 | Rejected, pre-dates the entire AI search shift |

The Lenny's Podcast episode is instructive. It is by far the highest-view result for Eli Schwartz and would be the obvious pick for anyone assembling a source list from search rankings. It is also from September 2024, which in this field is a different era — it predates AI Mode, the 2026 measurement debate, and most of what the other nine experts are currently arguing about. Sorting by popularity would have put it top of the list; sorting by publish date removed it.

## The Crawling Mondays find

Aleyda Solis's personal channel (`@aleydasolis`) returns nothing recent — its last upload was 2021. Searching by her name and taking the top results would have produced only the stale September 2025 guest appearances above.

Her actual current video output lives on a separate channel, *Crawling Mondays*, which the first two handle guesses (`@CrawlingMondays`, `/c/KevinIndig`-style paths) failed to resolve. Once resolved via the `/c/CrawlingMondaysbyAleyda` form, it returned five videos published between 12 July and 15 August 2026 — all directly on topic, the most recent one two days before collection.

Four were collected. Because the show is a roundtable format, those four transcripts also capture twelve additional named practitioners, making this single channel the highest-yield source in the project.

**The lesson, stated plainly:** the difference between "stale 2025 material from a well-known name" and "the best source in the set from the same person" was three failed channel-URL attempts. Discovery is worth doing properly.

## Collection failures, documented

Failures are recorded here rather than quietly dropped, because a collection method's limits are part of its description.

**Usman Akram — Hindi captions only.** His hour-long appearance on *The Ehmad Zubair Show* (14 May 2026, 57:54, 10,765 views) returned `success: false`. Rather than assume the video was private or the Actor broken, it was re-run in `list_only` discovery mode, which reports available caption tracks without fetching one. The video has exactly one track: auto-generated Hindi, flagged not translatable. No English track exists and no translation path is available, so nothing was collected. This is a language-coverage limit of the method, not a problem with the source.

**Daniel Shin Un Kang — audio-only.** His one substantial 2026 appearance (Expedia × Profound, with Profound CEO James Cadwallader) is distributed as a podcast, not to YouTube. No caption track exists to pull. Collecting it would require a different pipeline — audio download plus speech-to-text — which was out of scope for this phase and is noted as a future extension.

**Kevin Indig — own channel unresolvable.** A Growth Memo YouTube channel appears in search results, but no tested URL form returned uploads through the Actor. His collected video is therefore a guest appearance (Kalicube, July 2026), which turned out to be the more useful artifact anyway — his own posts are largely teasers for the newsletter, whereas the interview states his method and sample sizes out loud.

## Result

| | Count |
|---|---|
| Experts with usable 2026 video | 4 of 10 |
| Videos collected | 10 |
| Total runtime | 6h 22m |
| Total transcript volume | ~84,000 words |
| Videos found and rejected on date | 4 |
| Videos attempted and blocked | 2 |

## Total cost

~$0.18 USD across two Apify LinkedIn discovery scrapes, plus roughly $0.05 across all video discovery and transcript runs in Phase 4. Under $0.25 USD for the entire research base — comfortably inside free-tier credits.
