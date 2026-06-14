# karpathy-method-claude

A 3-layer framework for AI-assisted development: **spec → verifier → environment**, applied
before any code. Built for Claude Code and portable to Cursor and other AI coding tools.

## What it is

A reusable workflow that turns vague requests into a clear, checkpointed build process:

- **Spec** — define the real goal and the smallest useful step.
- **Verifier** — define what success and failure look like before implementing.
- **Environment** — encode conventions, guardrails, and protected files.

It works for coding, debugging, refactoring, planning, and code review.

## How to use it in Claude Code

1. The skill auto-loads from `.claude/skills/karpathy-method/`.
2. Invoke it for any non-trivial task — Claude works the three layers before writing code.
3. `claude.md` applies the non-negotiables and working style on every task.
4. Use the templates in the reference files to write a spec, a verification plan, and an
   environment note for a given task.

In other tools: point the assistant at `claude.md` and the `references/` files, or paste the
relevant template into your prompt.

## Folder structure

```
.
├── claude.md                                  # always-on project instructions
├── README.md
└── .claude/skills/karpathy-method/
    ├── SKILL.md                               # skill entry: when to use + 3-layer flow
    └── references/
        ├── spec.md                            # spec workflow + template
        ├── verifier.md                        # verification workflow + template
        └── environment.md                     # guardrails, protected files + template
```

The skill also ships supporting `docs/`, `workflows/`, and `templates/` folders; the files
above are the core of the framework.

## Setup

1. Clone the repo, or copy `.claude/skills/karpathy-method/` into your project's `.claude/skills/`.
2. Copy `claude.md` to your repo root (merge with an existing one if present).
3. Open any task and apply the spec → verifier → environment loop.

No build step or dependencies. Markdown only.
