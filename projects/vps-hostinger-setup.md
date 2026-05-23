---
ai-first: true
type: project
status: completed
tags:
  - infrastructure
  - vps
  - hosting
  - setup
related-people:
  - neo
---

# VPS Hostinger Setup

Configuração do VPS da izzi Spark na Hostinger.

## Descrição
VPS Hostinger KVM4 rodando a infraestrutura da izzi Spark.

## Configuração
- **Plano:** Hostinger KVM4
- **VPS IP:** 31.97.165.203
- **Painel:** Dokploy v0.29.5
- **URL Dokploy:** https://host.izzispark.cloud

## Status
✅ **Configurado e operacional**

## Decisões-Chave
1. **Hostinger** como provedor VPS (custo-benefício)
2. **Dokploy** como plataforma de deployment (self-hosted)

## Serviços Rodando
- Dokploy (painel de controle)
- Coder (dev environments)
- Banco de dados (PostgreSQL)

## Related
- [[dokploy-infra]] - Dokploy rodando neste VPS