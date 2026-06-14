# Verifier Layer

Define how output will be checked before you write it.

## Goal

Know what "done and correct" means in advance, so verification is not guesswork after the fact.

## Questions to answer

- What does success look like, concretely?
- What would fail the task?
- What tests or checks can prove the result?
- What edge cases must hold?
- What external signal (run, test, lint, another model) confirms correctness?

## Checks

- **Correctness** — does it do what the spec said? Match output against the stated goal.
- **Tests** — do new and existing tests pass? Add a test for the change when feasible.
- **Edge cases** — empty input, large input, errors, concurrency, boundaries.
- **Review** — readable, consistent with the codebase, no dead code, no leftover debug.

## Rules

- Define criteria before implementation.
- Prefer measurable checks over opinion.
- Use another model or a review pass when stakes are high.
- Do not trust output without validation.
- A failing check is information, not a setback — report it plainly.

## Verification template

```markdown
# Verify: <task name>

## Success criteria
- [ ] <observable condition that means done>

## Failure conditions
- <what would make this wrong>

## Checks to run
- [ ] Correctness: <how to confirm behavior>
- [ ] Tests: <command / which tests>
- [ ] Edge cases: <list>
- [ ] Review: <readability / convention check>

## Result
<pass | fail + evidence>
```
