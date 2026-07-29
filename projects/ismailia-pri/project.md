# P-003 — Land and Earn Grant Operations Assistant

## Record

| Field | Value |
|---|---|
| Primary stakeholder | Ishmel, Land and Earn program manager |
| Organization | Baxus is named in the PRD; relationship to PRI remains to be confirmed |
| Program | Land and Earn |
| Relationship owner | Carrie |
| Student owner | JL |
| Senior reviewer | Unassigned |
| Stage | Functional MVP / controlled-pilot gates outstanding |
| Prototype worktree | `/Users/carringtonhaykellar/candur/pri-land-and-earn` |
| Branch | `feature/land-and-earn-prd` |
| Handoff commit | `168f897fcb54c48705a3e3564cf9679c7728b352` |
| Local UI | `http://localhost:3001/` while the handed-off development server is available |
| Dashboard API | `/api/dashboard` |

## Product purpose

Land and Earn is a federally funded internship program serving people aged 16–24 across eight rural Promise Zone counties. The MVP helps a program manager assemble and validate employer reimbursement packets containing purchase orders, invoices, timesheets, payroll evidence, business-expense evidence, MOUs, and grant rules.

The product is an exception-management and funding-control assistant. It classifies and extracts documents, reconciles shared facts, maintains an append-only purchase-order ledger, flags missing or conflicting evidence, and drafts recipient-specific follow-up. The human program manager remains the final reviewer and approver.

## MVP boundaries

The product does not recruit participants, calculate payroll, move money, perform grant accounting, submit funder reports, send external email automatically, or make final reimbursement/compliance decisions autonomously.

## Prototype inventory

The worktree contains:

- a Vinext/Next/React application;
- Cloudflare D1 and R2 bindings declared for Sites hosting;
- Drizzle schema and ten migrations;
- dashboard, document, file, export, and operations APIs;
- document classification and extraction logic;
- role-based access and workspace identity helpers;
- fourteen documented automated tests;
- a PRD, completion audit, and local-verification record.

## Artifact register

| Artifact | Status |
|---|---|
| [Operational handoff](handoff-log.md) | Stored July 28, 2026 |
| [Product requirements document](/Users/carringtonhaykellar/candur/pri-land-and-earn/docs/land-and-earn-prd.md) | Draft v0.1 at handed-off commit |
| [Completion audit](/Users/carringtonhaykellar/candur/pri-land-and-earn/docs/completion-audit.md) | Implemented/external-dependency matrix |
| [Local verification](/Users/carringtonhaykellar/candur/pri-land-and-earn/docs/local-verification.md) | Synthetic fixtures only |
| [Prototype README](/Users/carringtonhaykellar/candur/pri-land-and-earn/README.md) | Still uses generic starter title/content |
| [Technical design](technical-design.md) | Evidence-based summary added |
| [Production review](production-review.md) | Conditional controlled-pilot assessment |

## Immediate next actions

1. Confirm whether “PRI” and the transcript name “Ismailia/Ismaila” referred to Ishmel, Baxus, a separate organization, or a transcription error.
2. Assign a senior production reviewer and a Baxus policy/fiscal owner.
3. Load redacted representative documents and create the labeled historical evaluation set.
4. Approve the AI provider and sensitive-data terms before any real youth or payroll records reach a model.
5. Verify hosted allowlists, backup/restore, incident response, data residency, breach notification, and retention/disposition operations.
6. Replace the generic starter README with project-specific setup and operating instructions.
