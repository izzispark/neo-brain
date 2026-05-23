---
ai-first: true
type: project
status: active
tags:
  - infrastructure
  - deployment
  - self-hosted
related-people:
  - neo
related-decisions:
  - dokploy-over-vercel
---

# Dokploy Infrastructure

Plataforma de deployment auto-hospedada da izzi Spark.

## Descrição
Dokploy v0.29.5 rodando em VPS Hostinger, gerenciando os projetos da izzi Spark.

## Configuração Atual
- **Versão:** Dokploy v0.29.5
- **URL:** https://host.izzispark.cloud
- **Hosting:** Hostinger KVM4
- **VPS IP:** 31.97.165.203

## Projetos Gerenciados
1. **Dev Env (coder)** - Coder + PostgreSQL ✅
2. **Website (frontend)** - izzi-website ⚠️ (falhando)

## Decisões-Chave
1. **Dokploy sobre Vercel/Netlify/Heroku** - Self-hosted, open source, controle total
2. **Self-hosted first** - Preferir soluções auto-hospedadas sobre SaaS

## Status
✅ **Deployed and running**

## Pendências
- SSH keys não configuradas (não consegue acessar servidores via Dokploy)
- `CODER_ACCESS_URL` não configurado

## Related
- [[vps-hostinger-setup]] - VPS subjacente
- [[coder-dev-env]] - Projeto Coder
- [[izzi-website]] - Projeto Website