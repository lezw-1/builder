---
name: analysis
description: Analyze Codebase starting with Feature Description
---

## Analysis: [Name]

**What:** [One sentence description]

---

### Details

**What Exists:**

| What                       | Where       |
| -------------------------- | ----------- |
| [existing file or pattern] | [path:line] |

**What Does Not Exist:**

| Requirement                   | Current State                             |
| ----------------------------- | ----------------------------------------- |
| [requirement from feature.md] | [not implemented / partially implemented] |

---

### Summary

[2-3 sentences: greenfield vs partial, closest existing patterns, key gaps]

**Important:**

- Include specific file paths and line numbers
- Only describe what exists, never suggest changes
- Use feature.md acceptance criteria as the checklist for "What Does Not Exist"
- Keep the analysis **simple and focused** — avoid over-engineering or adding scope beyond what is described

---

### Example

```
## Analysis: HTTPS Integration

**What:** Add TLS termination to the API gateway so all traffic is served over HTTPS.

---

### Details

**What Exists:**

| What                                          | Where                         |
| --------------------------------------------- | ----------------------------- |
| HTTP server listening on port 80              | `gateway/server.go:14`        |
| Nginx config with no TLS block                | `infra/nginx/nginx.conf:22`   |
| Self-signed cert script (dev only)            | `scripts/gen-cert.sh`         |
| Kubernetes Ingress resource (no TLS section)  | `infra/k8s/ingress.yaml:1`   |

**What Does Not Exist:**

| Requirement                              | Current State                                      |
| ---------------------------------------- | -------------------------------------------------- |
| TLS certificate provisioning             | Not implemented — no cert-manager or ACME config   |
| HTTPS listener on port 443               | Not implemented — only port 80 in nginx.conf       |
| HTTP → HTTPS redirect                    | Not implemented — no redirect rule in Nginx        |
| TLS secret in Kubernetes                 | Not implemented — Ingress has no `tls:` block      |
| HTTPS health check endpoints             | Not implemented — probes use HTTP scheme           |

---

### Summary

HTTPS is not yet implemented — the gateway, Nginx config, and Kubernetes Ingress all operate over plain HTTP. The closest existing pattern is the dev cert script, but there is no production TLS provisioning or cert-manager setup. Key gaps are TLS termination in Nginx, a cert secret in Kubernetes, and an HTTP-to-HTTPS redirect rule.
```
