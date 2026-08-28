# Code Style

## Critical — Naming

- **Use descriptive, intention-revealing names** — avoid abbreviations unless universally understood.
- **Name functions with a verb**: `getUserById`, `calculateTotal`, `sendNotification`.
- **Name booleans as true/false statements**: `isValid`, `hasPermission`, `canRetry`.

## Critical — Comments

- **Add comments for non-obvious algorithms**, workarounds, or external constraints.
- When using complex commands (e.g. Shell/Bash commands with more than 20 characters), **comment them**.
- **Add a short comment** (maximum 8 words) for every function, class, etc.
- When defining functions, **use this docstring format**:

  ```
  """Save a list of promises to the database.

      Args:
          promises: List of promises, each with promise, source, and date fields.
  """
  ```

- When writing executable code, **use a one-liner comment** (e.g. `# This executes a scraper`).
- When separating major sections, groups, or classes inside a file, **use a banner comment**:

  ```
  # ============================================================================
  # General
  # ============================================================================
  ```

- **Add a one-liner comment for every constant variable** — describe its purpose inline:

  ```ts
  const [prompt, setPrompt] = useState(''); // User's research prompt input
  const [loading, setLoading] = useState(false); // True while a run is in flight
  const [run, setRun] = useState<RunStatus | null>(null); // Latest run status from backend
  const [error, setError] = useState<string | null>(null); // Network or API error message
  const intervalRef = useRef<ReturnType<typeof setInterval> | null>(null); // Polling timer handle
  ```

## Critical — Error Handling

- **Fail fast at system boundaries** — validate early, reject invalid state before it propagates.
- **Never swallow exceptions silently** — always log, re-throw, or handle explicitly.
- **Return meaningful error messages** — include what failed and why, never expose internals.
- **Use retries only for transient failures** — with exponential backoff and a max attempt limit.

## Critical — README

- **Keep the README simple and up to date** with every significant change.
- **Use only these sections**: Contents, Usage, Links, References.
