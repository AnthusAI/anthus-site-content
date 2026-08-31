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

Write like a person talking to a peer. Smoother, more accessible, more engaging, more open than formal essay-speak. Use contractions: It's, don't, we're, that's. Never It is when It's is what you mean. Pithy. No emojis.
