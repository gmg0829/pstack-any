---
name: how
description: Walkthrough of how a subsystem works. Use for how does X work, explain this module, map the control flow, or where does Y live in the code.
---

# how

Produce an evidence-backed walkthrough.

## Output shape

1. **Overview** — one short paragraph
2. **Key concepts** — named ideas the reader needs
3. **How it works** — control/data flow with concrete symbols
4. **Where things live** — files and entry points
5. **Gotchas** — traps, invariants, non-obvious constraints

Cite code paths. Prefer reading the tree over guessing. If pstack-harness is available and bulk exploration would flood context, spawn a readonly explorer then summarize.
