# Anth.us site content

MDX articles, posts, solutions, images, and PlantUML diagrams for [anth.us](https://anth.us).

This repository is a **git submodule** at `src/site-content` in [AnthusAI/Anth.us](https://github.com/AnthusAI/Anth.us). The Gatsby site owns templates, components, and build tooling; this repo owns publishable content only.

## Layout

- `*.mdx` — long-form articles
- `posts/` — short posts
- `solutions/` — case studies
- `images/` — article and post images
- `diagrams/` — PlantUML sources

## Publishing

1. Push to `main` on this repo.
2. GitHub Actions syncs content to the configured S3 bucket (`ANTHUS_SITE_CONTENT_BUCKET`).
3. Optionally triggers an Amplify rebuild via `ANTHUS_AMPLIFY_WEBHOOK_URL`.

For local development, clone Anth.us with submodules:

```bash
git clone --recurse-submodules https://github.com/AnthusAI/Anth.us.git
cd Anth.us && npm start
```

## Editorial process

Story workflow and Kanbus board live in [anthus-semantic-knowledge-base](https://github.com/AnthusAI/anthus-semantic-knowledge-base), checked out separately or via Papyrus at `pods/anthus-blog`.


## Voice

House voice: parent `AGENTS.md` Editorial Guidelines (in the `Anth.us` site repo, one level up from this submodule). Chatticus is a separate site with its own voice — `Chattic.us-web/content/VOICE.md` does not apply here. The automated editorial-diagnose pipeline (Papyrus) also encodes this voice as a checkable profile: `publications/anthus/style-profile.yml`. Field-coverage / receipts articles use the **Agent Zoo** posture there (wonder from specifics) — no Agent Zoo desk on anth.us.

- **Wonder from specifics.** Curious and alive about what people and bots actually ship — numbers and named moves, not hype.
- Warm communal register; Anthus is a participant, not a press office.
- Confident and aspirational: no "coming soon" / "we're early" hedging. Claims must be checkable.
- At most one "X, not Y" contrast per piece.
- Write like a person talking to a peer. Contractions: It's, don't, we're, that's. Pithy. No emojis.
- **Articles never refer to themselves.** No "this article", "this post", "the rest of this piece", and no "below"/"above" as page references. Say the thing, or use a plain transition ("The measurements come first.").
- **Flagship stories open for a general reader.** First screen: the scenario, who it hurts, the one number; technical terms and product names after the picture, and the technical detail in linked drill-downs.
- **Plain statements on first read.** A sentence says what it means without asking the reader to decode it. Cut the line that performs insight instead of delivering it: the aphorism that equates a concrete thing with an abstraction ("The scorecard is the contract."), the fragment pair ("Not a demo. A habit."), the closing tag that announces a point was made instead of making it ("That's the whole argument."), and the reversal staged as a discovery ("The bug wasn't in the model. It was in the question."). These borrow the cadence of a shorthand the reader never agreed to, so they land as uncanny rather than memorable. The test: a reader outside the company can restate the sentence in plain words without guessing at what it alludes to. If the plain restatement is clearer, use it. If there is no plain restatement, the line was decoration.
- **Composites are labelled.** A persona that makes a measurement concrete is allowed when the author approves it and the text says it is a composite; it carries only measured facts and no real name.
