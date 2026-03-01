# Stage 3 — Generate

Goal: write the full, publish-ready piece **plus all required metadata**, tuned to the platform.

## Load your inputs

1. Read `references/universal-craft.md` — the writing fundamentals that apply everywhere.
2. Read the chosen platform's spec file in `platforms/` in full — both its **Craft Rules** and its **Data Requirements**.
3. Have your Stage-1 brief (platform, topic, audience + **knowledge level**, **goal, content type, freshness**, CTA goal) and Stage-2 content brief (verified facts, fresh angle, keyword) in hand.

## Calibrate to Audience Knowledge Level

The **knowledge level** from Stage 1 sets how much you explain: **Beginner** — define terms on first use, give background, use analogies, don't assume prior context. **Intermediate** — assume working familiarity, skip the 101, focus on the non-obvious. **Expert** — assume fluency, go deep, don't over-explain or pad with basics they'll find patronizing. Match this to the audience or the piece either loses beginners or bores experts.

## Let Content Type drive structure

The **content type** from Stage 1 sets the article's skeleton; the platform's craft rules then style it. Don't default everything to a generic essay shape. Rough structures:

- **How-To Guide / Tutorial** — problem → prerequisites → numbered/sequential steps → common pitfalls → result. Tutorials lean heavier on exact steps and (for dev platforms) working code.
- **Opinion / Thought Leadership** — claim → why it matters now → argument with evidence → counterpoint → takeaway. Voice-forward.
- **Case Study** — context/challenge → what was tried → what happened (with real numbers) → lessons.
- **Comparison** — criteria up front → option-by-option (often a table) → when-to-use-which → verdict.
- **Listicle** — tight intro → N substantive items (each earns its place) → synthesis, not just a list.
- **Research Summary** — what was studied → key findings → what it means → caveats.
- **Industry Analysis** — the shift → evidence/data → implications → outlook.
- **News Commentary** — what happened (brief) → the angle others miss → why it matters.

## Let Content Goal shape emphasis

The **goal** tilts the same structure: *Build Authority* → depth, original insight, credible sourcing. *Generate Leads / Promote* → a clear value-led path to the CTA (still value-first, never spammy). *Increase Engagement* → a stronger question/hook and a conversation-driving close. *Educate/Inform* → clarity and completeness. *Drive Traffic* → tighter SEO framing on title/description. Keep it honest — goal shapes emphasis, it doesn't license hype.

## Write the body

Combine universal craft + the platform's craft rules + content-type structure + goal emphasis + your researched material. Specifics:

- **Open with the platform's hook style.** Each platform spec defines what the opening must do (Medium's 3-line hook, LinkedIn's pre-fold ≤210 chars, beehiiv's lead story). Get this right first — it decides whether anyone reads on.
- **Match the platform's structure and length target.** Don't pad to hit a number; don't truncate a topic that needs room.
- **Use the researched specifics.** Drop in the named examples, real numbers, and fresh angle from Stage 2 — only the *verified* ones. This is what makes it not-generic.
- **Write in the platform's voice** (and the user's voice if samples were given). Sound human — vary sentence length, avoid templated-AI tells.
- **End with the platform's CTA style** (comment prompt, subscribe nudge, reply invite — whatever fits how that platform grows and the goal).

## Generate ALL required metadata

From the platform spec's Data Requirements block, produce every required field, respecting each limit exactly. Typically this includes some of:

- **Title / headline** — to the platform's headline rules.
- **Subtitle / subhead / excerpt** — where the platform has one.
- **SEO title** and **SEO/meta description** — within the platform's character limits (these often differ from the display title; some platforms truncate at ~60 chars title / ~156 desc).
- **Tags** — the right number, never exceeding the max (Medium 5, Dev.to 4, etc.), relevant and as-popular-as-makes-sense.
- **Cover/feature image** — keep the image *URL field* and the image *guidance* separate. The platform's URL field (e.g. Dev.to's `cover_image:`) must contain only a real URL or a clean placeholder like `<image URL — see options below>` / be left blank — never prose, or it breaks the paste. Below the metadata block, give the user a **"Cover image" section with three options** (in this order), so they can grab one fast and licensing-safe:
  1. **Find a free, licensable image** — provide 1-2 **ready-to-click search links** to free-to-use-commercially stock sources, pre-filled with a query that fits the cover concept and the platform's aspect ratio. Use these URL patterns (no API needed): Unsplash `https://unsplash.com/s/photos/<query>`, Pexels `https://www.pexels.com/search/<query>/`, Openverse `https://openverse.org/search/?q=<query>` (Openverse is good for explicitly CC-licensed results). Pick a query of 1-3 concrete nouns from the article's core idea. **Do not** paste an arbitrary image URL from a normal web search and tell them to publish it — most are copyrighted; point them at free-stock sources instead.
  2. **Generate an original** — if the environment can generate images, offer to create a custom cover to the platform's dimensions from the brief. Only generate if the user asks; the default deliverable stays a clean paste-ready file.
  3. **Brief (always include as fallback)** — the creative brief: exact dimensions for the platform, alt text, and a one-line description of what the image should show, so they can make or commission one.

  Match the image to the platform: e.g. Dev.to/Hashnode favor a clean technical or abstract-tech cover at 1000×420; LinkedIn 1200×644; Ghost/Medium 1200×630 landscape. Keep the cover concept on-topic, not a generic stock cliché (a literal "person at laptop" rarely helps). **Default behavior: always include the free-stock search link(s) (option 1) and the brief (option 3); offer option 2 (generate an original) as a one-line suggestion — only actually generate if the user asks.**
- **Canonical URL** — use the user's if cross-posting; otherwise note it's left blank for the original.
- **Slug** — keyword-friendly where the platform uses one.
- **Front matter** — for Dev.to/Hashnode, output the actual YAML front matter block ready to paste.

If a field genuinely needs the user (a canonical URL you don't have), output a clear placeholder like `canonical_url: <your original post URL>` rather than inventing one.

## Suggested visual assets

Modern content performs better with supporting visuals. Beyond the cover image, add a short **"Suggested visuals"** list to the metadata block — what would strengthen this specific piece and roughly where it goes. Draw from: hero image, diagrams (for processes/architecture), charts (for data/comparisons), tables (for structured comparisons — and actually include the table in the body where it fits), screenshots (for tutorials/how-tos), infographics (for summaries). Suggest only what genuinely helps; don't pad.

For each suggested visual, point the user to the fastest safe way to get it: a **free-stock search link** (Unsplash/Pexels/Openverse, query pre-filled) for photos; an offer to **generate** it if the environment supports image generation and it's an original graphic; or a note that a **diagram/chart/table** is best built by the user (and include any table directly in the body). Don't hand over copyrighted image URLs from general web search.

## Output of this stage

The complete draft + a metadata block with every required field filled to spec. Proceed to `pipeline/4-validate.md` before showing the user — do not deliver an unvalidated draft.
