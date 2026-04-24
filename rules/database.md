# Database

## Critical

- **Use migrations for all schema changes** — never modify schemas manually in production.
- **Index columns used in WHERE, JOIN, and ORDER BY** — measure query performance before and after.
- **Avoid N+1 queries** — use joins or batch fetching instead of looping single queries.
- **Use transactions for multi-step writes** — ensure atomicity or roll back on failure.
