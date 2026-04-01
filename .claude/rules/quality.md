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

## Git
- **Never commit** — always let the user review and commit changes.