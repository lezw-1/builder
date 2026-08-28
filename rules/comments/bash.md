# Bash Scripts

## Critical — Script Comments

- **`#!/usr/bin/env bash`** must be the first line of the file.
- **Header comment block** right after the shebang — what the script does. Style it as a banner so it stands apart from normal one-line comments:

  ```bash
  # ==================================================
  # <What the script does>
  # ==================================================
  ```

- **`set -euo pipefail`** near the top of the script, with a one-line comment above it explaining what it does.
- **One-line comment above each constant or function** — its purpose. Exception: one that gets logged as-is needs no comment — the logged value is self-explanatory, e.g.:

  ```bash
  CURRENT_STEP="apply the app-of-apps"
  echo "Step: $CURRENT_STEP"
  ```
