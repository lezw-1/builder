---
description: Execute implementation tasks from a feature's task list
---

# Execute Implementation

## Purpose

Iterate over and implement all tasks from a feature's `/features/<feature-folder>/tasks/` folder in order.

## Constraints

- DO NOT modify files outside the scope of the current task
- DO NOT skip steps defined in a task file
- DO NOT refactor or improve code unrelated to the current task
- DO NOT commit — let the user review and commit changes

## Rules

- Read and follow the rules referenced in each task file's **Rules** section

## Steps

1. Ask the user which feature to implement (or accept as input)
2. Read `feature.md` and `analysis.md` from the matching folder in `/features/` for context
3. List all task files in `/features/<feature-folder>/tasks/` sorted by filename (e.g. `01-`, `02-`)
4. For each task file in order:
   a. Read the task file
   b. Skip if **Status** is already `Done`
   c. Follow the task's **Steps** section in order
   d. Verify each **Acceptance Criteria** item passes
   e. Update the task file's **Status** to `Done`
   f. Present a summary of changes made and ask the user to review before continuing
5. After all tasks are done, present a final summary of all changes and files affected
