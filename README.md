# Builder

A Claude Code configuration for spec-driven, AI-assisted development — write a spec, then let the workflow guide implementation.

## Architecture

<img src="assets/diagrams/architecture.png" alt="Architecture" width="600" height="500" />

## Components

- **Commands** — slash commands that drive each phase of the workflow: `create-feature`, `create-analysis`, `create-tasks`, `execute-implementation`, `execute-test`
- **Rules** — passive instructions Claude always follows covering architecture, style, testing, security, API design, database, devops, and git conventions
- **Skills** — structured output templates invoked by commands to produce consistent artifacts (feature specs, analysis docs, task lists, READMEs)
- **Memory** — persistent context Claude builds up over time; not pushed to the repository

## Links

- [Claude Code](https://claude.ai/code) — the CLI this config is built for

## Inspired by

- [ralph](https://github.com/snarktank/ralph) — spec-driven Claude workflow
- [Kiro](https://github.com/kirodotdev/Kiro) — AI-assisted development environment
