# Redesign the Metric — From Proxy to Outcome

Use this prompt to diagnose a measurement system that is producing the wrong behaviour, then design an alternative that gets closer to the actual outcome the team cares about.

---

```
My team currently measures performance by [LIST CURRENT METRICS — be specific: tickets closed per sprint, commits per week, lines of code, etc.].

I believe these metrics are producing the wrong behaviour — here is what I observe: [DESCRIBE THE MISALIGNED INCENTIVE — what people are optimising for, and what that is costing].

Help me design an alternative measurement approach that gets closer to the actual outcome we care about. What would we need to track, and how would we collect that data?
```

---

**How to use:**

The observation about misaligned behaviour is the load-bearing part. A vague problem produces a vague alternative. "People are closing tickets without fixing root causes, so the same issues recur — we are spending roughly 40% of each sprint on work that was already done once" gives the AI a clear failure mode to design against.

The output to look for:
1. **The actual outcome:** what the team is trying to produce (system reliability, developer velocity, customer impact)
2. **Leading indicators:** what predicts that outcome before it is visible in the metric
3. **Collection method:** how you would actually gather the data without making measurement itself the new job

Use the redesigned metric proposal as a conversation starter with your manager — not as a finished system. Measurement change requires buy-in; a concrete alternative framed as "what if we also tracked X" gets further than "our current metrics are broken."
