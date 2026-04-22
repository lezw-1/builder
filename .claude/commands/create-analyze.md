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

## Steps

1. Invoke the analysis SKILL to get the template
2. Ask the user which feature to analyze (or accept a feature name as input)
3. Read `feature.md` from the matching folder in `/features/` to use as scope and context
4. If the user mentions additional files (tickets, docs, JSON), read them FULLY as well
5. Break down the research into composable areas (components, patterns, architecture)
6. Research the codebase using Glob, Grep, and Read to find files, patterns, and connections
7. Synthesize findings with specific file paths and line numbers
8. Save the analysis as `analysis.md` inside the feature's folder using the SKILL template
9. Present a concise summary and ask if the user has follow-up questions
