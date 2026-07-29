# P-006 — Production review

Decision: **EXISTING LIVE DEPLOYMENT; NOT APPROVED AS AUDITED OR SAFE BASED ON CURRENT HANDOFF EVIDENCE**

## Known facts

- FundGuide is publicly served from the linked Vercel project.
- Current PRI `main` contains CME Atlas and must not be deployed over FundGuide.
- The last known FundGuide source snapshot is `58a841f`.
- Legacy audit behavior described in the handoff is not suitable for durable compliance storage.

## Required review

- [ ] Recover the source in a separate branch/worktree.
- [ ] Reconcile source commit and deployed build.
- [ ] Identify users, data, and system-of-record responsibilities.
- [ ] Review authentication, authorization, rate limiting, and client isolation.
- [ ] Review persistence, backup, recovery, retention, and audit integrity.
- [ ] Verify secrets, third-party services, and environment configuration.
- [ ] Add runtime tests, monitoring, incident ownership, and rollback instructions.
- [ ] Decide whether public availability remains intentional.

Do not replace this deployment with CME Atlas or Land and Earn as a shortcut.

