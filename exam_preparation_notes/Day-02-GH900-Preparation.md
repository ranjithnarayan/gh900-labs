# GH-900 Preparation — Day 2
## GitHub Repositories

**Goal:** Understand repository structure, templates, branches, tags/releases, visibility, repository settings, and insights.

---

## Part 1 — Repository Concepts

### Repository anatomy
Typical repo:
```text
my-project/
├── src/
├── tests/
├── docs/
├── .github/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODEOWNERS
└── SECURITY.md
```

### CODEOWNERS
Defines individuals/teams responsible for specific paths.

Example:
```text
/tests/ui/  @qa-ui-team
/tests/api/ @qa-api-team
/security/  @security-team
```

**Exam shortcut:** who should review certain paths → `CODEOWNERS`.

### Creating repositories
A GitHub repo can be initialized with:
- name
- description
- visibility
- README
- `.gitignore`
- license

Local-first flow:
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <URL>
git push
```

### Repository templates
Use when you want many new repos to start from the same files/folder structure.

```text
Template repo
→ New repo A
→ New repo B
→ New repo C
```

### Template vs Fork
- **Fork** = related copy of an existing repo, often for contribution.
- **Template** = new independent repo from predefined structure.

### Default branch
One branch acts as default, commonly `main`, but it can be changed.

### Branch protection / rules
Can require:
- PRs
- reviews
- status checks
- restricted updates
- other merge/change conditions

### Tags
A tag normally points to a specific commit/version.

```text
A → B → C → D
        ↑
      v1.0
```

### Branch vs Tag
```text
Branch = moving pointer
Tag = named reference to a specific point
```

### GitHub Releases
Build on tags and can include:
- release title
- release notes
- assets/binaries/downloads

**Shortcut**
- exact code version → Tag
- publish version with notes/assets → Release

### Repository visibility
- Public
- Private
- Internal

### Stars
Bookmark/show interest in a repository.

### Watch vs Star
- Star = interest/bookmark.
- Watch = repository activity notifications.

### Repository Insights
Used for repository activity/health:
- contributors
- traffic
- code frequency
- network
- dependencies
- activity

### Dependency insights
Visibility into dependencies used across repos.

### Feature Preview
Try selected upcoming GitHub features where available.

---

## Day 2 Hands-on
In `gh900-labs`:

```bash
git switch -c feature/day2-notes
```

Create `day2.md`, commit it, then tag the commit:

```bash
git add day2.md
git commit -m "Add Day 2 repository notes"
git tag v0.1
git tag
```

Make another commit and observe that the branch moves while `v0.1` remains on the earlier commit.

---

## Quiz — Part 1

### Questions
1. File defining individuals/teams responsible for specific repo areas?  
A. SECURITY.md  
B. CODEOWNERS  
C. README.md  
D. LICENSE

2. 20 similar automation repos need same starter structure.  
A. Fork  
B. Repository template  
C. Release  
D. Tag

3. Best description of a Git tag?  
A. GitHub account  
B. Movable development line  
C. Named reference to a specific point/version  
D. Permission

4. Best branch vs tag distinction?  
A. Branch advances; tag normally identifies a particular commit  
B. Tags contain files, branches do not  
C. Tags only exist on GitHub  
D. Branches cannot contain commits

5. Publish v2.0 with notes/downloadable assets?  
A. Issue  
B. GitHub Release  
C. Discussion  
D. CODEOWNERS

6. Main purpose of branch rules?  
A. Compress history  
B. Control how important branches can change  
C. Fork repos  
D. Make repo public

7. Enterprise-visible but not public?  
A. Public  
B. Internal  
C. Fork  
D. Starred

8. Star primarily means?  
A. Permission  
B. Interest/bookmarking  
C. Auto review  
D. Ownership

9. Repo activity/contributors/traffic?  
A. Insights  
B. Issues  
C. Releases  
D. Discussions

10. Template vs fork?  
A. Same  
B. Fork helps contribute to existing repo; template creates new repo from predefined content  
C. Templates private-only  
D. Fork removes relation to original

11. External packages/libraries used by repos?  
A. Dependency insights  
B. Milestones  
C. Markdown  
D. PR review

12. Vulnerability reporting guidance?  
A. README.md  
B. CONTRIBUTING.md  
C. SECURITY.md  
D. `.gitignore`

### Your answers
1. B
2. B
3. C
4. A
5. B
6. B
7. B
8. B
9. A
10. B
11. A
12. C

### Review
**12/12 = 100%**

---

# Part 2 — Repository Settings & Scenarios

### Default branch
Primary branch used by many default operations. It is not the only branch.

### Archive
Preserve repo and history in inactive/read-only state.

### Delete
Remove repository. Destructive.

### Transfer
Change repository owner.

### Ownership vs collaboration
You can grant access without transferring ownership.

### Repository roles
High-level ladder:
```text
Read
Triage
Write
Maintain
Admin
```

Principle: least privilege.

### Scope
```text
Repository < Organization < Enterprise
```

### CODEOWNERS vs Branch Rules
```text
CODEOWNERS = WHO should review
Branch rules = WHAT conditions must be satisfied
```

---

## Quiz — Part 2

### Questions
1. Legacy repo no longer maintained but history must remain.  
A. Delete  
B. Archive  
C. Fork  
D. Transfer

2. Personal repo should now be company-owned.  
A. Clone  
B. Star  
C. Transfer  
D. Archive

3. Prevent direct push to `main`; require checks.  
A. CODEOWNERS  
B. Branch protection/rules  
C. Milestone  
D. Star

4. `/tests/` changes should request QA team automatically.  
A. CODEOWNERS  
B. Template  
C. Release  
D. Watch

5. Best least-privilege example?  
A. Give everyone admin  
B. Give only required permissions  
C. Make all public  
D. Transfer ownership to every collaborator

6. Correct hierarchy?  
A. Enterprise → Organization → Repository  
B. Repository → Enterprise → Organization  
C. Organization → Repository → Enterprise  
D. Repository → Organization → Enterprise

7. Want repo activity notifications.  
A. Star  
B. Watch  
C. Fork  
D. Tag

8. Save repo to revisit later.  
A. Watch  
B. Archive  
C. Star  
D. Release

9. Standard starter repo structure.  
A. Transfer  
B. Repository template  
C. Branch protection  
D. CODEOWNERS

10. User needs code contribution access but not ownership.  
A. Transfer ownership  
B. Grant appropriate repository access  
C. Delete/recreate  
D. Archive

11. Correct archive statement?  
A. Removes history  
B. Same as delete  
C. Preserves inactive/read-only state  
D. Same as fork

12. CODEOWNERS vs branch protection?  
A. WHO reviews vs WHAT rules must pass  
B. Same  
C. CODEOWNERS controls visibility  
D. Branch rules create forks

### Your answers
1. B
2. C
3. B
4. A
5. B
6. A
7. B
8. C
9. B
10. B
11. C
12. A

### Review
**12/12 = 100%**

---

## Day 2 Final Score
- Part 1: 12/12
- Part 2: 12/12
- **Total: 24/24 = 100%**

### Day 2 Revision Sheet
```text
Archive = preserve inactive repo
Delete = remove
Transfer = change owner
Template = new repo from standard structure
Fork = related copy for contribution

CODEOWNERS = who should review
Branch rules = what must be satisfied

Star = bookmark/interest
Watch = notifications

Public = everyone
Private = restricted
Internal = enterprise members
```

```text
Branch = moves with development
Tag = marks a specific commit/version
Release = published version with notes/assets
```
