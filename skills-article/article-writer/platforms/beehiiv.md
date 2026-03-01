# beehiiv

An email-first newsletter platform. The piece lands in an inbox competing with dozens of others, and over half of opens are on mobile. The **subject line** is make-or-break, the body must be scannable in blocks, and every issue drives one clear action. Top newsletters here run like media companies: consistent format, strong hooks, a reason to keep showing up.

## Craft Rules

### Headline / hook (subject line decides the open)
- **Keep it short** — under 40 characters performs best; the highest open rates skew under ~20. Mobile clients cut off after 30-40 chars.
- **Front-load the best part** — value prop or curiosity gap in the first ~30 chars.
- **Specific numbers beat vague promises** — "5 mistakes" destroys "common mistakes."
- Proven patterns: the Mistake ("The [common practice] mistake costing you [outcome]"), the Contrarian Take ("Why [common advice] is wrong about [topic]"), specific results/numbers, time-sensitive framing.
- Emojis only if judicious; avoid spam-trigger phrases.
- Generate **5-10 subject-line options** — treat them as A/B tests, not one-shot creative.

### Structure
- Built in **blocks**, not flowing essays. Open with a striking header/hook, then lead with the top-of-mind story as the first item.
- Clear sections with concise copy and semantic formatting (headings, lists, callouts, content breaks). Don't skip heading levels.
- Tight and skimmable; reduce cognitive load. A consistent recurring template builds the habit loop.

### Length
Flexible, format-dependent. Many beehiiv issues are short-to-medium and highly scannable (a few hundred to ~1,200 words). Match length to the format (daily brief = short; weekly deep-dive = longer). Favor density over padding.

### Voice
Direct, useful, consistent with the newsletter's persona. Value-forward — each issue must earn the open. Segment-aware language signals relevance.

### Growth mechanic
**The subject line (opens) + the recurring format (habit).** Opens are the top of the funnel; a familiar, reliable structure keeps subscribers reading week over week. beehiiv's A/B testing rewards multiple subject-line options.

### Call to action
Always include **one clear, obvious, singular CTA** — decide the goal before structuring (visit site, reply, register, upgrade). Competing CTAs dilute action.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Subject line | Required | **≤40 chars** (best ≤20), front-loaded | the single highest-leverage element |
| Preview/preheader text | Recommended | ~40-100 chars | the line shown after the subject in the inbox; extend the hook |
| Title / headline (in-body) | Required | concise | the issue's top header |
| Section headers | Recommended | clean hierarchy | for block structure |
| Primary CTA | Required | one, explicit | button or clear link with a single goal |
| Cover/header image | Optional | responsive, mobile-safe | preview on mobile before relying on it |
| SEO title / meta description | Optional | ≤60 / ≤160 | only if the issue is also published to the web archive |

### Notes
- Provide a set of subject-line options plus the recommended one.
- Always include the preheader — it's wasted real estate if left default.

## Publishing format

beehiiv uses a **block / rich-text editor**; raw markdown won't render. Set the **subject line and preheader** in the email's send settings (not the body). Build the body as blocks in the editor and place the single CTA as a button/link. The delivered file's metadata block is a checklist of fields to enter, not body content.
