# Architecture — HSMS Backend

## Intent

Backend for HSMS: multi-tenant housing-society operations covering plots, installments, visitors, announcements, authorization, and workflow-driven business rules. Express API with MongoDB, Redis helpers, Docker, and Vercel-compatible entrypoints.

## System shape

```text
Clients (web / resident app)
        ↓ JWT
   Express API (src/)
        ↓
 MongoDB · Redis · storage as configured
```

## Stack decisions

- Express
- TypeScript
- MongoDB / Mongoose
- Redis (ioredis)
- Docker
- Vercel serverless entry under `api/`

## Boundaries

- Secrets stay in environment variables / secret managers — never in git.
- Client bundles only receive public configuration (`NEXT_PUBLIC_*` / `VITE_*`).
- Tenant or role checks belong in middleware / server layers, not UI-only gates.
- Heavy or long-running work should not run inside short-lived serverless handlers unless designed for it.

## Quality bar

- Prefer typed contracts at API and domain boundaries.
- Ship a vertical slice (auth → persisted outcome) before a broad feature surface.
- Document trade-offs in PRs when changing data models or auth.

