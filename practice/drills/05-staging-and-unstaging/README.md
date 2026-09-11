# Drill 05: Staging and Unstaging

## Task

1. Open `draft.txt`. Make two separate edits: add a line under "Section A" and a different line under "Section B."
2. Run `git status` — both changes show as modified, unstaged (red).
3. Stage only the Section A change: `git add practice/drills/05-staging-and-unstaging/draft.txt`, then check `git status` again — it now shows staged (green).
4. Change your mind. Unstage it: `git restore --staged practice/drills/05-staging-and-unstaging/draft.txt`
5. Now stage and commit both changes together.

## Check yourself

`git status` should show "nothing to commit, working tree clean" at the end.
