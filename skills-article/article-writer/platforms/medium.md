# Medium

A long-form blog network that rewards depth, originality, and quality. The growth engine is **curation + the first 72 hours**: strong early read-through and engagement can push a piece into the main feed and reach far beyond your followers, even from zero followers. Medium also has strong Google domain authority, so SEO fields matter for long-tail search traffic.

## Craft Rules

### Headline / hook
- The headline is a framing device, not a summary — it should make the reader pause and want to resolve a tension, without feeling like clickbait (2026 readers scroll past anything manipulative).
- Work a searchable long-tail phrase in when natural; ask "would anyone search this exact phrase?" Avoid brutally generic phrases.
- Always pair it with a **subtitle** (the deck) that extends the promise and reinforces the keyword.
- The first 2-3 sentences (the three-line hook) must land the problem or promise — this decides read-through.

### Structure
- H2 subheadings every ~300-500 words; scannable.
- Short paragraphs, 2-4 sentences.
- A clear setup → development → payoff arc; curators reward intentional, complete pieces.
- Use pull quotes, bold, lists, and images semantically to vary rhythm.

### Length
1,500-3,000 words is the sweet spot. The algorithm favors substantial long-form; depth is what gets curated. Don't pad.

### Voice
Personal and authoritative — unique insight, lived experience, or original research, not recycled advice. Actionable: the reader leaves with something concrete.

### Growth mechanic
**Curation.** Optimize for originality, depth, polish, and genuine value; avoid clickbait, promo, SEO-spam feel, and generic listicles. Strong early engagement (claps, comments, read-ratio) in the first 72 hours feeds the algorithm.

### Call to action
Close with a reflection or question that invites comments and claps (engagement feeds curation). Soft follow/related-read prompt is fine; no hard selling.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Title (display) | Required | concise, intrigue + clarity | shown on Medium itself |
| Subtitle | Required | 1 line | the deck under the title; reinforces keyword |
| Tags | Required | **max 5** | relevant + as-popular-as-sensible; each is a discovery surface |
| Feature/preview image | Recommended | landscape, high-res | with alt text |
| SEO title | Optional | **≤60 chars** | Google truncates beyond ~60; can differ from display title; front-load keyword |
| SEO description | Optional | **≤156 chars** core, up to 200-300 total | main idea within first 156; Google auto-generates if blank |
| Custom story link (slug) | Optional | keyword-friendly | set via More options |
| Canonical URL | Optional | URL | set if the piece was first published elsewhere |

### Notes
- SEO title/description are set under the draft's "More settings → SEO Settings" and are separate from the display title/subtitle. Generate both; they can differ (display = expertise/curiosity for Medium readers; SEO = search-intent phrasing).
- Use all 5 tags — each is a separate way to be discovered.

## Publishing format

Medium uses a **rich-text editor** — pasted markdown does NOT render (`##` and `**` show as literal characters). In the delivered file: keep the body as clean markdown for readability, but tell the user to paste the body into Medium's editor and apply formatting there (or paste from a rendered source), and to enter **Tags, SEO title, SEO description, and canonical URL in Medium's own fields** (the "..." → More settings panel), not in the body. The metadata block in the file is a checklist of what to set, not something to paste into the post body.
