---
name: feature
description: Feature description
---

## Feature: [Name]

**What:** [One sentence description]
**Status:** Draft | In Progress | Done

---

### Details

**Frontend:**

- [component or UI detail]
- [state management approach]
- [validation rules]

**Backend:**

- [business logic]
- [data model changes]

**Database:**

- [new tables or fields]
- [migrations needed]

**DevOps:**

- [deployment changes (Helm, Docker, CI/CD)]
- [observability: metrics, logs, health checks]
- [environment-specific config or secrets]

**Security:**

- [auth/encryption considerations]

**Third-party / Integrations:**

- [external services used]

---

### Acceptance Criteria

Each criterion must be verifiable, not vague. "Works correctly" is bad. "Button shows confirmation dialog before deleting" is good.

- [ ] Specific verifiable criterion
- [ ] Another criterion
- [ ] Typecheck/lint passes

**Important:**

- Acceptance criteria must be concrete and testable
- Include quality checks (typecheck, lint) as criteria
- Keep the feature **simple and focused** — avoid over-engineering or adding scope beyond what is described

---

### Example

```
## Feature: Delete Account

**What:** Allow users to permanently delete their account from the settings page.
**Status:** Draft

---

### Details

**Frontend:**

- Add "Delete Account" button in Settings > Danger Zone
- Show confirmation dialog requiring user to type "DELETE" before proceeding
- Redirect to login page after successful deletion

**Backend:**

- Add endpoint to delete user account
- Revoke all active sessions and API tokens

**Database:**

- Add `deleted_at` timestamp column to `users` table
- Migration: `add_deleted_at_to_users`

**DevOps:**

- No new infrastructure required
- Expose `/healthz` liveness check if not already present
- Ensure `DELETION_ENABLED` env var is set per environment

**Security:**

- Require re-authentication (password confirmation) before deletion
- Apply least privilege: only the account owner can delete their own account

**Third-party / Integrations:**

- Cancel active Stripe subscriptions on deletion

---

### Acceptance Criteria

- [ ] "Delete Account" button appears in Settings
- [ ] Confirmation dialog requires typing "DELETE" — button disabled until matched
- [ ] Account is soft-deleted; user cannot log in afterward
- [ ] All sessions are invalidated immediately
- [ ] Stripe subscription is cancelled within 5 seconds of deletion
- [ ] Typecheck/lint passes
```
