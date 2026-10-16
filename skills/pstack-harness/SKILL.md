---
name: pstack-harness
description: Maps pstack neutral operations to the current agent harness. Read before spawn, ask-user, worklist, or when a sibling skill path is unclear. Covers Cursor, Claude Code, Codex, Grok, OpenCode, and generic fallback.
---

# pstack-harness

Other pstack skills describe **intent**, not tool names. This skill maps intent to the live harness.

## Detect once per session

1. Check environment signals if present (CLI env vars, known tool names in your inventory).
2. Match tool fingerprints:
   - Structured ask + Task/Agent with subagent types → often **Cursor** or **Claude Code**
   - `spawn_subagent` → often **Grok**
   - Codex-style plan/update tools → **Codex**
   - Unknown → **generic**
3. If still unclear, ask the user once which harness this is, then keep that answer for the session.
4. Read `references/<harness>.md` if it exists; otherwise use `references/generic.md`.

Do not re-detect on every skill call.

## Neutral operations

| Intent | Meaning | Rule |
|--------|---------|------|
| **spawn** | Run work in a separate agent/context | Use the host's subagent/task tool if present. Pass file paths, not huge dumps. Prefer background when the host supports it. |
| **ask-user** | Structured question with options | Use the host's ask/question tool if present; else plain question in the reply. |
| **worklist** | Visible ordered steps | Use the host's todo/plan tool if present; else a short numbered list in the reply and keep it updated. |
| **read-sibling** | Load another pstack skill | Resolve under the installed skills root (`skills/<name>/SKILL.md` or host equivalent). |
| **readonly-child** | Review/explore without edits | Request read-only / explore capability when the host has it; else instruct the child not to edit. |

Never invent a tool that is not in your inventory. Say which mechanism you used when it affects evidence.

## Degradation tiers

| Tier | Capability | How panels (arena / swarm / interrogate) run |
|------|------------|-----------------------------------------------|
| 1 | True parallel subagents + optional multi-model | Fan out, then aggregate |
| 2 | Subagents, single model | Parallel or sequential children, same model |
| 3 | No subagents | Sequential multi-angle passes **inline**; state the degradation |

## Models and roles

Skills name **roles** (code delegate, judgment, reviewer), not vendor slugs.

- If the host has a pstack models config, use it.
- Else inherit the parent session model.
- Do not invent model IDs you have not seen in the host's model list.

## Paths

Skills and playbooks live under the installed package's `skills/` tree. Prefer relative reads from this skill's location: `../poteto-mode/SKILL.md`, `../how/SKILL.md`, etc.
