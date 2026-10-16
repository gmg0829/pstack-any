# Feature

New or changed behavior from a named data shape.

1. **Name the data shape.** Core type/structure that owns the behavior.
2. **Settle boundaries** if crossing modules (architect): caller usage, types, ownership, errors.
3. **Implement the smallest vertical slice** that delivers observable behavior. Prefer deleting conflicting old paths in the same wave when possible.
4. **Verify** the observable behavior on the real surface.
5. **Reply:** shape chosen, what was built, how verified, what was left out.
