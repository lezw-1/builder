# Quality

## Comments
- Write comments to explain **why**, not what — the code itself should explain what.
- Add comments for **non-obvious algorithms, workarounds, or external constraints**.
- When using complex commands (e.g. Shell/Bash commands with more then 20 characters) then comment them

## Naming
- Use **descriptive, intention-revealing names** — avoid abbreviations unless universally understood.
- Functions should be named with a **verb**: `getUserById`, `calculateTotal`, `sendNotification`.
- Boolean variables and functions should read as **true/false statements**: `isValid`, `hasPermission`, `canRetry`.

## Functions & Methods
- Keep functions **short and focused** on a single task.
- **Return early** to reduce nesting; avoid deeply nested if/else chains.

## 12-Factor App
- **Codebase** — one repo, many deploys; never share code via copy-paste between apps.
- **Dependencies** — explicitly declare and isolate all dependencies; assume nothing is pre-installed.
- **Config** — store config in environment variables, never in code.
- **Backing services** — treat databases, queues, and caches as attached resources via URL/config.
- **Build / Release / Run** — strictly separate build, release, and run stages; never mutate a release.
- **Processes** — run as stateless processes; persist state only in backing services.
- **Port binding** — export services via a port; the app is self-contained, not injected into a web server.
- **Concurrency** — scale out via the process model, not by making processes bigger.
- **Disposability** — fast startup, graceful shutdown; treat processes as ephemeral.
- **Dev / Prod parity** — keep development, staging, and production as similar as possible.
- **Logs** — treat logs as event streams; write to stdout and let the environment route them.
- **Admin processes** — run admin/management tasks as one-off processes in the same environment as the app.

## Environment Consistency
- Pin **exact versions** for all dependencies — avoid floating ranges (`^`, `~`, `*`).
- Use a **lockfile** (`package-lock.json`, `poetry.lock`, etc.) and commit it.
- Document required **runtime versions** (Node, Python, etc.) in `.nvmrc`, `.python-version`, or equivalent.
- Never rely on **globally installed tools** — declare all tooling as project dependencies.
- Prefer **containerised environments** (Docker, devcontainer) to eliminate "works on my machine" issues.

## Git
- **Never commit** — always let the user review and commit changes.
- **Only push to `dev`** — never push to `prod` or any other branch.
- **Keep commit messages short** — maximum 10 words.
- **Pull requests from `dev` to `prod`** must be named `#1 dev`, `#2 dev`, etc. (incrementing number).
