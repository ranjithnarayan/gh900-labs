# GH-900 Preparation — Day 6
## Privacy, Security & Administration

**Goal:** Master identity, permissions, branch governance, EMU, Copilot policy concepts, and GitHub security tooling.

---

## Authentication vs Authorization
```text
Authentication = Who are you?
Authorization = What are you allowed to do?
```

Examples:
- password / passkey / 2FA → authentication
- Read / Write / Admin → authorization

### 2FA
Adds another factor beyond password.

### Passkeys
Cryptographic, phishing-resistant authentication credentials.

### PAT / SSH
Used for Git/CLI/API access in relevant scenarios.

---

## Repository roles
```text
Read
Triage
Write
Maintain
Admin
```

- Triage = manage Issues/PRs without normal code-write access.
- Write = normal code contribution.
- Admin = broadest repo control.

### Least privilege
Give users only the access required for their work.

---

## Organizations & Teams
Teams simplify permission management for groups.

Benefits:
- onboarding
- offboarding
- consistent access
- simpler management

### Visibility
- Public
- Private
- Internal

### Branch protection / rules
Can require:
- PR
- approvals
- status checks
- prevent direct changes

### CODEOWNERS vs Branch Rules
```text
CODEOWNERS = WHO should review
Branch rules = WHAT conditions must pass
```

---

## Enterprise Managed Users (EMU)
Enterprise-controlled identities for centralized lifecycle/governance.

### Organization-wide Copilot policies
Centralized control of Copilot availability/capabilities across org users.

---

## Secrets / Security Tools

### Secrets
Sensitive values should not be committed into source code.

### Secret scanning
Detect leaked API keys/tokens/credentials already present in repo content/history.

### Push protection
Help block/warn before detected secrets are pushed.

### Code scanning
Find vulnerabilities/coding errors in source.

### Dependabot
Dependency vulnerability/update assistance.

Shortcut:
```text
Code scanning = vulnerable code
Secret scanning = leaked credentials
Push protection = stop secret during push
Dependabot = vulnerable/outdated dependencies
```

---

## Day 6 Hands-on
Inspect:
```text
Repository → Settings
```
Look at:
- collaborators/access
- branches/rules
- Actions
- security settings

Also inspect account authentication settings:
- 2FA
- passkeys
- security keys

No need to change settings.

---

## Quiz — Part 1

### Your answers
1. A
2. B
3. B
4. B
5. D
6. B
7. C
8. A
9. B
10. B
11. A
12. B

### Concepts
1. Authn vs authz → identity vs permitted actions  
2. 2FA → extra factor  
3. Passkey → phishing-resistant cryptographic credential  
4. Least privilege  
5. Admin = broadest repo role  
6. Teams = group permission management  
7. Internal = enterprise members, not public  
8. Branch rules = protect important branches  
9. EMU = centralized identity management  
10. Secret scanning = detect leaked credentials  
11. Push protection = block/warn during push  
12. Secret scanning + Dependabot pairing

### Review
**12/12 = 100%**

---

## Quiz — Part 2

### Your answers
1. B
2. A
3. B
4. C
5. B
6. A
7. B
8. B
9. B
10. B
11. B
12. A

### Scenario summary
1. Can login but cannot push → Authorization  
2. Password alone should not be enough → 2FA  
3. Manage Issues/PRs, no code-write → Triage  
4. Normal contribution access → Write  
5. Central enterprise identity lifecycle → EMU  
6. Centrally control Copilot → org-wide Copilot policies  
7. Two approvals + CI before main → branch rules  
8. `/security/` reviewers → CODEOWNERS  
9. Detect committed API token → secret scanning  
10. Stop secret during push → push protection  
11. Vulnerable library dependency → Dependabot  
12. CODEOWNERS=who; branch rules=conditions

### Review
**12/12 = 100%**

---

## Day 6 Final Score
**24/24 = 100%**
