# Gap-Filling and Spaced-Repetition Quizzing

Two of AI's highest-leverage learning uses, grouped because they work together: fill the specific gap that is blocking you *now*, then make sure the fill actually stuck with spaced-repetition retrieval later.

---

## Prompt A — Mid-reading gap filler

Use this in the middle of reading, studying, or trying to do something — when one specific step is breaking your understanding.

```
I am working through [TOPIC / MATERIAL] and I'm stuck on one specific step.

What I do understand:
[X — describe the prior step clearly, in your own words]

What I do NOT understand:
[Why Y follows from X, or why Z is claimed, or what a specific term actually means here]

Please explain just that connection — not the whole topic, not the broader context. Just that specific step, in as few words as it takes to make it click.

If the gap you're about to fill assumes something else I might also not know, stop and check with me first.
```

---

## Prompt B — Adaptive quiz

For active recall at the end of a study session, or once you have worked through a chapter or module.

```
Quiz me on [TOPIC / WHAT I JUST STUDIED].

Rules:
- Start with foundational questions and increase difficulty as I get them right.
- Ask one question at a time. Wait for my answer.
- If I get one wrong, do not just give me the answer. Ask me a slightly easier version of the same underlying idea until I work my way to it.
- At the end, give me a short summary: what I know solidly, where I hesitated, and the one thing I should review before coming back.
```

For *application* over recall, swap in:

```
Give me a realistic scenario where I would need to apply [CONCEPT]. Do not tell me the answer — let me work through it. When I reason out loud, tell me where my reasoning goes wrong or gets shaky.
```

---

## Prompt C — Spaced repetition, on demand

Run a short quiz like Prompt B, then come back two days later and run:

```
Quiz me again on [TOPIC] — the same material we covered on [PRIOR DATE]. Focus first on the areas where I hesitated or got things wrong last time. Then test a couple of the areas I had solid, to make sure they're still solid.
```

Repeat a few days after that. **What keeps slipping across sessions is where the real learning work still is.**
