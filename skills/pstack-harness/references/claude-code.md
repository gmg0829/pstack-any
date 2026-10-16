# Claude Code harness

## spawn

Use the Agent / Task-style tool the session exposes. Prefer explicit read-only for reviewers.

## ask-user

Use `AskUserQuestion` when present.

## worklist

Use the session's todo / plan tools when present.

## models

Honor any project or user model routing the user configured. Do not invent provider slugs.
