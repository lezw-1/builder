# Helm Charts

## Critical — values.yaml Comments

- **One-line description** — briefly state what the section controls (only when not self-evident from the section name).
- **Comment every field** — describe its purpose inline above the key.
- **Document allowed values** on their own comment line: `# Allowed values: Always, IfNotPresent, Never`.
- **Document defaults or fallback behavior** when non-obvious: `# Default: Uses the chart's appVersion when empty.`
- **Blank line between fields** within a section for readability.
- **Never hardcode secrets** in values.yaml — document the expected external mechanism instead (e.g. `# Store sensitive values securely (e.g., External Secrets, Sealed Secrets).`).
