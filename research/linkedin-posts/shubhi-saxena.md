# LinkedIn Posts — Shubhi Saxena

**Profile:** https://www.linkedin.com/in/shubhi-saxena
**Headline:** Product Data Scientist. Builds A/B testing & experimentation infrastructure with ML and causal inference.
**Posts collected:** 1 (only post within the 3-month scrape window)
**Date range:** 15 June 2026 (single post)
**Source:** Apify `harvestapi/linkedin-profile-posts` Actor, scraped 16 June 2026

**Note on volume:** Shubhi is the lowest-volume expert in this dataset by a wide margin (1 post vs. 9-15 for everyone else). She was included precisely because of the *quality* of her single substantive post, not the volume. Her contribution to the research is not breadth of recent commentary but a rigorous experimental study most other practitioners in this space haven't attempted. The post below is what put her on the shortlist during the initial discovery scrape.

---

## Post 1 — 15 June 2026 — 21 likes, 4 comments — HIGH SIGNAL

URL: https://www.linkedin.com/posts/shubhi-saxena_datascience-abtesting-llm-activity-7472132046191247360-ygWq

I built a tool to A/B test Answer Engine Optimization (AEO) which is the art of getting your product recommended by ChatGPT or Gemini. It came back with no significant effect. The "optimized" content actually did slightly worse.

That's the result I'm proudest of. Here's why.

The point was never a lift number. It was building the thing that tells you whether a lift is real or just noise with a reusable eval + experimentation harness, with AEO as the first demo plugged into it.

A few highlights:
→ A crossover design: every question runs through both content versions, so each question acts as its own control which the noise-reduction trick most web A/B tests can't use.
→ An LLM-as-judge that scores whether the answer actually recommended the product, not just mentioned it (those are very different, and a keyword search misses it).
→ A power analysis that put my 40-question pilot at ~9% power. To detect a 20% lift for real, I'd need ~963 questions. So the honest verdict isn't "AEO fails" but it's "this experiment couldn't tell."

This is a controlled simulation, not the real engines. My RAG stands in for ChatGPT/Gemini rather than being them, and the judge is validated on a focused set of cases, so it's a clean test of the method, not a measurement of how Gemini or OpenAI actually rank. Scoping what an experiment can and can't claim is part of doing it well.

And as for the experimenters here: when you hit an underpowered null, what's your first move more data, a sharper metric, or a bolder treatment? Genuinely curious how others handle it.

Full write-up + open-source repo in the comments. 👇

#DataScience #ABTesting #LLM #Experimentation #GenAI

---

## Notes

- **Why one post is enough**: Most "AEO experts" in the dataset assert that schema, llms.txt, prompt engineering, or content rewrites improve AI citation rates. Almost none of them have run a properly-powered A/B test to verify those claims. Shubhi did, was honest that the result was null and the experiment was underpowered, and shipped the test harness as open source so others can run their own. This is the most intellectually honest content in the entire dataset.
- **What she contributes that no one else does**: Methodological rigor. Crossover designs, LLM-as-judge with calibration, explicit power analysis, distinction between "AEO fails" and "this experiment couldn't tell." Reading her single post alongside the prompt-tracking debate happening in the other expert files (Kevin Indig's posts on sampling and confidence intervals especially) creates a much sharper research base than any of the individual perspectives alone.
- **Open-source repo**: Shubhi published the experimentation harness publicly. The repo link is in the LinkedIn post comments. Worth following up for any future playbook work.
- **Limited LinkedIn activity is a feature, not a bug for this slot**: We intentionally accepted lower-volume in exchange for higher-quality methodology. Documenting this trade-off is itself part of the research-judgment story.
- Engagement counts shown are at time of scrape (16 June 2026).
