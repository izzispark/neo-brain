---
ai-first: true
type: project
status: active
tags:
  - development
  - infrastructure
  - docker
related-people:
  - neo
related-decisions:
  - docker-compose-coder
---

# Coder Development Environment

Ambiente de desenvolvimento remoto da izzi Spark.

## Descrição
Instância Coder para desenvolvimento remoto, rodando via Docker Compose no Dokploy.

## Configuração Atual
- **Versão:** Coder v2.15.3
- **Stack:** Docker Compose (Coder + PostgreSQL 17)
- **Service:** dev-env-coder (compose)
- **Projeto Dokploy:** OpvD7JOXnNYzf1c_ULEgT
- **Containers:** coder-1 (running), db-1 (healthy)
- **Uptime:** 12h+

## Status
✅ **Funcionando** - Coder e PostgreSQL operacionais

## Decisões-Chave
1. **Docker Compose** sobre outras opções (simplicidade, reprodutibilidade)
2. **PostgreSQL 17** como banco de dados
3. **Dokploy-managed** - gerenciado via painel Dokploy

## Pendências
- `CODER_ACCESS_URL` não configurado (acesso externo pode não funcionar)
- SSH keys não configuradas no Dokploy

## Related
- [[dokploy-infra]] - Plataforma de deploy
- [[vps-hostinger-setup]] - VPS subjacente