# DevOps

## Critical — CI/CD & Releases

- **Define CI/CD pipelines as code** — in version-controlled files.
- **Separate build, release, and run stages** — never mutate a release.
- When deploying, **use blue-green deployment** — maintain two identical environments; switch traffic on release.

## Critical — Dependencies & Environments

- **Pin exact versions** for all dependencies — avoid floating ranges (`^`, `~`, `*`).
- **Use and commit a lockfile** (`package-lock.json`, `poetry.lock`, etc.).
- **Document required runtime versions** in `.nvmrc`, `.python-version`, or equivalent.
- **Declare all tooling as project dependencies** — never rely on globally installed tools.
- **Keep dev/prod parity** — keep environments as similar as possible.

## Critical — Observability

- **Treat logs as event streams** — write to stdout, centralize collection, never rely on per-instance log access.
- **Centralize monitoring** — gain visibility to identify and debug issues quickly.
- When creating a service, **expose readiness/liveness health checks**.

## Critical — Multi-Region

- When implementing multi-region deployments, **analyze failure scenarios**, **assess failover mechanisms**, **evaluate data replication strategies** (RPO/RTO), and **formulate risk mitigation recommendations**.

## Preferred

- When possible, **use containerised environments** (Docker, devcontainer) to eliminate "works on my machine" issues.
