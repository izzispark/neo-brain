# Hot Swap Log

A hot swap is when we change direction mid-course. These are critical to track because they represent pivots in thinking or approach.

## Format
- **Date:** When the swap happened
- **Context:** What was happening before
- **Swap:** What changed and why
- **Result:** Did it work?

---

## Swap 001 - 2026-05-23
**Context:** Installing Playwright for browser automation
**Before:** Tried `pip install playwright` → failed (externally managed)
**Swap:** Created Python venv instead of system install
**Result:** ✅ Worked perfectly

## Swap 002 - 2026-05-23
**Context:** Installing GitHub CLI
**Before:** Tried apt repository → GPG key issues
**Swap:** Downloaded .deb directly from GitHub releases
**Result:** ✅ Worked perfectly

## Swap 003 - 2026-05-23
**Context:** Obsidian sync script - untracked files
**Before:** `git diff --quiet` only tracked modified files
**Swap:** Added check for untracked files via `git ls-files --others`
**Result:** ✅ Now syncs new files correctly

## Swap 004 - 2026-05-23
**Context:** GitHub repo organization
**Before:** Created repo under `josafaps` personal account
**Swap:** Recreated under `izzispark` organization
**Result:** ✅ Correct org, deleted old repo

## Swap 005 - 2026-05-23
**Context:** Browser-based login to Dokploy
**Before:** curl to API endpoints → 404
**Swap:** Used Playwright with Chromium (headless browser)
**Result:** ✅ Can now navigate and interact with Dokploy UI

## Swap 006 - 2026-05-23
**Context:** gh auth login interactive
**Before:** Expected interactive browser auth
**Swap:** Used `echo TOKEN | gh auth login --with-token` (non-interactive)
**Result:** ✅ Worked, faster

---

## Active Rules (Hot Swap Evolved)

1. **Browser automation** → Use Playwright with venv (not system Python)
2. **GitHub CLI** → Direct .deb download, not apt
3. **New files sync** → Always use `git add -A` (not just `git add .`)
4. **Repo creation** → Always under `izzispark` org, not personal
5. **Auth** → Prefer non-interactive token auth over browser flows

## Created
2026-05-23