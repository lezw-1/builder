# Architecture

## Critical — Structure

- **Use interfaces at layer boundaries** — allow substitution and decoupling between layers.
- **Reject circular dependencies** — if two layers depend on each other, extract a shared interface.
- **Decouple components** - each component owns its folder (e.g. ./frontend/) and all its configuration (.e.g ./frontend/package.json) — nothing component-specific belongs at the project root.
- **Design for the target platform** — keep deployment platform in mind (e.g. Kubernetes, Docker, Amazon Web Services)
- **Keep environments/stages explicit** — design for different stages (e.g. prod, dev, test, local)

## Critical — Resilience

- **Design for failure** — implement retries, circuit breakers, and fallbacks.
- **Run as stateless** — persist state only in backing components.

## Critical — Infrastructure

- **Use API gateways** — single entry point for requests, authentication, and routing.
- **Treat backing components as attached resources** — databases, queues, and caches via URL/config.
- **Provision infrastructure via code (IaC)** — not manual steps.

## Preferred

- When creating a diagram, **use draw.io** and store `.drawio` files in `assets/diagrams/`.
- When adding a new component or updating component, **create or update the architecture diagram** to reflect the change.
