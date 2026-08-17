# YouTube Transcripts — Index

Video and podcast material collected for the research topic **AI-powered SEO content production**.

**Collected:** 17 August 2026
**Method:** Apify Actors `johnvc/YoutubeTranscripts` and `starvibe/youtube-video-transcript`, called programmatically via MCP. Channel-level discovery was used to find each practitioner's most recent videos; transcripts were then pulled per video with English captions and full metadata. See `../other/discovery-methodology.md` for the full process, including what failed.
**Volume:** 10 videos, 6h 22m of source material, ~84,000 words of transcript.

Each file contains: video metadata (channel, publish date, duration, views and video ID at time of collection), a short note on why the video is in the research set, extracted key claims, and the **full verbatim transcript**. Transcripts are reflowed into paragraphs for readability; no wording is altered, and nothing is summarised or truncated.

---

## Owned-channel content

These practitioners publish video on their own channels, so the material reflects what they choose to teach rather than what an interviewer asks.

### Aleyda Solis — *Crawling Mondays*

Aleyda's channel is a roundtable series: each episode she hosts two to three named practitioners and works through one stage of an AI search optimization programme. The four episodes below were published within five weeks of each other and read as a sequence — definition, research, strategy, production.

| Published | Video | Duration | Views | File |
|---|---|---|---|---|
| 12 Jul 2026 | AI Search Optimization (GEO, AEO): What is it, Common Errors & How to Optimize AI for Success | 41:40 | 1,212 | [`2026-07-12-…`](aleyda-solis/2026-07-12-what-is-ai-search-optimization-common-errors.md) |
| 22 Jul 2026 | How To Do a Successful AI Search Audience and Prompt Research | 25:27 | 577 | [`2026-07-22-…`](aleyda-solis/2026-07-22-ai-search-audience-and-prompt-research.md) |
| 2 Aug 2026 | How to Establish an AI Search Optimization (GEO, AEO) Strategy and Goals | 27:11 | 820 | [`2026-08-02-…`](aleyda-solis/2026-08-02-ai-search-optimization-strategy-and-goals.md) |
| 15 Aug 2026 | How to Optimize your Content for AI Search (GEO, AEO) | 26:32 | 365 | [`2026-08-15-…`](aleyda-solis/2026-08-15-optimize-your-content-for-ai-search.md) |

**Why these four:** the 15 August episode is the single most on-topic piece of material in the entire research set — Cindy Krum, Gianluca Fiorelli and Celeste Gonzalez on how content for AI search actually gets briefed, produced and placed. The other three supply what a playbook needs around it: the empirical floor (indexability, crawl access), the input layer (how a prompt library is built and governed), and the reporting layer (what to promise a stakeholder and what not to).

**Guest practitioners captured across these four episodes:** Lidor Wysocki, Chris Green, Roxana Estingu, Andy Chadwick, Dan Taylor, Miriam Ellis, Tom Capper, Judith Lewis, Jonathan Moore, Cindy Krum, Gianluca Fiorelli, Celeste Gonzalez. This is a research multiplier — the roundtable format means these four files carry twelve additional practitioner voices beyond the ten in `sources.md`.

### Nathan Gotch

| Published | Video | Duration | Views | File |
|---|---|---|---|---|
| 15 Jul 2026 | a simple SEO strategy that actually works (no nonsense) | 18:59 | 2,399 | [`2026-07-15-…`](nathan-gotch/2026-07-15-simple-seo-strategy-that-works.md) |
| 3 Aug 2026 | Do This Before Creating Any SEO Content | 37:27 | 4,611 | [`2026-08-03-…`](nathan-gotch/2026-08-03-seo-super-intelligence-foundation.md) |
| 12 Aug 2026 | The Complete SEO Keyword Research Masterclass for 2026 | 71:26 | 4,288 | [`2026-08-12-…`](nathan-gotch/2026-08-12-keyword-research-masterclass.md) |

**Why these three:** Gotch is the only expert in the set who shows the full production workflow on screen rather than describing it. The 3 August video is the closest thing collected to a written spec for an AI content production stack — six named layers (model, data, brand intelligence, SME expertise, competitor intelligence, execution record) assembled as portable markdown before any drafting. The masterclass documents the complete data model for deciding *what* to produce, and the 15 July teardown turns "why aren't we cited in AI answers?" into a countable diagnostic.

---

## Guest appearances

For these two, the substantive 2026 video is interview content on other people's channels. Captions carry no speaker labels, so each file flags that claims attributed to the guest were verified from context.

| Expert | Published | Video | Host | Duration | Views | File |
|---|---|---|---|---|---|---|
| Kevin Indig | 10 Jul 2026 | Prompt Tracking, AI Visibility Measurement, and Why Trust Has Replaced Rank | Kalicube | 26:37 | 70 | [`2026-07-10-…`](kevin-indig/2026-07-10-prompt-tracking-ai-visibility.md) |
| Eli Schwartz | 10 Feb 2026 | What SEO Actually Looks Like in 2026 | 97th Floor | 39:44 | 411 | [`2026-02-10-…`](eli-schwartz/2026-02-10-what-seo-actually-looks-like-in-2026.md) |
| Eli Schwartz | 28 Apr 2026 | Stop Chasing AI Citations: Eli Schwartz on SEO, Google AI Mode and Product-Led SEO | AI SEO Show | 67:19 | 19,505 | [`2026-04-28-…`](eli-schwartz/2026-04-28-stop-chasing-ai-citations.md) |

**Why these three:** Kevin's Kalicube interview supplies the measurement numbers underneath the prompt-tracking posts already collected in `../linkedin-posts/kevin-indig.md` — the same claims, but with the method and the sample sizes attached. Eli is deliberately the counter-position in this set: he argues that most of what the other experts are building programmes around is ordinary SEO with a new name, and that B2B SaaS teams should relocate SEO into product rather than staff an AI-search discipline. A playbook assembled only from people who agree with each other is a weaker playbook.

---

## Coverage and gaps

**Video coverage by expert (from `../sources.md`):**

| Expert | Video collected | Note |
|---|---|---|
| Aleyda Solis | 4 | Own channel, weekly cadence |
| Nathan Gotch | 3 | Own channel, weekly cadence |
| Kevin Indig | 1 | Guest only; his own channel had no fetchable recent uploads |
| Eli Schwartz | 2 | Guest only; frequent podcast circuit |
| Usman Akram | 0 | **Video exists but is unusable — see below** |
| Hans van Gent | 0 | Podcast appearances are largely Dutch-language and pre-2026 |
| Daniel Shin Un Kang | 0 | One 2026 podcast appearance (Expedia × Profound) is audio-only, not on YouTube |
| Rahil Jain | 0 | LinkedIn-only publisher |
| Shubhi Saxena | 0 | LinkedIn-only publisher |
| Puneet Singh | 0 | LinkedIn-only publisher |

**The Usman Akram case, documented rather than hidden.** Usman appears on *The Ehmad Zubair Show* — "The Most Practical Guide to Starting SEO in 2026", published 14 May 2026, 57:54, 10,765 views. The first transcript fetch returned `success: false`. Rather than assume the video was private or the Actor was broken, the request was re-run in the Actor's `list_only` discovery mode, which returns available caption tracks without fetching one. Result: the video has exactly one caption track — auto-generated **Hindi**, flagged not translatable. There is no English track and no translation path, so no transcript was collected. The video is real, relevant and publicly available; the barrier is caption language, and that is worth knowing before anyone plans a collection run that assumes English captions exist.

**The honest read on this distribution:** six of the ten experts do not publish substantive video. That is not a failure of the search — it is a finding about where this particular field talks. The AI/SEO conversation splits cleanly: consultants and educators who monetise teaching (Aleyda, Gotch, Eli) publish long-form video, while in-house practitioners and technical specialists (Daniel, Puneet, Rahil, Shubhi, Usman) publish short-form written analysis on LinkedIn and nowhere else. A playbook built only from video would over-index on the teaching voice and miss the operator voice entirely, which is exactly why both folders exist.
