# P-005 — Production review

Decision: **LOCALLY VERIFIED; NOT APPROVED FOR PRODUCTION UNTIL A DEDICATED DESTINATION AND HARDENING PLAN ARE APPROVED**

## Positive evidence

- [x] Product purpose and scope are documented.
- [x] Both supported production build paths pass.
- [x] Lint and current tests pass.
- [x] A live ACCME request returned usable catalogue data.
- [x] The UI preserves accreditation and provider-verification language.
- [x] The upstream adapter validates several input dimensions and returns a generic failure response.
- [x] No production deployment was changed during handoff.

## Production blockers

- [ ] Create and verify a new CME Atlas hosting project.
- [ ] Confirm ACCME API terms, attribution, branding, and sustainable request patterns.
- [ ] Add runtime route tests and browser task coverage.
- [ ] Add upstream timeout/resilience behavior.
- [ ] Restrict outbound provider links to approved protocols.
- [ ] Bound deep pagination.
- [ ] Add production observability and an accountable responder.
- [ ] Remove or isolate the unprotected legacy `/api/audit` surface.
- [ ] Document deployment, rollback, incident, and ownership procedures for the chosen platform.

## Deployment prohibition

Do not run a production deployment from the current checkout until the user explicitly names **CME Atlas** and its destination. The existing Vercel link is FundGuide, and the existing Sites project is Land and Earn.

