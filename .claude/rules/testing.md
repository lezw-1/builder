# Testing

## Critical
- **Follow the testing pyramid** — many unit tests, fewer integration tests, minimal end-to-end tests.
- **Test behavior, not implementation** — tests should survive internal refactors.
- When fixing a bug, **write a test first** to prove the bug exists and that the fix resolves it.
- **Verify one behavior per test** — keep tests fast, isolated, and deterministic.

## Preferred
- When testing component interactions, **use real components** (e.g., service + database) with isolated environments.
- **Clean up test data** after each test run.
- **Treat test coverage as a floor**, not a ceiling — tests that never fail are not valuable.
