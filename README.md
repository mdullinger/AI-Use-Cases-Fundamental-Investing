# AI Use Cases for Fundamental Investing

Five agent-engineering principles distilled from building a research platform on
Claude Code — copy them straight into your own `CLAUDE.md` or agent config.

## Core message

Use AI to find and challenge evidence. Use code to calculate.
Keep judgment with the person accountable for it.

## Principles

1. **Use the least complex design that works.** Keep repeatable tasks in
   a fixed workflow. Add agent autonomy only where the task genuinely
   requires searching, choosing a path, or adapting to new information.
   Autonomy adds cost and latency — it has to earn its place.

2. **Give each agent a narrow job and explicit tools.** Define what it
   can read or change, what a good output looks like, and when it
   must stop or escalate. Prefer typed outputs and code-level checks
   over instructions alone — an instruction is a request; a type
   check is a guarantee.

3. **Manage context deliberately.** Retrieve what's relevant when it's
   needed, rather than loading everything into one giant prompt.
   Keep source material, extracted facts, analysis, and conclusions
   in distinct, addressable layers — never collapse them into one
   undifferentiated blob of "context."

4. **Put the controls that matter outside the model.** Permissions,
   spending limits, retries, timeouts, validation, and approval
   gates belong in code, not in a prompt asking politely. Require
   human review before any consequential, hard-to-reverse action.

5. **Evaluate the whole process, not just the final answer.** Keep
   traces of retrieval, tool calls, and handoffs, and test them
   against a fixed set of known cases. This is how you find out
   whether an error came from missing evidence, a bad calculation,
   or poor synthesis — the three failure modes look identical from
   the final answer alone.

---

The goal was never maximum autonomy. It's reliable research capacity —
with visible evidence, controlled actions, and measurable improvement.
