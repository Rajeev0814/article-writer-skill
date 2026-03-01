# Ghost

A self-hosted / Ghost(Pro) publication platform — blog + membership + email newsletter in one. Unlike the community platforms, there's no shared discovery feed; reach comes from **your own SEO, email list, and on-site navigation**. So on-page SEO metadata and a strong excerpt/feature image matter a lot — they drive both search ranking and the social/email card.

## Craft Rules

### Headline / hook
- A clear, keyword-aware post title that works as both the on-page H1 and the basis for search. Ghost defaults the meta title to the post title and meta description to the excerpt, but you should set both deliberately.
- Open with the problem/payoff; no long warm-up.

### Structure
- Title is H1; H2/H3 for sections. Use Ghost cards (callouts, bookmarks, galleries, code) where they help.
- Images need descriptive alt text (Ghost supports it) — both for accessibility and SEO.
- Internal links to related posts aid navigation and authority since there's no external feed doing discovery.

### Length
Flexible; depends on the publication's style (a membership essay site vs. a tutorial blog). Match the topic and the publication's established rhythm.

### Voice
Consistent with the publication's brand and audience. Can range from personal-newsletter to authoritative-blog — take cues from the user's existing voice or samples.

### Growth mechanic
**Owned SEO + email.** No algorithmic feed, so durable search traffic (clean meta title/description, keyword in slug, internal links, alt text) and the member email send are the engines. The feature image is the social + email card, so it carries weight.

### Call to action
Drive the publication's goal: subscribe/become a member, reply, or read a related post. Make it explicit.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Title | Required | clear, keyword-aware | the H1; also default meta title |
| Excerpt | Recommended | ~1-2 sentences | shown in lists + defaults the meta description; set it deliberately |
| Tags | Recommended | 5-10 typical | Ghost tags organize content + power navigation; first tag often = primary |
| Feature image | Recommended | landscape (1200×630 social-safe) | the social + email card; include alt text |
| Meta title (SEO) | Optional | ≤60 chars | set under post Settings → Meta data; override the default to avoid duplicate H1/title |
| Meta description (SEO) | Optional | ≤156-160 chars | set deliberately; don't let it auto-fill from body |
| Canonical URL | Optional | URL | set under Meta data if republished |
| Slug (URL) | Recommended | keyword-friendly | editable per post |
| Twitter/Facebook card title+desc | Optional | per-network override | available under post settings for social tuning |

### Notes
- Explicitly set meta title AND meta description — relying on the defaults (title + excerpt) is a common, ranking-costing miss, and an identical H1/meta-title can read as over-optimized.
- Provide a feature-image brief (dimensions + alt + what it depicts).

## Publishing format

Ghost's editor is **rich-text** (it can import markdown, but the live editor renders it). Paste/import the body, then set **Excerpt, Meta title, Meta description, Canonical URL, Slug, Tags, and Feature image** under the post's Settings → Meta data panel — not in the body. The delivered file's metadata block maps directly to those settings fields.
