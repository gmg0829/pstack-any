# Visual parity

Pixel-exact (or agreed tolerance) UI equivalence between two implementations.

1. Define **A** (reference) and **B** (candidate) and the surfaces/viewport to compare.
2. Capture both under the same conditions.
3. Diff systematically (not glance). List proven deltas only.
4. Fix only proven deltas. Re-capture after each batch.
5. Stop when captures match within the agreed rule.
6. **Reply:** surfaces compared, deltas found, fixes, final match evidence.
