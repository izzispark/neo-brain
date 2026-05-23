---
type: idea
status: captured
date: 2026-05-23
tags:
  - automation
  - pipeline
  - ci-cd
  - frontend
related-projects:
  - izzi-website
  - dokploy-infra
---

# Pipeline de Automação para Frontend

## Origem
- File: `boards/tasks.md` (line 14-15)
- Context: "Frontend Dockerfile Review - Azure Static Web Apps workflow causing build errors on Dokploy"

## Descrição
Criar pipeline de automação mais robusto para o frontend da izzi Spark, substituindo a dependência do Azure Static Web Apps.

## Contexto
- Azure Static Web Apps workflow usando Bun está causando build errors no Dokploy
- 4+ deploys falharam recentemente
- Necessita investigar Dockerfile e configuração de build

## Próximos Passos
1. Revisar Dockerfile atual
2. Configurar pipeline de build para Dokploy
3. Validar deploy automatizado

## Related
- [[izzi-website]]
- [[dokploy-infra]]