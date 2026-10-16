# Worktree cleanup

Reclaim disk from merged or abandoned worktrees (and similar host artifacts). Safety-gated.

1. List candidates with evidence (merged, gone remote, abandoned).
2. Never delete anything ambiguous without operator confirmation.
3. Prune only confirmed safe entries.
4. **Reply:** removed, kept, skipped-with-reason.
