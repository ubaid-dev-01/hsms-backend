<div align="center">

# HSMS Backend

**Housing Society Management System API — Express + MongoDB**

![Express](https://img.shields.io/badge/Express-404D59?style=flat&logo=express&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

[Repository](https://github.com/ubaid-dev-01/hsms-backend) · [Author](https://github.com/ubaid-dev-01) · [Portfolio](https://ubaid-dev-01.vercel.app)

</div>

---

## Overview

Backend for HSMS: multi-tenant housing-society operations covering plots, installments, visitors, announcements, authorization, and workflow-driven business rules. Express API with MongoDB, Redis helpers, Docker, and Vercel-compatible entrypoints.

## Features

- Multi-tenant society operations API
- Auth + role/policy gates
- Plot / billing / visitor domains
- Announcements and admin tooling
- Docker Compose + Dockerfile
- Health and ops endpoints

## Architecture

```text
Clients (web / resident app)
        ↓ JWT
   Express API (src/)
        ↓
 MongoDB · Redis · storage as configured
```

## Tech stack

- Express
- TypeScript
- MongoDB / Mongoose
- Redis (ioredis)
- Docker
- Vercel serverless entry under `api/`

## Project structure

```text
hsms-backend/
├── src/ api/ migrations/
├── docker-compose.yml
└── docs/
```

## Getting started

```bash
cp .env.example .env
npm install
npm run dev
```

## Environment

Use `.env.example` as the source of truth. Never commit production Mongo/Redis credentials.

## Scripts

| Command | Purpose |
| --- | --- |
| `npm run dev` / `build` / `start` | API lifecycle |
| `npm test` | Tests |

## Documentation

| Doc | Purpose |
| --- | --- |
| [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) | System shape, data flow, boundaries |
| [docs/SETUP.md](docs/SETUP.md) | Local install, env, runbook |
| [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md) | Branching, commits, PR checklist |
| [docs/API.md](docs/API.md) | API contract notes |

## Author

**M Ubaid Javaid** — Software Engineer (MERN / Next.js)

- GitHub: [https://github.com/ubaid-dev-01](https://github.com/ubaid-dev-01)
- Portfolio: [https://ubaid-dev-01.vercel.app](https://ubaid-dev-01.vercel.app)
- Email: mubaidjavaid97@gmail.com

## License

Source is published for portfolio and engineering review. Client product ownership is not implied unless stated in a case study.

