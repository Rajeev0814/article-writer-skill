# Platform spec format

Every file in `platforms/` follows this shape. To add a platform, copy this structure and fill it in. Two required sections: **Craft Rules** and **Data Requirements**.

## Template

```markdown
# <Platform Name>

<1-2 sentence orientation: what kind of platform, who reads it, and the ONE
growth/discovery mechanic that matters most.>

## Craft Rules

### Headline / hook
<The headline or opening convention and any length/format rules.>

### Structure
<How the piece is organized: subheading cadence, blocks vs. essay, section
template, paragraph length.>

### Length
<Target word count or range, and cadence norms.>

### Voice
<Tone and POV that fits the platform.>

### Growth mechanic
<The specific thing that drives reach on this platform and how the piece should
serve it — curation, Notes, subject-line opens, the feed's "see more" fold, etc.>

### Call to action
<What the ending should do, in this platform's style.>

## Data Requirements

A table of every metadata field the platform needs to publish, with limits.
Mark each Required or Optional. This block feeds Stage 1 (intake) and Stage 4
(validation). Be precise about numbers — they are checked.

| Field | Required? | Limit / spec | Notes |
|-------|-----------|--------------|-------|
| Title | Required | <chars> | ... |
| Tags | Required | max <N> | ... |
| SEO title | Optional | ≤60 chars | ... |
| Meta description | Optional | ≤156-160 chars | ... |
| Cover image | Optional | <W×H> | ... |
| Canonical URL | Optional | URL | for cross-posting |
| ... | | | |

### Paste-ready format
<If the platform ingests a specific block — e.g. YAML front matter — show the
exact template so Stage 3 can output it ready to paste.>
```

## Publishing format

<State whether the platform is **markdown-native** (body pastes and renders) or
a **rich-text editor** (raw markdown shows as literal characters). Say where the
metadata goes: inline/front-matter vs. entered in the editor's settings panel.
This drives Stage 5's "how to publish" line and how the metadata block is labeled.>
```

## Notes for authors

- **Data Requirements is what makes this skill more than a writing prompt.** Get the numbers exactly right — they're validated in Stage 4. When in doubt, verify against the platform's current docs.
- Keep each file focused; the pipeline reads the whole file during Stage 3, so don't bloat it.
- The "growth mechanic" line is high-value — it's the thing most generic writing advice misses and what makes the output feel native to the platform.
