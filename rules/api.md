# API Design

## Critical

- **Use nouns for resources, verbs for actions** — `GET /users`, not `GET /getUsers`.
- **Return correct HTTP status codes** — 200 success, 201 created, 400 bad request, 404 not found, 500 server error.
- **Version APIs from day one** — use URL prefix (`/v1/`) or headers.
- **Paginate list endpoints** — never return unbounded collections.
- **Use consistent error response format** — include `error`, `message`, and `code` fields.
