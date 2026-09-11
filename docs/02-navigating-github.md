# Section 02: Navigating GitHub

## 🎯 In this section

GitHub is the website where your Git repository lives online. By the end of this section you will be able to: tell Git and GitHub apart, set up a profile that doesn't look abandoned, read a repository the way an experienced contributor does, understand issues and labels, and find a beginner-friendly project to contribute to.

Everything here is look-and-understand, not touch-and-change. Nothing in this section modifies a repository. Forking, cloning, and opening your first pull request is Session 03.

Work through the Session 02 drills on the Practice drills page before moving on.

---

## 1. What GitHub Is (vs. Git)

Git is the tool on your computer (Section 01). GitHub is a website that hosts a copy of your Git repository online.

- **Git** tracks history. It works with no internet connection and doesn't need GitHub to function.
- **GitHub** stores that history online, adds a UI on top of it, and adds things Git itself doesn't have: issues, pull requests, project boards, and a place for other people to find and collaborate on your code.

GitHub is one *host* for Git repositories. GitLab and Bitbucket do the same job differently — this course uses GitHub because it's the one you'll run into most in open source.

---

## 2. Setting Up a GitHub Profile That Stands Out

Before you contribute anywhere, your profile is the first thing a maintainer sees when your name shows up on an issue or PR.

- **Profile photo:** a real photo or clear avatar, not the default egg/identicon.
- **Bio:** one line — what you do or what your learning. No need to overthink it.
- **Pinned repositories:** pin 4–6 repos to the top of your profile. Pick the ones you'd actually want a stranger to see first.
- **Profile README:** create a repository with the exact same name as your username (e.g. `yourusername/yourusername`) and add a `README.md`. GitHub renders it directly on your profile page.

None of this is required to contribute. It's the difference between a profile that looks active and one that looks like a placeholder.

---

## 3. Anatomy of a Repository

Every GitHub repository page has the same layout. Learn it once, recognize it everywhere:

- **File tree:** the folder/file structure of the project, browsable without cloning anything.
- **README (rendered):** GitHub automatically displays `README.md` below the file tree. This is the project's front door.
- **Branch dropdown:** shows which branch you're currently viewing. Defaults to `main`.
- **Commits tab:** the full commit history — every snapshot, in order, with who made it and when.
- **Releases / Tags:** marked versions of the project, if the maintainers use them.
- **About panel (sidebar):** short description, website link, topics/tags the maintainers chose.

---

## 4. Reading CONTRIBUTING.md & Project Rules

Well-maintained projects have a `CONTRIBUTING.md` file — check the file tree or the About panel for a link. Before you write a single line for someone else's project, read it. It usually tells you:

- How to set up the project locally
- Branch naming conventions
- Commit message format they expect
- How to run tests before submitting
- Where to find (or how to propose) issues to work on

Some repos also have a `CODE_OF_CONDUCT.md`. If a project has neither, that's a signal the maintainers may be less organized about accepting outside contributions — not a dealbreaker, just something to notice.

---

## 5. Issues & Labels

An **issue** is a tracked task, bug report, or discussion on a repository. This is where contribution usually starts.

- **Title & description:** what's wrong or what's wanted.
- **Labels:** color-coded tags maintainers use to categorize issues. The ones that matter most to you as a beginner:
    - `good first issue` — scoped small, meant for new contributors.
    - `help wanted` — maintainers are actively looking for outside help.
    - `bug` / `enhancement` / `documentation` — what kind of issue it is.
- **Comments:** discussion thread. Check if someone is already assigned or working on it before you start.
- **Assignees:** shows who (if anyone) has claimed the issue.

---

## 6. Finding Beginner-Friendly Projects

You don't need to guess which projects welcome new contributors — GitHub lets you search for exactly that:

- **github.com/topics/good-first-issue** — curated repositories that actively tag beginner issues.
- **github.com/topics/first-timers-only** — issues specifically reserved for first-time contributors.
- **Search bar syntax:** `label:"good first issue" state:open` inside any repo's Issues tab filters directly to what you can pick up.
- **Pick small, pick active:** favor projects with recent commits (check the Commits tab) over ones that haven't been touched in a year — a stale repo means slow or no review.

---

## 7. GitHub Search & Discovery (Stars, Forks & Watching)

Three buttons sit at the top of every repo — know what each one actually does before you use it:

- **Star:** bookmarks the repo to your profile. Signals popularity to others. Doesn't do anything functional.
- **Watch:** subscribes you to notifications for activity on the repo (issues, PRs, releases).
- **Fork:** creates your own copy of the repo under your account. This is the *first mechanical step* of contributing — covered in full in Session 03 — but useful to recognize now.

Beyond a single repo, GitHub's search bar works across the whole site:

- Search repositories, code, issues, and users from one search bar.
- Filter by language: `language:javascript`.
- Follow topics (e.g. `react`, `machine-learning`) to surface relevant projects in your feed.
- The **Explore** page (github.com/explore) surfaces trending and recommended repositories.

---

## 📌 Quick Reference

| What you want | Where / how |
| --- | --- |
| See a project's rules before contributing | `CONTRIBUTING.md` in the file tree |
| Find beginner-friendly work | Issues tab → `label:"good first issue"` |
| Check if a project is active | Commits tab → look at the last commit date |
| Get notified of repo activity | Watch button (top of repo) |
| Copy a repo to your own account | Fork button (top of repo) |
| See project version history | Releases / Tags |
| Search across all of GitHub | Search bar → filter by `language:`, topic, or type |
