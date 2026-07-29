# P-005 — CME Atlas

## Record

| Field | Value |
|---|---|
| Product | CME Atlas |
| Domain | Continuing medical education discovery |
| Primary data source | Public ACCME CME Passport catalogue API |
| Relationship owner | Unassigned |
| Student owner | Unassigned |
| Senior reviewer | Unassigned |
| Stage | Functional local product / deployment destination undecided |
| Worktree | `/Users/carringtonhaykellar/candur/pri` |
| Branch | `main` |
| Handoff commit | `48113a6bab4980a534512132a46330eb7d3e3456` |
| Local UI | `http://localhost:3000/` while the handed-off server is available |
| Production | No confirmed CME Atlas production deployment |

## Product purpose

CME Atlas searches the public catalogue behind ACCME CME Passport and presents current and upcoming continuing medical education activities. Users can search by specialty, condition, or skill; filter by delivery mode, credit type, and free participation; sort and paginate; and open provider or authoritative catalogue records.

The product correctly distinguishes provider accreditation from activity-level eligibility and directs users to verify dates, fees, registration, and credit with the provider.

## Critical deployment boundary

The checkout contains hosting links for two other products:

- the ignored Vercel project link serves FundGuide;
- `.openai/hosting.json` points to a private Sites project currently serving Land and Earn.

Neither destination is a CME Atlas deployment target. The safe default is to create a separate CME Atlas project.

## Artifact register

| Artifact | Status |
|---|---|
| [Agent instructions](/Users/carringtonhaykellar/candur/pri/AGENTS.md) | Requires handoff review and deployment identity confirmation |
| [Operational runbook](/Users/carringtonhaykellar/candur/pri/HANDOFF.md) | Complete at `48113a6` |
| [UofC handoff record](handoff-log.md) | Stored |
| [Technical design](technical-design.md) | Evidence-based summary |
| [Production review](production-review.md) | Local product ready; production blocked on isolated destination and controls |

## Immediate next actions

1. Assign product, relationship, and technical owners.
2. Confirm ACCME API usage expectations and product branding.
3. Create a new CME Atlas hosting project before any deployment.
4. Isolate or remove legacy FundGuide runtime code after confirming product ownership.
5. Add runtime/browser tests, upstream resilience, URL validation, observability, and pagination bounds.

