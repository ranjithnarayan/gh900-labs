# GH-900 Preparation — Day 1
## Git & GitHub Fundamentals + GitHub Basics

**Goal:** Build the core mental model for Git and GitHub, then validate it with exam-style questions.

---

## Part 1 — Git & GitHub Fundamentals

### Version control
Version control helps track:
- what changed
- who changed it
- when it changed
- previous versions
- parallel development
- collaboration without overwriting work

Git is a **distributed version control system (DVCS)**. Each developer can have a complete local repository and history.

### Git vs GitHub
**Git**
- Distributed version control system.
- Works locally.
- Does not require GitHub.
- Common commands: `git init`, `git add`, `git commit`, `git branch`, `git merge`.

**GitHub**
- Platform built around Git.
- Adds remote repositories, Pull Requests, Issues, Discussions, Actions, Projects, Codespaces, Copilot, security, organizations, etc.

**Exam shortcut**
- Local version tracking → Git.
- Collaboration/hosting/platform features → GitHub.

### Repository
A repository contains project files plus Git history.

Local repository:
```text
C:\projects\sdet-engineering-labs
```

Remote repository:
```text
github.com/<user>/<repo>
```

The hidden `.git/` folder stores Git metadata and history.

### Three Git areas
```text
Working Directory
      ↓ git add
Staging Area
      ↓ git commit
Local Repository
```

- **Working directory**: files being edited.
- **Staging area**: selected changes for the next commit.
- **Repository**: committed history.

### Commit
A commit represents a snapshot of tracked changes at a point in time.

A commit includes:
- ID/hash
- author
- date/time
- message
- changes
- parent commit

### Core Git commands
```bash
git init
git status
git add <file>
git add .
git commit -m "message"
git log
```

### Clone / Fetch / Pull / Push
```text
clone = get an existing repository locally for the first time
fetch = download remote information without automatically integrating
pull  = fetch + integrate
push  = send local commits to remote
```

### Branches
Branches allow isolated development.

```text
main
  |
  A---B
       \
        C---D
        feature-login
```

A branch is essentially a movable reference to a commit.

### HEAD
`HEAD` usually represents the currently checked-out position/branch.

### Merge
Merge integrates one branch into another.

### Merge conflicts
A merge conflict occurs when Git cannot safely determine how to combine conflicting changes.

### `.gitignore`
Used to ignore matching **untracked** files such as:
```text
venv/
__pycache__/
.env
```

Important: adding a tracked file to `.gitignore` does not automatically untrack it.

### GitHub Flow preview
```text
Create branch
→ Make changes
→ Commit
→ Push
→ Open Pull Request
→ Review
→ Merge
→ Delete branch
```

---

## Day 1 Hands-on
Create a practice repo:
```text
gh900-labs/
```

Commands:
```bash
git init
git status
git add README.md
git commit -m "Initial commit"
git log
git switch -c feature-notes
git add notes.txt
git commit -m "Add Git notes"
git switch main
git merge feature-notes
```

---

## Quiz — Part 1

### Questions
1. Which statement best describes Git?  
A. Cloud hosting service  
B. Distributed version control system  
C. Project-management platform  
D. CI/CD service

2. Before a modified file can be included in a commit, what normally happens?  
A. Push  
B. Pull  
C. Stage the change  
D. Create a Pull Request

3. Which command shows modified, staged, and untracked files?  
A. `git log`  
B. `git status`  
C. `git commit`  
D. `git diff --remote`

4. You want a local copy of an existing GitHub repo for the first time.  
A. Fetch  
B. Pull  
C. Clone  
D. Merge

5. Download remote changes without automatically integrating them.  
A. `git pull`  
B. `git fetch`  
C. `git push`  
D. `git clone`

6. What does `git push` primarily do?  
A. Copies remote repo locally  
B. Sends local commits to remote  
C. Adds files to staging  
D. Merges two local branches

7. Main purpose of a Git branch?  
A. Back up repo  
B. Isolated lines of development  
C. Replace commits  
D. Store Issues

8. What does `HEAD` typically identify?  
A. Oldest commit  
B. Remote repo  
C. Currently checked-out position/branch  
D. Staging area

9. A file was committed six months ago; today it is added to `.gitignore`. What happens?  
A. Git deletes it  
B. Git automatically stops tracking it  
C. Existing tracked file remains tracked  
D. Commit history is rewritten

10. Correct order?  
A. Commit → Stage → Modify  
B. Modify → Stage → Commit  
C. Stage → Push → Modify  
D. Push → Modify → Commit

11. Feature branch is ready for teammate review before `main`. Which GitHub feature?  
A. Issue  
B. Wiki  
C. Pull Request  
D. Release

12. Which statement is most accurate?  
A. Git and GitHub are the same product  
B. Git requires GitHub  
C. Git can work independently of GitHub  
D. GitHub only hosts repos created with GitHub Desktop

### Your answers
1. B  
2. C  
3. B  
4. C  
5. B  
6. D  
7. B  
8. C  
9. C  
10. B  
11. C  
12. C

### Review
**Score: 11/12 = 91.7%**

Only Q6 was incorrect.

Correct:
```text
git push = local → remote
git fetch = remote info → local, no automatic integration
git pull = remote → local + integrate
git merge = combine branch histories
```

---

# Part 2 — GitHub Basics

### Account structure
```text
Enterprise
  ↓
Organizations
  ↓
Repositories
  ↓
Users / Teams
```

- Personal account = individual.
- Organization = shared collaboration/access management.
- Enterprise = centralized governance across organizations.

### Repository visibility
- **Public** = broadly visible.
- **Private** = authorized users only.
- **Internal** = enterprise members, not the public.

### Collaborators and teams
Teams simplify group-based access management.

### Pull Requests
A PR proposes changes from one branch to another and supports:
- code review
- comments
- approvals
- change requests
- automated checks
- merge

### Review states
- Comment
- Approve
- Request changes

### Issues
Used to track actionable work:
- bugs
- features
- tasks
- documentation

### Issue vs PR
- Issue = track work.
- PR = propose code/file changes.

### Closing issues from PRs
Example:
```text
Fixes #42
Closes #42
```

### Labels
Categorization:
```text
bug
enhancement
documentation
priority-high
```

### Milestones
Group Issues/PRs toward a shared target or release.

### Discussions
Broader conversations/Q&A/ideas, not necessarily actionable work.

### README / Markdown
`README.md` is usually the main repo documentation entry point.

Common Markdown:
```markdown
# Heading
## Subheading
**bold**
*italic*
- item
[link](https://github.com)
```

### Fork vs Clone
- **Clone** = GitHub → local machine.
- **Fork** = GitHub-side copy under your account.

Typical open-source flow:
```text
Original repo
→ Fork
→ Clone
→ Branch
→ Change
→ Push
→ Pull Request
```

### Standard community files
- `README.md` — project overview/usage
- `CONTRIBUTING.md` — contribution guidance
- `CODE_OF_CONDUCT.md` — expected behavior
- `SECURITY.md` — vulnerability reporting
- `LICENSE` — legal use/modification/distribution terms

---

## Quiz — Part 2

### Questions
1. No write access to public repo; best first step?  
A. Clone  
B. Fork  
C. Merge  
D. Release

2. Main purpose of a PR?  
A. Download history  
B. Track defects  
C. Propose/review changes before merge  
D. Create local repo

3. Best feature for a reproducible software defect?  
A. Discussion  
B. Issue  
C. Wiki  
D. Release

4. Group 50 issues toward version 4.0?  
A. Label  
B. Milestone  
C. Fork  
D. Branch

5. Main difference between fork and clone?  
A. No difference  
B. Fork = GitHub-side copy; clone = local copy  
C. Clone = GitHub-side copy; fork = local copy  
D. Fork only for private repos

6. File explaining how to contribute?  
A. README  
B. `.gitignore`  
C. `CONTRIBUTING.md`  
D. LICENSE

7. File specifying permitted use/modification/distribution?  
A. README  
B. LICENSE  
C. SECURITY.md  
D. CODEOWNERS

8. Best for broader Q&A/community conversation?  
A. Actions  
B. PRs  
C. Discussions  
D. Commits

9. Visibility for enterprise members but not public?  
A. Public  
B. Private  
C. Internal  
D. Forked

10. Correct GitHub Flow sequence?  
A. Merge → Branch → Commit → PR  
B. Branch → Changes/Commits → PR → Review → Merge  
C. Issue → Merge → Clone → Push  
D. PR → Branch → Commit → Merge

11. Categorize issues as bug/documentation/enhancement?  
A. Milestones  
B. Labels  
C. Branches  
D. Releases

12. Correct statement?  
A. Organization can own repositories  
B. Only individuals can own repos  
C. Organizations cannot manage teams  
D. Enterprise = branch

### Your answers
1. B  
2. C  
3. B  
4. B  
5. B  
6. C  
7. B  
8. C  
9. C  
10. B  
11. B  
12. A

### Review
**Score: 12/12 = 100%**

---

## Day 1 Final Score
- Part 1: 11/12
- Part 2: 12/12
- **Total: 23/24 = 95.8%**

### Day 1 Final Revision Sheet
```text
Git:
init = create repo
add = stage
commit = save staged snapshot
branch = isolated development
merge = combine histories
clone = remote → local
fetch = download remote changes, no automatic integration
pull = fetch + integrate
push = local commits → remote
```

```text
GitHub:
Fork = GitHub-side copy
PR = propose/review changes
Issue = track actionable work
Discussion = broader conversation
Label = categorize
Milestone = group toward target/release
README = overview/usage
CONTRIBUTING = contributor guidance
SECURITY.md = vulnerability-reporting guidance
LICENSE = legal terms
```
