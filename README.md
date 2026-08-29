# Anth.us blog content

MDX articles, posts, solutions, images, and PlantUML diagrams for [anth.us](https://anth.us).

This repository is a **git submodule** at `src/blog` in [AnthusAI/Anth.us](https://github.com/AnthusAI/Anth.us). The Gatsby site owns templates, components, and build tooling; this repo owns publishable content only.

## Layout

- `*.mdx` — long-form articles
- `posts/` — short posts
- `solutions/` — case studies
- `images/` — article and post images
- `diagrams/` — PlantUML sources

## Publishing

1. Push to `main` on this repo.
2. GitHub Actions syncs content to the configured S3 bucket (`ANTHUS_BLOG_CONTENT_BUCKET`).
3. Optionally triggers an Amplify rebuild via `ANTHUS_AMPLIFY_WEBHOOK_URL`.

For local development, clone Anth.us with submodules:

```bash
git clone --recurse-submodules https://github.com/AnthusAI/Anth.us.git
cd Anth.us && npm start
```

## Editorial process

Story workflow and Kanbus board live in [anthus-semantic-knowledge-base](https://github.com/AnthusAI/anthus-semantic-knowledge-base) (mounted at `newsroom/` in the site repo).
