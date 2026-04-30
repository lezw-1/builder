---
name: task
description: Implementation step for a feature
---

## Task: [Short title]

**Id:** [Number, e.g. 01]
**Feature:** [Name of related feature]
**What:** [One sentence describing what to implement]
**Priority:** 1-10 (1 is high, 10 is low)
**Status:** Todo | In Progress | Done
**Rules:**

- `.claude/rules/principles.md`
- `.claude/rules/architecture.md`
- `.claude/rules/testing.md`
- `.claude/rules/style.md`
- `.claude/rules/api.md`
- `.claude/rules/database.md`
- `.claude/rules/security.md`
- `.claude/rules/git.md`
- `.claude/rules/devops.md`

---

### Details

- [Exact change to make in code]
- [Files/components affected]
- [Edge cases or constraints]

### Steps

1. [Concrete step]
2. [Next step]
3. [Final step]
4. Append a summary of changes made to `changelog.md` in the feature folder
5. Commit changes with a short message (max 10 words)

---

### Acceptance Criteria

- [ ] Specific, testable outcome
- [ ] Another verifiable condition
- [ ] Typecheck and lint pass

**Important:**

- Each criterion must be concrete and testable
- Include file paths and line numbers where relevant
- Reference acceptance criteria from feature.md
- Keep configuration minimal: strip verbose comments, move env-specific values to environment files, omit settings that match upstream defaults
- Keep tasks **very small and focused** — each task should do one thing (e.g. "create component with minimal config", not "build entire module")
- Each task must include a **verification step** at the end: a concrete, runnable check that proves the task works (e.g. start the service, hit an endpoint, run a command and observe output)

---

### Example

```
## Task: Add health check endpoint

**Id:** 03
**Feature:** User API
**What:** Add a `GET /health` endpoint that returns 200 OK.
**Priority:** 2
**Status:** Todo
**Rules:**

- `.claude/rules/api.md`
- `.claude/rules/style.md`

---

### Details

- Add a `/health` route to `api/routes.py`
- No auth required; returns `{ "status": "ok" }`

### Steps

1. Add `GET /health` handler in `api/routes.py`
2. Register the route in `api/app.py`
3. Run `curl localhost:8000/health` and confirm `200 { "status": "ok" }`
4. Append changes to `changelog.md` in the feature folder
5. Commit: `add health check endpoint`

---

### Acceptance Criteria

- [ ] `GET /health` returns `200 { "status": "ok" }`
- [ ] No authentication required
- [ ] `curl localhost:8000/health` succeeds locally
```
