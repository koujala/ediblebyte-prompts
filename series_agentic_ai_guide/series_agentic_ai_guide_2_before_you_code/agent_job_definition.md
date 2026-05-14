# Agent Job Definition Template

Before your team writes a single line of code, answer these three questions in writing. The resulting document is your political armor inside the enterprise — hand it to legal, skeptical VPs, and IT security rather than explaining from memory.

The article's example of a well-formed goal:

> *Reduce tier-1 escalations by 30% by resolving order status, return eligibility, and FAQ queries autonomously — with automatic handoff to a human agent for anything requiring policy exceptions or account-level decisions.*

Notice what a good definition contains: a measurable target, a specific scope, explicit boundaries (what goes to humans), and an implied success/failure criterion.

---

## The Three Questions

Use this prompt to generate a structured agent job definition document with an AI assistant, then refine it until every stakeholder — including those with no AI background — can read it and understand exactly what the agent does, what it doesn't do, and how success is measured.

```
I am defining the scope and success criteria for an enterprise AI agent before we write any code. Help me produce a clear, stakeholder-ready agent job definition document by working through these three questions with me.

**Question 1: What specific workflow does this agent own end-to-end?**

Context about our use case:
[DESCRIBE THE WORKFLOW IN 2-3 SENTENCES — what triggers it, what it processes, what it produces]

Draft the workflow ownership statement in plain language. Include:
- The defined inputs the agent receives
- The defined outputs the agent produces
- The explicit stop conditions — when does the agent hand off or halt?

The statement must use "owns" not "assists" or "helps with." It should be unambiguous.

---

**Question 2: What does success look like in 90 days?**

Our initial sense of success:
[DESCRIBE WHAT YOU'RE HOPING TO ACHIEVE — escalation rates, processing time, volume handled, etc.]

Refine this into a success criterion that is measurable, not aspirational. If the current framing is "users find it helpful," push back and propose a specific metric with a target number and a 90-day timeframe.

---

**Question 3: What should this agent never do without human review?**

Known high-stakes actions in this domain:
[LIST ANY ACTIONS THAT INVOLVE FINANCIAL CONSEQUENCE, POLICY EXCEPTIONS, ACCOUNT-LEVEL DECISIONS, PII ACCESS, OR IRREVERSIBLE CHANGES]

Produce a "never without human review" list. This becomes the first guardrail specification.

---

Once all three answers are drafted, combine them into a single agent job definition document written for a stakeholder who knows nothing about AI agents. If they can read it and understand exactly what the agent does, what it doesn't do, and how success is measured — the document is correct.
```

---

**How to use:** Run this prompt with your team before the first sprint planning session. The output document should be reviewed by at least one business stakeholder — not just the engineering team. If a stakeholder reads it and asks "but what does it actually do?" — the document needs more specificity.

**What most people get wrong:** Writing the definition in technical language for the engineering team and assuming it's enough. Write it for the person who will ask the hardest question in month six.
