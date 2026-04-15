<p align="center">
  <img src="assets/eb-logo.png" alt="EdibleByte" width="140">
</p>

# EdibleByte Prompts Library

A curated collection of specialized prompts for AI assistants (ChatGPT, Claude, and others), designed for real use in learning, thinking, writing, planning, and working with AI deliberately.

Each prompt is copy-paste ready — drop it into a new chat, fill in the bracketed `[PLACEHOLDERS]`, and iterate.

## Current contents

### Standalone prompts

- [`adaptive_tutor/`](adaptive_tutor/) — an adaptive, personalized tutoring system prompt that calibrates a full learning series to your subject, timeframe, and level.

### Prompt series

Companion prompt libraries for multi-part article series published on [ediblebyte.com](https://www.ediblebyte.com/publications) — which hosts links to the full catalogue of posts published on [LinkedIn](https://www.linkedin.com/in/koujala/) and [Substack](https://substack.com/@koujala). Each series folder here maps one-to-one to the posts of its source series.

- [`series_master_genai/`](series_master_genai/) — 30 reusable prompts drawn from the **Gen AI Mastery** series (9 articles). Covers prompting fundamentals, thinking partnerships, learning, writing, deep work, and professional workflows.

## How the repo is organised

**Standalone prompt folders** contain:
- A descriptively named prompt file (e.g. [`adaptive_tutor/tutor.md`](adaptive_tutor/tutor.md)) — the core prompt
- A `README.md` — usage notes and setup steps for ChatGPT / Claude Projects

**Series folders** contain:
- A top-level `README.md` indexing every post in the series
- One subfolder per post, named to match the live post URL slug
- Inside each post folder: a `README.md` linking back to the live article, plus one `.md` file per reusable prompt

## How to use a prompt

See [`USAGE.md`](USAGE.md) for one-off use and for step-by-step ChatGPT / Claude *Project* setup that applies to every prompt in this repo.

## Contributing

This repository is public and free to use, but we are **not accepting external contributions**. It is maintained as a curated collection by EdibleByte.

## License

See [`LICENSE`](LICENSE) for details.
