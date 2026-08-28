---
name: refactor
description: Refactor a file's comments to conform to .claude/rules/comments/*
---

## Refactor: [Target path]

**What:** [One sentence — which file(s) and which rule set applies]
**Rules:**

- `.claude/rules/comments/bash.md`
- `.claude/rules/comments/helm.md`
- `.claude/rules/comments/values.md`

---

### Details

- Resolve the target — the path(s) given as the skill argument, or the current diff if none given
- Pick the matching rule set by file type:
  - `*.sh` → `bash.md`
  - `values.yaml` / Helm chart values files → `values.md`
  - other Kubernetes/Helm manifests (`*.yaml`) → `helm.md`
- Add only what that rule set requires: header/section banners, one-line descriptions, per-field comments (including nested and list items), blank lines between fields, call-outs for non-default or manual-action behavior
- Leave every key, value, and line of logic untouched — this is a comment-only pass, not a functional refactor
- Skip files already fully compliant with their rule set

---

### Checklist

- [ ] Correct rule set applied per file type — never mixed (e.g. `values.yaml` uses `values.md`, not `helm.md`)
- [ ] All banners/comments the rule requires are present
- [ ] Diff touches comments only — no key, value, or logic changed

**Important:**

- If a file's type doesn't map to any rule in `.claude/rules/comments/`, stop and ask which rule to apply rather than guessing
- Do not commit — leave changes for the user to review (`.claude/rules/git.md`)

---

### Example

```
## Refactor: bootstrap/bootstrap.sh

**What:** Add bash.md-required comments to the bootstrap script.
**Rules:**

- `.claude/rules/comments/bash.md`

---

### Details

- Target: bootstrap/bootstrap.sh
- File type `*.sh` → apply bash.md
- Add header banner (Script/Description/Usage/Prerequisites) after the shebang
- Add section banners for major steps, a one-liner above each constant, and doc blocks above functions

---

### Checklist

- [x] bash.md applied
- [x] Header banner, section banners, constant comments, function doc blocks added
- [x] No keys/logic changed — comments only
```
