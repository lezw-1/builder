---
name: feature
description: Feature description
---

## Feature: [Name]

**What:** [One sentence description]
**Status:** Draft | In Progress | Done

---

### Details

Describe intent and behavior — not implementation details. No file names, function names, column names, or specific code changes.

**Frontend:**

- [user-facing behavior or UI element]
- [interaction or validation rule]

**Backend:**

- [business rule or operation]
- [data change or side effect]

**Database:**

- [data that needs to be stored or removed]
- [schema change required, without specifics]

**DevOps:**

- [infrastructure or deployment change needed]
- [observability requirement]
- [environment-specific config needed]

**Security:**

- [auth or access control requirement]

**Third-party / Integrations:**

- [external service interaction]

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
- Keep the feature description **generic** — describe intent and behavior, not implementation details (no file names, function names, or specific code changes)

---

### Example

```
## Feature: Delete Account

**What:** Allow users to permanently delete their account from the settings page.
**Status:** Draft

---

### Details

**Frontend:**

- "Delete Account" button in Settings > Danger Zone
- Confirmation dialog requiring the user to type "DELETE" before proceeding
- Redirect to login page after successful deletion

**Backend:**

- Delete account endpoint
- Revoke all active sessions and API tokens on deletion

**Database:**

- Soft-delete accounts; preserve data but prevent access
- Schema migration required

**DevOps:**

- No new infrastructure required
- Liveness check required if not already present
- Feature flag to enable/disable account deletion per environment

**Security:**

- Re-authentication (password confirmation) required before deletion
- Only the account owner may delete their own account

**Third-party / Integrations:**

- Cancel active billing subscriptions on deletion

---

### Acceptance Criteria

- [ ] "Delete Account" button appears in Settings
- [ ] Confirmation dialog requires typing "DELETE" — button disabled until matched
- [ ] Account is soft-deleted; user cannot log in afterward
- [ ] All sessions are invalidated immediately
- [ ] Stripe subscription is cancelled within 5 seconds of deletion
- [ ] Typecheck/lint passes
```
