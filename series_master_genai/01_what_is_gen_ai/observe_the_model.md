# Observe the Model: Fluency vs. Accuracy

A two-part test to see, first-hand, where a language model's fluency outruns its accuracy. Run both prompts in the same chat, back to back, then compare the tone and the substance of the answers.

---

## Prompt A — A topic you know deeply

```
I want to test your accuracy on something I know well.

Topic: [PICK A TOPIC YOU KNOW DEEPLY — your profession, a hobby, a subject you've studied]

Please answer this question in detail:
[WRITE A SPECIFIC, NON-TRIVIAL QUESTION ABOUT THAT TOPIC]

Be as specific as you can. Include any nuances, edge cases, or common misconceptions.
```

After you read the answer, ask yourself:
- What did it nail?
- Where did it slip into something that sounds right but isn't quite?
- Did it acknowledge uncertainty anywhere, or speak with uniform confidence throughout?

---

## Prompt B — A recent event

```
Now a second question, on a different topic.

What can you tell me about [A NEWS EVENT OR DEVELOPMENT FROM THE LAST FEW WEEKS]?

Be specific about dates, names, and numbers if you know them. If you are not sure about any of it, please say so explicitly rather than filling in plausible-sounding detail.
```

After reading this answer, notice:
- Did the model acknowledge its knowledge cutoff, or did it produce confident-sounding detail anyway?
- If it produced detail, is any of it actually correct?
- Does the tone of the answer give you any signal that it might be wrong? (Usually: no.)

---

**What this teaches you:** Confidence in tone has zero correlation with factual accuracy. The model's job is to generate fluent, coherent text — not to verify truth. Internalising this through direct observation is worth more than reading about it.
