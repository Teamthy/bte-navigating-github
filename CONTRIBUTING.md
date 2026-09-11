# Contributing to bte-navigating-github

Thanks for contributing. This is a practice repo, but the process is the real one — follow it exactly as you would on any other open source project.

## Before you start

1. Read [`docs/03-contributing-with-github.md`](docs/03-contributing-with-github.md) if you haven't gone through the course sections yet.
2. Pick an issue labeled [`good first issue`](../../issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).
3. Comment on the issue to claim it. Don't start work on an issue someone else has already claimed.

## Branch naming

`fix-<short-description>` or `add-<short-description>`, e.g. `fix-typo-glossary`.

## Commit messages

Follow [`docs/commit-message-pattern.md`](docs/commit-message-pattern.md). Short version: start with a verb (`Add`, `Fix`, `Update`, `Remove`, `Refactor`), reference the issue number:

```
Fix typo in glossary (#7)
```

## Pull requests

- One issue per PR. Don't bundle unrelated fixes.
- Include `Closes #<issue-number>` in the PR description so it auto-links.
- Fill out the PR template — don't delete the sections.
- Expect review comments. Push follow-up commits to the same branch; don't open a new PR.

## What NOT to do

- Don't PR directly against `main` without a feature branch.
- Don't force-push (`git push --force`) after a reviewer has left comments.
- Don't edit files outside the scope of your claimed issue.

## Code of Conduct

This project follows the [Code of Conduct](CODE_OF_CONDUCT.md). Be respectful — most people here are contributing for the first time ever.
