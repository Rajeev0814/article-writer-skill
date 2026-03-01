# Stage 4 — Validate

Goal: test the generated draft + metadata against the platform's **hard requirements** before the user ever sees it. This is the "testing" stage — it catches spec violations (too many tags, SEO title over the limit, missing canonical field) that would otherwise force the user to fix things by hand.

Run this every time, even for quick requests. It's fast and it's the difference between "a draft" and "publish-ready."

## How to validate

Open the platform spec's **Data Requirements** block and its **Craft Rules**, and check the draft against each. Build the checklist from the platform's actual rules — below is the general shape; the platform file gives the exact numbers.

### Metadata checks (hard limits — must pass)

- **Tag count** ≤ the platform max (Medium 5, Dev.to 4, etc.) and all relevant.
- **SEO title** within the character limit (commonly ≤60 so Google doesn't truncate).
- **SEO/meta description** within limit (commonly ≤156-160).
- **Title / headline** length appropriate for the platform.
- **Subject line** within limit where it's an email platform (beehiiv ≤~40 chars, front-loaded).
- **Every required field present** — none of the platform's mandatory fields left missing.
- **Cover image** — the URL field is a real URL/clean placeholder (never prose), and a "Cover image" options section is present below the metadata with: a free-stock search link, an offer to generate (if supported), and the brief (dimensions matching the platform + alt text). Licensing-safe — no copyrighted image URL handed over for publishing.
- **Front matter** (Dev.to/Hashnode) is valid and complete — and contains no prose where a URL is expected (e.g. `cover_image:` must be a URL or blank, never an image description; the description belongs in the metadata block above).
- **Canonical URL** present or correctly left as a labeled placeholder.

### Craft checks (quality gates)

- **Hook** does its job in the platform's required space (e.g. LinkedIn newsletter pre-fold ≤210 chars, or LinkedIn *post* hook ≤~140 mobile fold, actually lands before the fold). For a LinkedIn post, also check the **total body ≤3,000 chars** (hashtags and emojis included) — two separate counts.
- **Length** is within the platform's target range.
- **Structure** matches the platform AND the content type (subheading cadence, blocks vs. essay, steps for a how-to, table for a comparison).
- **One clear idea**, specific (not generic), real CTA present that fits the goal.
- **Voice** fits the platform and sounds human.

### SEO checks (where the platform is search-driven: Medium, Hashnode, Ghost, Dev.to)

- **Title length** within limit and keyword reasonably placed (toward the front).
- **Meta description length** within limit and includes the target phrase naturally.
- **Heading hierarchy** is clean — one H1, logical H2/H3, no skipped levels.
- **Keyword placement** — primary keyword appears in title, an early paragraph, and at least one subhead, without stuffing.
- **Internal-linking opportunities** — note 1-3 places where the user could link related posts (you can't know their archive, so suggest the anchor points).

### Fact-verification checks

- **No UNVERIFIED claim** from Stage 2 made it into the body as if it were fact. If one did, remove it, reframe it qualitatively, or flag it to the user.
- **No fabricated** statistics, studies, or quotes. Every number/quote traces to a real source.
- **Currency / freshness** — for Current and News-Based pieces, time-sensitive claims ("the latest", "currently", dates) reflect verified current info, not stale data. For Evergreen pieces, the reverse: no needless *absolute* date-stamps (a specific year, a named current-year version) that will age it — though relative phrases like "this year" or "recently" are fine.

### Technical validation (for code/technical pieces — Dev.to, Hashnode, technical Medium/Ghost)

- **Code is syntactically plausible** and uses real, current APIs, functions, flags, and commands — not invented ones. You can't execute it here, so verify against documentation where possible and **flag anything you can't confirm** rather than presenting it as certain.
- **Commands and config** are real and correctly formed (right flags, right syntax for the named tool/version).
- **Versions / compatibility** — any version-specific claim ("as of vX", "this works in Y") is checked, not assumed.
- **Steps actually work in sequence** — a tutorial's steps don't reference something not yet created, and the order is runnable.
- When something can't be verified, say so in the piece ("verify against your version") rather than asserting it confidently.

### Readability checks

- **Sentence length** varies; no run of long, clause-heavy sentences. Break them up.
- **Paragraph length** mostly 2-4 sentences (platform-appropriate); no walls of text.
- **Heading structure** breaks the piece into scannable sections at the platform's cadence.
- **Passive voice** isn't overused — prefer active where it reads stronger.
- **Repetition** — no phrase, sentence-opener, or point repeated. Watch for the same word starting several paragraphs.

### Humanization + fluff checks (catch the AI tells)

- **Natural transitions** — sections connect like a person wrote them, not "Furthermore / Moreover / In conclusion" scaffolding.
- **Conversational flow** — reads aloud naturally for the platform's register.
- **No AI clichés** — cut "In today's fast-paced world", "It's worth noting", "Let's dive in", "game-changer", "delve into", "Leadership isn't about…" openers, gratuitous em-dashes.
- **Fluff detection** — cut sentences that say nothing, padding added to hit a length, and restatements of the obvious. Every sentence must earn its place; if removing it loses nothing, remove it. Empty intensifiers ("very", "really", "incredibly") and hedge-stacking ("it could perhaps potentially") are fluff.
- **No generic filler** — no hollow throat-clearing, no "this is important because it's important" loops.
- **No repetitive phrasing** — varied vocabulary and sentence shapes, not a uniform rhythm.

Readability and humanization are partly judgment calls — read a sample aloud mentally. Stage 5 does the actual polish; here you're flagging what needs it.

## When something fails — fix in place OR regenerate

Each failure falls into one of two kinds. Decide which, then act:

**Local fix (patch in place).** The piece is fundamentally right and one field is out of bounds. Trim tags to the max keeping the strongest, shorten an over-length SEO title, tighten a hook that runs a few chars past the fold, add a missing field, fix prose that landed in a YAML value. Apply the fix, then re-run the checklist on the affected items.

**When the user explicitly asked for the out-of-bounds thing.** If a limit is broken because the *user* demanded it ("make it 3000 words" on a beehiiv brief, "use these 8 tags" on Dev.to's max-4), don't silently override them. Surface the conflict: state the platform's limit and why it exists, then let them choose — keep their request (and note it may not fit the platform's norms or may be rejected by the platform, e.g. Dev.to will only accept 4 tags), or adjust to fit. For *hard platform limits the platform technically enforces* (Dev.to 4 tags), explain it can't exceed that and trim. For *soft norms* (ideal length), the user can override with eyes open. Honor explicit intent; just make the tradeoff visible.

**Structural failure (go back to Stage 3 and regenerate).** The problem isn't one field — the piece doesn't fit the platform. Signs: the hook *concept* can't be made to land in the platform's limit without losing its point; the length is far off the target (e.g. a 2,400-word essay submitted as a beehiiv brief, or a 350-word stub for a Medium deep-dive); the structure is wrong for the platform (flowing essay where blocks are required, no framework where LinkedIn needs one); the voice doesn't match. **Don't paper over these with edits.** Return to `pipeline/3-generate.md`, regenerate the affected part (or the whole piece) against the platform spec, then run Stage 4 again from the top.

### The loop

1. Run the full checklist.
2. If everything passes → proceed to Stage 5.
3. If only local issues → fix in place, re-check the affected items, then proceed.
4. If any structural issue → go back to Stage 3, regenerate, return to step 1.
5. Cap at **2 regeneration passes.** If it still doesn't fit after two, stop looping and tell the user plainly what won't fit and why (e.g. "this topic genuinely needs ~1,500 words, which is long for a beehiiv brief — want it as a Medium piece instead, or split into two issues?"). Don't silently ship something that fails, and don't loop forever.

For programmatically checkable things (character counts, tag counts), actually count rather than eyeballing — write the count out. Example: "SEO title: 54 chars ✓ (limit 60)", "Tags: 5/5 ✓", "Subject line: 38 chars ✓ (limit 40)".

## Output of this stage

A short pass/fix summary (you'll surface a condensed version to the user in Stage 5) and a draft that now satisfies every hard requirement. Proceed to `pipeline/5-review.md`.
