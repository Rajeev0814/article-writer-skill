# Hashnode

A developer blogging platform where every post belongs to a publication (e.g. `username.hashnode.dev`). Like Dev.to it's tag-feed driven — users follow technology tags during signup and see tagged posts in their feed — but it's more blog-like, with first-class SEO controls (separate meta title/description, slug, canonical via `originalArticleURL`).

## Craft Rules

### Headline / hook
- Clear, keyword-bearing titles. Lead with the primary keyword where natural, and use it in the title, slug, and meta description. Short, scannable titles tend to win on CTR, but don't truncate clarity to chase a character count — a clear longer title beats a cramped keyword-stuffed one.
- Open with the concrete problem and the payoff.

### Structure
- Title is the H1; use H2 for main sections and H3 for sub-sections (don't reuse H1 in the body).
- Code blocks with language tags, images to break up long text (every article should have at least a cover image), embedded widgets where useful.
- Internal links to related posts in the same publication pass authority and aid discovery.

### Length
Flexible; substantive technical depth performs best. A focused tutorial or a longer deep-dive both work — match the topic.

### Voice
Practical and authoritative; developer peer-to-peer. Accuracy first. Show experience and working examples.

### Growth mechanic
**Tags + SEO.** Tags route the post to followers of those technologies; strong on-page SEO (keyword in title/slug/meta, internal links, cover image for the social card) drives durable search traffic. Cross-post with `originalArticleURL` set to the canonical source.

### Call to action
Invite discussion or point to related posts/series. A newsletter subscribe prompt fits if the user runs one.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Title | Required | keyword-bearing; clear over short | the H1 |
| Subtitle | Optional | 1 line | shown under the title |
| Tags | Required | up to ~5, by `slug` + `name` | route to tag-followers; use `{ slug, name }` form |
| Cover image | Recommended | landscape, high-res | needed for an appealing social card; default is bland |
| Slug | Recommended | keyword-friendly | include the target keyword |
| SEO meta title | Optional | ≤60 chars | set via `metaTags`; can differ from display title |
| SEO meta description | Optional | ≤156-160 chars | set via `metaTags`; defaults to subtitle if blank |
| Canonical URL | Optional | URL via `originalArticleURL` | the writable field for canonical (not the read-only `canonicalUrl`) |
| Series | Optional | series name | for ordered multi-part content |

### Notes
- Generate the meta title + description explicitly (don't rely on defaults) — they drive search CTR.
- Always include a cover image brief (dimensions + alt + what it depicts), since the social card is much weaker without one.
- If cross-posting, set canonical via `originalArticleURL`.

## Publishing format

Hashnode is **markdown-native** for the body — paste the markdown body straight into the editor and it renders. Some metadata is set in the editor UI rather than front matter: **Tags, Slug, SEO meta title/description, cover image, and the canonical (`originalArticleURL`)** go in Hashnode's "Article Settings" / draft settings panel. The delivered file's metadata block lists exactly what to enter there.
