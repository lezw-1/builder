---
description: Execute the test task from a feature's task list
---

# Execute Tests

## Purpose

Run and verify the test task from a feature's `/features/<feature-folder>/tasks/` folder.

## Constraints

- DO NOT write tests for behavior outside the feature's scope
- DO NOT mock components that can be tested with real instances
- DO NOT skip failing tests — fix them or report the failure
- DO NOT commit — let the user review and commit changes

## Rules

- `.claude/rules/testing.md` — testing pyramid, behavior-based tests, one behavior per test
- Read and follow the rules referenced in the task file's **Rules** section

## Steps

1. Run `/clear` to clear context
2. Ask the user which feature to test (or accept a feature name as input)
3. Read `feature.md` from the matching folder in `/features/` for acceptance criteria
4. Find and read the test task file from `/features/<feature-folder>/tasks/`
5. Follow the task's **Steps** section to write and run the tests
6. Run the full test suite and verify all tests pass
7. Verify each **Acceptance Criteria** item in the task file passes
8. Update the task file's **Status** to `Done`
9. Present a summary of test results and coverage
