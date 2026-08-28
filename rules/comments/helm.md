# Helm / Kubernetes Manifests

## Critical — Manifest Comments

- **One-line description** — state what the section controls or configures (only when not self-evident from the section name).
- **Comment every field** — describe its purpose inline above the key, including nested fields (e.g. list items, sub-objects).
- **Call out intentional/manual actions** — e.g. `# Upgrade intentionally by changing this value.` for version pins that require a deliberate bump.
- **Document allowed values or references** when a field links to another field, e.g. `# Repository alias referenced by $values.`.
- **Blank line between fields and between list items** within a section for readability.
- **Explain non-default behavior** — e.g. why self-management, automated sync, or drift correction is enabled.
