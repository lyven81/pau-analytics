# Lead Check — 2026-11-25

**Run time:** 2026-11-25 (automated scheduled run)
**Status:** ⚠️ API UNREACHABLE

---

## Error

The Web Chat Lead Manager API at `https://web-chat-lead-manager-production.up.railway.app/api/leads` could not be reached.

**Reason:** The outbound egress proxy for this cloud session blocks the Railway host (`web-chat-lead-manager-production.up.railway.app:443`) with HTTP 403 — the host is not on the allowlist for this session.

This is a network policy restriction in the cloud execution environment, not a problem with the Railway app itself.

---

## What This Means

- No lead data was fetched.
- No follow-up messages were drafted.
- No lead summary is available for today.

---

## How to Fix

**Option A — Manual check (immediate):**
1. Open `https://web-chat-lead-manager-production.up.railway.app` in your browser.
2. Review leads with status `New` or `Qualifying` manually.

**Option B — Allow the host in Claude Code (permanent fix):**
- Add `web-chat-lead-manager-production.up.railway.app` to the allowed outbound hosts for your Claude Code cloud environment.
- See: https://code.claude.com/docs/en/claude-code-on-the-web for environment network policy configuration.

---

## Note

This same error has occurred on 2026-11-22, 2026-11-23, and 2026-11-24. **This is day 4 of consecutive failures.** The lead check will continue to fail on every scheduled run until the network policy is updated.

---

## Next Run

This check is scheduled to run again tomorrow. If the host is added to the allowlist before then, the next run will fetch leads and draft messages automatically.
