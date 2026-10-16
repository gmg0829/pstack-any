---
name: blast-radius
description: For a small-looking change, find what else it could break and prove safety with a running check. Use for blast radius, what could break, or is this change safe.
---

# blast-radius

1. Identify the change set.
2. Find dependents, shared state, and callers.
3. State the risk hypotheses.
4. **Prove** safety with a running check where possible — not assertion alone (**prove-it-works**).
5. **Reply:** dependents, risks, the one fact that makes it safe (or the gap if unproven).
