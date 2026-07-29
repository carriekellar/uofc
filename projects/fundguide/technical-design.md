# P-006 — Technical design

Status: **Recovery evidence only / architecture review not completed**

The current PRI `main` branch is CME Atlas, so it is not an authoritative source for FundGuide. The last known FundGuide snapshot is `58a841f`.

The current checkout retains legacy FundGuide surfaces including `/api/audit`, a D1 schema/migrations, an audit store, `xlsx`, and platform configuration. These remnants do not prove that they exactly match the live FundGuide build.

The handoff specifically warns that:

- the legacy audit route is not protected by authentication, authorization, or rate limiting;
- its Vercel adapter uses in-memory process storage;
- records may disappear across cold starts or deployments and are not reliably shared across instances.

Before writing a full design, recover `58a841f` in an isolated worktree and compare it with the deployed Vercel build and configuration.

