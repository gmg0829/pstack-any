# pstack-any models (example)

Roles name intent, not vendor IDs. Copy to a host-specific location if your harness supports per-role routing.

```text
# default roles — inherit parent when unset
code-delegate: inherit-parent
judgment: inherit-parent
reviewer: inherit-parent
swarm-worker: inherit-parent

## Optional harness sections (examples only)
## grok
# code-delegate: grok-4
# judgment: grok-4

## claude-code
# judgment: opus
# code-delegate: sonnet
```

If the host cannot set per-child models, all roles run on the session model. That is fine.
