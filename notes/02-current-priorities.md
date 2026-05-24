# Current Priorities

## Active Tasks

### 🔴 Zitadel CSP Fix (URGENT — 2026-05-24)
- **Problem:** Login blocked by CSP violations (8 connect-src blocked to http://auth.izzispark.cloud)
- **Root cause:** ZITADEL_EXTERNALSECURE=false → environment.json returns HTTP api URL
- **Fix 1:** Change ZITADEL_EXTERNALSECURE=true in /opt/zitadel/docker-compose.yml
- **Fix 2:** Apply CSP middleware to auth-zitadel-secure router
- **SSH:** New dokploy key registered in Dokploy UI, needs VPS authorized_keys

### 1. Website Deploy Fix ⚠️ URGENT
- **Problem:** Frontend deployments failing (Azure/Bun pipeline)
- **Error:** 4+ failed deploys in recent history
- **Impact:** Production frontend not updating
- **Next:** Investigate Dockerfile and build configuration

### 2. Neo Brain Setup ✅ DONE
- Vault: `~/.obsidian-vault` → `izzispark/neo-brain`
- Sync: Real-time via inotifywait script
- Status: Live and syncing

### 3. Dokploy Onboarding ✅ DONE
- Instance: https://host.izzispark.cloud
- Projects: Dev Env (coder), Website (frontend)

## SSH Keys (Updated 2026-05-24)
- **New key:** `ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFTeftllpc7ylCyq5wbpAiajDwCWwmXQkpphDYUNa7Ex dokploy`
- **Status:** Registered in Dokploy UI. Need to add to VPS authorized_keys.
- **Private:** Downloaded locally by Josafá (never share)

## Pending Decisions

### SSH Key on VPS
- Add public key to authorized_keys via Hostinger hPanel → SSH Access
- Then Dokploy can SSH to VPS and execute fixes

### Coder Access URL
- Current docker-compose uses `CODER_ACCESS_URL` (not set)
- Need to configure for proper Coder external access

## Roadmap
- [ ] Fix Zitadel CSP (blocking login)
- [ ] Fix Website deploy (Azure/Bun pipeline)
- [ ] SSH key configuration for Dokploy
- [ ] Coder Access URL configuration

## Created
2026-05-23
## Updated
2026-05-24
