# Use Case Fitness Check

Evaluate whether a proposed use case is the right first agent problem. Not every problem is a good first agentic AI problem — the goal is to find a narrow, high-impact, measurable use case that gives you a real chance of reaching production.

The article frames this as a 2x2: High Impact / Low Complexity is where you start. High Impact / High Complexity is Phase 2 or 3 once you have evidence.

---

## The Prompt

```
I am evaluating whether [PROPOSED USE CASE — e.g., "automating tier-1 IT ticket triage"] is the right first agentic AI problem for our team to build. Help me assess it against the five traits of a good first-agent use case and the three anti-patterns to avoid.

**Our use case:**
[DESCRIBE THE PROPOSED WORKFLOW IN 2-3 SENTENCES]

**Evaluate against the five traits of a good first-agent candidate:**

1. **High volume, repetitive, well-defined inputs** — Does the agent encounter the same pattern hundreds of times, or one-of-a-kind problems?
   Our situation: [DESCRIBE VOLUME AND VARIABILITY]

2. **Clear success/failure criteria** — Can you tell within seconds whether the agent got it right?
   Our situation: [DESCRIBE HOW YOU WOULD EVALUATE CORRECTNESS]

3. **Existing data that is already reasonably clean** — Is the agent blocked by data quality problems on day one?
   Our situation: [DESCRIBE THE CURRENT STATE OF RELEVANT DATA]

4. **A human currently doing this work who can validate agent outputs** — Do you have a baseline to compare against and a subject matter expert to catch errors?
   Our situation: [DESCRIBE WHO CURRENTLY DOES THIS WORK]

5. **Stakes that are meaningful but not catastrophic if the agent makes a mistake** — Is a wrong answer recoverable, or front-page news?
   Our situation: [DESCRIBE THE CONSEQUENCE OF AN AGENT ERROR]

**Check against the three anti-patterns to avoid for a first agent:**

- Does this use case touch financial approvals, compliance decisions, or PII as primary actions? (If yes: the governance overhead before launch is prohibitive.)
- Does this workflow have no existing documentation or process definition? (If yes: the agent will learn bad habits, and you won't know it.)
- Does the relevant "data" live in people's heads or email threads? (If yes: data engineering work will consume the timeline before you write a prompt.)

**Produce:**
1. A fitness score for each of the five traits (Strong / Weak / Unclear — with a one-sentence explanation)
2. A flag for each of the three anti-patterns (Present / Not present / Unclear)
3. An overall recommendation: Start Here, Defer to Phase 2, or Do Not Start — with a one-paragraph rationale
4. If the recommendation is not "Start Here": suggest one modification that would make this use case more appropriate, or identify a narrower slice of the same domain that would qualify
```

---

**How to use:** Run this before committing to a use case. If two or more of the five traits score "Weak," the use case is a Phase 2 problem at best. If any anti-pattern is present, stop and find a narrower slice or a different domain.

**What the article says about the research:** Bain and Deloitte research converges on the same advice — focus on a few business domains to generate early value rather than just building capabilities. This is not timid thinking. It is the fastest path to getting more budget and fewer obstacles.
