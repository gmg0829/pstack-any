# Principles index

Apply when relevant. Name only principles that changed a decision.

## Core

| Principle | Rule |
|-----------|------|
| laziness-protocol | Bias to deletion and the smallest change that solves the problem |
| foundational-thinking | Core types and structures first; scaffold before feature noise |
| redesign-from-first-principles | Treat new requirements as if foundational from day one |
| attack-the-premise | When fixes share a failing premise, test the premise directly |
| subtract-before-you-add | Remove dead weight first |
| minimize-reader-load | Fewer layers, less hidden state, collapse one-caller wrappers |
| outcome-oriented-execution | Converge on target architecture; avoid throwaway compatibility states |
| experience-first | User delight over implementer convenience |
| exhaust-the-design-space | 2–3 alternatives before committing on novel decisions |
| build-the-lever | Tool/script/codemod over one-off hand work |

## Architecture

| Principle | Rule |
|-----------|------|
| model-the-domain | Structure over scattered conditionals |
| boundary-discipline | Guards at edges; pure logic inside |
| type-system-discipline | Illegal states unrepresentable; parse at boundaries |
| make-operations-idempotent | Same end state under retries/crashes |
| migrate-callers-then-delete | One wave; no permanent dual APIs |
| separate-before-serializing-shared-state | Eliminate concurrent sharing of the same mutable location |

## Verification

| Principle | Rule |
|-----------|------|
| prove-it-works | Real artifact, not proxy |
| fix-root-causes | First wrong place; guards only for legitimate states |
| sequence-verifiable-units | Small units each ending in a check |
| test-behavior-not-implementation | Assert what observers see |
| explain-the-number | Know the limiter before trusting a measurement |

## Meta

| Principle | Rule |
|-----------|------|
| guard-the-context-window | Bulk in children; summaries in parent |
| never-block-on-the-human | Reversible work proceeds |
| encode-lessons-in-structure | Lint/runtime/script over repeated prose |
