# Scientist — Literature Summary from Abstracts

The highest-impact Basics Phase move for a researcher: a literature summary that would take a full day — done in an hour.

**What changes:** Literature review time drops from two days to two hours of reviewing and editing.

## The prompt

```
Here are abstracts from [number] papers on [topic]:
[paste abstracts, clearly numbered]

From these, give me:
1. A structured synthesis of the key findings — grouped by theme, not by paper
2. Where the findings agree and where they conflict
3. What methodological approaches were used and their limitations
4. What questions remain unanswered based on this body of work
5. Three gaps that a new study in this area could address

I'm writing the literature review section of a [paper / thesis / grant application].
Tone: academic but clear. Cite by author/year where relevant.
```

## How to use

Paste the actual abstracts — numbered clearly (Paper 1, Paper 2, etc.) so the model can reference them when noting conflicts. Replace `[number]` and `[topic]` with your specifics. Specify the purpose — paper, thesis, or grant application — since this affects depth and framing.

Always validate the synthesis against the source papers. The model can misread nuance in scientific language, overstate consensus where papers genuinely disagree, or miss methodological distinctions that matter in your field. The output is a structured starting point, not a submission-ready section.

The three gaps section is typically the most useful for originality — use it as a prompt for your own thinking about where a new study could contribute.
