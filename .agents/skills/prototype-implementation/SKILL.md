---
name: prototype-implementation
description: Build a lightweight, clickable frontend prototype from an approved prototype scope in an existing client repository. Use when an agent must rapidly turn an agreed product concept, user flow, wireframe, or scope into a responsive demonstration using mock data, client-side interactions, clear limitations, and a shareable preview—not a production application.
---

# Prototype Implementation

Implement a clickable frontend demonstration that helps stakeholders understand the proposed product. Optimize for speed, clarity, and a convincing primary flow while preserving an explicit boundary between prototype behavior and production functionality.

## Preconditions

Require:

- an approved prototype scope;
- an existing client repository;
- branding assets when supplied.

Read repository instructions and inspect the current stack before editing. Preserve unrelated work and existing conventions. If the scope is missing or materially ambiguous, resolve the smallest blocking question before building.

## Prototype boundary

Build:

- frontend only;
- responsive layouts;
- client-side routing;
- primary navigation and user flows;
- familiar UI patterns;
- placeholder content and mock interactions;
- local JSON fixtures or typed in-memory objects;
- reusable, readable components.

Do not build:

- backends, server actions, or API routes;
- databases, persistence, ORMs, Supabase, Firebase, or Prisma;
- authentication or authorization;
- external API calls or integrations;
- email, payments, background jobs, or search indexing;
- real file uploads;
- infrastructure not required for the demonstration.

Buttons may simulate behavior locally. Label simulated, unavailable, and non-persistent behavior honestly. Never imply that a prototype protects data, sends messages, processes payments, or performs another real operation.

## Stack selection

Prefer the repository's existing frontend stack. When starting from a compatible minimal repository, prefer:

- React;
- Next.js;
- TypeScript;
- Tailwind CSS.

Use a component library only when it materially accelerates delivery and matches the project:

- shadcn/ui;
- Radix;
- Lucide Icons.

Avoid unnecessary dependencies. Do not replace an established stack merely to match this preference.

## Workflow

### 1. Inspect

- Confirm the active repository, branch, status, and applicable instructions.
- Locate the approved scope, existing UI, scripts, package manager, and branding assets.
- Identify unrelated or uncommitted changes and preserve them.
- Record the available validation and preview commands.

### 2. Translate the scope

Extract:

- intended audience and primary user;
- demonstration goal;
- required screens and routes;
- primary happy-path flow;
- essential states and mock interactions;
- supplied visual constraints;
- explicit non-goals.

Do not expand the product beyond the approved scope. Prefer one complete, understandable flow over many shallow screens.

### 3. Plan the mock model

Define the smallest fixture shape needed for the demonstration. Store it in local JSON or typed TypeScript objects.

Include realistic sample data and the states stakeholders need to see, such as:

- empty;
- populated;
- selected;
- success;
- validation or simulated error.

Do not include real client records, personal information, credentials, or secrets.

### 4. Implement

- Establish navigation and client-side routes.
- Build the primary flow first.
- Use reusable components for repeated patterns.
- Keep state local and non-persistent.
- Make controls visibly respond to user actions.
- Use concise, realistic product copy rather than filler text.
- Keep animation minimal and purposeful.
- Support common desktop and mobile widths.
- Preserve keyboard access, visible focus, semantic controls, readable contrast, and reduced-motion preferences.

### 5. Verify

Run the repository's relevant checks. At minimum:

- type checking when available;
- linting;
- production build;
- existing tests;
- a focused browser walkthrough of every required route and primary interaction;
- responsive and keyboard checks.

Confirm there are no accidental network calls, backend routes, credentials, real persistence, broken links, clipped content, or misleading production claims.

### 6. Document

Create or update the project README with:

- project purpose;
- local setup and run commands;
- technologies used;
- routes and primary flow;
- source of mock data;
- checks performed;
- prototype limitations.

State prominently:

> This is a demonstration prototype. It uses mock data, does not persist changes, and is not a production application.

Add a concise implementation summary describing what works, what is simulated, and what would require production engineering.

### 7. Commit

Use focused commits organized around coherent features when commits are authorized by the repository workflow. Use clear messages. Never include unrelated changes, generated secrets, local configuration, or build caches.

### 8. Share a preview

Create an accessible preview only when deployment is authorized and the destination is unambiguous. Prefer:

- Cloudflare Pages or an approved Sites preview/version;
- Vercel Preview;
- Netlify Preview.

Do not overwrite an existing production deployment, relink a project, or claim production readiness. Record the preview URL, source commit, access level, and known limitations.

## Completion standard

Deliver:

- a working clickable prototype;
- the required routes and primary user flow;
- responsive, accessible UI;
- mock fixtures and simulated interactions;
- passing relevant checks;
- focused Git history when authorized;
- a README and implementation summary;
- a shareable preview when authorized.

The handoff must clearly distinguish implemented demonstration behavior from simulated behavior and future production work.
