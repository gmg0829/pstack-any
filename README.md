# pstack-any

Harness-agnostic packaging of Lauren Tan's (**@poteto**) pstack engineering workflows.

**If you want to go fast, go deep first.** Throughput without quality is not the goal.

Official upstream (Cursor plugin): https://github.com/cursor/plugins/tree/main/pstack

This repo keeps the same playbooks and principles. Skills name **neutral operations**. **pstack-harness** maps them onto Cursor, Claude Code, Codex, Grok, OpenCode, or a generic sequential fallback.

## Install

### skills CLI

```bash
npx skills add gmg0829/pstack-any
```

### Copy

```bash
cp -R skills/* /path/to/agent/skills/
```

| Agent | Typical path |
|-------|----------------|
| Claude Code | `.claude/skills/` or `~/.claude/skills/` |
| Cursor | project / user skills |
| Codex | `.agents/skills/` |
| Grok | `~/.grok/skills/` |
| OpenCode | `.opencode/skills/` |

See `docs/install.md`.

## Quick start

```text
/poteto-mode this bug happens when idle. repro first, then fix and verify.
```

```text
Use poteto-mode: add --json. text output byte-identical. verify both.
```

```text
/poteto-help which skill for reviewing this branch?
```

## Inventory

### Orchestration

| Skill | Role |
|-------|------|
| **poteto-mode** | Match playbook, worklist, route specialists, evidence, unslop |
| **pstack-harness** | Detect host; map spawn / ask / worklist |
| **poteto-help** | Pick the right skill and hand you a prompt |

### Playbooks (23)

investigation · bug-fix · feature · refactoring · perf · hillclimb · runtime-forensics · trace-forensics · prototype · visual-parity · authoring-a-skill · eval · babysit · shipping · autonomous-run · orchestrate · autopilot-full · autopilot-stack · session-pickup · pause-safely · multi-phase-plan · worktree-cleanup · opening-a-pr

### Specialists (16)

how · why · architect · arena · swarm · interrogate · blast-radius · tdd · show-me-your-work · figure-it-out · benchmark-checklist · technical-writing · recall · teach · reflect · unslop

### Principles

Full index: `skills/poteto-mode/references/principles.md` (core, architecture, verification, meta).

## Harness tiers

1. Parallel subagents (optional multi-model)
2. Subagents, single model
3. No subagents → sequential multi-angle review (stated in the reply)

## License

MIT. Upstream methodology © Lauren Tan. Packaging © pstack-any contributors. See `LICENSE`, `ATTRIBUTION.md`, `UPSTREAM.md`.
