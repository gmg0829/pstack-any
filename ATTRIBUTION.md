# Attribution

## Upstream

The engineering methodology in this repository — playbooks, principle names, and the "go deep first" workflow style — originates from **Lauren Tan** (`@poteto`) and the official Cursor plugin:

- https://github.com/cursor/plugins/tree/main/pstack

That work is MIT licensed. Copyright (c) 2026 Lauren Tan.

## This port

**pstack-any** is an unofficial, harness-agnostic packaging. It:

- Keeps the methodology and playbook intent
- Rewrites runtime assumptions so skills name neutral operations, not Cursor-only tools
- Adds a `pstack-harness` adapter that maps those operations onto the current agent

It is not affiliated with or endorsed by Lauren Tan or Cursor.

## Related ports (not dependencies)

Community ports that explore similar goals include (non-exhaustive):

- praveen221/pstack-grok
- mdsmithaustin/pstack
- backnotprop/pstack
- michael-denyer/pstack-claude
- painhardcore/pstack
- muhalifalgibran/open-stack

Use the official Cursor plugin when you are on Cursor and want the full upstream experience.
