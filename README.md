## Contents

Claude Code configuration with rules and skills for autonomous development.

<img src="assets/diagrams/architecture.png" alt="Architecture" width="600" height="500" />

- `script.sh` — executes Claude autonomously to build new features from a PRD
- `.claude/rules/` — passive instructions Claude always follows 
- `.claude/skills/` — active workflows Claude executes on demand 
- `.claude/memory/` — persistent context Claude retains across sessions (not handled by git)

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
