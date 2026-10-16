# Trace forensics

Diagnose a **captured** profiling artifact (cpuprofile, trace, spindump, heap snapshot).

1. Load the artifact. Do not guess from source alone.
2. Reduce to the smoking gun (hot path, retainer chain, wait graph).
3. Map to source: file, symbol, line.
4. If the artifact is huge, summarize in a child context (**guard-the-context-window**) and keep the reduced finding in the main thread.
5. **Reply:** artifact path, reduced finding, source map. Fix only if asked — else hand to bug-fix or perf.
