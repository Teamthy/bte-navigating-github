# Drill 09: Syncing Your Fork After a Merge

Do this after your Drill 04 PR gets merged. Applies Section 03, Topic 7.

## Task

1. Switch to your local `main`: `git checkout main`
2. Pull the merged change down from the real project: `git pull upstream main`
3. Push the update to your own fork so it matches: `git push origin main`
4. Delete your now-merged branch, locally and on GitHub:
   ```bash
   git branch -d add-your-name
   git push origin --delete add-your-name
   ```

## Check yourself

`git branch` should show only `main` — no leftover feature branches. Your fork's `main` on GitHub should show your merged commit.
