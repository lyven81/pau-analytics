# Lead Check — 2026-08-20

**Status: BLOCKED — API unreachable from remote execution environment**

---

## What Happened

The scheduled lead-check ran automatically at its configured time but could not reach the Web Chat Lead Manager API.

- **API URL:** `https://web-chat-lead-manager-production.up.railway.app/api/leads`
- **Error:** `EGRESS_BLOCKED` — the Railway domain is blocked by the network egress proxy in the Claude Code cloud environment.
- Both `curl` and `WebFetch` were attempted. Both returned the same block.

This has also been the case since at least 2026-08-19 (yesterday's run hit the same block).

---

## What To Do

This scheduled task cannot run from the cloud environment because Railway is blocked by the egress proxy.

**To fix this, choose one of:**

1. **Run the lead check manually** — open Claude Code on your local machine and type: `check leads`
2. **Allowlist the Railway domain** — contact support at claude.ai to request that `web-chat-lead-manager-production.up.railway.app` be added to the egress allowlist for your environment.
3. **Remove this scheduled task** — if you only want lead checks run manually, delete the cron schedule to stop these daily blocked runs.

---

*Run at: 2026-08-20 (automated schedule)*
