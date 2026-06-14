# Spec Layer

Translate a task into a buildable plan before writing code.

## Goal

Get from "what was asked" to "what is actually needed and the smallest step toward it."

## Questions to answer

- What is the actual goal behind the request?
- What is the smallest useful version that delivers value?
- What assumptions are we making, and which need confirming?
- What is the next checkpoint where a human reviews?
- What is explicitly out of scope for now?

## Rules

- Prefer short iteration loops.
- Break large tasks into smaller milestones.
- Confirm the goal before implementation.
- Do not build extra scope early.
- State assumptions out loud; do not hide them in code.

## Spec template

```markdown
# Spec: <task name>

## Goal
<the real outcome, in one or two sentences>

## Smallest useful version
<the minimum slice worth building first>

## Assumptions
- <assumption — confirmed | needs confirming>

## Out of scope
- <thing we are deliberately not doing yet>

## Checkpoints
1. <first reviewable milestone>
2. <next milestone>

## Open questions
- <question for the user, if any>
```
