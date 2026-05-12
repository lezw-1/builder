---
name: readme
description: Write or update a README for the current project or component
---

# [Project or Component Name]

[One-sentence headline — what it does and for whom]

## Architecture

[Short description of how the system is structured — layers, patterns, data flow]

## Components

- **[Component]** — [what it does]
- **[Component]** — [what it does]

## Deployment (optional)

### Local

Copy env vars and start the stack:

```sh
cp .env.example .env
docker-compose up --build
```

Access at `http://localhost:{port}`.

### Dev

Env variables can be found in: `[env file path]`.

Deployment is orchestrated by the CI/CD workflow in `.github`.

Access at:

```
http://dev.{domain}
https://dev.{domain}
```

### Prod

Env variables can be found in: `[env file path]`.

Deployment is orchestrated by the CI/CD workflow in `.github`.

Access at:

```
http://{domain}
https://{domain}
```

## Links (optionaL)

- [Label](url) — short description

## Inspired by (optional)

- [Label](url) — short description

**Important:**

- In the `Components` section, mark entries that correspond to paths in `.gitignore` with `(ignored)` after the description
- Only use the sections defined in this skill — do not add extra sections
- Keep it short — one sentence per concept, no filler
- Code blocks for every command
- No badges, no emojis, no marketing language
- `Deployment` section is optional — omit if not applicable
- `Inspired by` section is optional — omit if not applicable
- `Links` section is optional — omit if not applicable
- Backlog goes in a separate `BACKLOG.md` file, not in the README
- Do not commit — let the user review first

---

### Example

````
# Notify

A notification service that delivers email and push alerts for internal platform events.

## Architecture

<img src="assets/diagrams/architecture.png" alt="Architecture" width="600" height="500" />

## Components

- **API** — FastAPI service that receives notification requests via `POST /v1/notify`
- **Worker** — Celery worker that processes jobs from the queue asynchronously
- **Queue** — Redis-backed task queue between the API and worker
- **Email** — SMTP adapter for transactional email delivery
- **Push** — Firebase Cloud Messaging adapter for mobile push alerts
- **Database** — PostgreSQL storing notification history and delivery status

## Deployment

### Local

Copy env vars and start the stack:

```sh
cp .env.example .env
docker-compose up --build
```

Access at `http://localhost:8000`.

### Dev

Env variables can be found in: `helm/environments/dev.yaml`.

Deployment is orchestrated by the CI/CD workflow in `.github`.

Access at:
```
http://dev.notify.example.com
https://dev.notify.example.com
```

### Prod

Env variables can be found in: `helm/environments/prod.yaml`.

Deployment is orchestrated by the CI/CD workflow in `.github`.

Access at:
```
http://notify.example.com
https://notify.example.com
```

## Links

- [Firebase Cloud Messaging](https://firebase.google.com/docs/cloud-messaging) — push notification delivery platform
- [Celery Docs](https://docs.celeryq.dev) — distributed task queue used for async job processing

## Inspired by

- [The Twelve-Factor App](https://12factor.net) — methodology for building scalable, maintainable services
````
