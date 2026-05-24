---
ai-first: true
type: project
status: active
tags:
  - brain
  - vault
  - obsidian
  - knowledge-management
related-people:
  - neo
  - josafa
---

# Neo Brain

Vault de conhecimento pessoal do CTO da izzi Spark.

## Descrição
Sistema de gerenciamento de conhecimento baseado em Obsidian, sincronizado em tempo real com GitHub.

## Repositório
- **GitHub:** [[izzispark/neo-brain]]
- **Local:** `~/.obsidian-vault`
- **Sync:** Script `obsidian-sync.sh` com inotifywait (debounce 3s)

## Configuração Atual
- **Stack:** Obsidian + Git + inotifywait
- **Status:** ✅ Ativo e sincronizando
- **Criado:** 2026-05-23

## Decisões-Chave
1. **Repositório sob org `izzispark`** (não conta pessoal)
2. **Sync em tempo real** via inotifywait (não polling)
3. **Commits automáticos** após debounce de 3 segundos

## Related
- [[izzi-spark]] - Empresa
- [[josafa]] - Fundador