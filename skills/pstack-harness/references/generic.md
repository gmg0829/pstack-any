# Generic harness

Use when the host is unknown or has no subagent API.

## spawn

Do the work in the current session. For "N reviewers", run N sequential passes with different angles (correctness, invariants, edge cases, reader load). Label each pass. Synthesize at the end.

## ask-user

Ask in normal prose. If options help, list them as 1/2/3.

## worklist

Numbered list in the reply. Update status in subsequent replies (done / in progress / blocked).

## readonly-child

Same session; do not edit until the parent step says to implement.

## Evidence

Still required. Run commands, read files, capture output. Generic does not mean skip verification.
