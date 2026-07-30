---
name: prototype-discovery-client-onboarding
description: Turn a completed client discovery call and supporting materials into a concise, approved frontend prototype scope, documented onboarding status, and implementation-ready handoff. Use immediately after discovery when an agent must summarize evidence, identify gaps without inventing requirements, prepare or complete authorized CRM/repository/workspace tasks, and hand the result to the Prototype Implementation skill—not when writing a production specification.
---

# Prototype Discovery & Client Onboarding

Convert discovery evidence into a high-level clickable-prototype agreement and a traceable internal handoff. Keep the scope narrow, visual, and testable without introducing unnecessary implementation detail.

## Inputs

Use the available:

- discovery transcript;
- meeting notes;
- CRM record;
- company information;
- emails, documents, and linked assets.

Identify the authoritative source for each material fact. Treat automated transcripts as fallible, especially for names, organizations, dates, amounts, and technical terms.

## Safety and authority

Before storing or linking materials:

- confirm recording/transcription consent when applicable;
- follow repository and organization instructions;
- avoid placing secrets, regulated data, private identifiers, or minors' contact information in repositories or tickets;
- preserve source access controls;
- distinguish authorized actions from prepared recommendations;
- never claim that a repository, CRM record, ticket, workspace, or external account was created unless the action succeeded.

Creating repositories, external workspaces, CRM records, tickets, invitations, or messages requires user authority and an unambiguous destination. Prepare the fields and mark the action **Blocked—authorization required** when that authority is absent.

## Workflow

### 1. Inventory the evidence

List every source with:

- title or description;
- date;
- location or link;
- access restrictions;
- reliability concerns.

Do not copy sensitive source contents into a less-protected system merely for convenience.

### 2. Summarize discovery

Extract only what the evidence supports:

- company overview;
- primary users;
- core problem and current workflow;
- desired outcome;
- important workflows;
- nice-to-have features;
- timeline;
- success criteria.

Separate:

- **Confirmed:** stated or demonstrated by the client;
- **Assumption:** a reversible interpretation needed to prepare the scope;
- **Open question:** missing information that could change the prototype;
- **Conflict:** sources that disagree.

Do not silently convert assumptions into requirements.

### 3. Define the prototype scope

Produce a concise scope containing the following sections.

#### Objective

Write one paragraph describing what the prototype will demonstrate, for whom, and what decision or understanding it should enable.

#### Primary user flows

List only the smallest flows needed for the demonstration. Examples:

- landing;
- mock sign-in;
- dashboard;
- create item;
- view item;
- settings.

Label sign-in and other simulated behavior as mock. Do not include a flow merely because it is common in production software.

#### Screens

For each screen, state:

- purpose;
- primary user;
- key information;
- available actions;
- important empty, success, or simulated-error state.

#### Components

Prefer familiar components:

- navigation or sidebar;
- cards;
- tables or lists;
- forms;
- buttons;
- search and filters;
- modals;
- toasts.

Do not invent complex custom interactions unless discovery evidence requires them.

#### Prototype success criteria

Write observable demonstration criteria, such as:

- a stakeholder can complete the primary flow without explanation;
- every required screen is reachable;
- controls visibly simulate the expected result;
- desktop and mobile layouts remain usable;
- limitations are visible and understandable.

Do not use production performance, reliability, or security claims as prototype success criteria.

### 4. Apply the technical boundary

Assume:

- frontend only;
- no backend or API routes;
- no authentication or authorization;
- no database or persistence;
- no external API calls or integrations;
- mock data and local static state only;
- client-side routing;
- responsive layouts.

Do not include a production architecture.

Explicitly list as out of scope:

- authentication and user management;
- payments;
- database and persistence;
- API integrations;
- notifications and email;
- background jobs;
- production security engineering;
- performance optimization;
- production deployment and operations.

Safe handling of discovery materials and credentials remains mandatory even though production security engineering is out of prototype scope.

### 5. Record assumptions and questions

Keep assumptions separate from approved requirements. For each assumption, record:

- the assumption;
- why it was needed;
- impact if wrong;
- who can confirm it.

Prioritize open questions as:

- **Blocking:** changes objective, primary flow, users, or data;
- **Before implementation:** affects screen or interaction design;
- **Later:** useful for production but unnecessary for a clickable prototype.

### 6. Complete or prepare onboarding

Track every item with one status:

- **Completed** — include evidence or link;
- **Prepared** — ready for an authorized person to execute;
- **Blocked** — state the missing authority, information, or access;
- **Not applicable** — explain why.

Checklist:

- GitHub repository exists or creation is prepared;
- approved project workspace exists or is prepared;
- client CRM record is created or updated;
- client contacts are verified;
- meeting notes are stored in the approved location;
- transcript is stored with appropriate access;
- repository is associated with the CRM/project record;
- implementation ticket is created or drafted;
- scope, branding, emails, documents, and prototype assets are linked through an artifact index.

Reuse existing records and repositories when they are authoritative. Do not create duplicates.

### 7. Review with the client or owner

Request approval of:

- objective;
- primary users and flows;
- screens;
- success criteria;
- assumptions;
- explicit non-goals.

Record the approver, date, decision, and requested changes. If approval has not occurred, label the document **Draft—not approved for implementation**.

### 8. Prepare the implementation handoff

Make the handoff self-contained for `$prototype-implementation`. Include:

- client and project identifiers;
- approved scope status and approver;
- objective and audience;
- required routes, screens, and primary flow;
- component and interaction expectations;
- mock-data entities and representative states;
- branding assets and visual constraints;
- acceptance criteria;
- assumptions and unresolved non-blocking questions;
- explicit non-goals and prototype limitations;
- repository, branch, workspace, ticket, and asset links;
- required checks;
- preview access expectations;
- manual actions or blocked onboarding items.

Do not include secrets, private contact details, or raw sensitive records. Link to approved source locations instead.

End with:

```text
Use $prototype-implementation to implement this approved handoff in the linked client repository.
```

## Deliverables

Produce:

1. executive summary;
2. prototype scope;
3. assumptions and source conflicts;
4. prioritized open questions;
5. evidence-backed onboarding checklist;
6. implementation handoff.

Use the repository's existing documentation conventions. Clearly label draft versus approved status and completed versus prepared onboarding work.

## Completion standard

Complete the skill only when:

- discovery claims are traceable to sources;
- missing information and conflicts are explicit;
- scope stays within a clickable frontend prototype;
- onboarding status is truthful and linked to evidence;
- client/owner approval is recorded or the handoff is marked draft;
- the implementation handoff contains everything `$prototype-implementation` needs without requiring access to the raw transcript.
