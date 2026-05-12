## Contents

Claude Code configuration with rules and skills for spec-driven, autonomous development.

A spec-first workflow: write a well-thought-out spec, then use it to guide AI-assisted development.

<img src="assets/diagrams/architecture.png" alt="Architecture" width="600" height="500" />

## Workflow

```
create-feature → create-analysis → create-tasks → execute-implementation → execute-test
```

Each phase runs in a clean context. Outputs are saved to a `/features/<date>-<name>/` folder.

## Structure

```
.claude/
  commands/        — slash commands that drive each workflow phase
  rules/           — passive instructions Claude always follows
  skills/          — templates invoked by commands
  memory/          — persistent context across sessions (not tracked by git)
assets/
  diagrams/        — architecture diagrams (draw.io + png)
```

## Commands

| Command | Purpose |
|---|---|
| `/create-feature` | Interview the user and write a `feature.md` spec |
| `/create-analysis` | Analyze the codebase against a feature spec, write `analysis.md` |
| `/create-tasks` | Build a numbered task list from the feature + analysis |
| `/execute-implementation` | Implement each task file in order |
| `/execute-test` | Run and verify the test task |

## Rules

| Rule | Purpose |
|---|---|
| `architecture.md` | Layered architecture, strict layer boundaries, draw.io diagrams |
| `principles.md` | Core engineering principles |
| `api.md` | API design conventions |
| `database.md` | Database conventions |
| `devops.md` | DevOps and deployment conventions |
| `git.md` | Git workflow |
| `security.md` | Security practices |
| `style.md` | Code style |
| `testing.md` | Testing pyramid, behavior-based tests |

## Links

- `prod` — stable, production-ready config
- `dev` — active development

## References

- Inspired by: https://github.com/snarktank/ralph

- https://github.com/kirodotdev/Kiro
