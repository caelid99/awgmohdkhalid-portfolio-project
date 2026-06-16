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

## Total cost

~$0.18 USD across two Apify discovery scrapes. Well within free-tier credits.
