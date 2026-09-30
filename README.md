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
- **Plain statements on first read.** Every sentence says what it means the first time a reader outside the company reads it. Titles, excerpts, captions, and alt text included. The patterns to catch are listed under "Plain statements on first read" at the end of the voice section.
- **Composites are labelled.** A persona that makes a measurement concrete is allowed when the author approves it and the text says it is a composite; it carries only measured facts and no real name.

### Plain statements on first read

The most damaging tell in machine-drafted copy is prose that imitates the texture of a person writing without carrying the content. It reaches for idioms, metaphors, and knowing phrases, assembles them slightly off, and leaves the reader to work out what was meant. The intent is to sound fluent and insider. The effect is the opposite: it reads as performed rather than said, and readers register that before they can name it. A sentence that sounds good and says nothing is worse than one that sounds ordinary and says something.

The patterns, so they can be caught in new copy:

- **Metaphor in place of the fact.** "The calibration became the weather" instead of "the calibration drifted a little each week." A comparison is allowed only after the plain fact is on the page and only if it makes the fact easier to picture. A fact in the next sentence does not rescue a metaphor in the opening paragraph, title, or excerpt: a reader who meets the metaphor first leaves before the fact arrives.
- **Character traits for measurements.** Confidence isn't "honest," a model doesn't "admit" or "know," and a score doesn't "tell the truth." Name the measurement and what it means for the reader: "when it says 90 percent, it's right about 90 percent of the time." After that sentence has appeared, "calibrated" is fine.
- **Abstract noun doing a person's job.** "The arithmetic had her as a side effect", "the pipeline learned to hesitate." Name who did what.
- **The aphorism that equates a concrete thing with an abstraction.** "The scorecard is the contract." Say what the scorecard does.
- **Riddle closers.** A short last line that sounds final and has to be decoded: "That's the whole argument." "What had collapsed was the bill." If the paragraph has a point, state the point.
- **Fragment pairs.** "Not a demo. A habit." Slogans, not sentences. Join them with a verb.
- **Borrowed idiom used slightly wrong.** Trade slang or catchphrases dropped in to sound native. If you wouldn't say it aloud to a client's CFO, don't write it.
- **Mannered compression.** Skipping a step so the sentence sounds terse: "He had never spat in a tube. People who shared his blood had." Write the missing step.
- **The reversal staged as a discovery.** "The bug wasn't in the model. It was in the question." Allowed once per piece, and only when it is literally true.

The test before publishing: a reader who has never seen this site can restate each sentence in plain words without guessing at what it alludes to. If the plain restatement is clearer, use it. If there is no plain restatement, the line was decoration. Limatus runs a partial version of this check from the Anthus style profile; the rest is the editor's job.
