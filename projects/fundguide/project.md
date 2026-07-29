# P-006 — FundGuide

## Record

| Field | Value |
|---|---|
| Product | FundGuide |
| Domain | Funding-allocation review assistant |
| Relationship owner | Unassigned |
| Student owner | Unassigned |
| Senior reviewer | Unassigned |
| Stage | Existing live Vercel product / source recovery required for maintenance |
| Public deployment | `https://fundguide-prototype.vercel.app` |
| Last known source snapshot | `58a841f` in the PRI repository history |
| Current `main` | CME Atlas — not FundGuide |

## Critical maintenance rule

There is no dedicated FundGuide branch in the handed-off repository. To resume work, create a separate branch and worktree rooted at `58a841f`. Do not rewind `main` or deploy current `main` to the linked FundGuide Vercel project.

## Artifact register

| Artifact | Status |
|---|---|
| Source recovery commit | `58a841f` |
| [PRI operational handoff](/Users/carringtonhaykellar/candur/pri/HANDOFF.md) | Documents deployment mismatch and recovery path |
| [UofC handoff record](../cme-atlas/handoff-log.md) | Stores cross-product topology |
| [Technical design](technical-design.md) | Limited to recovered handoff evidence |
| [Production review](production-review.md) | Existing deployment not independently audited |

## Immediate next actions

1. Assign a FundGuide product owner.
2. Create a dedicated recovery branch/worktree from `58a841f`.
3. Verify that the recovered source matches the live Vercel deployment.
4. Inventory data, authentication, authorization, storage, monitoring, and support.
5. Decide whether to maintain, migrate, archive, or retire the deployment.

