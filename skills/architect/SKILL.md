---
name: architect
description: Settle caller's usage, types, and module shape before implementing code that crosses a function or module boundary. Use for architect, design the boundary, or before a cross-cutting change.
---

# architect

Do this **before** implementation when a change crosses a boundary.

## Produce

1. **Caller usage** — who calls, with what, what they assume
2. **Types / data shape** — inputs, outputs, illegal states made unrepresentable where practical
3. **Ownership** — who owns lifecycle and errors
4. **Boundary placement** — validation and parsing at the edge; pure logic inside
5. **Rejected shapes** — one or two alternatives and why not

Then implement only what this note settles. Prefer smallest change and model-the-domain.
