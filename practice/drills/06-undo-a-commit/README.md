# Drill 06: Undo a Commit

## Task

1. Open `log.txt`, add a line, then commit it with a deliberately bad message: `git commit -m "stuff"`
2. Realize the message is bad. Undo the commit without losing the change: `git reset --soft HEAD^`
3. Run `git status` — your edit is back in the staging area, uncommitted.
4. Commit again with a proper message following the `Add/Fix/Update` convention.

## Check yourself

`git log --oneline -1` should show your corrected message, not "stuff."
