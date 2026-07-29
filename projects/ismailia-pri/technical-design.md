# P-003 — Technical design

Status: **Implemented MVP / external production evidence outstanding**

Evidence base: prototype worktree at commit `168f897fcb54c48705a3e3564cf9679c7728b352`.

## Application shape

- Vinext with Next 16, React 19, TypeScript, and Vite.
- Cloudflare D1 for structured records and R2 for original documents.
- Drizzle ORM with an implemented schema and migrations.
- API routes for dashboard data, document intake/retrieval, packet export, and operational mutations.
- Workspace identity and allowlists for program-manager and fiscal-reviewer roles.
- Optional AI extraction adapter with local structured-fixture behavior.

## Core domain

- programs, employers of record, placement organizations, contacts, and interns;
- employer reimbursement packets and reimbursement periods;
- purchase orders, amendments, and append-only funding-ledger events;
- versioned MOUs and governing public/private policy sources;
- original documents, normalized fields, source evidence, and confidence;
- wage and business-expense claims;
- validation exceptions, review decisions, and audit history;
- follow-up/reminder drafts and packet exports.

## Key controls represented in the implementation

- original file preservation and SHA-256 duplicate detection;
- documents may support multiple packets without duplicate storage or ledger commitment;
- corrected invoices supersede earlier versions and post traceable deltas;
- Priority 1 exceptions block approval;
- expense eligibility cites IRS, federal/ARC, grant/budget, and effective MOU evidence;
- all external messages remain drafts with no send endpoint;
- approval is an explicit human action;
- program-manager mutations and fiscal-reviewer read access are separated;
- sensitive normalized data has guarded retention/disposition behavior;
- audit events record material access and changes.

## AI boundary

The application may classify documents and extract fields, but uncertain values, conflicts, overrides, approval, and external communication require human review. Private grant rules and signed MOUs cannot be replaced by general public policy sources.

## Runtime and routes

- UI: `/`
- Dashboard data: `/api/dashboard`
- Additional APIs: `/api/documents`, `/api/files`, `/api/export`, `/api/operations`
- `/dashboard` is not an application page and is expected to return `404`.

## Documented verification

The prototype’s July 22 local record reports:

- TypeScript passed;
- ESLint passed;
- production build passed;
- fourteen tests passed;
- multi-file processing, duplicate control, shared evidence, invoice correction, approval blocking, role enforcement, draft generation, original retrieval, ZIP export, and retention guard ordering were exercised;
- only synthetic fixtures were used.

These are prototype-maintainer records. UofC has not rerun build or test commands during this handoff because the user directed that the active development server remain undisturbed.

## Known technical gaps

- representative Baxus historical formats and labeled accuracy evaluation;
- authoritative signed award, budget/amendments, and employer MOU evidence;
- approved tolerances, override authority, and expense interpretations;
- hosted allowlist and role verification;
- backup/restore and disposition rehearsal;
- incident response, data residency, breach notification, and AI-vendor approval;
- project-specific README and operator runbook.
