# GH-900 Preparation — Day 13
## Under-Covered Topics + Hands-On

**Goal:** Close smaller syllabus gaps that appeared in mocks but had not received deep training.

Topics covered:
- GitHub Desktop
- GitHub Mobile
- Saved Replies
- Project Insights
- Product-selection distinctions

---

# Part 1 — Detailed Theory

## GitHub Desktop
GUI client for Git/GitHub workflows on desktop.

Typical flow:
```text
Clone/open repo
→ create branch
→ edit files
→ inspect changes/diff
→ commit
→ push
→ create PR
```

GitHub Desktop does **not replace Git**. It provides a GUI over Git/GitHub operations.

### Desktop vs CLI
- CLI = scripting, advanced commands, precise terminal control.
- Desktop = visual diffs, easy branch switching, GUI commits/sync.

### Desktop Clone vs Fork
Same underlying concepts:
```text
Clone = local copy
Fork = GitHub-side related copy
```

### Desktop sync terms
```text
Fetch origin
Pull origin
Push origin
```
retain the same Git meanings.

---

## GitHub Mobile
Official GitHub mobile app for Android/iOS.

Best for:
- notifications
- Issues
- PRs
- reviews
- mentions
- repo activity
- on-the-go collaboration

Not a full IDE or CI runner.

Shortcut:
```text
GitHub Desktop = local Git GUI
GitHub Mobile = on-the-go collaboration
```

---

## Saved Replies
Reusable response text in Issues/PRs/Discussions.

Example:
```text
Thanks for reporting this.
Please provide:
- steps to reproduce
- expected behavior
- actual behavior
- environment/version
- logs/screenshots
```

### Saved Reply vs Issue Template
```text
Issue template = structures input when Issue is created
Saved reply = reusable output/response from maintainer
```

### Saved Reply vs PR Template
```text
PR template = structure PR description
Saved reply = reusable response after conversation starts
```

---

## Project Insights
Charts/analytics over Project data.

### Current charts
Snapshot of Project now:
- work by status
- work by assignee
- work by priority
- work by iteration

### Historical charts
Change over time:
- completed work
- remaining work
- trends
- bottlenecks

### Burn-up
Shows completed vs total/remaining work over time.

### Project Insights vs Project View
```text
Project View = manage individual items
Project Insights = analyze aggregate data
```

### Project Insights vs Repository Insights
```text
Project Insights = work-management analytics
Repository Insights = repository analytics
```

Repository Insights examples:
- traffic
- contributors
- code activity
- dependencies

---

## Product Selection Map
```text
GitHub Desktop = GUI Git on computer
GitHub Mobile = collaboration from phone
github.dev = quick browser editor
Codespaces = full cloud dev environment
GitHub Actions = automation/CI/CD
GitHub Projects = plan/track work
Project Insights = charts/analytics
Saved Replies = reusable response text
```

---

# Part 2 — Hands-On

## Hands-on 1: GitHub Desktop
Use existing `gh900-labs`.

Add local repo to GitHub Desktop:
```text
File → Add Local Repository
```

Observe:
```text
Current Repository
Current Branch
Changes
History
Fetch origin
```

Map:
```text
Current Branch ≈ git branch / git switch
Changes ≈ git status + git diff
History ≈ git log
Fetch origin ≈ git fetch
```

Create:
```text
feature/day13-desktop
```

Create `day13-desktop.md`, review visual diff, commit, publish/push branch, and create PR.

---

## Hands-on 2: Saved Replies
Create a saved reply:
```text
Request bug details
```

Body:
```text
Thanks for reporting this.

Could you please provide:
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment/version
- Relevant logs or screenshots
```

Insert/preview it in an Issue.

---

## Hands-on 3: Project Insights
Use existing:
```text
GH-900 Study Project
```

Ensure work items have statuses:
```text
Done
In Progress
Todo
```

Inspect/create charts by:
- Status
- Priority
- historical progress if available

Main concept:
```text
Project items
→ aggregate
→ charts/analytics
```

---

## Hands-on 4: GitHub Mobile
Optional.

If app is available:
- inspect notifications
- PR review requests
- mentions
- assignments
- repo activity

No installation required just for the exam.

---

## Day 13 Assessment — 15 Questions

### Your answers
1. B
2. B
3. A
4. B
5. B
6. B
7. B
8. B
9. B
10. A
11. A
12. C
13. B
14. B
15. B

### Review
**15/15 = 100%**

Confirmed:
- Desktop vs Mobile
- Saved Replies vs templates
- Project Insights vs Project Views
- Project Insights vs Repository Insights
- github.dev vs Codespaces

---

## Day 13 Outcome
The smaller under-covered current-syllabus topics were considered closed.
