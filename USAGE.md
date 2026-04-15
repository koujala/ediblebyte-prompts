# Usage

How to use any prompt in this repository. Two modes: a **one-off** paste for a single task, or a **Project** setup for recurring use with its own memory and files.

## One-off use

1. Open the prompt file you want.
2. Copy its contents into a new chat in ChatGPT or Claude.
3. Replace the bracketed `[PLACEHOLDERS]` with your specifics.
4. Send — and iterate on the response.

## Recurring use — run it inside a Project

For any prompt you expect to reuse, paste it into the **Instructions** field of a ChatGPT or Claude *Project*. Projects keep the prompt's instructions, memory, and uploaded files scoped to one workspace, so each use of it stays isolated and resumable.

### ChatGPT Projects

1. Click **New Project** in the left sidebar.
2. Open **Settings** and select **Project-Only** memory.
3. Name it (e.g., *My Tutor*, *My Writing Partner*) and click **Create Project**. The project should auto-open; if not, open it from the sidebar.
4. *Optional:* click the default folder icon next to the title to set a custom color and icon.
5. Click the **three-dot menu** → **Project settings**. Paste the contents of the prompt file into the **Instructions** field.
6. Use the **Sources** button inside the project to attach reference files (notes, textbooks, prior work) whenever needed.

### Claude Projects

1. Click **Projects** in the left panel, then **Create Project** (next to the project title).
2. Give it a name and description.
3. Once the project opens, you'll have options to manage **memory**, add **instructions**, and upload **files**.
4. Paste the contents of the prompt file into the **Instructions** section.
5. Attach any supporting files via the files option.

### First message

Once the Project is set up, start a new chat and fill in any `[PLACEHOLDERS]` the prompt expects as your first message. Each folder's `README.md` notes the specific placeholders for the prompts in it.

## Tips

- **Iterate — don't accept the first output.** The first response tells you what the model understood and what it missed. Steer with follow-ups like *"too formal, rewrite conversationally"* or *"reframe for engineers, not executives"*.
- **Bring context.** A vague prompt produces a generic answer. Tell the model your audience, constraints, and what "good" looks like.
- **Own the important sentences.** For anything going out under your name, rewrite the opening, the key point, and the closing in your own words. AI drafts — you author.
