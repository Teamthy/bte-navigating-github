# Drill 03: Causing and Fixing a Merge Conflict

## Task

1. On `main`, open `shared.txt` and change line 1 to anything. Commit it.
2. Create a branch from *before* that commit: `git checkout -b conflict-branch HEAD^`
3. On `conflict-branch`, change line 1 to something different. Commit it.
4. Switch to `main` and merge: `git merge conflict-branch`
5. Git will report a conflict in `shared.txt`. Open it, resolve it (see `docs/merge-conflicts-explained.md`), then:
   ```bash
   git add shared.txt
   git commit -m "Resolve merge conflict in shared.txt"
   ```

## Check yourself

Open `shared.txt` — there should be no `<<<<<<<`, `=======`, or `>>>>>>>` markers left in it.
