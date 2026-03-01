# Stage 5 — Review & final touch

Goal: a final quality pass that lifts the piece from "correct" to "good," then deliver it cleanly. Validation (Stage 4) confirmed it meets the rules; this stage makes it genuinely worth reading.

## Final-touch review pass

Read the whole piece once as a reader, not a writer, and improve:

- **Opening punch.** Does the first line actually earn the next one? If it warms up or states the obvious, rewrite it sharper.
- **Cut the filler.** Remove throat-clearing, hollow transitions ("In conclusion", "At the end of the day"), and any sentence that doesn't add. Tighten.
- **De-AI the prose.** Break up uniform paragraph lengths, vary sentence rhythm, kill the giveaway tics (every paragraph same shape, overused em-dashes, "X isn't about Y" openers, "It's worth noting"). It should read like a person wrote it.
- **Specificity check.** Replace any remaining vague claim with a concrete detail, number, or example. Generic advice underperforms everywhere.
- **One-idea check.** Could the reader say in one sentence what this was about? If it sprawls, cut the weakest tangent.
- **Flow + transitions.** Make sure sections connect and the arc builds to the close.
- **CTA lands.** The ending should point the reader somewhere with intent, in the platform's style.
- **Accuracy.** No invented facts; claims from Stage 2 are represented faithfully.

Apply the edits directly — don't just list problems.

## Quality scorecard

After polishing, score the piece. **Always include a short scorecard with the delivery; produce the full version only if the user asks** (or asks you to "review"/"score" something).

Score each dimension out of 10, based on the actual piece:

- **Research Quality** — are claims specific, current, and verified (vs. generic/unsourced)?
- **Clarity** — is the one idea obvious and the argument easy to follow?
- **Readability** — sentence/paragraph rhythm, scannability, structure for the platform.
- **SEO** — title/description/keyword/heading-hierarchy strength (for search platforms; mark N/A for pure-email/feed pieces like beehiiv/LinkedIn where it doesn't apply).
- **Originality** — fresh angle vs. recycled consensus.
- **Engagement** — hook strength + how well the close invites response/action.

Then an **Overall: X/10** (a considered average, not arithmetic — weight by what matters for this platform and goal).

- **Short version (default, always shown):** one line — `Scorecard: Research 8 · Clarity 9 · Readability 8 · SEO 7 · Originality 8 · Engagement 9 → Overall 8.2/10`. Optionally one short "biggest lever" note if a dimension is weak.
- **Full version (on request):** the same scores, each with a sentence of justification, plus a short **Improvement Suggestions** list (2-4 concrete, actionable items).

Be honest — a scorecard that's all 9s is useless. If something scores low, say why and what would lift it. If a quick fix would clearly raise a score, just apply it rather than only noting it.

## Deliver

**Default output: a Markdown file** the user can paste into the platform's editor.

- Save it as a Markdown (`.md`) file with a descriptive name, e.g. `medium-onboarding-metrics.md`. Use whatever file-output mechanism the current environment provides (a file-writing/output tool, an artifact, a downloads or outputs directory, etc.). If the environment has no way to produce a file, fall back to delivering the piece inline.
- Structure the file so the metadata is clearly separated from the body — a metadata block at the top (title, subtitle/excerpt, tags, SEO title, SEO description, cover image spec + alt, canonical URL, slug, front matter where relevant), then the article body below. For Dev.to/Hashnode, put the actual paste-ready front matter at the very top.
- **Label the metadata block by how it's used**, per the platform's "Publishing format" note. For markdown-native platforms (Dev.to: front matter + body pastes whole and renders; Hashnode: body pastes, some fields via UI) say so. For rich-text platforms (Medium, Substack, beehiiv, LinkedIn, Ghost) make clear the metadata block is a **checklist of fields to enter in the editor's settings panel**, not text to paste into the body — and that raw markdown won't render in the body, so the user should paste and format in the editor (or you can also provide the body as plain prose if they prefer).
- Make the file visible to the user (present/attach it, or share the link/path) using whatever mechanism the environment offers.

Before the file, give a **brief** note (2-4 sentences): the platform it's tuned for, the headline/subject-line choice and why, the validation result in one line (e.g. "all fields within limits — 5/5 tags, SEO title 54 chars"), a one-line **how to publish** per the platform's format (e.g. "Dev.to: paste the whole file into the markdown editor and flip published to true" / "Medium: paste the body, then set tags + SEO in the More-settings panel"), and a one-line **cover image** pointer (the free-stock search link, with an offer to generate an original if they'd prefer). Keep it short; the article is the deliverable.

If the user explicitly asked for the piece inline, write it inline instead of a file, still with the metadata block on top.

## Offer one next step

Close with a single relevant follow-up — pick the one most useful here, don't stack them:

- "Want me to adapt this for another platform?"
- "Want a few alternative headlines?"
- **Repurpose** it into a LinkedIn post, X thread, newsletter summary, executive summary, or short video script — offer this, and generate only if the user says yes. Don't auto-produce repurposed versions; one article is the deliverable unless asked.
- (Substack) "Want a Notes teaser to promote it?"
- (If the scorecard flagged a weak spot) "Want me to push the [weak dimension] further?"

One offer, phrased naturally. If the user already signaled what they want next, do that instead of offering.
