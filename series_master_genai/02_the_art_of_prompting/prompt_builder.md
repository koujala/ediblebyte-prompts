# Prompt Builder: Role + Task + Context + Format

A scaffold for constructing strong prompts. Not every prompt needs all four elements — but when output is falling short, the missing piece is almost always one of these.

## The scaffold

```
Role:    [Who should the model be for this task? Assign a role — it activates the vocabulary, tone, and priorities of that persona.]
         e.g. "You are a senior communications consultant."
              "Act as a patient, encouraging tutor."

Task:    [What, specifically, do you want it to do? Use directive verbs — avoid "help me with" or "tell me about".]
         e.g. "Write a 200-word summary..."
              "Generate 10 alternative approaches to..."
              "Identify the three weakest arguments in this text."

Context: [What can the model not infer on its own? Audience, constraints, what you have tried, what "good" looks like.]
         e.g. "My audience is non-technical executives who are sceptical of AI."
              "This is for an internal Slack message, not a formal report."
              "I have tried X and Y already — neither worked because..."

Format:  [How should the output be structured? Length, layout, any shape that matches how you will use it.]
         e.g. "Respond in bullet points, maximum 5."
              "Write in three short paragraphs."
              "Give me a table with two columns: option and trade-off."
```

## Worked examples

### Personal — Daily planning

```
You are a productivity coach. It is Monday morning.

I have the following on my plate this week:
[LIST TASKS]

My energy is typically highest before noon. I have two non-negotiable meetings on Wednesday.

Help me build a realistic daily plan that protects my deep work time and does not set me up to fail by Friday.
```

### Professional — Stakeholder communication

```
I am a senior engineer presenting a recommendation to shift our team from a monolithic architecture to microservices.

My audience includes:
- the CTO (technically fluent, wants risk and cost data)
- two non-technical VPs (need business impact framed simply)

Write a 300-word executive summary that works for both audiences simultaneously. Lead with the business case.
```

### Creative — Writing in your voice

```
Here are three examples of how I write:
[PASTE SAMPLES]

Study the tone, sentence rhythm, and vocabulary.

Now write a 200-word LinkedIn post announcing that I have joined a new company. The post should sound exactly like me — not like a press release.

Avoid clichés like "excited to announce" or "thrilled to share." End with something that invites genuine conversation.
```

## Iteration is the real skill

Your first prompt is a draft, not a final brief. Steer with follow-ups like:

- *"That's close but too formal — rewrite it with a more conversational tone."*
- *"You've given me 10 ideas but most are generic. Throw out the obvious ones and give me 5 that are genuinely unexpected."*
- *"You misunderstood the audience. These are engineers, not executives. Reframe accordingly."*

The conversation is the work.
