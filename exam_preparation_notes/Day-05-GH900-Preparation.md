# GH-900 Preparation — Day 5
## GitHub Actions, Copilot, Codespaces & Modern Development

**Goal:** Understand modern GitHub development tools and know which one fits a scenario.

---

## GitHub Actions
Automation platform for:
- build
- tests
- linting
- packaging
- deployment
- scheduled jobs
- security checks

### Workflow file
Stored under:
```text
.github/workflows/
```

### Core hierarchy
```text
Workflow
  ↓
Jobs
  ↓
Steps
```

### Event / trigger
Causes workflow to start:
- `push`
- `pull_request`
- `schedule`
- manual trigger
- issue activity

### Runner
Machine/environment where a job executes.

Types:
- GitHub-hosted
- self-hosted

Use self-hosted when jobs must run inside private/internal infrastructure.

### Action vs Workflow
- Workflow = whole automation.
- Action = reusable automation component used by a step.

### Example
```text
PR created
→ install Node
→ install dependencies
→ run lint
→ run API tests
→ run UI smoke
→ result
```

---

## GitHub Copilot
AI-assisted development:
- suggestions
- explaining code
- generating tests
- refactoring
- docs
- debugging

### Agent Mode
Broader multi-step task handling:
```text
Inspect repo
→ identify relevant files
→ modify multiple files
→ run/check code
→ iterate
```

### Multi-model support
Copilot can support different AI models for supported experiences.

### Copilot plans
High-level:
- Individual
- Business
- Enterprise

Main exam concept: organization/enterprise governance differences, not pricing trivia.

---

## GitHub Codespaces
Cloud-hosted development environment.

Useful for:
- terminal
- dependencies
- runtime
- debugging
- build/test
- consistent environment

### Dev container
Defines reproducible environment configuration, usually under:
```text
.devcontainer/
  devcontainer.json
```

### github.dev
Lightweight browser editor.

Shortcut:
```text
Need quick edit → github.dev
Need full runtime/terminal/testing → Codespaces
```

---

## Day 5 Hands-on
Create:
```text
.github/workflows/hello.yml
```

Example:
```yaml
name: GH900 Hello

on:
  push:

jobs:
  hello:
    runs-on: ubuntu-latest

    steps:
      - name: Say hello
        run: echo "Hello from GitHub Actions"
```

Map:
```text
push = event
GH900 Hello = workflow
hello = job
ubuntu-latest = runner
Say hello = step
```

---

## Quiz — Part 1

### Your answers
1. B
2. B
3. B
4. A
5. B
6. B
7. A
8. B
9. B
10. A
11. B
12. B

### Questions & correct concepts
1. Actions primarily = automate workflows → B  
2. Workflow starts from event/trigger → B  
3. Workflow → Job → Step → B  
4. Runner = execution environment → A  
5. Private corporate network → self-hosted runner → B  
6. Copilot = AI dev tool → B  
7. Agent Mode = broader multi-step coding tasks → A  
8. Multi-model = supported different AI models → B  
9. Codespaces = cloud dev environment → B  
10. Dev container = reproducible dev env → A  
11. Build/test/debug in cloud → Codespaces → B  
12. Quick browser edit → github.dev → B

### Review
**12/12 = 100%**

---

## Quiz — Part 2

### Your answers
1. B
2. B
3. A
4. B
5. B
6. A
7. B
8. B
9. B
10. B
11. A
12. A

### Scenario summary
1. Auto tests on every PR → Actions  
2. Run on push to main → event/trigger  
3. Build/API/UI test units → jobs  
4. Checkout/install/run test → steps  
5. Internal network execution → self-hosted runner  
6. AI explain method/generate tests → Copilot  
7. Multi-file changes/run checks/iterate → Agent Mode  
8. README typo in browser → github.dev  
9. Ready-to-use cloud dev env → Codespaces + dev container  
10. Codespaces fuller than github.dev  
11. Reproducible tooling/config → dev container  
12. Workflow contains jobs; jobs contain steps; jobs run on runners

### Review
**12/12 = 100%**

---

## Day 5 Final Score
**24/24 = 100%**

### Final Revision
```text
Actions = automation
Event = trigger
Workflow → Job → Step
Runner = execution environment
Self-hosted runner = internal/private environment
Copilot = AI coding assistance
Agent Mode = broader multi-step task
Codespaces = full cloud dev environment
Dev container = reproducible environment
github.dev = lightweight browser editing
```
