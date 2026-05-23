---
ai-first: true
type: project
status: active
tags:
  - frontend
  - website
  - deployment
  - critical
related-people:
  - neo
related-decisions:
  - frontend-stack-pending
---

# izzi Website

Frontend do site da izzi Spark.

## Descrição
Website institucional da izzi Spark, implantado via GitHub Actions para Dokploy.

## Situação Atual
⚠️ **PROBLEMA:** Deploys falhando continuamente

## Configuração
- **Repo:** `izzi-spark-website`
- **Branch:** main
- **Org:** [[izzispark]]
- **Webhook:** `https://host.izzispark.cloud/api/deploy/2WRwQ_UHZiVSfTRrxC432`
- **Build:** Dockerfile

## Problema Conhecido
- Azure Static Web Apps workflow usando Bun
- Dokploy build está falhando
- 4+ deploys falharam recentemente

## Stack Técnica
- **Frontend:** (to be documented)
- **CI/CD:** GitHub Actions → Dokploy
- **Build:** Bun (Azure pipeline)

## Próximos Passos
1. Investigar Dockerfile e configuração de build
2. Corrigir pipeline Azure/Bun
3. Validar deploy no Dokploy

## Decisões-Chave
- Migração de Azure Static Web Apps para Dokploy (incompleta)
- Build via Dockerfile (necessita revisão)

## Related
- [[dokploy-infra]] - Infra de deploy
- [[vps-hostinger-setup]] - VPS subjacente