# Dev.to

A developer community (built on Forem). Discovery is tag-feed driven — users follow tags, and articles surface to people following those tags. Readers are technical and value accuracy, working code, and practical depth over polish. It ingests Markdown with **YAML front matter**, so the metadata is part of the paste-ready output.

## Craft Rules

### Headline / hook
- Clear, specific, benefit- or problem-oriented titles work best ("How I cut our CI time from 22 to 4 minutes" beats "Thoughts on CI"). Developers scan for relevance.
- Open with the concrete problem and what the reader will be able to do by the end. Skip the long preamble.

### Structure
- Liberal use of H2/H3 headings, fenced code blocks (with language tags), and inline code.
- Show real, runnable code and command output. Explain the why, not just the what.
- Lists, callouts, and embedded gists/tweets/GitHub links are well-supported and encouraged for skimmability.

### Length
Flexible — from a focused 500-word tip to a 2,000+ word deep dive. Match the topic; developers tolerate length when it's substantive and code-backed.

### Voice
Practical, peer-to-peer, no fluff. First-person experience ("here's what worked") lands well. Accuracy is non-negotiable — wrong technical claims get called out in comments.

### Growth mechanic
**Tags + community engagement.** The right tags put the piece in front of the people who follow them. Genuine, non-promotional value earns reactions (hearts/unicorns/bookmarks) and comments. Cross-post with a `canonical_url` pointing to the original to protect SEO.

### Call to action
Invite discussion (a real question), point to a repo, or ask what readers would do differently. Avoid purely promotional CTAs — the community and content policy disfavor them.

## Data Requirements

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| `title` | Required | concise, specific | front-matter field |
| `published` | Required | `true` / `false` | set `false` for draft; flip to publish |
| `tags` | Required | **max 4**, comma-separated | lowercase, no spaces; e.g. `javascript,webdev,tutorial` |
| `description` | Recommended | ~1 sentence, ≤~150 chars | used in Twitter/OG cards |
| `cover_image` | Optional | URL, **best 1000×420** | must end in an image extension |
| `canonical_url` | Optional | URL | set if first published elsewhere — protects SEO |
| `series` | Optional | series name | keep consistent across a multi-part series |

### Paste-ready front matter
Output this block at the very top of the file, ready to paste into the Dev.to Markdown editor:

```yaml
---
title: <title>
published: false
description: <one-line description>
tags: <tag1>,<tag2>,<tag3>,<tag4>
cover_image: <image URL, or leave this value blank — never put a prose description here>
canonical_url: <original URL if cross-posting, else omit this line>
series: <series name if applicable, else omit this line>
---
```

- **`cover_image` takes a URL only.** Put the image creative brief (what it should depict + alt text) in the metadata block above the front matter, not in this value — prose here breaks the paste.
- **Hard rule: never exceed 4 tags.** Validation must enforce this.
- Leave `published: false` so the user reviews before going live.

## Publishing format

Dev.to is **markdown-native**: the entire delivered file (YAML front matter + markdown body) pastes directly into the Dev.to markdown editor and renders correctly — including tags, description, cover_image, and canonical_url via the front matter. This is a true copy-paste-and-publish flow. Just remind the user to flip `published: false` → `true` when ready.
