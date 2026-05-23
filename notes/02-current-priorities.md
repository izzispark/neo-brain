# Current Priorities

## Active Tasks

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
- SSH Keys: None configured (TODO)

## Pending Decisions

### SSH Keys
- Need to create SSH key for Dokploy server access
- Configure for Git operations and server access

### Coder Access URL
- Current docker-compose uses `CODER_ACCESS_URL` (not set)
- Need to configure for proper Coder external access

### Frontend Build Fix
- Azure Static Web Apps workflow moved to Bun
- Dokploy build is failing - needs Dockerfile review

## Roadmap Discussion
- Awaiting Josafá's input on next business priorities
- Technical debt: SSH keys, Coder URL, Frontend deploy

## Created
2026-05-23