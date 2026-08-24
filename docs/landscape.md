# Landscape Notes — how this list's data was gathered

Last full pass: **2026-08-24**, via GitHub API + repo docs + engineering blogs.
Star counts move weekly in this space; treat them as a snapshot, not scripture.

## Term timeline (verified)

| When | What |
|---|---|
| pre-2026 | "harness" as eval-harness vocabulary (METR, SWE-bench, SWE-agent) |
| 2025-11 | Anthropic — *Effective Harnesses for Long-Running Agents* |
| **2026-02** | **OpenAI — *Harness Engineering* (Ryan Lopopolo) — the coining post** |
| 2026-02+ | lopopolo/harness-engineering anthology (2.5k★) |
| 2026-04 | martinfowler.com follow-up |
| 2026-05 | walkinglabs open book; arXiv 2604.25850 |
| 2026-07 | Lilian Weng — *…for Self-Improvement*; HumanLayer counterpoint (2.5k★) |

## Field measurements we took ourselves

- **macOS 26 sandbox-exec obituary**: profiles parse fine, real exec SIGABRTs
  (checked: `posixshm-read*` doesn't exist; `file-read-metadata` doesn't save it).
  A sandbox runner that can't run `/bin/echo` is not a runner — fail closed.
  See [bayshier/harness-engineering](https://github.com/bayshier/harness-engineering)
  for the probe pattern.
- **Tencent CN market-data CDNs** filter by TLS fingerprint: curl passes,
  JVM gets connection-reset or HTTP-200-empty. Dual-source failover is
  load-bearing, not decorative.
- **MCP stdio e2e**: fire requests serially with delays; concurrent bursts
  lose responses in SDK 2.0.1.

## Removal policy

Projects archived, or demonstrably stale > 6 months with critical bugs open,
get removed at the next pass. Re-additions welcome with evidence of revival.

## Honest unknowns

- The exact first utterance of "harness engineering" before the OpenAI post
  (X is unsearchable from our tooling).
- Cursor background agents' underlying isolation tech (docs behind a JS shell).
- Which named companies run E2B vs Daytona in production (marketing claims only).
