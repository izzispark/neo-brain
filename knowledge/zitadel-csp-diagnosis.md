---
date: 2026-05-24
type: knowledge
tags: [zitadel, csp, auth, bug-fix, priority-high]
ai-first: true
stated: high
---

# Zitadel CSP Diagnosis (2026-05-24)

## Problem
Login at https://auth.izzispark.cloud/ui/login blocked by CSP violations.
Blocked: 8 `connect-src` directives all pointing to `http://auth.izzispark.cloud` (port 80).

## Root Cause Confirmed

### environment.json (fetched 2026-05-24)
```json
{
  "api": "http://auth.izzispark.cloud",
  "issuer": "https://auth.izzispark.cloud",
  "clientid": "374243810965914371"
}
```

- `api` field returns **HTTP** URL (port 80)
- Browser on HTTPS tries port 80 → **CSP blocks**
- `issuer` correctly returns HTTPS

### Zitadel compose env var (root cause)
```
ZITADEL_EXTERNALSECURE=false  ← ROOT CAUSE
```
Location: `/opt/zitadel/docker-compose.yml` on VPS 31.97.165.203

### CSP middleware (exists, correct)
File: `/etc/dokploy/traefik/dynamic/auth-izzispark-csp.yml`
```yaml
connect-src 'self' https://auth.izzispark.cloud  ✓ CORRECT
```
CSP header is fine. Problem is environment.json returning HTTP.

## Fix Required (2 changes)

### Fix 1: Change ZITADEL_EXTERNALSECURE to true
File: `/opt/zitadel/docker-compose.yml`
```
ZITADEL_EXTERNALSECURE=true
```
This makes environment.json return `api: "https://auth.izzispark.cloud"`.

### Fix 2: Apply CSP middleware to HTTPS router
File: `/etc/dokploy/traefik/dynamic/auth-izzispark.yml`
Router `auth-zitadel-secure` needs:
```yaml
middlewares:
  - auth-csp
```

## SSH Access
Dokploy SSH key (created 2026-05-24):
```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFTeftllpc7ylCyq5wbpAiajDwCWwmXQkpphDYUNa7Ex dokploy
```
Private key downloaded by Josafá. Public key registered in Dokploy UI.
Need to add public key to VPS authorized_keys.

## Validation
After fix:
1. `curl https://auth.izzispark.cloud/ui/console/assets/environment.json`
   → should show `"api": "https://auth.izzispark.cloud"`
2. No CSP violations in browser DevTools
3. Login flow completes

## Related
- [[projects/dokploy-infra]]
- [[knowledge/zitadel-admin-credentials]]
- [[knowledge/ssh-keys]]
