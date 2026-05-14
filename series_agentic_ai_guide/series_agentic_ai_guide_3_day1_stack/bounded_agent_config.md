# Bounded Agent Configuration Template

Define an agent's configuration with explicit autonomy bounds before writing any application logic. The article states: "An agent with no boundaries is not an agent — it's a liability."

The article's example configuration for a customer support agent:

```python
agent_config = {
    "max_iterations": 5,          # forced human handoff after 5 steps
    "max_tool_calls_per_run": 10, # hard ceiling on API calls
    "response_timeout_seconds": 30,
    "confidence_threshold": 0.75, # below this → escalate, don't decide
    "allowed_tools": [
        "order_status_lookup",
        "return_eligibility_check",
        "faq_search"
    ]
    # NOT in allowed_tools: account_modify, refund_issue, billing_update
}
```

Notice: what the agent cannot do is listed explicitly — not just what it can do.

---

## The Prompt

```
I am designing the bounded configuration for an enterprise AI agent. Help me define the explicit autonomy constraints before any application code is written.

**Agent name and use case:**
[NAME AND ONE-SENTENCE DESCRIPTION OF WHAT THIS AGENT DOES]

**Step 1: Define the execution bounds**

For each parameter, ask me for context and then propose a value with a rationale:

- max_iterations: The maximum number of plan-act-observe-refine loops before the agent forces a human handoff. (Too high = runaway loops; too low = premature escalation.)
  Context about our workflow complexity: [HOW MANY STEPS DOES A TYPICAL CASE REQUIRE?]

- max_tool_calls_per_run: The hard ceiling on external API/tool calls per execution. (Each call has latency and cost implications.)
  Context about our tool usage: [WHICH TOOLS WILL THE AGENT USE AND HOW OFTEN PER CASE?]

- response_timeout_seconds: Maximum time to wait for a response before failing gracefully.
  Context about our SLA requirements: [WHAT IS AN ACCEPTABLE WAIT TIME FOR THE END USER OR DOWNSTREAM SYSTEM?]

- confidence_threshold: The minimum confidence level below which the agent escalates rather than decides. (Expressed as a value between 0 and 1.)
  Context about our tolerance for autonomous decisions: [HOW MUCH DO WE TRUST THE AGENT TO DECIDE INDEPENDENTLY AT LAUNCH?]

**Step 2: Define the allowed tools list**

List every external system or API the agent is permitted to call:
[LIST ALL TOOLS THE AGENT NEEDS — e.g., order_status_lookup, faq_search, ticket_create]

Now explicitly list the tools that are NOT allowed — actions the agent must never take without a human confirmation step:
[LIST HIGH-STAKES ACTIONS — e.g., account_modify, refund_issue, billing_update, record_delete]

**Step 3: Produce the configuration**

Output a complete agent_config object in Python dict format (or YAML if preferred) with:
- All numeric bounds populated with proposed values and inline comments explaining each
- allowed_tools as an explicit list
- A commented-out section of disallowed tools with the reason each is excluded

**Step 4: Identify the stop conditions**

What are the specific conditions under which this agent must stop and hand off to a human, regardless of iteration count?
[DESCRIBE ANY DOMAIN-SPECIFIC STOP CONDITIONS — e.g., customer requests a refund over $500, user mentions legal action]

Add these as a stop_conditions list in the configuration.
```

---

**How to use:** Complete this before writing application logic. The configuration is a specification document, not just code — share it with a business stakeholder and one IT/security stakeholder for review before the first sprint. Their sign-off on the allowed-tools list is worth three months of building in isolation.

**What most people get wrong:** Teams define what the agent can do and skip the stop conditions. An agent without a maximum iteration count can loop indefinitely. An agent without a confidence threshold will guess when it should escalate. These are not edge cases — they are the first failure modes you will encounter in production.
