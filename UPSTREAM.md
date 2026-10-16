# Upstream

- Source methodology: cursor/plugins `pstack` (Lauren Tan / @poteto)
- License: MIT
- This repository does not track upstream commit-by-commit. When merging ideas from upstream, prefer methodology text over Cursor-specific tool names.

## What we keep

- Playbook catalog and step intent (investigation, bug-fix, feature, shipping, …)
- Principle names and meanings
- Evidence-first, smallest-change, data-shape-first norms
- Specialist intents: how, why, architect, arena, swarm, interrogate, …

## What we change

- No `Task` tool, no Cursor plugin manifest as the only install path
- Skills describe neutral operations (spawn, ask, worklist, read sibling skill)
- `pstack-harness` maps neutral operations to the live agent
- Missing capabilities degrade honestly (sequential review instead of fake multi-model panels)
