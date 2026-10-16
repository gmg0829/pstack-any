# Grok harness

## spawn

Prefer `spawn_subagent` when available. Children typically cannot spawn further children — parent owns fan-out.

- Code-style delegates: background when supported
- Reviewers: read-only / explore capability when available
- Pass paths, not inlined file dumps

If `spawn_subagent` is missing, fall back to `generic.md`.

## ask-user

Use `ask_user_question` when present; else plain prose.

## worklist

Use the host todo tool if present; else numbered list.

## models

Use only model slugs the host lists. Roles without a config line inherit the parent model.
