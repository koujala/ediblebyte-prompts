# Human-in-the-Loop Pattern Selector

Choose the right HITL design for your use case and document it before building. The article is clear: HITL must be designed in from the start, not bolted on after launch. And it should not be framed as a temporary concession — it is your data collection mechanism.

From the article: "Every human decision that corrects or confirms the agent is a labeled example. That data is what you use to justify expanding autonomy in Phase 3."

---

## The Three HITL Patterns

| Pattern | How it works | Best for |
|---|---|---|
| **Draft-and-review** | Agent prepares the action; human confirms before it executes | Emails, reports, recommendations, outbound communications |
| **Exception-based escalation** | Agent handles routine cases autonomously; escalates edge cases to a human | Support triage, document classification, data tagging |
| **Confidence-gated autonomy** | Agent acts autonomously above a confidence threshold; routes to human below it | Gradual autonomy expansion as production data builds |

---

## The Prompt

```
I am designing the human-in-the-loop layer for an enterprise AI agent MVP. Help me select the right HITL pattern and document the complete design.

**Agent and use case:**
[NAME AND DESCRIPTION OF WHAT THE AGENT DOES]

**Step 1: Assess which HITL pattern fits**

Describe our workflow:
- Volume of cases per day: [NUMBER]
- Typical case disposition time without HITL: [E.G., "2 minutes per case"]
- Proportion of cases that are routine vs. edge cases (estimate): [E.G., "80% routine, 20% require judgment"]
- Consequence of an unchecked agent error (financial, legal, reputational): [DESCRIBE]
- Availability and capacity of human reviewers: [HOW MANY REVIEWERS, HOW MUCH TIME]

Based on this, recommend the most appropriate HITL pattern and explain why the other two are less suited for this use case at launch.

**Step 2: Define the HITL design for the chosen pattern**

For the selected pattern, document:

1. **Trigger conditions:** What specifically causes the agent to route to a human? (Be explicit — "low confidence" is not enough. Define the threshold, the action types, or the content signals that trigger review.)

2. **Handoff format:** What information does the human reviewer receive? (Include: what the agent was asked, what it proposed to do or say, its confidence signal if applicable, and any relevant context from the interaction.)

3. **Reviewer actions available:** What can the human do? (Approve as-is / Edit and approve / Reject and reroute / Escalate further)

4. **SLA for human review:** How long does the agent wait before timing out or notifying the requester of a delay?

5. **Data capture:** What is recorded from every human review decision? (This is the labeled dataset that justifies autonomy expansion in Phase 3.)

**Step 3: Document the "never autonomous" list**

List the specific action types that require human approval regardless of confidence score throughout the MVP phase:
[LIST FROM YOUR AGENT JOB DEFINITION — actions in the "never without human review" category]

**Step 4: Define the MVP success threshold**

The goal of the MVP is not full automation. The goal is to demonstrate that the agent handles 70–80% of cases correctly before the conversation about expanding autonomy begins. Define what "correctly" means for this use case:
[DESCRIBE WHAT CORRECT LOOKS LIKE FOR A CASE IN THIS DOMAIN]

Produce a one-paragraph HITL design summary suitable for sharing with a compliance or business stakeholder.
```

---

**How to use:** Complete this alongside the bounded agent configuration. Share the output with one compliance stakeholder before building. If they have objections, you want to know now — not after three sprints of implementation.

**The reframe that matters:** The goal of the MVP is not to remove HITL as quickly as possible. The goal is to collect enough labeled decisions to justify — with data — where and when HITL can be safely reduced.
