# P-005 — Handoff log

## 2026-07-28 — CME Atlas / PRI repository

| Field | Verified handoff value |
|---|---|
| Worktree | `/Users/carringtonhaykellar/candur/pri` |
| Branch | `main` |
| Commit | `48113a6bab4980a534512132a46330eb7d3e3456` |
| Commit subject | `Add CME Atlas agent handoff` |
| Worktree state | Clean |
| Local application | `http://localhost:3000/` |
| Live request | Reported 18 activities returned for the cardiology query |
| Vinext/Sites build | Passed |
| Next.js/Vercel build | Passed |
| ESLint | Passed |
| Tests | 2 passed, 0 failed |
| Production change | None |

## Source and deployment snapshot

| Surface | Product | State |
|---|---|---|
| `main` source | CME Atlas | current source |
| ignored `.vercel/project.json` | FundGuide | public live deployment |
| `.openai/hosting.json` | Land and Earn | private Sites deployment |

No Git remote is configured in the PRI checkout.

## Linked worktrees

- `/Users/carringtonhaykellar/candur/pri` — `main` at `48113a6`
- `/Users/carringtonhaykellar/.buzz-dev/.scratch/pri-accme-explorer` — `feature/accme-course-explorer` at `bd3d665`
- `/Users/carringtonhaykellar/candur/pri-land-and-earn` — `feature/land-and-earn-prd` at `168f897`

## Recovery rule

FundGuide’s last known source snapshot is ancestor commit `58a841f`. Resume its maintenance by creating a separate branch/worktree rooted at that commit. Do not rewind `main`, delete or force-update other product branches, or deploy CME Atlas through either existing hosting link.

The local server, linked worktrees, and production deployments were not changed during UofC intake.

