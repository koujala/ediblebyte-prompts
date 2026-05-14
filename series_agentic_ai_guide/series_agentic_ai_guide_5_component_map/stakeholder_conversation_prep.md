# Stakeholder Conversation Prep

Prepare specific, document-backed responses to the three predictable stakeholder conversations every enterprise agentic AI project will face. These conversations are coming — prepare for them before they happen.

From the article: "Vague concerns evaporate when you're specific. They compound when you respond with equal vagueness."

The article's concrete example: A legal stakeholder raises concerns about data residency. "We have controls in place" is a vague response. "All requests route through our LLM gateway which enforces data residency via [specific configuration], and every request is logged here — here's a sample entry" is a specific response. The second answer ends the conversation. The first answer extends it.

---

## The Three Stakeholder Conversations

**The security conversation:** "Where does our data go, and who can see it?"
Answered by: LLM gateway configuration, data residency settings, prompt logging audit trail.

**The compliance conversation:** "How do we prevent the agent from making decisions it shouldn't?"
Answered by: guardrail configuration, HITL design, escalation flow.

**The business value conversation:** "Is this actually working?"
Answered by: observability dashboard — task completion rate, escalation rate, cost per interaction, before/after comparison.

---

## The Prompt

```
I need to prepare for three predictable stakeholder conversations about our enterprise AI agent. Help me build specific, document-backed responses to each — not general assurances, but precise answers tied to our actual configuration.

**Agent and use case:**
[NAME AND DESCRIPTION]

---

**Conversation 1: The Security Conversation**
"Where does our data go, and who can see it?"

Our current security posture:
- LLM gateway in use: [NAME — E.G., Portkey, LiteLLM, TrueFoundry, or "none yet"]
- Data residency configuration: [E.G., "All requests stay within EU region," "Routed through our VPC," or "Not yet configured"]
- What is logged and who has access to logs: [DESCRIBE]
- Whether customer or employee PII can appear in prompts: [YES / NO / DEPENDS — EXPLAIN]
- PII detection and redaction controls in place: [DESCRIBE OR "NONE YET"]

Draft a specific, one-paragraph response to "Where does our data go, and who can see it?" that references our actual configuration — not general principles. Include a sentence identifying the document or dashboard where a skeptical stakeholder could verify the answer independently.

Also identify: what is the single biggest gap in our current security posture that we should close before this conversation happens?

---

**Conversation 2: The Compliance Conversation**
"How do we prevent the agent from making decisions it shouldn't?"

Our current compliance posture:
- Hard guardrails in place: [LIST — E.G., PII detection, block lists, output format validation, jailbreak detection]
- Soft guardrails in place: [LIST — E.G., confidence thresholds, topic scope enforcement]
- HITL design for high-stakes actions: [DESCRIBE WHICH ACTIONS REQUIRE HUMAN REVIEW AND HOW]
- Escalation flow for out-of-scope or ambiguous cases: [DESCRIBE]
- Actions the agent is explicitly prevented from taking: [LIST FROM YOUR "NEVER WITHOUT HUMAN REVIEW" DOCUMENT]

Draft a specific, one-paragraph response to "How do we prevent the agent from making decisions it shouldn't?" Walk through the guardrail configuration, HITL design, and escalation flow — don't just assert they exist. The answer should be specific enough that a legal stakeholder understands exactly what controls are in place and where they are enforced.

Also identify: what compliance gap, if any, should be closed before the first production deployment?

---

**Conversation 3: The Business Value Conversation**
"Is this actually working?"

Our current observability data:
- Period covered: [E.G., "First 6 weeks of production"]
- Task completion rate (autonomous, no escalation): [%]
- Escalation rate: [%]
- Cost per interaction: [AMOUNT]
- Baseline before agent (if available): [E.G., "Average handle time was 8 minutes; agent resolves 74% of cases in under 30 seconds"]
- Volume handled to date: [NUMBER OF CASES]
- Any incidents, errors, or notable failures: [DESCRIBE OR "NONE"]

Draft a specific, data-forward response to "Is this actually working?" Make the case with numbers. Include a before/after comparison where data exists. End with what the data says about the next capability or autonomy expansion — so the business understands this is a foundation, not a ceiling.

---

**Final output:**
Produce a one-page stakeholder briefing document that contains all three responses in plain language, suitable for sharing before a review meeting. Format it as: Agent Overview (two sentences) → Security (one paragraph) → Compliance (one paragraph) → Business Value (one paragraph with key metrics called out). No technical jargon — assume the reader knows nothing about AI agents but is a competent business or legal professional.
```

---

**How to use:** Complete this before any stakeholder review meeting. Share the output document in advance — 24-48 hours before the meeting — so stakeholders arrive having already read it. The meeting should be for questions and decisions, not for first exposure. If you cannot complete the prompt because you don't have the data (especially for the security and compliance sections), that is a signal: close those gaps before the meeting, not after.

**From the article's research:** MIT Sloan research confirms that in real enterprise agent deployments, 80% of the effort goes not to prompt engineering or model tuning — but to data engineering, stakeholder alignment, governance, and workflow integration. The teams that struggle are the ones who budget as if the hard part is the AI.
