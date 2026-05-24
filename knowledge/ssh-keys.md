---
date: 2026-05-24
type: knowledge
tags: [ssh, infra, security]
ai-first: true
stated: high
---

# SSH Keys — izzi Spark

## Chave Dokploy (criada 2026-05-24 via Dokploy UI)

**Tipo:** ed25519
**Usuário:** dokploy

```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFTeftllpc7ylCyq5wbpAiajDwCWwmXQkpphDYUNa7Ex dokploy
```

## Como usar

Esta é a **chave pública**. A **chave privada** foi baixada pelo Josafá localmente via Dokploy UI.

## Registro no VPS

A chave pública deve ser adicionada ao `authorized_keys` no VPS (31.97.165.203):
- Via Hostinger hPanel → VPS → SSH Access

## Chave Anterior (deletada 2026-05-24)
```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIKVfboiA7nRqg21AvsmjOsKzE6GMt3nTM+p3nBD8yaPF dokploy-izzi-spark
```
(Deletada e recriada via Dokploy UI)

## Related
- [[projects/dokploy-infra]]
- [[projects/vps-hostinger-setup]]
