# Perf

Measured slowness. Improve against a baseline.

1. **Establish a baseline** on the real surface (same load shape the user cares about). Record method, sample count, and the number.
2. **Hypothesize** from the profile or measurement, not from taste.
3. **Change one lever at a time.** Measure before/after with the same method.
4. **Accept only** changes that improve the measured number and whose limiter you can explain (**explain-the-number**, **benchmark-checklist**).
5. Revert changes that do not move the metric.
6. **Reply:** baseline, limiter, change, after number, how measured.
