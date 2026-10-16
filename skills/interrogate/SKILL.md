---
name: interrogate
description: Adversarial review of a diff or change set. Use for interrogate, challenge this, stress-test this code, find blind spots, or multi-angle review.
---

# interrogate

## Steps

1. **Scope** the diff (user paths, git diff against base, or recent work).
2. **State intent** in one paragraph from the user message / commits / PR text.
3. **Review from independent angles** (use pstack-harness spawn when available; else sequential inline):
   - correctness and invariants
   - edge cases and failure modes
   - reader load and accidental complexity
   - missing tests or unverified behavior
4. **Synthesize** a verdict: must-fix / should-fix / nit / dismiss with reason.
5. **Do not auto-apply** changes. Present findings for the operator or parent playbook.
