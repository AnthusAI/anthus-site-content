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

House voice: `Chattic.us-web/content/VOICE.md`. Full Anth.us rules in parent `AGENTS.md` Editorial Guidelines. Field-coverage / receipts articles use the **Agent Zoo** posture there (wonder from specifics) — no Agent Zoo desk on anth.us.

- **Wonder from specifics.** Curious and alive about what people and bots actually ship — numbers and named moves, not hype.
- Warm communal register; Anthus is a participant, not a press office.
- Confident and aspirational: no "coming soon" / "we're early" hedging. Claims must be checkable.
- At most one "X, not Y" contrast per piece.
- Write like a person talking to a peer. Contractions: It's, don't, we're, that's. Pithy. No emojis.
