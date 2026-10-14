# GH-900 Preparation — Day 3
## Collaborate Using GitHub

**Goal:** Master Pull Requests, reviews, merge strategies, Issues, Discussions, notifications, mentions, linking work, Gists, Wikis, and GitHub Pages.

---

## Pull Requests
PR lifecycle:
```text
Create branch
→ Make changes
→ Commit
→ Push
→ Open PR
→ Discuss / Review
→ Checks
→ Approve / Request changes
→ Merge
```

A PR is a collaboration space around proposed changes.

### Draft Pull Requests
Used when work is visible but not ready for final review/merge.

### Review outcomes
- Comment
- Approve
- Request changes

### Merge methods
**Merge commit**
- preserves individual commits
- preserves explicit merge point

**Squash and merge**
- combines PR commits into one commit on target branch

**Rebase and merge**
- preserves individual commits
- linear history
- no explicit merge commit

Shortcut:
```text
One clean commit → Squash
Linear history → Rebase
Explicit merge point → Merge commit
```

### Merge conflicts
Conflicting changes require resolution before integration.

### Linking PRs and Issues
Example:
```text
Fixes #50
Closes #50
```
Helps traceability and can auto-close the linked Issue when merged.

### Issues
Can include:
- title/description
- assignees
- labels
- milestones
- comments
- linked PRs

### Assignee vs Reviewer
- Assignee = person responsible for doing/managing work.
- Reviewer = person evaluating proposed changes.

### Filters
Help find relevant Issues/PRs, e.g. open bugs assigned to you.

### Issue templates
Standardize issue submissions (steps, expected, actual, environment, etc.).

### PR templates
Standardize PR descriptions (summary, testing, risk, linked issue, etc.).

### Discussions
Use for broader questions, ideas, announcements, architecture discussions.

### Notifications / Mentions / Subscriptions
- `@mention` draws attention and can generate a notification.
- Subscribe = follow a specific Issue/PR.
- Watch = broader repository notifications.

### Gists
Lightweight sharing of snippets/files.

### Wikis
Longer-form collaborative project documentation.

### GitHub Pages
Publish a static website/project documentation site.

Shortcut:
```text
Gist = snippet/files
Wiki = project knowledge
Pages = published website
```

---

## Hands-on Gap Identified
At first, only the local Git repo existed. The missing bridge was:

```text
Local Git repository
      ↕
GitHub remote repository
```

### Create GitHub remote repo
Create empty repo on GitHub without README/.gitignore/license.

Then:
```bash
git branch -M main
git remote add origin https://github.com/<username>/gh900-labs.git
git remote -v
git push -u origin main
```

Concepts:
```text
origin = conventional remote name
main = local branch
origin/main = local reference representing remote main
```

### Day 3 end-to-end hands-on
- Create GitHub Issue
- Create feature branch
- Make/commit changes
- Push branch
- Open PR
- Link PR to Issue
- Review/inspect changes
- Merge
- Observe linked Issue closure

---

## Quiz — Part 1

### Questions
1. Incomplete work visible for early feedback?  
A. Release  
B. Draft PR  
C. Milestone  
D. GitHub Page

2. Serious fixes required before merge?  
A. Approve  
B. Request changes  
C. Star  
D. Fork

3. 12 small commits → one target-branch commit?  
A. Merge commit  
B. Squash and merge  
C. Fork and merge  
D. Clone and merge

4. Replay commits for linear history?  
A. Squash  
B. Rebase and merge  
C. Fork  
D. Archive

5. Primary benefit of linking PR to Issue?  
A. Storage  
B. Traceability  
C. Visibility change  
D. New org

6. Person responsible for Issue work?  
A. Reviewer  
B. Assignee  
C. Follower  
D. CODEOWNER only

7. Standard bug submission fields?  
A. Repo template  
B. Issue template  
C. Release template  
D. Branch template

8. Community question about architecture direction?  
A. Issue  
B. Discussion  
C. Commit  
D. Tag

9. `@qa-team` in comment?  
A. Fork repo  
B. Draw team's attention  
C. Auto merge  
D. Change visibility

10. Small standalone code snippet?  
A. Gist  
B. Milestone  
C. Pages  
D. Branch protection

11. Extensive collaborative docs?  
A. Star  
B. Wiki  
C. Tag  
D. Fork

12. Static documentation website?  
A. Issues  
B. Gists  
C. GitHub Pages  
D. Labels

### Your answers
1. B
2. B
3. B
4. B
5. B
6. B
7. B
8. B
9. B
10. A
11. B
12. C

### Review
**12/12 = 100%**

---

## Quiz — Part 2

### Questions
1. Auto-close Issue #82 when PR merges?  
A. `Fixes #82`  
B. Add bug label  
C. Star issue  
D. Convert to discussion

2. Feedback on incomplete feature?  
A. Release  
B. Draft PR  
C. Tag  
D. Archive branch

3. Many poor bug reports missing details?  
A. Issue template  
B. Repo template  
C. Release per bug  
D. More stars

4. Every PR should include summary/testing/risk?  
A. PR template  
B. Issue template  
C. README  
D. Milestone

5. Follow only one Issue?  
A. Watch repo  
B. Subscribe to Issue  
C. Fork repo  
D. Star repo

6. Clean `main`, one commit per feature?  
A. Merge commit  
B. Squash and merge  
C. Rebase and merge  
D. Fork and merge

7. Preserve individual commits and explicit merge point?  
A. Squash  
B. Merge commit  
C. Rebase  
D. Tag and merge

8. `/security/` should auto-request Security team?  
A. CODEOWNERS  
B. Issue template  
C. Milestone  
D. Pages

9. Broad architecture discussion?  
A. Issue  
B. Discussion  
C. PR  
D. Release

10. See only open bugs assigned to you?  
A. Filtering/search  
B. Releases  
C. Branch protection  
D. Gists

11. Short reproducible code sample?  
A. Wiki  
B. Pages  
C. Gist  
D. Milestone

12. Correct assignee/reviewer pairing?  
A. Assignee=reviewer  
B. Assignee=responsible for work; Reviewer=evaluates changes  
C. Assignee=owner only  
D. Same meaning

### Your answers
1. A
2. B
3. A
4. A
5. B
6. B
7. C
8. A
9. B
10. A
11. C
12. B

### Review
**11/12 = 91.7%**

Only Q7 was incorrect.

Correct answer: **B. Merge commit**

Why:
```text
Merge commit
= preserve individual commits
+ explicit merge point

Rebase and merge
= preserve individual commits
+ linear history
- no explicit merge commit
```

---

## Day 3 Final Score
- Part 1: 12/12
- Part 2: 11/12
- **Total: 23/24 = 95.8%**

### Day 3 Revision Sheet
```text
Draft PR = visible, not final-review ready
Issue = actionable work
Discussion = conversation/ideas/Q&A
Issue template = standardize issue submissions
PR template = standardize PR descriptions
Assignee = responsible for work
Reviewer = evaluates changes
@mention = draw attention
Subscribe = follow specific conversation
Gist = snippet/files
Wiki = collaborative docs
Pages = static website
```

```text
Merge commit = preserve commits + explicit merge point
Squash = many commits → one
Rebase = preserve commits + linear history
```
