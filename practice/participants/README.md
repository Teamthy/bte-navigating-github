# Participants Wall

This is where **every attendee** practices the real PR flow (Drill 04) at the same time, without colliding with anyone else.

## The rule

Each person creates exactly **one new file**: `practice/participants/<your-github-username>.md`. Never edit anyone else's file. Because everyone is adding a new file instead of editing a shared one, PRs from 50 different attendees can all merge without a single conflict.

## How to add yours

1. Copy `TEMPLATE.md` to `practice/participants/<your-github-username>.md`
2. Fill it in
3. Commit, push, open a PR — see `docs/03-contributing-with-github.md`

Your PR auto-merges within a minute or two if it only touches your own file (see `.github/workflows/auto-merge-participants.yml`). No need to wait on a human reviewer.
