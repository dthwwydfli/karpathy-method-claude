# Environment Layer

Make the workspace predictable so the agent works inside known rules.

## Goal

Encode conventions, guardrails, and protected files once, so every task respects them without re-explaining.

## Questions to answer

- What repo conventions already exist (structure, naming, style)?
- What files or folders are protected from edits?
- What hooks, linters, or tests should run automatically?
- What repeated task should become a skill, script, or template?

## Rules

- Keep reusable context in files, not in memory.
- Use hooks for hard enforcement; prose alone is not a guardrail.
- Use skills for reusable reasoning and workflows.
- Keep the workspace structured and discoverable.
- When a rule keeps getting broken, move it from prose to a check.

## Environment template

```markdown
# Environment: <repo name>

## Conventions
- Language / framework: <...>
- Style: <formatter, lint rules>
- Structure: <where things live>

## Protected files
- <path> — do not edit
- <path> — edit only with explicit approval

## Automatic checks
- Lint: <command / hook>
- Tests: <command / hook>
- Pre-commit: <...>

## Repeated tasks → reusable
- <task> → <skill | script | template>
```
