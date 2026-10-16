---
name: swarm
description: N workers across different slices or races, then one aggregated report. Use for swarm, fan-out coverage, partition the work, or parallel slices.
---

# swarm

## Phases

1. **Frame** — done predicate; partition into slices and/or race shape; declare first-pass / rank-all / best-of if racing.
2. **Fan out** — one worker per slice (harness spawn or sequential). Each gets writable output paths and exact scope.
3. **Aggregate** — parent synthesizes; do not pass through a single child's story as truth.
4. **Report** — one verdict/report tied to the predicate.

Missing subagents → sequential slices with the same aggregation duty.
