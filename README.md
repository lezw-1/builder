## Contents

Claude Code configuration with rules and skills for autonomous development.

Spec driven is used spec-first approach: well thought-out spec is written first, then used in the AI-assisted development workflow.

Research → Plan → Implement → Validate. Clear context between each. Save everything to a sym-linked thoughts/ directory (use npx humanlayer thoughts init).

<img src="assets/diagrams/architecture.png" alt="Architecture" width="600" height="500" />

- `script.sh` — executes Claude autonomously to build new features from a PRD
- `.claude/rules/` — passive instructions Claude Code always follows 
- `.claude/skills/` — active workflows Claude Code executes on demand 
- `.claude/memory/` — persistent context Claude Code retains across sessions (not handled by git)

## Usage

```bash
./script.sh [max_iterations]
```

Claude reads `prd.json`, picks the highest priority unfinished story, implements it, and repeats until all stories pass or max iterations is reached.

## Links

- `prod` — stable, production-ready config
- `dev` — active development

## References

- Inspired by: https://github.com/snarktank/ralph

## ToDo 

- insert Testing
- insert dependency management


## workflow

create (done) -> analyze (wip)-> plan (open) -> implement (open) -> test (open)