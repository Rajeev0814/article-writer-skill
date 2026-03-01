# Stage 2 — Research the topic

Goal: gather enough real, specific, *verified* material that the article is concrete and accurate — not generic filler, and not fabricated facts. Specificity is what makes content perform everywhere (named examples, real numbers, current facts). Fabricated statistics and fake quotes are the single biggest failure mode of writing agents, so this stage both gathers and **verifies**. Output: a short **content brief** the writing stage draws from.

## Scale effort to Research Depth (from Stage 1)

- **None** — skip this stage entirely. No external research. For pure opinion, creative pieces, or "draft from what I gave you." Go straight to Stage 3 using the user's own material; don't search. **One backstop even here:** if the user's own material contains a specific, checkable factual claim that would mislead readers if wrong (a statistic, a date, a claim about a real company/person/product), don't launder it into confident published prose. Either attribute it to the user ("in your experience…"), soften it to opinion, or flag it back to them — None means "no research effort," not "amplify a possible falsehood." If such a claim is load-bearing and risky, suggest bumping to at least Basic to verify it.
- **Basic** — little or no external research. For personal essays, opinion, reflection where the value is the perspective. 0-1 searches. Don't bolt on research the piece doesn't need.
- **Standard** — verify the few load-bearing facts. Typical informative piece. ~2-4 searches.
- **Deep** — well-sourced from multiple authorities; map the existing conversation to find a fresh angle. "State of X", comparisons, industry analysis. ~5-10 searches.
- **Expert** — publication-grade. Primary sources, careful cross-checking, citation-ready. Technical, financial, medical, or high-stakes topics. As many searches as accuracy demands.

If unsure, look at the topic: a "lessons I learned" reflection is Basic; a "best X tools in 2026" comparison is Deep; a "how Postgres query planning works" tutorial is Expert.

## Respect Freshness (from Stage 1)

- **News-Based** — recency is critical. Search for the latest, confirm dates, ensure no claim is stale. The value decays, so move fast.
- **Current** — verify that "current state" claims (latest version, who leads, what exists now) are actually current, not from old data.
- **Evergreen** — opposite concern: don't bake in *absolute* date-stamps that age the piece. Avoid "as of 2026", "the new X", named current-year versions, or fleeting current-event references unless essential. *Relative* time phrases ("this year", "recently", "these days") are fine — they stay true whenever the piece is read. Frame timelessly so it still reads well a year from now.

## What to gather

- **Current facts and figures** for the angle — recent data, dates, versions, prices, named tools/companies. Use the actual current year in queries.
- **Concrete examples** you can name and cite, not hypotheticals.
- **The existing conversation** on the topic, so the piece adds a fresh angle rather than repeating consensus (Medium curation and Substack growth both reward originality).
- **A target keyword's real search framing** if SEO matters for the platform (Medium, Hashnode, Ghost, Dev.to) — how people actually phrase the search.

## Source credibility — prefer higher-tier sources

When sources conflict or you're choosing what to trust, rank by credibility (highest first):

1. **Official documentation** (the product/standard's own docs)
2. **Peer-reviewed research papers**
3. **Government / standards-body sources**
4. **Established industry reports** (reputable analysts, recognized institutions)
5. **Reputable publications** (well-regarded journalism/trade press)
6. **Company blogs** (useful but treat as interested parties)
7. **Community discussions** (forums, social) — use for leads and color, verify before asserting

Cite the strongest source available for any load-bearing claim. Flag when a key claim only has low-tier support.

## Fact verification (do this before writing, not after)

For every concrete claim you intend to use, verify:

- **Statistics / numbers** — confirm against a credible source; check it's current, not years stale. Note the date.
- **Company / product information** — names, ownership, features, status (things change; a "current" claim from old data is a trap).
- **Dates** — when something happened, launched, or applies.
- **Quotes** — only attribute a quote you can verify; never invent or paraphrase-into-quotation. Follow copyright limits (short, attributed, in your own words otherwise).
- **Flag uncertain claims** — if you can't verify something but it matters, either drop it, reframe it qualitatively ("many teams report…" rather than a fake "73%"), or mark it in the brief as `UNVERIFIED` so Stage 4 can catch it before delivery.

Hard rule: **never fabricate** a statistic, study, quote, or source to sound authoritative. A reframed qualitative statement beats a made-up number.

## Output of this stage

A compact content brief: the sharpened angle; 3-8 specific facts/examples/data points to use, each with its source and a verified/unverified tag; the fresh take that differentiates the piece; and the target keyword's framing if relevant. Carry this into `pipeline/3-generate.md`.
