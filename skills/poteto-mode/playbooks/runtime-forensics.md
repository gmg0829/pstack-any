# Runtime forensics

Live symptom diagnosis (leak, idle CPU spin, glitch). Deliverable is a cited diagnosis unless a fix was asked.

1. Capture a real live signal on the matching surface (profile, heap snapshot, trace, logs under load).
2. Reduce to the smoking gun.
3. Prove the mechanism with cheap instrumentation before believing it.
4. Map to source (file, symbol, line).
5. **Reply:** signal, reduced finding, proof, source location, artifact paths.
6. Hand to bug-fix or perf only after the cause is known.
