# Stage 1 — Intake

Goal: get just enough to write well, then move. The bar is **topic required; everything else inferred and stated, asked only when genuinely ambiguous.** Pull from the conversation first. Don't interrogate — making a clear, stated assumption beats a back-and-forth almost every time.

## Required

- **Topic** — what the piece is about. The only true requirement. If even this is vague ("something about productivity"), propose 2-3 sharper angles and let the user pick.

**If the user asks for several platforms at once** ("write this for Medium and LinkedIn"): don't pick one arbitrarily or try to serve both with one generic draft. Write the first platform's version fully through the pipeline, then offer to adapt it for the others — each adaptation reloads that platform's spec and reworks headline, length, structure, and metadata. Confirm which platform to start with if it isn't obvious.

**Two modes — detect which one this is.** A request is either:

- **Generate mode (default)** — the user gives a topic and wants a new piece written. Run the full pipeline as described.
- **Refine mode** — the user already has a draft and wants it made publish-ready ("here's my post, optimize it for Medium", "fix my English and format this for Dev.to", "tighten this and add the metadata"). In refine mode: **don't discard their work or rewrite it from scratch** — preserve their voice, structure, and intent. Skip net-new generation; instead treat their draft as the body and run it through Stage 3's *metadata + structure-fit* parts, Stage 4 (validate against the platform), and Stage 5 (polish + scorecard). Research (Stage 2) only kicks in to verify specific factual claims in their draft or fill a gap they flagged — not to rebuild the piece. If their draft is far off the platform's norms (e.g. a 3,000-word essay they want as a beehiiv brief), say so and offer to restructure rather than silently overhauling their words. Language cleanup (grammar, clarity for non-native speakers) is fair game in refine mode and should preserve meaning.

## Inferred by default (state your assumption, don't ask unless ambiguous)

Read the topic and the conversation, choose a sensible value for each, and say it in one line before writing (e.g. *"Writing this as a how-to guide for early-career PMs, aimed at building authority — say if you'd rather a different angle."*). Only stop to ask when a wrong guess would waste the whole piece.

- **Platform** — which supported platform. Can't be silently ignored, because platforms produce structurally different artifacts (a Medium deep-dive ≠ a beehiiv brief). But you can **default + state** rather than block: pick the most sensible platform for the topic and announce it ("I'll write this for Medium unless you'd prefer another"). If the topic strongly implies one (a dev tutorial → Dev.to; a professional career reflection → LinkedIn), default to it. Ask only if it's a real toss-up. (Unsupported platform named → say so, offer the closest fit, e.g. another email platform → beehiiv base.) **LinkedIn has two distinct formats** — a short native **feed post** (`linkedin-post.md`, no title/SEO, ≤3,000 chars) and a long-form **newsletter** (`linkedin.md`, subscribable, with title + metadata). "LinkedIn post" → the feed post; "LinkedIn newsletter/article" → the newsletter. If the user just says "LinkedIn" and the topic is short/punchy, default to the post; if it's long-form or they mention subscribers, the newsletter — and state which you picked.
- **Content Goal** — what the piece should *achieve*. The same topic becomes a different article depending on this. Infer one of: Educate, Inform, Persuade, Build Authority, Generate Leads, Increase Engagement, Drive Traffic, Promote a Product/Service. Default tends to Educate/Build Authority unless the framing signals selling or lead-gen.
- **Content Type** — the form, which drives structure: How-To Guide, Tutorial, Opinion, Thought Leadership, Case Study, Comparison, Listicle, Research Summary, Industry Analysis, News Commentary. Infer from the topic (a "how to X" → How-To; an "X vs Y" → Comparison; a personal take → Opinion/Thought Leadership). This sets structure in Stage 3 — don't leave it implicit. **If the requested content seems poorly suited to the chosen platform** (e.g. a meme/joke roundup for LinkedIn's professional feed, or a deeply personal confessional for Dev.to's technical audience), note it in one line and offer the better-fitting angle or platform — don't just format mismatched content and let it underperform. The user can still proceed; just make the fit visible.
- **Audience** — who reads it ("early-career PMs", "indie hackers"). A sharp niche beats "everyone." Infer; confirm only if it materially changes the piece.
- **Audience Knowledge Level** — how much the reader already knows: **Beginner** (define terms, assume little background), **Intermediate** (assume working familiarity, skip the basics), **Expert** (assume fluency, go deep, don't over-explain). This single variable reshapes a piece more than almost anything — how much you define, assume, and how deep you go. Infer from topic + audience (a "intro to X" → Beginner; a deep technical comparison for practitioners → Expert).
- **Freshness** — how time-bound the piece is, a *separate axis from research depth*: **Evergreen** (timeless — tutorials, principles, how-tos; deliberately avoid date-stamping that ages it, e.g. don't write "in 2026" unless needed), **Current** (reflects the present state — "best X tools", "state of Y"; verify things are up to date), **News-Based** (tied to a recent event — commentary, reactions; recency and accurate dates are critical, and the piece should be written/published fast). A piece can be deeply researched yet evergreen, or lightly researched yet news-based — infer this independently.
- **Research Depth** — how much verification/sourcing the piece warrants: **None** (no external research — pure opinion, creative, or "draft from what I gave you"; don't search at all), **Basic** (light/no research — personal essays, reflection; 0-1 searches), **Standard** (a few verified facts — typical informative piece), **Deep** (well-sourced, multiple authorities — "state of X" pieces, comparisons), **Expert** (publication-grade, primary sources, careful citation — technical or high-stakes). Infer from topic + goal + freshness; this directly drives Stage 2's effort. (News-Based almost always implies at least Standard; Evergreen opinion can be None/Basic.)

## When to actually ask (and how)

Ask only when inference would be a coin-flip that changes the artifact. When you do, prefer an interactive option-picker if the environment offers one (a tappable single/multi-select) — easier than typing, especially on mobile. Reasonable things to surface:

- **Platform**, if the topic genuinely fits several equally.
- **Angle**, if the topic is too vague to pick one.
- **Goal**, only if the topic is ambiguous between, say, Educate vs. Promote (the difference reshapes the piece).
- **Length/edition** where it forks the piece (LinkedIn short vs. long-form).

Batch into one call. If no picker tool exists, ask one grouped prose question. Never ask about things you can generate (tags, SEO fields) — those are yours to produce.

## Optional inputs (use if offered, never force)

Desired length, target SEO keyword/phrase, voice samples or prior posts, a specific story/stat to include, a canonical URL if cross-posting, a publication/series name, the CTA goal.

## Check the platform's data requirements

Open the chosen platform's spec in `platforms/` and read its **Data Requirements** block (tags + max count, SEO title/description limits, cover image spec, canonical URL, subtitle/excerpt). For each field decide: generate it yourself (most — tags, SEO title, description) or get it from the user (a canonical URL only they have). Generate what you can; ask only for what truly needs them.

## Output of this stage

A short internal brief carried forward: topic/angle, platform, **goal, content type, research depth, freshness, audience + knowledge level**, target keyword (if any), CTA goal, and the platform's required metadata fields with limits. Move to `pipeline/2-research.md`.
