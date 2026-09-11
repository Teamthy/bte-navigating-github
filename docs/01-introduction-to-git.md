# Section 01: Introduction to Git

## 🎯 In this section

Git is the tool that runs on your computer and tracks every change to your project. By the end you will be able to: understand how Git tracks a project, install Git and set your identity, track files with `git add`, save snapshots with `git commit`, push to a remote, undo mistakes safely, and work on branches without breaking the main copy.

Everything here is local. The website side, GitHub, is Session 02. Opening your first real pull request is Session 03.

Work through the Session 01 drills on the Practice drills page before moving on.

---

## 1. What Git Is & The 3 Zones

Before diving into commands, understand that Git tracks your project across 3 main zones on your computer:

1. **Working Directory:** The files on your computer that you are currently editing in your code editor (VS Code, etc.).
2. **The Staging Area (Index):** A temporary holding zone where you select which modified files you want to include in your next snapshot.
3. **Local Repository (History):** The permanent history of snapshots (commits) saved locally on your machine.

There's a 4th zone, the **Remote (GitHub):** an online copy of your repository hosted on GitHub so others can collaborate and review your code. Session 02 covers it in full.

---

## 2. Install Git

Git is a free tool that runs in your terminal and tracks every change to a folder of files. Install it once, then verify it works.

**Windows:** download the installer from git-scm.com and install with the default options. Git Bash comes with it, so use Git Bash for all commands in this course.

**macOS:** download from git-scm.com, or run `brew install git` if you use Homebrew.

**Linux (Ubuntu/Debian):** run `sudo apt install git` in your terminal.

Check that it worked by opening your terminal and typing:

```bash
git --version
```

If it prints a version number, git is ready. If your terminal says "command not found", restart the terminal and try again.

---

## 3. Configure Git (Tell Git Who You Are)

Git stamps every commit with a name and an email, so the project can credit your work. Set them once on your computer:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

- Use the email on your GitHub account.
- Don't want your real email public? On GitHub, go to Settings > Emails, copy the address that ends in `users.noreply.github.com`, and use that instead.

See everything you have set:

```bash
git config --list
```

**Optional default:** make new repositories start on the `main` branch instead of the older `master` name:

```bash
git config --global init.defaultBranch main
```

---

## 4. Checking Status & Staging Files

### Check your status (`git status`)

Whenever you want to see what files you've modified, created, or deleted, run:

```bash
git status
```

- **Red files:** modified or new files Git sees, but aren't staged yet.
- **Green files:** staged files ready to go into a snapshot.

### Stage files (`git add`)

Git doesn't automatically save every file you touch. Tell it which files to include in your next snapshot.

To stage a specific file:

```bash
git add path/to/file.tsx
```

To stage all modified and new files in the current folder:

```bash
git add .
```

---

## 5. Committing Snapshots

A **commit** takes all your staged files and locks them into a permanent snapshot in your local history, with a message explaining what you did.

```bash
git commit -m "Add admin dashboard attempt tracking page"
```

**Best pratice:** write clear, concise commit messages starting with a verb — *Add*, *Fix*, *Update*, *Refactor*.

---

## 6. Pushing to a Remote

Commits live on your computer until you **push** them up to a remote — your repository on GitHub.

```bash
git push origin <branch-name>
```

*(Example: `git push origin user-cleanup`)*

---

## 7. Undoing Mistakes

Mistakes happen. Here's how to travel backward when things go wrong.

**You changed a file, haven't staged it, and want to throw away the changes:**

```bash
git restore <filename>
```

**You staged a file (`git add`) but want to unstage it:**

```bash
git restore --staged <filename>
```

**You committed, but realized you made a mistake or forgot something:**

```bash
git reset --soft HEAD^
```

This undoes your last commit without losing your code — everything goes back to staged/modified so you can fix it and commit again.

---

## 8. Working with Branches

Branches let you work on a new feature or fix without touching the main stable code (usually `main`).

**Check which branch you're on:**

```bash
git branch
```

**Create and switch to a new branch:**

```bash
git checkout -b feature/my-new-feature
```

*(Or: `git switch -c feature/my-new-feature`)*

**Switch between existing branches:**

```bash
git checkout branch-name
```

---

## 📌 Quick Cheat Sheet (Copy-Paste Reference)

| Action | Command |
| --- | --- |
| Check git is installed | `git --version` |
| Set your name | `git config --global user.name "Your Name"` |
| Set your email | `git config --global user.email "you@example.com"` |
| See your settings | `git config --list` |
| Check status of files | `git status` |
| Stage all changes | `git add .` |
| Save snapshot (commit) | `git commit -m "Your message here"` |
| Push branch to GitHub | `git push origin <branch-name>` |
| Download latest changes from GitHub | `git pull` |
| View commit history | `git log --oneline` |
| Unstage a file | `git restore --staged <filename>` |
| Undo last commit (keep code) | `git reset --soft HEAD^` |
| See current branch | `git branch` |
| Create + switch branch | `git checkout -b branch-name` |
