<p align="center">
  <img src="assets/eb-logo.png" alt="EdibleByte" width="140">
</p>

# EdibleByte Prompts Library

A curated collection of specialized prompts for AI assistants (ChatGPT, Claude, and others), designed for real use in learning, thinking, writing, planning, and working with AI deliberately.

Each prompt is copy-paste ready — drop it into a new chat, fill in the bracketed `[PLACEHOLDERS]`, and iterate.

## Current contents

### Standalone prompts

- [`adaptive_learning_tutor_prompt/`](adaptive_learning_tutor_prompt/) — an adaptive, personalized tutoring system prompt that calibrates a full learning series to your subject, timeframe, and level.
- [`six_prompts_for_high_stakes/`](six_prompts_for_high_stakes/) — 6 prompts for high-stakes moments: clearing assumptions, finding understanding gaps, stress-testing decisions, separating feedback from noise, practising strategic silence, and closing every session with the one thing worth carrying forward.
- [`master_ai_30_day_roadmap/`](master_ai_30_day_roadmap/) — day-by-day prompts across three phases: Claude App (learn and produce, days 1–14), Claude CoWork (automate, days 15–21), and Claude Code (build and ship, days 22–30).

### Prompt series

Companion prompt libraries for multi-part article series published on [ediblebyte.com](https://www.ediblebyte.com/publications) — which hosts links to the full catalogue of posts published on [LinkedIn](https://www.linkedin.com/in/koujala/) and [Substack](https://substack.com/@koujala). Each series folder here maps one-to-one to the posts of its source series.

- [`series_master_genai/`](series_master_genai/) — 30 reusable prompts drawn from the **Gen AI Mastery** series (9 articles). Covers prompting fundamentals, thinking partnerships, learning, writing, deep work, and professional workflows.
- [`series_ai_by_role/`](series_ai_by_role/) — 16 role-specific prompts across 13 roles (teacher, sales, PM, lawyer, HR, finance, healthcare, creative, and more). Each prompt targets the highest-friction task in that role's week.
- [`series_social_dynamics_at_work/`](series_social_dynamics_at_work/) — 20 prompts across 15 posts on workplace dynamics: feedback, visibility, negotiation, meetings, recognition, and navigating the gap between what's said and what's meant.
- [`series_learning_traps/`](series_learning_traps/) — 18 prompts across 13 posts on the mental traps that stall learning: premature closure, the illusion of understanding, tutorial plateau, passive consumption, and more.
- [`series_self_deception/`](series_self_deception/) — 19 prompts across 12 posts on blind spots and self-awareness: validation loops, confidence vs. competence, the comfortable lie, the hindsight ratchet, and more.
- [`series_expertise_and_mastery/`](series_expertise_and_mastery/) — 14 prompts across 10 posts on expert-level thinking: the expert trap, adjacent blind spots, the simplicity inversion, and recovering the beginner's mind.
- [`series_agentic_ai_guide/`](series_agentic_ai_guide/) — 9 prompts across 4 posts on building agentic AI systems: defining agent scope, use case fitness checks, Day 1 stack configuration, and stakeholder communication.
- [`series_ai_learning_path/`](series_ai_learning_path/) — 31 prompts from posts 2, 4, and 5: role-specific illustrative prompts (post 2), fully-templated role prompt libraries (post 4), and wall-breaking fix prompts for common stall points (post 5).
- [`series_ai_customization/`](series_ai_customization/) — 2 decision-framework prompts: RAG vs fine-tuning selection, and LoRA/QLoRA/adapter choice given compute and task constraints.
- [`series_ai_pilot_failure/`](series_ai_pilot_failure/) — 1 prompt: the pre-pilot diagnostic scoring an AI initiative across 8 dimensions before writing a line of code.
- [`series_building_ai_team/`](series_building_ai_team/) — 1 prompt: designing the JD and interview process for a bilingual first AI hire.
- [`series_claude_force_multipliers/`](series_claude_force_multipliers/) — 1 prompt: auditing your CLAUDE.md against your actual codebase to surface missing, stale, or mislevelled context.
- [`series_software_to_ai_engineer/`](series_software_to_ai_engineer/) — 1 prompt: rewriting an AI engineering JD to filter for production instincts rather than ML theory.

## How the repo is organised

**Standalone prompt folders** contain:
- A descriptively named prompt file (e.g. [`adaptive_learning_tutor_prompt/tutor.md`](adaptive_learning_tutor_prompt/tutor.md)) — the core prompt
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
