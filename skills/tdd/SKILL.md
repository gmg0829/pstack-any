---
name: tdd
description: Write a failing check first, then the fix, when a cheap local test path exists. Use for tdd, failing test first, or red green refactor on a local path.
---

# tdd

1. Confirm a **cheap local** test path exists. If expensive or unclear, say so and skip.
2. Write the failing check that expresses the bug or desired behavior.
3. Run it — confirm red.
4. Implement the minimal fix.
5. Run — confirm green.
6. Refactor only while green.
