# Research Sources — AI-Powered SEO Content Production

## Overview

This document lists the 10 experts selected as primary sources for this research project. Each was chosen based on three criteria:
1. Active publishing in the last 90 days (LinkedIn, YouTube, podcasts, or newsletter)
2. Practitioner experience (real client work, case studies, or in-house SEO leadership) — not just commentators
3. Distinct perspective on how AI is reshaping SEO content production

**Topic scope:** How modern SEO practitioners use AI tools (LLMs, automation, programmatic approaches) to produce content that ranks and drives qualified B2B SaaS traffic in 2025–2026.

**Selection methodology:** Hybrid approach combining Apify-based LinkedIn discovery scrapes with curated knowledge of the space. See `research/other/discovery-methodology.md` for full details.

---

## What has been collected

| | Volume | Source range | Method |
|---|---|---|---|
| **LinkedIn posts** | 112 posts across 10 authors | April – June 2026 | Apify `harvestapi/linkedin-profile-posts`, scraped 16 June 2026 |
| **YouTube transcripts** | 10 videos, 6h 22m, ~84,000 words | February – August 2026 | Apify `johnvc/YoutubeTranscripts` and `starvibe/youtube-video-transcript`, collected 17 August 2026 |

Full video index and coverage notes: `research/youtube-transcripts/README.md`.

---

## Selected Experts

### 1. Hans van Gent
- **Role/Company:** Independent SEO + Growth Systems Consultant
- **LinkedIn:** https://www.linkedin.com/in/jcvangent
- **Why high-signal:** Publishes multi-paragraph essays grounded in named-source experiments (OtterlyAI, Ahrefs, Semrush). Breaks down platform-by-platform GEO data with hard numbers (e.g. schema markup +1,500% on Google AIO, –71% on ChatGPT). References practitioner interviews from BrightonSEO directly.
- **Angle they bring:** Forensic skepticism. Pushes back on universal GEO playbooks and argues each AI platform is a separate retrieval contest.
- **Recent content collected:** 10 original LinkedIn posts, 1–15 June 2026 → `linkedin-posts/hans-van-gent.md`. No video collected: his podcast appearances (SEO Cast, SEO Connect) are largely Dutch-language and predate 2026.

### 2. Daniel Shin Un Kang
- **Role/Company:** Head of Organic & Agentic Search, Expedia Group (ex-YC, ex-SoftBank)
- **LinkedIn:** https://www.linkedin.com/in/itsdankang
- **Why high-signal:** Leads AEO at one of the world's largest travel platforms. Writes from operator perspective with thoughtful frameworks (cites Ben Horowitz's "lead bullets" model). Currently hiring a Principal PM to scale the channel.
- **Angle they bring:** Enterprise-scale AEO operations. Realistic about what does and doesn't work at scale.
- **Recent content collected:** 9 original LinkedIn posts, 16 March – 11 June 2026 → `linkedin-posts/daniel-shin-un-kang.md`. No video collected: his one substantial 2026 appearance (Expedia × Profound, with Profound CEO James Cadwallader) is audio-only and not published to YouTube, so no caption track exists to pull.

### 3. Usman Akram
- **Role/Company:** Discoverability Lead, Modash (B2B SaaS — influencer discovery tool)
- **LinkedIn:** https://www.linkedin.com/in/usman-akram5000
- **Why high-signal:** Published a real client case study showing 96% organic traffic growth over 8 months on Modash's programmatic SEO subfolder, with specific frameworks still in use today. Practitioner with verifiable results.
- **Angle they bring:** B2B SaaS programmatic SEO from the inside. Transparent about what worked and what's still being iterated.
- **Recent content collected:** 15 LinkedIn posts, May – June 2026 → `linkedin-posts/usman-akram.md`. Video **attempted and failed**: his hour-long appearance on *The Ehmad Zubair Show* (14 May 2026, 57:54, 10,765 views) has exactly one caption track — auto-generated Hindi, flagged not translatable. Confirmed via the transcript Actor's `list_only` discovery mode rather than assumed. See `youtube-transcripts/README.md`.

### 4. Rahil Jain
- **Role/Company:** AI Automation / AI Engineering consultant (ex-Goldman Sachs, ex-Amazon, CS BITS Pilani)
- **LinkedIn:** https://www.linkedin.com/in/rahilnjain
- **Why high-signal:** Data-rich analysis posts comparing programmatic SEO winners and losers post–Core Updates (Zapier, Tripadvisor, Wise vs. G2, Datanyze, Causal). Cites specific traffic losses (G2 –80%, Causal –99.52%) and survival thresholds.
- **Angle they bring:** Engineering-meets-SEO. Treats pSEO as systems design with data moats, not template copying.
- **Recent content collected:** 11 substantive LinkedIn posts, 5–12 June 2026 → `linkedin-posts/rahil-jain.md`. No video: LinkedIn-only publisher.

### 5. Aleyda Solis
- **Role/Company:** International SEO consultant. Founder of Orainti and SEOFOMO (the most widely-read weekly SEO newsletter). Active SEO community organizer.
- **LinkedIn:** https://www.linkedin.com/in/aleyda
- **YouTube:** https://www.youtube.com/@CrawlingMondays — *Crawling Mondays*, weekly roundtable series
- **Newsletter/Blog:** https://seofomo.co
- **Why high-signal:** Runs SEOFOMO, which curates 10+ SEO/AI Search practitioners' best work weekly — a research multiplier. Co-organizes industry events (Mujeres en SEO Summit, SEO Padel Open, AI Search Leaders community) that anchor the global SEO community. Has published frameworks for AI Search measurement and AI Search prompt library construction.
- **Angle they bring:** Community hub and curator — connects the field. Different role to the deep technical posters; brings horizontal visibility across what the entire SEO industry is currently testing and saying.
- **Recent content collected:** 15 LinkedIn posts, 10–16 June 2026 → `linkedin-posts/aleyda-solis.md`. Plus **4 Crawling Mondays episodes, 12 July – 15 August 2026** (2h 01m) → `youtube-transcripts/aleyda-solis/`. The roundtable format means these four transcripts also capture 12 additional named practitioners (Cindy Krum, Gianluca Fiorelli, Chris Green, Dan Taylor, Andy Chadwick, Tom Capper, Judith Lewis and others) — the single highest-yield source in the set.

### 6. Nathan Gotch
- **Role/Company:** Co-founder & CEO, Rankability (SEO software product). Author of *AI SEO for Dummies*.
- **LinkedIn:** https://www.linkedin.com/in/nathangotch
- **YouTube:** https://www.youtube.com/@nathangotch
- **Why high-signal:** Builds and ships product in the AI-SEO space. Posts taxonomies for the evolving SEO/AEO/AGEO terminology debate. Has skin in the game commercially.
- **Angle they bring:** Tooling-first perspective. Thinks about how to instrument and measure the new SEO landscape. In video he demonstrates the workflow on screen rather than describing it — the only expert in the set who does.
- **Recent content collected:** 9 substantive LinkedIn posts, 23 April – 15 June 2026 → `linkedin-posts/nathan-gotch.md`. Plus **3 videos, 15 July – 12 August 2026** (2h 08m) → `youtube-transcripts/nathan-gotch/`, including the "SEO super intelligence" foundation episode that specs a six-layer AI content production stack.

### 7. Shubhi Saxena
- **Role/Company:** Product Data Scientist (ML, A/B testing, causal inference)
- **LinkedIn:** https://www.linkedin.com/in/shubhi-saxena
- **Why high-signal:** Built an open-source A/B testing tool for AEO with proper crossover design, LLM-as-judge scoring, and power analysis. Was intellectually honest that her own "optimized" content underperformed — the kind of integrity rare in this space.
- **Angle they bring:** Experimental rigor. Distinguishes signal from noise in AEO claims that most practitioners treat as fact.
- **Recent content collected:** 1 LinkedIn post, 15 June 2026 → `linkedin-posts/shubhi-saxena.md`. This is the thinnest collection in the set — her publishing cadence is low, and the single post was the only one inside the scrape window. She is retained because the one post is methodologically the strongest artifact collected, not because the volume justifies it. No video.

### 8. Puneet Singh
- **Role/Company:** Head of SEO, Mojo Dojo
- **LinkedIn:** https://www.linkedin.com/in/puneet-singh0
- **Why high-signal:** Active in-house SEO leader. Sharp observation posts on contradictions in Google's public messaging (e.g. John Mueller on llms.txt vs. Lighthouse 13.3 quietly adding an Agentic Browsing audit for it).
- **Angle they bring:** Technical SEO evolution toward agent-readability. In-house perspective on emerging machine-usability standards.
- **Recent content collected:** 13 substantive LinkedIn posts, 4 May – 16 June 2026 → `linkedin-posts/puneet-singh.md`. Largest single-author collection in the set. No video: LinkedIn-only publisher.

### 9. Kevin Indig
- **Role/Company:** Growth Advisor, author of *Growth Memo* newsletter (ex-Shopify Director of SEO, ex-G2 VP of SEO)
- **LinkedIn:** https://www.linkedin.com/in/kevinindig
- **Newsletter:** https://www.growth-memo.com
- **Why high-signal:** One of the most respected voices on AI's impact on SEO. *Growth Memo* publishes deeply researched weekly essays with data and original frameworks. Posts regularly on LinkedIn with substance, not engagement bait.
- **Angle they bring:** Strategic synthesis across the AI/SEO landscape. Bridges in-house experience with broad industry visibility.
- **Recent content collected:** 15 LinkedIn posts, 28 May – 15 June 2026 → `linkedin-posts/kevin-indig.md`. Plus **1 interview, 10 July 2026** (26:37, Kalicube) → `youtube-transcripts/kevin-indig/`. The interview is the useful complement to the posts: his LinkedIn output is largely teasers pointing at Growth Memo, whereas the interview states the underlying method and sample sizes out loud (the 2.2% citation-retention figure, the ~50-person user panel, the link-quality correlation).

### 10. Eli Schwartz
- **Role/Company:** Growth advisor, author of *Product-Led SEO* (the canonical B2B SaaS SEO book; ex-SurveyMonkey)
- **LinkedIn:** https://www.linkedin.com/in/schwartze
- **Why high-signal:** Foundational thinker on B2B SaaS SEO specifically. Continues to publish on AI's effect on the product-led SEO model. Background of advising actual SaaS companies on growth.
- **Angle they bring:** Product-led SEO frameworks applied to the AI era. Directly relevant to 100Hires' B2B SaaS context — and deliberately the dissenting voice in this set.
- **Recent content collected:** 14 original LinkedIn posts, 2–15 June 2026 → `linkedin-posts/eli-schwartz.md`. Plus **2 interviews, 10 February and 28 April 2026** (1h 47m) → `youtube-transcripts/eli-schwartz/`. He is on the podcast circuit constantly, so the two selected are the most recent substantive ones; older appearances (e.g. Lenny's Podcast, September 2024) were found and deliberately excluded as too stale for a field moving this fast.

---

## Selection Notes

**Geographic and role diversity:** The list spans in-house SEO leaders (Daniel, Puneet, Usman), founder/operators (Nathan, Kevin), independent consultants (Hans, Eli, Aleyda), technical specialists (Rahil, Shubhi), and community organizers (Aleyda). This ensures the research base captures multiple practitioner perspectives, not one viewpoint repeated 10 times.

**Mid-project revision (Tim Stoddart → Aleyda Solis):** After collecting Tim Stoddart's 15 most recent LinkedIn posts, review showed his current LinkedIn output is mostly general business/founder content rather than SEO/AEO. Despite his strong SEO/content background (former Copyblogger CEO, newsletter at timstodz.com), only ~2 of 15 posts directly addressed the research topic. He was swapped for Aleyda Solis, whose content split (40% directly SEO/AI Search-relevant, 60% community/events) is meaningfully stronger, and whose SEOFOMO newsletter alone surfaces 10+ other practitioners' work each week. This swap is documented as a deliberate research-judgment call, not a quiet correction. See `research/other/discovery-methodology.md` for full rationale.

**The swap paid off twice.** Aleyda was selected on the strength of her curation and community role. What the video collection phase then found is that her *Crawling Mondays* channel is the highest-yield single source in the project — four episodes carrying twelve additional named practitioners, published within five weeks of collection, structured as a sequence that maps almost exactly onto the stages a production playbook needs.

**What was deliberately excluded:** Despite high engagement metrics, posts from recruiters publishing job openings, freelancers using comment-baiting tactics ("Comment 'X' for my system!"), and agency self-promotional carousels were excluded from the initial discovery scrape. These dominated the keyword-search results but provided no practitioner insight. In the video phase, guest appearances older than roughly twelve months were excluded on the same principle — in a field where the measurement consensus shifted twice in 2026, a 2024 interview is a historical document, not a source.

**Deliberately keeping a dissenter.** Eli Schwartz argues that AEO/GEO is roughly 95% conventional SEO with new branding, that LLM visibility is unmeasurable and should be funded from brand budget, and that most AI-citation tactics teams are buying do not work. That directly contradicts the programmes Aleyda, Kevin and Nathan describe building. Both positions are collected in full rather than resolved here, because a playbook that has not been stress-tested against its strongest critic is a marketing document.

**Gaps acknowledged:**
- The list under-represents non-English-language practitioners (though Aleyda partially addresses this — she's Nicaraguan, based in Madrid, and posts in both English and Spanish). The Usman Akram Hindi-captions failure is a concrete instance of this gap having teeth: relevant material exists and is simply unreachable with an English-captions collection method.
- It under-represents the in-house SEO leadership pool generally, since most senior in-house SEO leaders don't publish much on LinkedIn. Future iterations should pursue these voices through podcasts and conference recordings, not LinkedIn alone.
- Shubhi Saxena's collection is a single post. Retained on quality, flagged on volume.
- Video coverage is concentrated: 7 of 10 videos come from two experts. Six of the ten experts publish no substantive video at all — a finding about the field, documented in `youtube-transcripts/README.md`, rather than a gap in the search.

**Why this list supports a real playbook:** Each expert brings either (a) verifiable case-study data, (b) named-source experimentation, (c) operational scale experience, or (d) community-multiplier reach. Synthesized together, they should produce a playbook grounded in evidence rather than opinion. The video layer adds what LinkedIn structurally cannot: the full reasoning chain behind a claim, the on-screen workflow, and the parts practitioners say out loud in conversation but would not post.
