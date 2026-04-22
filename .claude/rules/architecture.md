# Architecture

## Critical — Structure

- **Use interfaces at layer boundaries** — allow substitution and decoupling between layers.
- **Reject circular dependencies** — if two layers depend on each other, extract a shared interface.

## Critical — Resilience

- **Design for failure** — implement retries, circuit breakers, and fallbacks.
- **Run as stateless processes** — persist state only in backing services.
- **Scale out via the process model** — not by making processes bigger.
- **Enable fast startup and graceful shutdown** — treat processes as ephemeral.

## Critical — Infrastructure

- **Use API gateways** — single entry point for requests, authentication, and routing.
- **Implement service discovery** — allow microservices to locate and communicate dynamically.
- **Export services via port binding** — the app is self-contained.
- **Treat backing services as attached resources** — databases, queues, and caches via URL/config.
- **Provision infrastructure via code (IaC)** — not manual steps.
- **Run admin tasks as one-off processes** — in the same environment as the app.

## Preferred

- When creating a diagram, **use draw.io** and store `.drawio` files in `assets/diagrams/`.
- When adding a new component or updating component, **create or update the architecture diagram** to reflect the change.
