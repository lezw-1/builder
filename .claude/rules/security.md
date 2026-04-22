# Security

## Critical

- **Validate all external input** — never trust data from users, APIs, or third parties.
- **Use parameterized queries** — never concatenate user input into SQL or commands.
- **Store secrets in environment variables or a vault** — never in code, configs, or logs.
- **Apply least privilege** — grant only the minimum permissions needed.
- **Authenticate every API endpoint** — default to deny, explicitly allow.
- **Scan dependencies for known vulnerabilities** — automate with Dependabot or Snyk.
