# Cheat Sheet: Copy-Paste Reference

## Setup

| Task | Command |
| --- | --- |
| Check git is installed | `git --version` |
| Set your name | `git config --global user.name "Your Name"` |
| Set your email | `git config --global user.email "you@example.com"` |
| See your settings | `git config --list` |

## Everyday Git

| Task | Command |
| --- | --- |
| Check status of files | `git status` |
| Stage all changes | `git add .` |
| Stage one file | `git add path/to/file` |
| Save snapshot (commit) | `git commit -m "message"` |
| View commit history | `git log --oneline` |
| Unstage a file | `git restore --staged <filename>` |
| Discard uncommitted changes | `git restore <filename>` |
| Undo last commit (keep code) | `git reset --soft HEAD^` |

## Branches

| Task | Command |
| --- | --- |
| See current branch | `git branch` |
| Create + switch branch | `git checkout -b branch-name` |
| Switch branches | `git checkout branch-name` |
| Delete a merged branch | `git branch -d branch-name` |

## Remotes & Contributing

| Task | Command |
| --- | --- |
| Clone your fork | `git clone <fork-url>` |
| Link the original project | `git remote add upstream <original-url>` |
| List remotes | `git remote -v` |
| Push branch to your fork | `git push origin branch-name` |
| Pull latest from original project | `git pull upstream main` |
| Delete a remote branch | `git push origin --delete branch-name` |

## GitHub Search

| Task | Syntax |
| --- | --- |
| Find beginner issues in a repo | `label:"good first issue" state:open` |
| Search by language | `language:javascript` |
