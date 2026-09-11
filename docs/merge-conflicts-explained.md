# Merge Conflicts, Explained

## Why they happen

Git merges changes automatically when it can. A **merge conflict** happens when two branches changed the *same lines* of the *same file* in different ways, and Git can't guess which version you want.

This isn't an error you did something wrong — it's normal, especially when multiple people work on the same file.

## What it looks like

When a conflict happens, Git marks the file directly, in place:

<<<<<<< HEAD
This is the version on your current branch.
=======
This is the version from the branch you're merging in.
>>>>>>> other-branch
```

- Everything between `<<<<<<< HEAD` and `=======` is **your** version.
- Everything between `=======` and `>>>>>>> other-branch` is **the incoming** version.

## How to fix one

1. Run `git status` — it lists every file with a conflict.
2. Open each conflicted file. Decide what the final content should be — keep yours, keep theirs, or write something that combines both.
3. **Delete the conflict markers themselves** (`<<<<<<<`, `=======`, `>>>>>>>`). Leaving them in is the most common mistake — the file will look "fixed" but still contains broken markers.
4. Stage the resolved file:
   ```bash
   git add path/to/file
   ```
5. Commit:
   ```bash
   git commit -m "Resolve merge conflict in path/to/file"
   ```

## Avoiding conflicts in the first place

- Pull the latest changes (`git pull upstream main`) before starting new work.
- Keep branches short-lived — the longer a branch exists, the more likely `main` has moved underneath it.
- Keep PRs small and scoped to one issue, so fewer lines overlap with other people's work.

## Practice

Drill `03-merge-conflict` in [`practice/drills/`](../practice/drills/03-merge-conflict) is a safe place to cause and fix a real conflict before it happens on a real PR.
