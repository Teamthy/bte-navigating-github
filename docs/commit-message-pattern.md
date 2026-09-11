# Commit Message Pattern

Every commit in this course follows one pattern:

```
<Verb> <what changed> (#issue-number)
```

The issue number is optional for practice drills, required for real contributions (Section 03).

## Approved verbs

| Verb | Use when |
| --- | --- |
| `Add` | New file, new section, new content that didn't exist before |
| `Fix` | Correcting something broken — a bug, typo, or broken link |
| `Update` | Changing existing content or behavior |
| `Remove` | Deleting a file or section |
| `Refactor` | Restructuring without changing what it does |

## Good vs. bad

| Bad | Good |
| --- | --- |
| `stuff` | `Fix typo in glossary (#7)` |
| `updates` | `Update branch naming convention in CONTRIBUTING.md` |
| `fixed it` | `Fix broken link to CONTRIBUTING.md in README (#12)` |
| `wip` | `Add participant template file` |
| `changes to docs` | `Add "detached HEAD" definition to glossary` |

## Why this matters

`git log --oneline` is only useful if the messages mean something. A history of `fix`, `update`, `stuff` tells a reviewer nothing about what actually happened — they have to open every commit to find out. A verb-first, specific message means someone can skim the whole history and understand the project's story without opening a single diff.

## Rules of thumb

- Keep the first line under ~50 characters.
- Describe *what changed*, not *how you felt about it* — `Fix broken link` not `finally fixed that annoying link`.
- One logical change per commit. If your message needs "and" to describe it, it's probably two commits.
