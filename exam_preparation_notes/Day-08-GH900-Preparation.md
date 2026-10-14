# GH-900 Preparation — Day 8
## End-to-End GitHub Hands-On

**Goal:** Practice one integrated workflow that touches Git, collaboration, Actions, Projects, and repository settings.

---

## Part 1 — Create an Issue
Example title:
```text
Add Day 8 end-to-end workflow
```

Description includes:
- feature branch
- notes
- PR
- Actions
- link PR to Issue
- merge

Use label:
```text
documentation
```

---

## Part 2 — Sync local repo
```bash
git switch main
git pull
git status
```

Create branch:
```bash
git switch -c feature/day8-workflow
```

---

## Part 3 — Make and commit a change
Create:
```text
day8.md
```

Then:
```bash
git status
git add day8.md
git status
git commit -m "Add Day 8 end-to-end workflow notes"
```

Observe:
```text
Untracked → Staged → Committed
```

---

## Part 4 — Push branch
```bash
git push -u origin feature/day8-workflow
```

---

## Part 5 — Open Pull Request
Target:
```text
feature/day8-workflow → main
```

Use:
```text
Closes #<issue-number>
```

---

## Part 6 — Inspect PR areas
- Conversation
- Commits
- Checks
- Files changed

---

## Part 7 — Add GitHub Actions validation
Create:
```text
.github/workflows/gh900-check.yml
```

Example:
```yaml
name: GH900 Validation

on:
  pull_request:
  push:

jobs:
  validate:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Display repository files
        run: ls -la

      - name: Validate Day 8 file
        run: test -f day8.md
```

Then:
```bash
git add .github/workflows/gh900-check.yml
git commit -m "Add GH900 validation workflow"
git push
```

Map:
```text
pull_request / push = events
GH900 Validation = workflow
validate = job
ubuntu-latest = runner
each named command = step
```

---

## Part 8 — Review and Merge
Inspect file changes and checks.

Use **Squash and merge** if available to demonstrate:
```text
multiple feature commits → one commit on main
```

Delete feature branch after merge.

---

## Part 9 — Verify automatic Issue closure
Because PR included:
```text
Closes #<issue-number>
```
the linked Issue should close after merge.

---

## Part 10 — Sync local main
```bash
git switch main
git pull
git log --oneline
```

---

## Part 11 — Project tracking
In the existing Project:
```text
Complete Day 8 End-to-End GitHub Lab
Priority = High
Status = Done
```

---

## Part 12 — Security/Settings inspection
Inspect:
```text
Repository → Settings
```
Look for:
- access
- branch rules
- Actions permissions
- security

---

## Your Result
You reported:

> **Day 8 hands-on complete.**

### Day 8 Review
Practical objectives completed successfully.

Full practiced flow:
```text
Issue
→ branch
→ change
→ commit
→ push
→ PR
→ Actions check
→ review
→ merge
→ Issue closure
→ pull latest main
```

This was the most integrated practical day of the course.
