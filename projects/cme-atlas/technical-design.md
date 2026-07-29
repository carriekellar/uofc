# P-005 — Technical design

Status: **Implemented local product / production hardening outstanding**

Evidence base: `/Users/carringtonhaykellar/candur/pri` at `48113a6bab4980a534512132a46330eb7d3e3456`.

## Application shape

- Vinext/Cloudflare and standard Next.js/Vercel build paths;
- Next 16, React 19, TypeScript, Vite, and Node 22;
- client-side search/filter/pagination interface;
- server-side `/api/activities` proxy to the public ACCME activity-search service;
- responsive CSS and social metadata/preview asset.

## Catalogue adapter

The route:

- trims and length-limits query inputs;
- accepts allowlisted delivery modes and credit types;
- requests active activities overlapping today through December 31, 2100;
- caches upstream results for five minutes;
- returns a generic `502` when the upstream service fails;
- does not currently require an API key or local environment variable.

## Current product behavior

- search by specialty, condition, or skill;
- delivery-mode, credit-type, and free-participation filters;
- sorting by ending soon or title;
- pagination in groups of 18;
- current/upcoming status;
- links to provider pages and authoritative CME Passport records.

## Legacy surface in the checkout

The source tree still contains a FundGuide `/api/audit` route, D1 schema/migrations, audit store, `xlsx`, and supporting platform configuration. The audit route lacks authentication, authorization, and rate limiting; its Vercel implementation uses non-durable in-memory storage. It must not be described as production compliance storage.

## Documented verification

- ESLint passed;
- Vinext/Sites build passed;
- Next.js/Vercel build passed;
- two source-level tests passed;
- local page returned HTTP 200;
- a live local ACCME query reported 2,185 matches and returned 18 activities on page 1.

The result count is time-sensitive. UofC did not rerun these commands or disturb the handed-off local server.

## Technical gaps

- no dedicated production destination;
- source-level tests do not exercise route or browser behavior;
- no explicit upstream timeout, retry, or circuit breaker;
- provider-supplied URLs lack an explicit `http:`/`https:` allowlist;
- no production monitoring, latency metrics, or catalogue-health alert;
- unbounded positive page values can create very large upstream skips;
- ACCME API usage and branding expectations require confirmation;
- legacy FundGuide runtime code needs isolation after an explicit ownership decision.

