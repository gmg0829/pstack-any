# pstack-any

Harness-agnostic packaging of Lauren Tan's (**@poteto**) pstack engineering workflows.

**If you want to go fast, go deep first.** Throughput without quality is not the goal.

| | |
|--|--|
| Upstream (Cursor plugin) | [cursor/plugins · pstack](https://github.com/cursor/plugins/tree/main/pstack) |
| This repo | Unofficial port · neutral operations · multi-harness adapters |
| License | MIT · see `LICENSE`, `ATTRIBUTION.md`, `UPSTREAM.md` |

Skills name **neutral operations**. **pstack-harness** maps them onto Cursor, Claude Code, Codex, Grok, OpenCode, or a sequential fallback.

---

## Install

### skills CLI

```bash
npx skills add gmg0829/pstack-any
```

### Manual copy

```bash
git clone https://github.com/gmg0829/pstack-any.git
cp -R pstack-any/skills/* /path/to/agent/skills/
```

| Agent | Typical path |
|-------|----------------|
| Claude Code | `.claude/skills/` or `~/.claude/skills/` |
| Cursor | project / user skills |
| Codex | `.agents/skills/` |
| Grok | `~/.grok/skills/` |
| OpenCode | `.opencode/skills/` |

More detail: `docs/install.md`.

| Profile | Skills |
|---------|--------|
| Minimal | `poteto-mode`, `pstack-harness`, `unslop` |
| Recommended | + `how`, `why`, `architect`, `interrogate`, `tdd` |
| Full | entire `skills/` tree |

---

## Quick start

| Goal | Prompt |
|------|--------|
| Bug with evidence | `/poteto-mode this bug happens when idle. repro first, then fix and verify.` |
| Feature slice | `Use poteto-mode: add --json. text output byte-identical. verify both.` |
| Pick a skill | `/poteto-help which skill for reviewing this branch?` |
| Confirm install | `/poteto-mode confirm harness detection and list playbooks` |

---

## Orchestration

| Skill | Role |
|-------|------|
| **poteto-mode** | Match playbook · worklist · route specialists · evidence · unslop |
| **pstack-harness** | Detect host · map spawn / ask-user / worklist · degrade honestly |
| **poteto-help** | Map intent → skill/playbook · return a copy-paste prompt |

---

## Playbooks (23)

| Playbook | When to use |
|----------|-------------|
| **investigation** | Read-only how / why / are-we-sure |
| **bug-fix** | Repro → root cause with runtime evidence → minimal fix → verify |
| **feature** | Named data shape → boundaries → smallest vertical slice → verify |
| **refactoring** | Capture behavior → structural change only → re-verify |
| **perf** | Baseline → measure → accept only explained improvements |
| **hillclimb** | Loop hypotheses with before/after measurement; one commit per win |
| **runtime-forensics** | Live symptom: capture signal → reduce → prove mechanism → map to source |
| **trace-forensics** | Same for a captured profile / trace / heap snapshot |
| **prototype** | Minimal observable sketch to settle a design fork |
| **visual-parity** | Pixel-exact (or agreed) equivalence between two UIs |
| **authoring-a-skill** | Write or edit a `SKILL.md` |
| **eval** | Blinded test of skill/prompt impact on agent behavior |
| **babysit** | Drive PR/stack to merge-ready (CI, conflicts, threads) |
| **shipping** | Independently verify; land only contiguous verified run from root |
| **autonomous-run** | Long run without stopping; persist a decision trail |
| **orchestrate** | Multi-day coordinator: many PRs / workers |
| **autopilot-full** | Independent PRs to merged with root verdicts |
| **autopilot-stack** | One linear stack for the operator to review and land |
| **session-pickup** | Resume prior in-flight work from trail / git / state |
| **pause-safely** | Clean suspend for later pickup |
| **multi-phase-plan** | Phases with verifiable exits |
| **worktree-cleanup** | Safety-gated prune of merged/abandoned worktrees |
| **opening-a-pr** | Small ordered commits, conventional title, briefing body |

Paths: `skills/poteto-mode/playbooks/`.

---

## Specialists (16)

| Skill | Intent |
|-------|--------|
| **how** | Overview · key concepts · flow · where it lives · gotchas |
| **why** | Design history; separate recorded intent from inference |
| **architect** | Before crossing a boundary: callers, types, ownership, errors |
| **arena** | N attempts at the same problem; graft the best |
| **swarm** | Partition slices; aggregate one report |
| **interrogate** | Multi-angle adversarial review; do not auto-apply |
| **blast-radius** | Dependents + shared state; prove safety with a running check |
| **tdd** | Failing check first when a cheap local path exists |
| **show-me-your-work** | Decision trail the operator can commit |
| **figure-it-out** | Custom short rigorous sequence ending in verification |
| **benchmark-checklist** | Vet limiter, method, noise, end-to-end relevance |
| **technical-writing** | Docs, RFCs, PR bodies, commit subjects |
| **recall** | Rebuild current-state brief from session + history |
| **teach** | Layered understanding, not just a summary |
| **reflect** | Encode session lessons into structure |
| **unslop** | Strip AI tells from prose |

---

## Principles

Full table: `skills/poteto-mode/references/principles.md`.

| Group | Examples |
|-------|----------|
| Core | laziness-protocol · foundational-thinking · attack-the-premise · subtract-before-you-add |
| Architecture | model-the-domain · boundary-discipline · type-system-discipline |
| Verification | prove-it-works · sequence-verifiable-units · explain-the-number |
| Meta | guard-the-context-window · never-block-on-the-human · encode-lessons-in-structure |

Name only principles that changed a decision.

---

## Harness tiers

| Tier | Capability | Arena / swarm / interrogate |
|------|------------|-----------------------------|
| **1** | Parallel subagents · optional multi-model | Fan out, then aggregate |
| **2** | Subagents · single model | Parallel or sequential children |
| **3** | No subagents | Sequential multi-angle passes inline · state the degradation |

Adapters: `skills/pstack-harness/references/` (`generic`, `grok`, `claude-code`, `codex`, `cursor`).

---

## Layout

```text
skills/
  poteto-mode/          # orchestrator + playbooks + principles
  pstack-harness/       # host detection + adapters
  poteto-help/
  how/ why/ architect/ …
docs/
config/models.example.md
```

---

## License

MIT. Upstream methodology © Lauren Tan. Packaging © pstack-any contributors.
