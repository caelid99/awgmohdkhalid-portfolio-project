# Playbook — AI-Powered SEO Content Production for B2B SaaS

**Author:** Awg Mohd Khalid ([@caelid99](https://github.com/caelid99))
**Built from:** 112 LinkedIn posts and 10 video transcripts collected in [`/research`](research/), April–August 2026
**Version:** 1.0, 17 August 2026

Every recommendation below carries its source. Where the sources disagree, I say which side I take. Where I think a well-known practitioner is wrong, I say that too.

**Who this is for:** a B2B SaaS company with an existing site, some organic traffic, and one to three people who own content. Not enterprise, not a pre-product startup. Eli Schwartz's test applies before anything else here does — do not spend more on this channel than you can plausibly get back, and company size is not the deciding factor, expected ROI is (source: Eli Schwartz, [LinkedIn, 13.06.2026](https://www.linkedin.com/posts/schwartze_many-companies-should-not-hire-an-seo-consultant-activity-7471607327637450752-8qUt)). If your pipeline comes from your founder's network, skip this document.

---

## The one-paragraph version

Build the retrieval foundation before you write anything — crawlability, an entity record, a compressed expert knowledge base. Choose topics bottom-of-funnel first, in one category at a time. Draft with AI but brief it properly, because briefing is where AI content fails, not generation. Publish first-party data you own, because that is the strongest cited-content signal anyone has measured. Then spend most of your remaining effort off-site, because AI systems weight what others say about you more heavily than what you say about yourself. Measure with a small fixed prompt panel run repeatedly, report it as polling rather than ranking, and never quote a share-of-voice number.

---

## Phase 0 — Gates before you start

**0.1 Confirm the site is retrievable at all.** Indexability is a precondition, not an optimisation: the URLs visible in AI chatbots are the indexable ones, and a non-indexable page has "virtually zero" chance of appearing (source: Chris Green via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). Most LLMs do not render JavaScript the way Google and Bing do, and some generate a screenshot instead of rendering — so content behind accordions and dropdowns is invisible to them, and facts must exist in the server-side raw response (source: Roxana Estingu via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). Agents are "super lazy by design": they take the least-effort path, ignore hidden elements, and work to a time budget, so put facts in the raw HTML and avoid clever layers (same source).

*Free check:* Microsoft Clarity's AI Visibility Dashboard reports request counts, share of traffic, unique pages requested, robots.txt rule violations and access per bot operator, at no cost (source: Aleyda Solis, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/aleyda_likely-the-easiest-and-cheapest-way-to-check-activity-7472300676442750977-6Um4)).

**0.2 Diagnose before you plan.** Good strategy starts with a diagnosis, not a solution — clients arrive with a vision, a symptom ("traffic is down") or a proposed solution ("I want to do AI"), and the job is to diagnose the underlying business problem rather than validate the proposal (source: Jonathan Moore via Aleyda Solis, [Crawling Mondays, 02.08.2026](https://www.youtube.com/watch?v=49_tMQrCB_U)). Moore's red flags: activities before diagnostics, tactics driving strategy, goals confused with measures, no guiding principles (same source).

**0.3 Separate your two goals and name them.** Revenue goals and "mushy emotional" executive-visibility goals are both legitimate, but they need different reporting and should never be merged into one dashboard (source: Eli Schwartz, [97th Floor, 10.02.2026](https://www.youtube.com/watch?v=_ix-OEw48DY)). If your CEO wants the brand to appear when they open ChatGPT on the way to work, that is a real goal — just do not fund it out of the line item that drives pipeline.

**0.4 Set the budget rule now.** Treat AI-answer visibility as a brand channel funded from brand budget, not by cannibalising a working SEO programme (source: Eli Schwartz, [97th Floor, 10.02.2026](https://www.youtube.com/watch?v=_ix-OEw48DY)).

*Owner: whoever owns the channel. Cadence: once, then revisited quarterly.*

---

## Phase 1 — Build the production foundation (weeks 1–2)

This phase is stolen almost wholesale from Nathan Gotch, who is the only practitioner in the research set who demonstrates the whole workflow on screen rather than describing it.

**1.1 Assemble six layers before writing anything:** the model, data, brand intelligence, subject-matter expertise, competitor intelligence, and an execution record logging every action taken so the system can later diagnose why something did or didn't work (source: Nathan Gotch, [YouTube, 03.08.2026](https://www.youtube.com/watch?v=vVJB2FjOF2k)).

**1.2 Keep the knowledge base as markdown files on your own machine**, not inside a provider, so the same source of truth moves between Claude, Codex, Perplexity or Grok — "that way these AI providers don't own your stuff" (same source).

**1.3 Write five brand artifacts:** campaign strategy, brand voice, business profile, offers, and an **entity record** as the campaign's source of truth, with brand aliases captured up front. Check the entity record line by line — launching on wrong entity data actively harms AI-platform performance (same source).

**1.4 Include what the brand never says.** A brand bible needs tone of voice, how the brand addresses users, and specifically the things the brand never says — omitting it is what produces copy that obviously wasn't written by someone who knows the brand (source: Gianluca Fiorelli via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**1.5 Interview one to three subject-matter experts and compress the transcripts.** Do not dump raw transcripts into the knowledge base — compress each for retrieval, roughly a two-hour interview to ~2,900 words and a 10,000-word transcript to ~2,100, targeting three to five expertise artifacts (source: Nathan Gotch, [YouTube, 03.08.2026](https://www.youtube.com/watch?v=vVJB2FjOF2k)).

**1.6 Match model power to task.** Running a frontier reasoning model on deterministic compression work is "absolute overkill" that "cooks credits"; reserve frontier models for heavy reasoning (same source).

**1.7 Pull the data layer and date-stamp every import:** Search Console (16-month export, capped around 1,000 queries in the UI; use the API via Google Cloud for up to 50,000), GA4, Bing Webmaster Tools, and rank tracking covering both traditional positions and AI mentions. Labelling each import with its date keeps the system organised and reduces hallucination (same source).

**1.8 Build a structural swipe file.** Run 5–10 important keywords, take the top 2–3 pages each, and cross-reference against citations pulled from ChatGPT, Perplexity and Claude. The URLs that both rank *and* are used as retrieval sources are the ones worth templating — model the structure, not the content (same source). Deviating from a structure that hundreds of assets prove works is "a massive gamble"; differentiate on expertise and information gain instead (same source).

⚠️ **Conflict-of-interest note:** Gotch is founder and CEO of Rankability, and this workflow ends with "Rankability automates this entire process." I have kept the process because it is specific, internally coherent and demonstrated live on video. I have not adopted his tool recommendations. See §8.

*Owner: content lead. Cadence: once per campaign, refreshed at 90 days.*

---

## Phase 2 — Decide what to produce (week 2)

**2.1 One category, 90–180 days, a mile deep.** Blanket keyword research across the whole site is explicitly rejected; the strategy itself should take about a day to build — "it's easy to develop the strategy. It's hard to execute" (source: Nathan Gotch, [YouTube, 15.07.2026](https://www.youtube.com/watch?v=3sHPiOIHPTY) and [YouTube, 12.08.2026](https://www.youtube.com/watch?v=9CajZ7SJQ_w)).

**2.2 Start at the bottom of the funnel.** Work the five awareness stages from most-aware backwards; chasing broad, high-volume "unaware" topics first is the classic mistake, and `best + [solution] (+ location)` is where "most of the magic happens" (source: Nathan Gotch, [YouTube, 12.08.2026](https://www.youtube.com/watch?v=9CajZ7SJQ_w)). This converges with Hans van Gent's independent finding: mapping a client's surviving click paths landed every time on bottom-of-funnel, high-specificity pages, which most teams deprioritise (source: Hans van Gent, [LinkedIn, 11.06.2026](https://www.linkedin.com/posts/jcvangent_232-clicks-per-1000-searches-reach-the-open-activity-7470822986602811394-k8cV)). And with Eli Schwartz: the 2020 listicle playbook is dead because the LLM generates the listicle and interrogates the user itself, leaving SEO the specific, mid-funnel decision content that follows (source: Eli Schwartz, [97th Floor, 10.02.2026](https://www.youtube.com/watch?v=_ix-OEw48DY)).

Three practitioners with different incentives arriving at the same place is the strongest signal in this entire research base. **If you take one thing from this playbook, take this one.**

**2.3 Demote search volume to one variable among several.** Demand can equally be proven by Search Console impressions, Reddit/Quora engagement, or first-party sources such as sales calls. Run an 80/20 split — 80% proven demand, 20% experimental zero-volume bets (source: Nathan Gotch, [YouTube, 12.08.2026](https://www.youtube.com/watch?v=9CajZ7SJQ_w)).

**2.4 Score competition at three levels — domain, page, and brand.** The brand level is the AI-era addition: brands that underperform in traditional rankings still get recommended in AI answers because of reviews, consensus and off-site signals (same source).

**2.5 Prioritise by existing position.** Positions 2–15 are low-hanging fruit and always take priority over new pages; position 50+ becomes a clustering opportunity; no ranking at all is untapped (same source).

**2.6 Cap the work.** Filter a raw set of 500–1,000 keywords to roughly 100, then to 25–50 unique-intent keywords, or 10–20 for a focused sprint — targeting 500 "creates tons of paralysis" (same source).

*Owner: content lead. Cadence: once per 90-day sprint.*

---

## Phase 3 — Build the prompt panel (week 3, then weekly)

This is the measurement instrument, and it needs to be built before you publish so you have a baseline.

**3.1 A keyword is not a prompt.** Prompts built as extended keywords are wrong: keywords were always a user's translation of a problem into engine-friendly language, and with an LLM the user skips that translation and types the problem (source: Roxana Estingu via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY); the same point is made independently by Myriam in [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)).

**3.2 Keep the panel small and fixed.** Start with a minimum viable list covering your single most important audience and product line (source: Aleyda Solis, [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)). Clients asking to track 10,000–12,000 prompts because they track that many keywords are "boiling the ocean" — cost with very little ROI, because prompt results are far more volatile than a linear SERP (source: Andy Chadwick via Aleyda Solis, same episode).

For a B2B SaaS starting point, Kevin Indig's concrete recommendation is ~40 seed prompts split 12 brand / 12 category / 16 problem, weighting problem prompts because that is where purchase intent lives (source: Kevin Indig, [LinkedIn, 09.06.2026](https://www.linkedin.com/posts/kevinindig_good-prompt-tracking-starts-with-sample-design-activity-7470197035565002752-T8ow)).

**3.3 Structure the library in three parts:** core prompts (stable, highest-priority journeys), experimental prompts (new products, markets, audiences), and monitoring prompts (reputation, brand representation, risk) — because AI is now a recommendation engine affecting branding, not only a retrieval system (source: Aleyda Solis, [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)).

**3.4 Append the ICP to every prompt and run one pass per ICP.** A context-free base prompt changed direction across 25,000 runs with up to 60% difference between runs, dropping to roughly 20% once persona context was supplied. If two ICPs return different results and you are visible for one and not the other, that is a concrete targeting gap (source: Andy Chadwick via Aleyda Solis, same episode).

**3.5 Run each prompt 3–5 times, weekly — never daily.** After the same prompt runs three times in ChatGPT, only 2.2% of citations remain, measured across 815,000 prompt-page pairs; a tracker that runs each prompt once is measuring volatility, not visibility (source: Kevin Indig, [LinkedIn, 12.06.2026](https://www.linkedin.com/posts/kevinindig_a-prompt-tracker-that-runs-each-prompt-once-activity-7471161915302563840-I-ln)). Daily tracking is "way too noisy" and gets averaged out anyway (source: Kevin Indig, [Kalicube, 10.07.2026](https://www.youtube.com/watch?v=8VArL1BNixA)). Report confidence intervals and keep the raw answers for audit (source: Kevin Indig, [LinkedIn, 12.06.2026](https://www.linkedin.com/posts/kevinindig_a-prompt-tracker-that-runs-each-prompt-once-activity-7471161915302563840-I-ln)).

**3.6 Score every platform separately, never blended.** Monthly citation drift differs sharply by platform — Perplexity 40.5% (steadiest), Copilot 53.4%, ChatGPT 54%, Google AI Overviews 60% (most erratic) — and sourcing behaviour differs too: Perplexity pulls from live web search and behaves closest to classic SEO and digital PR, ChatGPT skews to consensus and listicle sources, and AI Overviews overlaps 54% with classic organic rankings (source: Andy Chadwick citing Rand Fishkin, via Aleyda Solis, [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)).

**3.7 Insist on grounded responses, include some branded prompts, and expect the cost to be roughly what rank tracking costs** — that price point keeps the sample large enough to overcome localisation and personalisation noise (source: Tom Capper via Aleyda Solis, [Crawling Mondays, 02.08.2026](https://www.youtube.com/watch?v=49_tMQrCB_U)).

**3.8 Never track a prompt nobody owns.** If no one is responsible for a prompt, leave it out — some belong to support or customer experience rather than marketing. Set up tagging and segments before you start, because retrofitting via CSV re-upload duplicates prompts and doubles the cost (source: Myriam via Aleyda Solis, [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)).

**3.9 Wait 30 days before reading results**, not one week, and validate a trend before you start tracking it — prompt tracking is "an ideal scenario in a sanitized lab space," a best case that gives direction rather than reality (same source).

**3.10 Do not use the default prompts your tool generates.** Tools reverse-engineer prompts from the content and URLs you already have, which makes a flattering visibility score a self-fulfilling prophecy (source: Andy Chadwick via Aleyda Solis, same episode). Aleyda adds that no tool she has seen asks about your unique selling proposition (source: Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**3.11 Watch the wording for sentiment bias.** Asking "can I trust them?" biases the answer negative before the model says anything, and a premium brand flagged negative because an answer called it expensive is a context problem, not a sentiment problem (source: Myriam and Aleyda Solis, [Crawling Mondays, 22.07.2026](https://www.youtube.com/watch?v=hOPJ3C2lWqo)).

*Owner: whoever owns reporting. Cadence: build once, run weekly, review monthly.*

---

## Phase 4 — Produce (ongoing)

**4.1 Brief, don't prompt.** The biggest AI content mistakes are not in commanding AI to write but in briefing it — what sourcing you give it, what instructions, what role priming, and whether it has the brand bible (source: Gianluca Fiorelli via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**4.2 Never start from a blank canvas — "the magic is in the edit."** Stated as equally true of writing, design, AI content and AI coding (source: Nathan Gotch, [YouTube, 15.07.2026](https://www.youtube.com/watch?v=3sHPiOIHPTY)).

**4.3 Publish one number you own, per page, dated and attributed.** This is the best-evidenced production lever in the entire research base, and it comes from three independent studies:
- A peer-reviewed Princeton and Georgia Tech study (KDD 2024) found adding original statistics was the biggest lever tested, at **+41% visibility** — with the author's own caveat that this was a controlled benchmark, not the live web, and should be treated as direction rather than promise (source: Hans van Gent, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/jcvangent_google-asks-which-page-is-best-ai-search-activity-7472267647301169152-pj9_)).
- Yext studied **17.2 million AI citations** and found pages containing first-party data were cited **4.31x more per URL** (same source).
- Burson's analysis of 85 companies across 7 AI platforms — the "Credibility Paradox" — found concrete, specific claims scored higher on believability than abstract positioning every time; "used by 4,000 logistics teams to cut delivery errors by 30%" beats constant vague mentions (source: Hans van Gent, [LinkedIn, 09.06.2026](https://www.linkedin.com/posts/jcvangent_getting-cited-in-ai-answers-means-nothing-activity-7470085838752690176-kFQz)).

Note the nuance van Gent himself supplies: Omniscient Digital's analysis of 23,387 citations on *branded* queries found reviews and social proof at 57% and original research at 5.4% — so original research wins the informational queries that build a name, and reviews win branded queries once the name exists (source: Hans van Gent, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/jcvangent_google-asks-which-page-is-best-ai-search-activity-7472267647301169152-pj9_)).

**4.4 Build competitor comparison pages, in this order:** `[competitor] alternatives` as the seed, repeated for every competitor, then `competitor vs competitor`, then `vs us`. It "kills two birds with one stone" — ranking for competitor queries while promoting yourself on the page (source: Nathan Gotch, [YouTube, 15.07.2026](https://www.youtube.com/watch?v=3sHPiOIHPTY)).

**4.5 One core topic per page**, placed in the URL, meta description, title tag, H1 and first sentence, with variants through the body. A secondary keyword ranking badly is the signal to splinter off a dedicated page (source: Nathan Gotch, [YouTube, 12.08.2026](https://www.youtube.com/watch?v=9CajZ7SJQ_w)).

**4.6 Do not write pages in isolation.** Treating a page as standalone rather than part of a cluster — and ignoring the buyer journey that may start or land there — is Fiorelli's first named mistake (source: Gianluca Fiorelli via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**4.7 Let format follow purpose.** Do not force everything into bullet points and tables because you think it chunks better (source: Aleyda Solis, same episode).

**4.8 Hard cap on scaled AI publishing.** Language models pull primarily from Google and Bing indexes, and Google spent 2022–2024 demoting overly optimised content. Teams building at scale with AI are producing exactly the pages Google penalised two years ago: a two-to-three-month surge in traffic and citations, then losing all of it on a three-to-six-month lag — and when organic visibility falls, LLM visibility follows (source: Lidor Wysocki via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). Corroborating: Originality AI checked every site hit with a Google manual action and found 100% contained AI content, and Google's rater guidelines now score all-AI pages in the lowest quality tier (source: Hans van Gent, [LinkedIn, 12.06.2026](https://www.linkedin.com/posts/jcvangent_claude-fable-5-shipped-3-days-ago-the-most-activity-7471158655627923456-4bFj)) — though see §5.3 for why I treat that second figure carefully.

**4.9 Do not publish research output raw.** Convert it into a structured, designed asset (source: Nathan Gotch, [YouTube, 15.07.2026](https://www.youtube.com/watch?v=3sHPiOIHPTY)).

*Owner: content lead + SMEs. Cadence: continuous, reviewed per sprint.*

---

## Phase 5 — Go off-site, and spend most of your effort here (ongoing)

This is where the research base is most emphatic and where most B2B SaaS teams under-invest.

**5.1 The website is the last stop, not the first.** Onsite work is table stakes; people learn about the brand elsewhere, and AI systems trust what humans say about you more than what you say about you (source: Cindy Krum via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)). An LLM summarises across multiple places, so if the only site talking about you is your own, you are not in the summary (same source).

**5.2 Kevin Indig reaches the same conclusion from data.** Across hundreds of thousands of query/page pairs checked against Semrush link metrics, the strongest correlation with AI visibility was Semrush's aggregate link quality score above 0.5 — which he calls a partial red herring, because the causal driver is more likely brand *mentions* on authoritative sites, plus their context, sentiment and attributes (source: Kevin Indig, [Kalicube, 10.07.2026](https://www.youtube.com/watch?v=8VArL1BNixA)). Separately: the source set AI cites is topic-specific — competitor domains account for 33.5% of citations for invoicing questions but 7% for "starting a business" — so lifting a PR plan from an adjacent topic misses the set that matters (source: Kevin Indig, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/kevinindig_ai-trusts-a-different-set-of-sources-for-activity-7472249744724156417-dz3F)).

**5.3 Run the citation audit and let it become the outreach list.** Export every AI citation for your target queries and count brand mentions. In Gotch's live teardown the brand appeared 4 times across 82 citations, and 3 of those were self-serving — effectively one real mention. Four topics produced roughly 20 earned-media opportunities; ten to twenty topics becomes a couple of hundred outreach targets, sorted by source type: blogs and news for outreach, press releases (which do get picked up as citations), Reddit as earned media, and retail or marketplace listings as distribution (source: Nathan Gotch, [YouTube, 15.07.2026](https://www.youtube.com/watch?v=3sHPiOIHPTY)).

**5.4 Prioritise by where citations actually come from.** Check the citation sources for the prompts representing your journeys, expect product, help and community pages to be cited rather than category pages, compare competitor cited pages onsite and offsite, and where your content exists but is not cited, diagnose why — JavaScript reliance, poor structure, ambiguous wording, or missing stats that would make it the trustable factual source (source: Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**5.5 LinkedIn is a retrieval surface for B2B, not just a distribution channel.** Semrush ran 325,000 prompts through ChatGPT, Google AI Mode and Perplexity and got 89,000 cited LinkedIn URLs — citation rates of 14.3% (ChatGPT Search), 13.5% (AI Mode) and 5.3% (Perplexity), making LinkedIn the #2 most-cited domain overall and #1 for B2B queries. Between November 2025 and February 2026 profile citations fell from 33.9% to 14.5% while post citations rose from 26.9% to 34.9% — AI cites the post, not the profile (source: Rahil Jain, [LinkedIn, 05.06.2026](https://www.linkedin.com/posts/rahilnjain_why-linkedin-is-now-an-seo-channel-for-b2b-activity-7468516684312723457-fcAm)). I cite this because the underlying study is named and checkable; see §8 for why I do not rely on this author's unsourced figures.

**5.6 Put named humans in front of it.** Models favour user-generated platforms with real conversations and real expertise, so promote named experts from the brand into communities, YouTube and LinkedIn (source: Lidor Wysocki via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). YouTube is one of the most-cited sources in AI Overviews (source: Cindy Krum via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**5.7 Mine your reviews for positioning, not just sentiment.** Read review text for unexpected USPs, for what reviewers actually care about, and for gaps against competitors — then make those points prevalent across site, video and social (source: Celeste Gonzalez via Aleyda Solis, same episode).

*Owner: whoever owns PR/brand, jointly with content. Cadence: continuous.*

---

## Phase 6 — Report (monthly)

**6.1 Report three layers.** Leading indicators (are bots crawling, can they retrieve), mid-funnel (mentions and citations in *relative* terms because of noise), lagging (self-reported attribution at signup, CRM attribution for B2B). Everything is directional — "there is no direct bridge anymore" (source: Kevin Indig, [Kalicube, 10.07.2026](https://www.youtube.com/watch?v=8VArL1BNixA)). Aleyda's parallel three-layer framing is AI Presence, AI Readiness, Business Impact (source: Aleyda Solis, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/aleyda_how-to-measure-success-in-ai-search-ill-activity-7472178249708675072-juZt)).

**6.2 Add "how did you find us?" to the conversion flow.** A SimilarWeb study with Rand Fishkin tracking a week of user behaviour found a meaningful share of AI-generated brand recall converting into direct brand searches, which analytics attributes to nothing (source: Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). This one line of code recovers more attribution than any tool in this document.

**6.3 Use relative visibility against a named competitive set** as the primary mid-funnel metric — it is the best available, and anyone over-relying on directly attributable revenue "will never justify the costs relative to the outcome" (source: Chris Green via Aleyda Solis, same episode).

**6.4 Do not say "ranking in citations."** Capper's point is that dropping the phrase alone improves how teams think about the metric; the value is being mentioned and recommended positively, with or without a link, and the right mental model is closer to buying print or billboard advertising (source: Tom Capper via Aleyda Solis, [Crawling Mondays, 02.08.2026](https://www.youtube.com/watch?v=49_tMQrCB_U)).

**6.5 Anchor the business case on a journey signal, not the referrer number.** Log files may show AI sending 1% of traffic while clickstream shows AI as a waypoint in 80% of journeys — both real. Defend budget on branded search lift, organic-to-direct ratio, or post-citation cohort behaviour, with the 1% as supporting evidence (source: Hans van Gent, [LinkedIn, 02.06.2026](https://www.linkedin.com/posts/jcvangent_your-log-files-say-ai-sends-1-of-your-traffic-activity-7467534235294351360-Bq3z)). When observed data isn't available, run a four-week geographic incrementality test on one segment (source: Philip J Armstrong of Semrush via Hans van Gent, same post).

**6.6 Do not delete your GA4 custom channel groups.** GA4's new "AI Assistant" channel is misclassifying — ChatGPT as "Unassigned", Claude as "Referral", app clickthroughs as Direct — because it still depends on referral data browsers and apps don't reliably pass (source: Puneet Singh, [LinkedIn, 16.06.2026](https://www.linkedin.com/posts/puneet-singh0_ga4-googleanalytics-seo-activity-7472502338759348224-b2om)).

**6.7 Track the follow-up questions the answer nudges**, not only whether you appear — "LLM answers are zero-click to the square" — and look for repetition across them to design the conversational journey (source: Gianluca Fiorelli via Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**6.8 Do not act during a core update rollout.** Do not roll back content on day-3 or day-5 numbers, and audit only after the rollout completes — most recoveries come at the next core update, not between them (source: Hans van Gent, [LinkedIn, 01.06.2026](https://www.linkedin.com/posts/jcvangent_saturday-may-30-was-the-loudest-day-of-googles-activity-7467213215811403777-lRUS)).

*Owner: reporting owner. Cadence: monthly, with a quarterly strategy review.*

---

## 7. Where experts disagree

### 7.1 Is prompt tracking worth doing at all?

**Kevin Indig says yes, if you treat it as polling rather than ranking.** He concedes the critics' premise — five people can run the same prompt and get five different answers — and argues the fix is sampling discipline: repeated runs, fixed panels, confidence intervals, personas, auditable raw answers. He compares it to weather forecasting and credit scores, and points out keyword rank was never fully deterministic either (source: Kevin Indig, [LinkedIn, 08.06.2026](https://www.linkedin.com/posts/kevinindig_ai-answers-are-probabilistic-but-prompt-activity-7469704803720482816-DO-D) and [Kalicube, 10.07.2026](https://www.youtube.com/watch?v=8VArL1BNixA)).

**Eli Schwartz says mostly no.** Prompt tracking "probably won't move the needle" for most brands, with one exception: knowing whether customers can find you on prompts directly about your product. He calls AI visibility close to meaningless and share-of-voice the worst offender — "taking a bucket of water from the ocean and trying to calculate what share of the ocean it represents," since the universe of prompts is unknowable. He recommends a conventional brand tracking survey instead (source: Eli Schwartz, [LinkedIn, 04.06.2026](https://www.linkedin.com/posts/schwartze_prompt-tracking-probably-wont-move-the-needle-activity-7468280462025826304-ZNrh) and [AI SEO Show, 28.04.2026](https://www.youtube.com/watch?v=QPm1GA_5CZA)).

**I side with Indig on method and Schwartz on scope.** Indig's sampling argument survives Schwartz's objection: the bucket-of-ocean critique kills *share of voice as a percentage* but does not kill *relative movement on a fixed panel you defined*. You are not estimating the ocean; you are watching the same forty buoys every week. But Schwartz is right that the exception he names — can customers find you on prompts about your actual product — carries almost all the value, which is why §3.2 puts 16 of 40 seed prompts on problem intent and why §6 forbids reporting a share-of-voice number. The honest position: track, but never publish a percentage that implies you know the denominator.

### 7.2 Does AI-specific technical work (schema, llms.txt, chunking) do anything?

**Rahil Jain says yes and is prescriptive:** a 40–60 word answer at the top of every page, wrapped in FAQPage, HowTo or Article schema, plus engine pairings (Wikipedia/ChatGPT, Reddit/Perplexity, LinkedIn/Copilot) (source: Rahil Jain, [LinkedIn, 06.06.2026](https://www.linkedin.com/posts/rahilnjain_the-aeo-playbook-week-3-recap-activity-7468885268733792256-G3UW)).

**Puneet Singh says the evidence does not support it.** Ahrefs tracked 1,885 pages that added JSON-LD schema across AI Overviews, AI Mode and ChatGPT and found no meaningful uplift — AI Overview citations dropped slightly. He is careful about what that proves: every page already had 100+ citations, so it shows schema won't lift pages AI already trusts, and may still matter for pages with weak entity understanding (source: Puneet Singh, [LinkedIn, 12.05.2026](https://www.linkedin.com/posts/puneet-singh0_we-tracked-1885-pages-adding-schema-ai-activity-7459812664685285376-ogYj)). He also quotes Google's own guide directly: "You don't need to create new machine readable files, AI text files, markup, or Markdown" and "Structured data isn't required for generative AI search" (source: Puneet Singh, [LinkedIn, 17.05.2026](https://www.linkedin.com/posts/puneet-singh0_googles-guide-to-optimizing-for-generative-activity-7461919581121560576-8519)).

**Aleyda Solis goes further and argues the workarounds are actively wrong** — pre-rendering purely because LLMs don't render JavaScript, publishing markdown files to get ingested, forcing bullet points and tables for chunking (source: Aleyda Solis, [Crawling Mondays, 15.08.2026](https://www.youtube.com/watch?v=o2I3UXbGFNE)).

**I side with Puneet and Aleyda.** Rahil's version is the most actionable and the least evidenced — none of the three prescriptions carries a source, while the opposing position has a named 1,885-page study and Google's published documentation behind it. Schema is hygiene: implement it correctly once because it helps traditional search, then stop treating it as an AI lever. The tell is that Puneet argues *against his own side's interest* by limiting what the Ahrefs study proves — that is what source skepticism looks like, and it is why I trust his conclusion more than Rahil's.

**Worth preserving from the losing side:** Usman Akram documented Google contradicting itself on llms.txt — Search Central calling it unnecessary on 15 May 2026 while the Chrome team shipped a Lighthouse 13.3 "Agentic Browsing" audit checking for it ten days earlier, and Google's own Gemini API docs carry one (source: Usman Akram, [LinkedIn, 21.05.2026](https://www.linkedin.com/posts/usman-akram5000_googles-own-documentation-called-llmstxt-activity-7463197856812687362-m-9J)). Puneet's reconciliation is the useful one: search optimises for discovery, agents need functionality, so llms.txt is a machine-usability question, not a ranking one (source: Puneet Singh, [LinkedIn, 21.05.2026](https://www.linkedin.com/posts/puneet-singh0_seo-technicalseo-aeo-activity-7463023594323816448-Fv8g)).

### 7.3 Should you run your own experiments, or apply other people's findings?

**Usman Akram gives teams permission to skip original research.** With a new AI search study appearing weekly, he argues you do not have to reverse-engineer the models yourself — plenty of smart people are already doing that, and your job can be to take their insights and drive business outcomes. To be fair to him: he frames this as permission rather than prohibition, says neither role is more important than the other, and includes himself among the people running experiments (source: Usman Akram, [LinkedIn, 02.06.2026](https://www.linkedin.com/posts/usman-akram5000_seo-aeo-seostrategy-activity-7467536584251269120-EXRD)).

**Chris Green says the opposite:** warehouse everything — Search Console, analytics, access logs — and build your own dashboards and correlations rather than waiting for data science teams already busy with higher-precedence work (source: Chris Green via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)).

**Shubhi Saxena shows what running your own actually yields.** She built a crossover-design A/B test for AEO where every question runs through both content versions, with an LLM-as-judge scoring whether the answer *recommended* the product rather than merely mentioning it. The result was null — the "optimized" content performed slightly worse. Her power analysis put the 40-question pilot at ~9% power, requiring roughly 963 questions to detect a 20% lift, so she refused to read the null as "AEO fails," calling the honest verdict "this experiment couldn't tell" (source: Shubhi Saxena, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/shubhi-saxena_datascience-abtesting-llm-activity-7472132046191247360-ygWq)).

**I side against Usman here, and Shubhi is the reason.** His argument runs entirely on analogy — Tesla, the Wright brothers, the internet — and analogies about who *invents* a technology do not tell you anything about who should *test* it in their own context. Meanwhile Shubhi's post demonstrates the concrete cost of not testing: she ran the numbers and found her 40-question study was underpowered by a factor of roughly twenty-four, meaning it could never have detected the effect it was looking for.

That is the problem with consuming research rather than producing it. Every practitioner in this base is quoting studies at each other and almost none of them state a sample size or a power calculation — including several I cite approvingly above. Usman's division of labour only works if the consumer can tell a real finding from an underpowered one, and nothing in his post equips them to. The practical version I would actually run: you do not need to experiment monthly, but you need one person who can read a study critically, and the cheapest way to build that skill is to run one small test badly and see what you learn.

### 7.4 Is AEO a distinct discipline, or SEO with new vocabulary?

**Eli Schwartz says it is SEO.** 95% of what people do for AEO, aside from marketing, is ordinary SEO; it is very unlikely you find something cited in an LLM that was not already performing in search for similar terms; and he consults for one of the largest LLM companies in the world where every problem they bring him is an ordinary SEO problem (source: Eli Schwartz, [AI SEO Show, 28.04.2026](https://www.youtube.com/watch?v=QPm1GA_5CZA)). His supporting datapoint: Anthropic, where he had been consulting, hired for a traditional SEO lead rather than an AEO or GEO specialist (source: Eli Schwartz, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/schwartze_the-best-seo-job-ive-ever-seen-is-below-activity-7472313480243666945-2_Xc)).

**Daniel Shin Un Kang says there is a genuinely new customer.** He argues agents are a third segment alongside B2C and B2B — "Business to Agent" — with a parallel purchase journey, and that a brand can be visible to every human and business on earth while invisible to the systems assembling the shortlist. Expedia formally announced B2A work at its Explore conference, and its CEO called AEO the company's fastest-growing channel on the Q1 earnings call (source: Daniel Shin Un Kang, [LinkedIn, 11.06.2026](https://www.linkedin.com/posts/itsdankang_is-y-combinators-make-something-people-activity-7470852395779022848-awzc) and [LinkedIn, 12.05.2026](https://www.linkedin.com/posts/itsdankang_answer-engine-optimization-aeo-is-now-activity-7460031051030085632-0Pe5)).

**I side with Schwartz on hiring and Kang on product.** For a B2B SaaS company of the size this playbook targets, Schwartz is right operationally: the skills are SEO skills, the tools are SEO tools, and hiring an "AEO specialist" on the strength of a certification from an AEO tool vendor is a mistake he names explicitly (source: Eli Schwartz, [LinkedIn, 11.06.2026](https://www.linkedin.com/posts/schwartze_who-should-you-hire-for-aeo-activity-7470822331762937856--arR)). But Kang's argument is not really about staffing — it is that the thing being evaluated is shifting from the page to the product, which is why his own prescription is "systems that produce a content portfolio that stays legible to agents" plus "genuine underlying product value," and no silver bullet (source: Daniel Shin Un Kang, [LinkedIn, 09.06.2026](https://www.linkedin.com/posts/itsdankang_principal-product-manager-answer-engine-activity-7470127624770514946-pqwj)). That is compatible with Schwartz, who reaches the same destination by a different route: relocate SEO into product. Two people who present as opponents agreeing on the conclusion is worth more than either argument alone.

*Note on both: Kang's posts double as recruitment ads for the team he was building, and Schwartz's Anthropic datapoint is a single company's hiring decision used as industry evidence, in a post promoting a client's job opening. Neither invalidates the argument; both should be read with the incentive visible.*

---

## 8. What I rejected and why

**8.1 Rahil Jain's unsourced statistical corpus.** Rejected as a foundation for any recommendation. His posts carry the most precise-sounding numbers in the research base — "17–38% overlap between top-10 rankings and AI citations", "97.4% of AI citations come from non-Tier-1 sources", "161% more likely to be cited", "failing Core Web Vitals costs 2 to 4 positions", "LCP cap dropped from 2.5s to 2.0s" — and almost none carry a source (source: Rahil Jain, [LinkedIn, 06.06.2026](https://www.linkedin.com/posts/rahilnjain_the-aeo-playbook-week-3-recap-activity-7468885268733792256-G3UW), [09.06.2026](https://www.linkedin.com/posts/rahilnjain_internal-linking-the-cheapest-seo-win-of-activity-7469959574867873792-zMPk), [12.06.2026](https://www.linkedin.com/posts/rahilnjain_core-web-vitals-2026-the-composite-score-activity-7471045530203103232-toZS)). Two specific failures decided it:
- **He contradicts himself within 24 hours.** On 7 June the March 2026 core update "wiped 60 to 80% of AI content farms in 12 days"; on 8 June it "wiped 60 to 90% of templated AI sites in 72 hours" (source: Rahil Jain, [LinkedIn, 07.06.2026](https://www.linkedin.com/posts/rahilnjain_march-2026-core-update-what-actually-changed-activity-7469234820766908416-pimn) and [08.06.2026](https://www.linkedin.com/posts/rahilnjain_programmatic-seo-2026-survivors-losers-activity-7469627677918830592-06Cs)).
- **The same result appears in two different anonymous case studies.** A backlinks/digital-PR engagement produces "+40% organic traffic"; an internal-linking audit produces "+40% organic traffic" (sources as above, 09.06.2026 and 10.06.2026).

I kept exactly one thing from him — the Semrush LinkedIn citation study in §5.5 — because that one is named, sized and independently checkable.

**8.2 "Skip your own research."** Rejected, reasoning in §7.3.

**8.3 The Originality AI "100% of manually-actioned sites contained AI content" figure, as a causal claim.** I cite it in §4.8 as corroboration and nothing more. The figure is relayed without sample size or link, and "penalised sites contain AI content" is a long way from "AI content causes penalties" — the base rate of AI content across all sites in 2026 is plausibly high enough to make the statistic near-vacuous (source: Hans van Gent, [LinkedIn, 12.06.2026](https://www.linkedin.com/posts/jcvangent_claude-fable-5-shipped-3-days-ago-the-most-activity-7471158655627923456-4bFj)). The scaled-AI-content warning in §4.8 stands on Wysocki's mechanism and timeline, not on this number.

**8.4 Blocking Googlebot.** Aleyda relayed a publisher playbook ending in "consider blocking Googlebot as well" if referrals collapse further (source: Aleyda Solis relaying Shahzad Abbas, [LinkedIn, 11.06.2026](https://www.linkedin.com/posts/aleyda_the-llms-have-caused-enough-damage-to-publishers-activity-7470746984648212480-Pp54)). Rejected for this audience without hesitation. It is a coherent position for a news publisher whose product *is* the page. A B2B SaaS company's product is the software; organic search is a demand channel, not the revenue itself, and the same LLMs you would be defending against are pulling primarily from Google's index (source: Lidor Wysocki via Aleyda Solis, [Crawling Mondays, 12.07.2026](https://www.youtube.com/watch?v=7hrGPw-p2RY)). Blocking Google to protect AI visibility is self-defeating here.

**8.5 "Don't buy LLM-only tools" as an absolute.** Schwartz compares it to buying a tool that only tracks Bing (source: Eli Schwartz, [97th Floor, 10.02.2026](https://www.youtube.com/watch?v=_ix-OEw48DY)), and he is right about the general case. But Jonathan Moore's alternative is better than either buying or abstaining: start with manual checks and build a cheap tracker on DataForSEO APIs, given there are over 90 prompt trackers in the market (source: Jonathan Moore via Aleyda Solis, [Crawling Mondays, 02.08.2026](https://www.youtube.com/watch?v=49_tMQrCB_U)). I rejected the absolute and kept the cost ceiling from §3.7.

---

## 9. My original ideas

### 9.1 A negative-control prompt panel

**Nobody in the research base proposes this**, and it follows directly from two things they do establish.

The problem: Kevin Indig measured 2.2% citation retention after three runs of the same prompt, and Andy Chadwick reports monthly citation drift of 40–60% depending on platform. So when your weekly panel moves, you have no way to tell whether your content did it, or the platform did.

**The idea:** alongside your 40 tracked prompts, run 8–10 **control prompts you will never optimise for** — questions in an adjacent category you do not sell into, or about a product attribute you deliberately never write about. Track them identically, weekly, same runs, same personas.

The control panel gives you a platform-noise baseline. If your tracked prompts move 15% and your controls move 14%, you learned nothing about your content that week — you measured the weather. If your tracked prompts move 15% and your controls sit at 3%, you have something. Over a quarter, the control series is also a free early-warning system for model updates: a step change across all controls at once is a platform event, and you will see it before the vendor blog posts about it.

**Why it could work:** this is a placebo arm, and it is standard in every field that measures noisy interventions — Shubhi Saxena reaches for the same statistical instinct with her crossover design, where each question acts as its own control (source: Shubhi Saxena, [LinkedIn, 15.06.2026](https://www.linkedin.com/posts/shubhi-saxena_datascience-abtesting-llm-activity-7472132046191247360-ygWq)). Nobody has ported it from the lab to the live tracking panel. The cost is small and calculable: 25% more prompts on a panel that Capper says should cost about what rank tracking costs (source: Tom Capper via Aleyda Solis, [Crawling Mondays, 02.08.2026](https://www.youtube.com/watch?v=49_tMQrCB_U)). And it directly answers Schwartz's strongest objection — that these numbers are unfalsifiable — by making the measurement falsifiable in the only way that matters: you can now show what a *null* week looks like.

**How it could fail:** if the controls are chosen badly — too close to your category, so your own content moves them; or too far, so they sit on a different part of the platform's behaviour and drift independently. Choosing them is a judgment call and I have not tested how sensitive the method is to that choice.

### 9.2 Publish the SME interview, don't just compress it

Gotch's workflow interviews one to three subject-matter experts and compresses each transcript into a lean artifact *for the model's knowledge base* (source: Nathan Gotch, [YouTube, 03.08.2026](https://www.youtube.com/watch?v=vVJB2FjOF2k)). The raw interview is then thrown away. Nobody in the research base suggests publishing it.

**The idea:** publish the interview itself as a dated, attributed, lightly-edited public Q&A — the same asset, second use.

**Why it could work:** it is precisely the artifact three separate studies say gets cited. It is first-party (Yext: 4.31x more citations per URL), it is concrete and specific rather than abstract positioning (Burson's credibility paradox), and it is attributable expertise from a named human, which is what Wysocki argues models favour (sources as cited in §4.3 and §5.6). It also costs nothing incremental — you are already paying for the interview, the recording and the transcription in Phase 1. And it produces the one thing a B2B SaaS content team can genuinely never be out-competed on: what your own engineers and customers know, which no competitor can regenerate with a better model.

**How it could fail:** raw interviews are often boring, and a lightly-edited transcript published at volume is exactly the low-effort content §4.8 warns against. This works as a small number of genuinely substantive interviews, not as a content-volume strategy.

---

## 10. Weaknesses of this playbook

**It is built on a source base with a structural bias.** Six of the ten experts researched publish no substantive video, and 7 of the 10 videos come from two people — consultants and educators who monetise teaching. In-house operators publish short written analysis or nothing. So this playbook over-represents the consultant view of the work and under-represents what it is like to run this inside a company with a roadmap, a legal team and competing priorities.

**Almost none of the numbers I cite are independently verified.** I verified that each source said what I claim they said. I did not verify that the underlying studies exist, were conducted properly, or say what the practitioner relaying them says they say. The Princeton/Georgia Tech +41% figure, the Yext 17.2M citation analysis, the Burson credibility study, the Semrush LinkedIn corpus — all are second-hand in this document. Van Gent is the only source in the set who consistently flags this problem about his own citations, which is partly why I lean on him.

**The core measurement recommendation is untested by me.** The whole of Phase 3 rests on Indig's sampling argument. I find it persuasive and I have argued why. I have not run a prompt panel, and neither §7.1 nor §9.1 has survived contact with a real dataset.

**The strongest recommendation may have the weakest mechanism.** §4.3 tells you to publish first-party data because three studies associate it with citations. None of them establishes *why*, and at least one plausible confound is obvious: organisations that produce original data are also organisations with PR teams, budget and existing authority. The correlation may be measuring the company, not the content.

**The time horizon is short and the field is unstable.** Wysocki's decay finding says the penalty for scaled AI content arrives on a three-to-six-month lag. My source material spans February to August 2026. Anything published in the last quarter of that window has not had time to be proven wrong yet — including Aleyda's 15 August episode, which is two days older than this document.

**No B2B SaaS company has run this end to end**, including me. Usman Akram's Modash case (+96% programmatic traffic over eight months) is the closest thing to a full B2B SaaS result in the set, and it is from 2024, pre-dates most of the AI-search shift, and is self-reported without third-party verification (source: Usman Akram, [LinkedIn, 08.06.2026](https://www.linkedin.com/posts/usman-akram5000_seo-geo-seostrategy-activity-7469540756099846144-XK8O)).

**Missing entirely:** cost and staffing models (nobody in the set gives real numbers), anything about localisation beyond one rule, the legal exposure raised by the German court ruling on AI Overview liability (source: Aleyda Solis, [LinkedIn, 14.06.2026](https://www.linkedin.com/posts/aleyda_seofomo-activity-7471961330585894912-mnAx)), and any perspective from outside English-language practice — a gap made concrete by the one video I could not collect because its only captions were Hindi.

---

## 11. Who I would NOT recommend following, and why

### Rahil Jain — do not use as a source of facts

He is the most quotable practitioner in this research base and the least reliable one. The case is not about his conclusions, several of which I agree with; it is about whether a reader can trust the numbers he attaches to them.

| Problem | Evidence |
|---|---|
| **Self-contradiction within 24 hours** | The March 2026 core update wiped "60 to 80% of AI content farms in 12 days" ([07.06.2026](https://www.linkedin.com/posts/rahilnjain_march-2026-core-update-what-actually-changed-activity-7469234820766908416-pimn)) and "60 to 90% of templated AI sites in 72 hours" ([08.06.2026](https://www.linkedin.com/posts/rahilnjain_programmatic-seo-2026-survivors-losers-activity-7469627677918830592-06Cs)) |
| **Identical results in unrelated case studies** | "+40% organic traffic" from digital PR ([10.06.2026](https://www.linkedin.com/posts/rahilnjain_backlinks-in-2026-do-they-still-matter-activity-7470320844330893312-8g0F)) and "+40% organic traffic" from internal linking ([09.06.2026](https://www.linkedin.com/posts/rahilnjain_internal-linking-the-cheapest-seo-win-of-activity-7469959574867873792-zMPk)), both from unnamed B2B SaaS clients |
| **Precise figures with no source** | "161% more likely to be cited", "97.4% of AI citations from non-Tier-1 sources", "76% of SEOs still pay $300+ per link", "the March 2026 spam update wiped PBNs in 19.5 hours" |
| **Consequential technical claims asserted** | "The LCP cap dropped from 2.5s to 2.0s" and "failing CWV costs 2 to 4 positions" — the two claims most likely to trigger engineering work, both unsourced ([12.06.2026](https://www.linkedin.com/posts/rahilnjain_core-web-vitals-2026-the-composite-score-activity-7471045530203103232-toZS)) |
| **Conflicts with better-sourced peers** | His "60% of Google searches end with zero clicks" sits against Usman Akram's 68% for 2026, attributed to Rand Fishkin, published the same month |

The pattern is unusually legible because his posts are dense with figures — precision is doing the work that sourcing should. A reader who acts on the CWV claim commissions engineering work on an unverified threshold. **What he is genuinely good at is framing**: the Information Gain scoring rubric and the "build the data moat before the templates" principle are both useful ideas. Read him for shape, never for numbers, and check every figure before repeating it.

### Nathan Gotch — follow the video, discount the LinkedIn

A qualified caution, not a rejection. His video work is the most useful material in this entire research base, and Phases 1 and 2 lean on it heavily — because on video he demonstrates the workflow live rather than asserting it. His LinkedIn is a different product. Roughly one post in eight carries even an anecdote, the highest-detail workflow posts terminate in a Rankability or Search OS pitch (source: Nathan Gotch, [LinkedIn, 06.05.2026](https://www.linkedin.com/posts/nathangotch_when-creating-pages-for-seo-aeo-they-activity-7457790873058291712-1MuE)), one is straightforward comment-bait gating a prompt from his own product ([23.04.2026](https://www.linkedin.com/posts/nathangotch_how-to-secretly-dominate-your-seo-competitors-activity-7453088642262040576-QOsY)), and he contradicts himself on terminology within a month — prescribing "Search Everywhere Optimization" as his number one tip on [16.05.2026](https://www.linkedin.com/posts/nathangotch_ive-been-seo-for-15-years-crazy-heres-activity-7461381040524357632-fLI_), then saying on [10.06.2026](https://www.linkedin.com/posts/nathangotch_aeo-is-a-strong-replacement-for-seo-because-activity-7470554969113550848-WRUD) that he prefers it but does not think it will stick.

He also owns a product that automates the exact process he teaches. That does not make the process wrong — it is demonstrated on screen and internally consistent, which is why I kept it — but every tool recommendation inside it should be treated as advertising, and I have not adopted any of them.

### Who I would recommend, for contrast

**Shubhi Saxena**, on a single post — the only practitioner in the set who ran a controlled experiment, reported a null result against her own hypothesis, calculated her own statistical power, and stated plainly what her study could not claim. She has nothing to sell. In a field where everyone is quoting studies at each other, she is the only one who showed her working.

---

## 12. How to verify anything in this document

Every citation above links to either a LinkedIn post URL or a YouTube video URL. The underlying collected material sits in this repository:

- LinkedIn posts, by author: [`research/linkedin-posts/`](research/linkedin-posts/)
- Full video transcripts, by video: [`research/youtube-transcripts/`](research/youtube-transcripts/)
- Collection index and known gaps: [`research/youtube-transcripts/README.md`](research/youtube-transcripts/README.md)
- Expert selection and rationale: [`research/sources.md`](research/sources.md)
- How the sources were found, and what failed: [`research/other/discovery-methodology.md`](research/other/discovery-methodology.md)

Where a claim came from a guest on Aleyda Solis's *Crawling Mondays* roundtable rather than from Aleyda herself, I have attributed it to the guest and named the episode, because the distinction matters for judging the source.
