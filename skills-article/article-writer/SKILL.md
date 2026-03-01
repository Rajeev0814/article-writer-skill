---
name: article-writer
description: Write or refine a publish-ready article, newsletter, or post for a specific publishing platform — Medium, Substack, beehiiv, LinkedIn (newsletter or feed post), Dev.to, Hashnode, or Ghost. Use whenever the user wants to write, draft, or generate an article, blog post, newsletter, essay, or LinkedIn post for any of these — or wants an existing draft made publish-ready (optimize, reformat, fix, tighten, or add platform metadata). Triggers include "write a Medium article", "draft a Substack post", "beehiiv newsletter", "LinkedIn post", "optimize my draft for Medium", or any request for platform-optimized content even without naming the format. Each platform has its own headline rules, structure, length, voice, growth mechanics, and required metadata (Medium max 5 tags, Dev.to max 4, plus SEO title/description, cover image, and canonical URL fields). Runs a full pipeline — gather requirements, research, generate or refine to spec, validate against hard rules, then review and polish.
---

# Article Writer

Produce a publish-ready article tailored to the platform it will live on, **including the exact metadata that platform requires** (tags, SEO title/description, cover image spec, canonical URL, etc.). The same idea performs very differently on Medium vs. Substack vs. Dev.to — headline conventions, length, voice, growth mechanics, and required publishing fields all differ. This skill applies each platform's real conventions and ships the metadata alongside the body so the user can paste straight into the editor.

## How to use this skill

Run the pipeline below **in order**. Each stage is a separate file in `pipeline/` — read it when you reach that stage. Don't skip stages; each one feeds the next. The skill is built to stay low-friction: it requires only a **topic**, infers the rest (platform, goal, content type, freshness, audience + knowledge level, research depth) and states its assumptions, asking only when a wrong guess would waste the piece. It works in two modes, detected at intake: **generate** (write a new piece from a topic) and **refine** (take the user's existing draft and make it publish-ready without rewriting it from scratch). Always run 4 (validate) and 5 (review) — those are what separate a publish-ready piece from a rough draft.

| Stage | File | Purpose |
|-------|------|---------|
| 1. Intake | `pipeline/1-intake.md` | Establish topic + infer platform, **goal, content type, freshness, audience + knowledge level, research depth**; identify required metadata fields |
| 2. Research | `pipeline/2-research.md` | Gather + **verify** facts (scaled to depth, None = skip; respect freshness), ranked by source credibility — no fabricated stats |
| 3. Generate | `pipeline/3-generate.md` | Write the body (content-type structure, goal emphasis, knowledge-level calibration, platform craft) + all metadata + suggested visuals |
| 4. Validate | `pipeline/4-validate.md` | Test hard limits + SEO, fact/freshness, **technical**, readability, humanization/fluff checks; loops back to Stage 3 if a structural rule fails |
| 5. Review | `pipeline/5-review.md` | Polish + **quality scorecard**; deliver a publish-ready file with per-platform how-to-publish; offer repurposing on request |

## Platforms

Each platform has a spec file in `platforms/` containing both its **craft rules** (headline, structure, length, voice, growth mechanic) and its **data requirements** (the metadata fields + limits). These files are **platform adapters**: the 5-stage pipeline is fully platform-agnostic, and a platform's specific rules load only when that platform is selected (in stage 3, with its limits reused in stages 1 and 4). This keeps the core workflow clean and makes adding a platform a drop-in.

| Platform | Spec file | Type |
|----------|-----------|------|
| Medium | `platforms/medium.md` | Long-form blog |
| Substack | `platforms/substack.md` | Email + essay |
| beehiiv | `platforms/beehiiv.md` | Email newsletter |
| LinkedIn newsletter | `platforms/linkedin.md` | Professional feed + email |
| LinkedIn post | `platforms/linkedin-post.md` | Professional feed (short native post) |
| Dev.to | `platforms/devto.md` | Developer community |
| Hashnode | `platforms/hashnode.md` | Developer blog |
| Ghost | `platforms/ghost.md` | Self-hosted publication |

`references/universal-craft.md` holds the writing fundamentals that apply on every platform — stage 3 layers the platform spec on top of these.

## Adding a new platform later

The architecture is built for this. To add a platform:
1. Copy the format described in `platforms/_schema.md` into a new `platforms/<name>.md` (fill in craft rules + data requirements).
2. Add one row to the Platforms table above.

Nothing else changes — the pipeline reads whatever platform file it's pointed at. One platform per request keeps output focused; after delivering, offer to adapt the piece for another platform (each adaptation reloads the relevant spec and reworks headline, length, structure, and metadata — not a copy-paste).

## Scope

This skill writes and packages content. It does not publish, schedule, or post anything. For factual or current topics, it verifies claims via search (stage 2) rather than inventing details.

**Integrity guardrail.** This skill optimizes content for reach and persuasion, which is exactly why it must not be pointed at harm. Don't use it to produce material that is deceptive or dangerous — disinformation, fabricated statistics or fake expert quotes presented as real, health/financial/legal claims that could hurt someone if wrong, scams or manipulative sales copy, harassment, or content that misrepresents who is speaking. Persuasive framing for a legitimate position is fine; engineering something false or harmful to spread further is not. If a request crosses that line, say so plainly and offer to help with an honest version instead — applying SEO and hook techniques to make harmful content travel further is the one thing this skill should refuse.
