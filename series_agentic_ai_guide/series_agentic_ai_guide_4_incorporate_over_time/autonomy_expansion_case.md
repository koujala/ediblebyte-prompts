# Autonomy Expansion Case Builder

Build the data-backed case for reducing human review requirements for a specific action type. This is a business decision as much as a technical one — the data is engineering, the decision is governance.

From the article: "Document the data. Get the sign-off from the business owner and your legal or compliance stakeholder. Expand autonomy incrementally — one action type at a time, with a monitoring window after each change."

What most people get wrong: treating autonomy expansion as an engineering decision. It isn't.

---

## The Prompt

```
I am preparing the case for expanding agent autonomy on a specific action type. Help me build a structured document that separates the data analysis (engineering) from the governance decision (business and compliance) and is suitable for presenting to a business owner and a legal or compliance stakeholder.

**Agent and use case:**
[NAME AND DESCRIPTION]

**Action type under consideration for autonomy expansion:**
[SPECIFIC ACTION — E.G., "approving standard return requests under $100," "closing resolved IT tickets without human confirmation," "sending draft responses to customers"]

---

**Part 1: The Evidence Base**

Production data for this action type (from the past [NUMBER] months):

- Total cases involving this action type: [NUMBER]
- Cases currently routed to human review: [NUMBER] ([%] of total)
- Of human-reviewed cases, how often did the human approve the agent's proposed decision without changes? [%]
- How often did the human modify the agent's proposal before approving? [%]
- How often did the human reject the agent's proposal entirely? [%]
- Cost of maintaining human review for this action type per month: [TIME / DOLLARS / HEADCOUNT HOURS]
- Any incidents or near-misses associated with this action type? [DESCRIBE OR "NONE"]

Analyze this data and assess: does the evidence support expanding autonomy? What is the strength of the case — strong, moderate, or insufficient?

---

**Part 2: The Risk Assessment**

For this specific action type:

- What is the worst-case outcome if the agent makes an incorrect autonomous decision? [DESCRIBE]
- Is that outcome reversible? [YES — HOW / NO — WHY]
- What safeguards would remain in place even after human review is reduced? (Guardrails, logging, anomaly alerts)
  [LIST REMAINING CONTROLS]
- Are there regulatory, compliance, or contractual constraints on autonomous execution of this action type?
  [DESCRIBE OR "NONE IDENTIFIED"]

Produce a risk summary: what is the residual risk after expansion, and what controls mitigate it?

---

**Part 3: The Expansion Design**

Propose a specific expansion design — not a binary "remove HITL" but an incremental step:

- Proposed new threshold: what % of cases for this action type would be autonomous vs. still routed for review?
  (E.G., "Approve autonomously when confidence > 0.85 and transaction value < $X")
- Proposed monitoring window: how long and what metrics will be tracked before the next review?
  [E.G., "30 days, tracking: error rate, reversal rate, escalation rate for adjacent action types"]
- Rollback trigger: what would cause immediate reversion to full human review?
  [E.G., "Error rate exceeds 2% in any 7-day window"]

---

**Part 4: The Sign-Off Document**

Produce a one-page governance summary that includes:
1. What the agent currently does vs. what it will do after expansion (plain language)
2. The evidence that justifies this change (3-5 bullet points from Part 1)
3. What safeguards remain in place
4. The monitoring plan and rollback trigger
5. A signature block for: [BUSINESS OWNER NAME / ROLE] and [LEGAL OR COMPLIANCE STAKEHOLDER NAME / ROLE]

Format this as a document suitable for a non-technical stakeholder to read, sign, and file.
```

---

**How to use:** Do not present this case informally. Write the Part 4 governance summary, share it in advance of the sign-off meeting, and give stakeholders time to read it. The meeting is for questions and decision — not for first exposure.

**The principle from the article:** Expand autonomy one action type at a time. A monitoring window after each change is not bureaucracy — it is what makes the next expansion easier to justify.
