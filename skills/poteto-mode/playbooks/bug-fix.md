# Bug fix

You own the task. Plan, review, verify.

Every shipped line traces to runtime evidence. "Might help" is a hypothesis, not a fix. When evidence refutes a hypothesis, revert what it motivated.

1. **Reproduce** on the matching surface yourself. Ask the user only with a specific reason the surface cannot reach the target, after you have tried.
2. **Binary-search the cause.** Hypotheses out; runtime evidence in. Instrument when state is unclear. Confirm the mechanism before writing the fix.
3. **Plan the fix.** If it crosses a boundary, run **architect** first. Implement only the justified change (smallest change / laziness-protocol).
4. **Verify** on the same surface. Original repro must pass.
5. When a cheap local test path exists, prefer failing check then fix (**tdd**).
6. **Reply:** what broke, root cause, fix, how verified. Paste failing-then-passing evidence when possible.
