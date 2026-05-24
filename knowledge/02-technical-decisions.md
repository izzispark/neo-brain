# Technical Decisions

## Architecture Principles
1. **Self-hosted first** — Prefer self-hosted solutions over SaaS when cost/effort makes sense
2. **Simplicity over sophistication** — Avoid over-engineering
3. **GitOps** — All config and infrastructure as code where possible

## Decisions Made

### Dokploy over Vercel/Netlify/Heroku
- **Why:** Self-hosted, open source, full control
- **Context:** izzi Spark needs control over infrastructure
- **Status:** ✅ Deployed and running

### Coder for Development Environments
- **Why:** Remote dev environments, team collaboration
- **Context:** Need consistent dev environment across team
- **Status:** ✅ Running v2.15.3

### Docker Compose for Coder stack
- **Stack:** Coder + PostgreSQL 17
- **Why:** Simple, reproducible, Dokploy-managed
- **Status:** ✅ Running with health checks

## Pending Decisions

### Frontend Stack
- **Current:** Website deploy via GitHub
- **Issue:** Build failing (Azure/Bun pipeline)
- **Needs:** Dockerfile review, possibly migrate build process

### Coder External Access
- **Current:** `CODER_ACCESS_URL` not set
- **Impact:** May not be accessible externally
- **Needs:** Domain/subdomain configuration

### SSH Key Management
- **Current:** No SSH keys in Dokploy
- **Impact:** Can't access servers via Dokploy
- **Needs:** Generate and configure SSH keys

## Created
2026-05-23