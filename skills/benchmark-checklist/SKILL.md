---
name: benchmark-checklist
description: Vet a measured number before you report or act on it. Use before trusting a speedup, regression, throughput, or latency figure.
---

# benchmark-checklist

Before trusting a number, check:

1. **Limiter** — what actually bounds the result?
2. **Method** — same workload, warmups, sample count?
3. **Errors / noise** — variance, outliers, failed runs?
4. **Repeats** — more than one run when noise matters?
5. **End-to-end relevance** — does this number match the user-visible path?

If any item fails, do not act on the number until fixed. Cite **explain-the-number**.
