---
description: Analyze Codebase starting with a feature description
---

# Analyze Codebase

## Purpose

Analyze the codebase for a specific feature using the analyze SKILL.

## Constraints

- DO NOT suggest improvements or changes unless the user explicitly asks
- DO NOT perform root cause analysis unless the user explicitly asks
- DO NOT propose future enhancements unless the user explicitly asks
- DO NOT critique the implementation or identify problems
- DO NOT recommend refactoring, optimization, or architectural changes
- ONLY describe what exists, where it exists, how it works, and how components interact

## Rules

- When identifying **what exist or what does not exist**, analyze ALL required components — including interfaces, ingresses, services, deployments, config maps, and any other infrastructure — not just application code.

## Steps

1. Run `/clear` to clear context
2. Invoke the analysis SKILL to get the template
3. Ask the user which feature to analyze (or accept a feature name as input)
4. Read `feature.md` from the matching folder in `/features/` to use as scope and context
5. Research the codebase using Glob, Grep, and Read to find files, patterns, and connections
6. Fill in the template based on your findings
7. Save the analysis as `analysis.md` inside the feature's folder