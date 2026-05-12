---
description: Implementation Plan based on feature description and codebase analyze
---

# Implementation Plan

## Purpose

Create a detailed implementation plan for a specific feature using the task SKILL.

## Constraints

- DO NOT write the full plan in one shot — get buy-in at each major step
- DO NOT leave open questions in the final plan — resolve them before finalizing
- DO NOT assume — verify with code

## Rules

- `.claude/rules/architecture.md` — layered architecture, strict layer boundaries, draw.io for diagrams
- `.claude/rules/principles.md` - important principles

## Steps

1. Run `/clear` to clear context
2. Invoke the task SKILL to get the template
3. Ask the user which feature to plan (or accept a feature name as input)
4. Read `feature.md` and `analysis.md` from the matching folder in `/features/` for scope and context
5. Plan structure with the user
6. Create a task for creating a feature branch from `dev` named `feature/<feature-name>` (e.g. `feature/add-encryption`) and save it as the first task file (e.g. `01-create-branch.md`) in `/features/<feature-folder>/tasks/` using the SKILL template
7. Save each remaining task as a separate file in `/features/<feature-folder>/tasks/` using the SKILL template (e.g. `02-setup-workflow.md`, `03-add-encryption.md`)
8. Create a dedicated test task that use rule testing.md — save it as the last task file before documentation (e.g. `05-tests.md`)
9. Create a README task using the readme SKILL — it should update the project `README.md` to reflect the feature changes; save it as the final task file (e.g. `06-readme.md`)
10. Create a BACKLOG task — it should update or create `BACKLOG.md` at the project root with any follow-up items or deferred improvements; save it after the README task (e.g. `07-backlog.md`)
11. Create a `changelog.md` file in the feature folder listing all planned changes grouped by task
