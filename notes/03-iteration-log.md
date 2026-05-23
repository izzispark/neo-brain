# Neo OS - Iteration System

## Purpose
Every interaction with Josafá is an iteration. This system captures learnings, tracks hot swaps, and enables self-improvement over time.

## How It Works
1. **Iteração** — Each conversation/decision = iteration
2. **Hot Swap** — When approach changes mid-course, log it
3. **Learnings** — Capture what worked/didn't
4. **Self-Improve** — Update approach based on feedback

## Current Iteration
- **Iteration:** 001
- **Started:** 2026-05-23
- **Context:** First session with Josafá on WhatsApp

## Iteration Log

### Iteration 001 (2026-05-23)
**Context:** Initial onboarding session
**Goal:** Setup brain, configure tools, understand current state

**What happened:**
1. ✅ Accessed Dokploy (host.izzispark.cloud) - first time
2. ✅ Installed Playwright for browser automation
3. ✅ Found Coder running (v2.15.3 + PostgreSQL)
4. ✅ Found Website frontend failing (Azure/Bun pipeline)
5. ✅ Setup Neo Brain vault → izzispark/neo-brain
6. ✅ GitHub CLI login with PAT
7. ✅ Moved repo from josafaps to izzispark org
8. ✅ Deleted old repo
9. ✅ Created obsidian-sync.sh with inotifywait
10. ✅ Populated initial brain notes

**Hot Swaps:**
- Started with browser login to Dokploy → worked but needed Playwright install
- Tried apt install for gh → failed → downloaded .deb directly
- First vault sync only tracked modified files → patched to include untracked files

**Learnings:**
- Dokploy has 2 projects: Dev Env (coder) + Website
- Coder is working, Website deploys failing
- User communicates in Portuguese BR
- User is hands-on, wants to understand technical details

**Next iteration goals:**
- Fix Website deployment issue
- Create SSH keys in Dokploy
- Configure CODER_ACCESS_URL

## Archived Iterations
(None yet - this is iteration 001)

## Hot Swap Log
| When | What Changed | Why |
|------|-------------|-----|
| 2026-05-23 | Playwright install approach | apt broken → venv + deps |
| 2026-05-23 | Git sync script | Only tracked modified → tracked all (add -A) |
| 2026-05-23 | gh install | apt repo signed → direct .deb download |

## Self-Improvement Actions
1. **Always confirm** before making breaking changes (even though I have context)
2. **Log hot swaps** as they happen so we track evolution
3. **End of each major task** → write learnings to vault
4. **Check vault first** before assuming anything about past decisions

## Created
2026-05-23