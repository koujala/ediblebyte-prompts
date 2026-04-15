# Adaptive Tutor Prompts

This folder contains prompts and resources for creating adaptive tutoring AI systems that can personalize educational experiences based on individual learner characteristics, progress, and needs.

## Overview

Adaptive tutoring leverages artificial intelligence to create personalized learning paths that adjust in real-time to each student's:

- Current knowledge level
- Learning pace and style
- Areas of strength and weakness
- Engagement and motivation levels
- Preferred teaching methods

## Files

- `tutor.md`: System prompt template for adaptive tutor AI assistants

## Usage

We recommend running this prompt inside a **Project** in either ChatGPT or Claude. Projects keep your tutor's instructions, memory, and uploaded files scoped to one workspace, so each learning journey stays isolated and resumable.

### ChatGPT Projects

1. Click **New Project** in the left sidebar.
2. Open **Settings** and select **Project-Only** memory.
3. Name it (e.g., *My Tutor*) and click **Create Project**. The project should auto-open; if not, open it from the sidebar.
4. Optional: click the default folder icon next to the title to set a custom color and icon.
5. Click the **three-dot menu** → **Project settings**. From here you can rename the project and add **Instructions** — paste the contents of [`tutor.md`](tutor.md) into the Instructions field.
6. Use the **Sources** button inside the project to attach reference files (textbooks, notes, syllabi) whenever needed.

### Claude Projects

1. Click **Projects** in the left panel, then **Create Project** (next to the project title).
2. Give it a name and description.
3. Once the project opens, you'll have options to manage **memory**, add **instructions**, and upload **files**.
4. Paste the contents of [`tutor.md`](tutor.md) into the **Instructions** section.
5. Attach any supporting files (course materials, prior notes) via the files option.

Once set up, start a new chat inside the project and replace `[SUBJECT]` and `[TIMEFRAME]` in your first message — the tutor will generate your full learning plan before beginning.

## Related Topics

- Personalized learning
- Intelligent tutoring systems
- Educational technology
- AI in education
