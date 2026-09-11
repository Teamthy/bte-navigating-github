# Drill 02: Branching

## Task

1. Create a new branch: `git checkout -b practice-branch`
2. Confirm you're on it: `git branch` (the current branch has a `*` next to it)
3. Open `scratch.txt` and add any line.
4. Stage and commit it on this branch.
5. Switch back to `main`: `git checkout main`
6. Notice `scratch.txt` no longer shows your change — it's only on `practice-branch`.

## Check yourself

Run `git log --oneline --all --graph` to see both branches and where they diverge.
