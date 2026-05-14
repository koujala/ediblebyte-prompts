# Day 1 Stack Review

Assess whether an MVP implementation covers all 7 non-negotiable Day 1 components and identify which failure modes remain open. Use this before declaring the MVP production-ready.

From the article's summary table — each component addresses a specific failure mode:

| Component | Failure Mode It Prevents |
|---|---|
| Bounded Agent Definition | Runaway loops, uncontrolled actions |
| Prompt Management | Unexplained behavior changes, debugging black holes |
| LLM Gateway | Unchecked costs, no fallback, data exposure |
| Tool Integration (narrow) | Over-permissioned agents, first-incident risk |
| Guardrails | Compliance failures, PII leakage, policy violations |
| Human-in-the-Loop | Premature autonomy, lost evidence base |
| Basic Observability | No visibility, no 90-day review story |

---

## The Prompt

```
I need to review whether our enterprise AI agent MVP covers all 7 non-negotiable Day 1 components before we declare it production-ready. For each component, I will describe our current implementation, and I need you to assess coverage and identify gaps.

**Agent and use case:**
[NAME AND DESCRIPTION]

---

**Component 1: Bounded Agent Definition**

Our implementation:
[DESCRIBE HOW THE AGENT'S SCOPE, MAX ITERATIONS, TOOL CEILING, TIMEOUT, AND CONFIDENCE THRESHOLD ARE CURRENTLY CONFIGURED]

Assess: Is the agent bounded with explicit stop conditions? Is the allowed-tools list explicit and reviewed? Flag any missing constraints.

---

**Component 2: Prompt Management**

Our implementation:
[DESCRIBE HOW SYSTEM PROMPTS ARE STORED, VERSIONED, AND DEPLOYED — E.G., "Prompts are in a Git repo with semantic versioning," or "Prompts are hardcoded strings in the application"]

Assess: Can we roll back to a previous prompt version in one operation? Can we compare versions? Is there an audit trail of changes? Flag if prompts are buried in code or lack version control.

---

**Component 3: LLM Gateway**

Our implementation:
[DESCRIBE THE GATEWAY IN USE OR EXPLAIN WHY NONE IS IN PLACE — E.G., "We use Portkey with per-team cost limits," or "We call the OpenAI API directly"]

Assess: Is cost monitoring with hard limits in place? Is there fallback/retry logic for provider outages? Is there prompt logging? Flag if calls go directly to a provider with no control layer.

---

**Component 4: Tool Integration**

Our implementation:
[LIST ALL TOOLS THE AGENT CAN CALL AND HOW ACCESS WAS SCOPED — E.G., "Three read-only API integrations, reviewed by IT and business owner"]

Assess: Is access scoped to least privilege? Has the tool list been reviewed by a stakeholder outside engineering? Flag any write or modify permissions that have not been reviewed.

---

**Component 5: Guardrails**

Our implementation:
[DESCRIBE HARD CONSTRAINTS (PII detection, block lists, injection detection, format validation) AND SOFT GUARDRAILS (confidence thresholds, topic scope) IN PLACE]

Assess: Are hard constraints enforced at the gateway or pre-execution? Are soft guardrails configured for this specific domain? Flag any categories (PII, jailbreak, format) that are unaddressed.

---

**Component 6: Human-in-the-Loop**

Our implementation:
[DESCRIBE THE HITL PATTERN IN USE, WHAT TRIGGERS REVIEW, WHAT THE REVIEWER SEES, AND HOW DECISIONS ARE RECORDED]

Assess: Is HITL designed in — not bolted on? Are "never autonomous" actions enforced? Is human review data being captured for future evidence? Flag if HITL is aspirational rather than implemented.

---

**Component 7: Basic Observability**

Our implementation:
[DESCRIBE WHAT IS CURRENTLY LOGGED — REQUEST/RESPONSE, TOKEN/COST TRACKING, LATENCY, ERROR RATES — AND WHERE IT IS VISIBLE]

Assess: Can we trace an exact execution path after the fact? Are costs visible per-request and per-day? Are errors and guardrail triggers alertable? Flag if "we can check the logs" is the answer — that is not an observability system.

---

**Produce:**
1. A coverage verdict for each component: Covered / Partial / Not covered
2. For each gap: the specific missing element and the failure mode it leaves open
3. A prioritized list of what to address before going to production — ordered by which failure mode is most likely to surface first
4. An overall readiness assessment: Production-ready / Ready with known risks / Not ready
```

---

**How to use:** Run this review with the team before the first production deployment. Share the output with one technical stakeholder outside the team (e.g., a security or platform engineer) for a second opinion on gaps. The goal is not a perfect score — it is an honest picture of which risks are open and a decision to accept or close each one before launch.
