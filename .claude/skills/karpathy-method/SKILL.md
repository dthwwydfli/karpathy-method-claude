---
name: karpathy-method
description: Use when planning, coding, debugging, refactoring, or reviewing in any AI coding tool. Forces spec, verifier, and environment layers before implementation so vague requests become a clear, checkpointed build process.
---

# Karpathy Method

Turn a vague request into a clear build process. Three layers, in order, before any code.

## Core flow

1. **Spec** — define the real goal and the smallest useful step.
2. **Verifier** — define what success and failure look like.
3. **Environment** — check conventions, guardrails, and protected files.
4. **Implement** — only after the above is clear. Stop at the next checkpoint.

Reference files hold the detail:
- `references/spec.md`
- `references/verifier.md`
- `references/environment.md`

## Layer 1: Spec

Before coding, identify:
- The real goal (not the literal request).
- The smallest useful version of the task.
- Assumptions that need confirming.
- The next checkpoint for review.

Ask clarifying questions when the goal is unclear. Prefer small, testable steps over large all-at-once plans. See `references/spec.md`.

## Layer 2: Verifier

Before shipping, define:
- What success looks like.
- What counts as failure.
- What to check manually.
- What to check with code, tests, or another model.

Use a critic mindset. Do not assume the first answer is correct. See `references/verifier.md`.

## Layer 3: Environment

Check:
- Repo structure and existing conventions.
- Files that must not be edited.
- Required hooks, linting, or tests.

Respect guardrails. If a rule must be enforced, put it in a hook or script, not only in prose. See `references/environment.md`.

## When to use

- New features.
- Refactors.
- Debugging.
- AI-assisted planning.
- Code review.
- Hackathon / fast build workflows.

## How to apply per task type

- **Coding** — full loop: spec → verifier → environment → implement.
- **Debugging** — spec = reproduce + expected behavior; verifier = the failing case now passes; environment = no protected files touched.
- **Refactoring** — spec = behavior stays identical; verifier = existing tests still green; environment = respect module boundaries.
- **Planning** — spec + verifier only; produce checkpoints and success criteria, no code yet.
