# Section 03: How to Contribute to a Project Using GitHub

## 🎯 In this section

This is where everything comes together. Session 01 gave you Git on your computer. Session 02 taught you how to read a repository on GitHub. This section walks the full path from "I found a project" to "I have a real pull request open" — fork, clone, branch, commit, push, review, merge.

By the end you will be able to: fork and clone a repository, pick an issue and work on it correctly, open a pull request that gets reviewed instead of ignored, and avoid the mistakes that make maintainers close a PR without looking at it twice.

Work through the Session 03 drills on the Practice drills page before moving on.

---

## 1. Forking a Repository

A **fork** is your own copy of someone else's repository, created under your GitHub account. You can't push directly to most projects you don't own — forking gives you a copy you're allowed to push to.

- On the project's GitHub page, click **Fork** (top right).
- GitHub creates `github.com/your-username/repo-name` — a full copy, history included.
- This only happens once per project. After that, you clone *your* fork, not the original.

---

## 2. Cloning Your Fork & Setting Up Remotes

**Clone** your fork to your computer:

```bash
git clone https://github.com/your-username/repo-name.git
cd repo-name
```

This gives you one remote, `origin`, pointing at your fork. But the original project keeps moving after you fork it — you need a second remote to stay in sync with it:

```bash
git remote add upstream https://github.com/original-owner/repo-name.git
```

Check both are set correctly:

```bash
git remote -v
```

- **`origin`** — your fork. You push here.
- **`upstream`** — the original project. You pull from here to stay current.

This is the single most confused concept for new contributors. If you only remember one thing from this topic: **you push to `origin`, you pull from `upstream`.**

---

## 3. Picking an Issue & Creating a Branch

Find an issue labeled `good first issue` (Section 02, Topic 6). Before writing any code:

- Comment on the issue saying you'd like to work on it. Some maintainers assign it to you; some don't require this — check `CONTRIBUTING.md`.
- Confirm nobody else is already assigned or has an open PR for it.

Then create a branch off `main` for your work:

```bash
git checkout -b fix-issue-42
```

**Best practice:** name the branch after what it does or the issue it closes, not something generic like `patch-1`.

---

## 4. Making Changes & Committing

This is Section 01, applied for real. Edit the files the issue asks for, then:

```bash
git status
git add .
git commit -m "Fix broken link in installation docs (#42)"
```

Referencing the issue number in your commit message helps reviewers trace the change back to why it exists. Keep the commit scoped to the issue — don't fix unrelated things in the same commit "while you're in there."

---

## 5. Pushing & Opening a Pull Request

Push your branch to your fork (`origin`, not `upstream`):

```bash
git push origin fix-issue-42
```

On GitHub:

1. Go to your fork. You'll usually see a yellow banner: **"Compare & pull request."** Click it.
2. Confirm the base repository is the *original* project, not your fork, and the base branch is `main`.
3. Write a clear title and description. If your PR fully resolves the issue, include `Closes #42` in the description — GitHub auto-closes the issue when the PR merges.
4. Click **Create Pull Request**.

---

## 6. The Code Review Process

Opening the PR isn't the end — it's the start of a conversation.

- A maintainer may leave **review comments** on specific lines, or **request changes** on the whole PR.
- Don't open a new PR to fix feedback. Make the changes on the same branch and push again:

```bash
git add .
git commit -m "Address review feedback"
git push origin fix-issue-42
```

The existing PR updates automatically with your new commits — no new PR needed.

- Respond to comments, even briefly, so the reveiwer knows you've seen them.
- If a review goes quiet for a while, a polite follow-up comment is normal, not rude.

---

## 7. Merging & Syncing Your Fork

Once your PR is approved and merged, your fork's `main` is now behind the real project's `main`. Sync it before your next contribution:

```bash
git checkout main
git pull upstream main
git push origin main
```

Then delete the now-merged branch, locally and on GitHub, to keep things tidy:

```bash
git branch -d fix-issue-42
git push origin --delete fix-issue-42
```

---

## 8. Common Mistakes New Contributors Make

- **Opening a PR straight from `main`** instead of a feature branch — makes it hard to work on anything else while it's in review.
- **No issue reference** in the PR — reviewers can't tell why the change exists.
- **Huge, unfocused PRs** — bundling five unrelated fixes into one PR makes it harder to review and more likely to get rejected outright.
- **Ignoring `CONTRIBUTING.md`** — every project has different conventions; skipping this step is the fastest way to get a PR closed unread.
- **Force-pushing over review history** (`git push --force`) after a reviewer has already commented — it can wipe the context of their feedback. Use `git push` normally; ask before force-pushing.
- **Going silent after requested changes** — an abandoned PR with unaddressed feedback is worse than not opening one at all.

---

## 📌 Quick Reference

| Step | Command / Action |
| --- | --- |
| Copy the project to your account | Click **Fork** on GitHub |
| Download your fork | `git clone https://github.com/you/repo.git` |
| Link back to the original project | `git remote add upstream <original-url>` |
| Start work on an issue | `git checkout -b branch-name` |
| Save your changes | `git add .` → `git commit -m "message (#issue)"` |
| Upload your branch | `git push origin branch-name` |
| Open the PR | "Compare & pull request" on GitHub |
| Update a PR after feedback | Commit + `git push origin branch-name` again |
| Sync your fork after merge | `git pull upstream main` → `git push origin main` |
| Clean up a merged branch | `git branch -d branch-name` |
