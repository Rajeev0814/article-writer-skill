# LinkedIn Post

A short native post in the LinkedIn feed — distinct from a LinkedIn *newsletter* (`linkedin.md`). It's a single text update (no title, no separate body/headline) that lives in the professional feed and competes for attention scroll-by-scroll. The 2026 algorithm rewards **dwell time and comments** over raw reach, and the "see more" fold is the make-or-break moment: most of the post is hidden until the reader clicks. Every post should teach, prove, or humanize in a way a professional audience finds worth pausing on.

## Craft Rules

### Headline / hook
There's no title field — **the first 1-2 lines ARE the post**, all the reader sees before the "see more" fold. This is the single most important element.
- Mobile truncates around **~140 characters**, desktop around **~210**. Write the hook to land within the **mobile ~140-char cutoff** so it works for both.
- Open with a bold statement, a surprising statistic, a relatable question, or a stakes-laden line. "I got fired 3 times before 30. Here's what I learned" beats "I want to share some career advice."
- Never open with "I'm excited to announce…" / "Happy to share…" — it wastes the most valuable real estate. Lead with the insight, not the announcement.
- Avoid generic AI-tell openers ("Leadership isn't about…").

### Structure
- **Very short paragraphs — 1-2 sentences each — with a blank line between them.** LinkedIn readers scan vertically; dense blocks get skipped. No single wall of text.
- A reliable arc: hook (pre-fold) → setup/stakes → 3-5 short value beats or a mini-story → a payoff line → CTA.
- Line breaks and whitespace are the formatting. Optional: 2-5 emojis as visual bullets/breaks (kept professional), and Unicode bold sparingly for emphasis (Unicode formatting doesn't add to the character count beyond the styled characters).
- One idea per post. It should be sayable in a sentence.

### Length
- **Hard limit: 3,000 characters** (everything counts — letters, spaces, emojis at ~2 chars each, hashtags including the # symbol). Going over truncates your CTA/punchline.
- **Engagement sweet spot: ~1,300-2,000 characters.** Long enough to tell a real story or land a genuine insight, short enough to respect the scroll. Shorter posts can work for a single punchy take, but the data favors this range for starting conversations. Don't pad to hit it.

### Voice
Professional but human — real stories and specific stakes over abstract advice. First-person and conversational. Write for one specific reader/niche, not "every professional." Authority + authenticity.

### Growth mechanic
**The "see more" click + dwell time + comments.** The hook earns the click (itself an engagement signal the algorithm boosts); short scannable paragraphs hold attention; a question-based close drives the comments that the feed rewards most. 3-5 relevant hashtags roughly double reach vs. none — but they count against the character budget, so **stack them at the very bottom** so they don't push your core message past the fold. Best windows for professional audiences: Tue-Thu mornings.

### Call to action
End with a **question** that invites comments — comments and dwell time are what the algorithm rewards most. Keep it specific and easy to answer ("What's the one X you'd…?"). Avoid "link in comments" patterns that bury the value; if linking out, say so plainly.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Post body | Required | **≤3,000 chars total**; aim ~1,300-2,000 | the whole post — no separate title field |
| Hook (first 1-2 lines) | Required | land within **~140 chars** (mobile fold), ≤210 desktop | validated separately — the make-or-break field |
| Hashtags | Recommended | **3-5**, stacked at the very bottom | count toward the 3,000 limit; 2x reach vs none; >10 looks spammy |
| Emojis | Optional | ~2-5, professional | count as ~2 chars each; use as visual breaks, not decoration |
| Image/media | Optional | square 1080×1080 or 1200×627 landscape | a relevant image lifts dwell time; include alt text |
| Mentions (@) | Optional | as relevant | tag people/companies only when genuinely relevant |

### Notes
- There is **no title, subtitle, SEO, or canonical field** — a feed post has none of these. Don't generate them; the body is the whole artifact. (If the user wants SEO/metadata, they likely want a LinkedIn *newsletter* — use `linkedin.md`.)
- Validate two character counts explicitly: the **hook** (≤~140 mobile fold) and the **total post** (≤3,000). Both are easy to overshoot.
- Count emojis and hashtags toward the total — they're not free.

## Publishing format

LinkedIn's post composer is **plain text with Unicode formatting only** — there's no markdown, no rich-text headings. The delivered body should be ready to paste *as-is* into the composer: real line breaks between short paragraphs, hashtags stacked at the bottom, any emphasis applied as Unicode bold/italic (not `**markdown**`). Tell the user to paste the body straight into the "Start a post" box, attach the image if one's suggested, and check the hook isn't cut off in the preview before posting. There are no separate metadata fields to fill — the post body is the entire deliverable.
