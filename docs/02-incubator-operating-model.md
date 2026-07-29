# Incubator operating model

## Roles

The source material uses three roles: **C = customer, S = student, E = senior engineer/educator**.

### Customer

An initial customer is usually a small business with roughly one to five users and a specific operational bottleneck. The customer contributes workflow knowledge through calls, texts, email, video meetings, examples, and feedback.

Customer responsibility:

- name the problem and show the current workflow;
- identify the people and data affected;
- approve the scope and acceptance criteria;
- test the prototype with real examples;
- name one decision maker and one day-to-day contact.

### Student product owner

The whiteboard hypothesizes that one student may eventually manage 10 or more clients. This is a **target to test**, not a safe starting ratio.

Student responsibility:

- conduct and summarize discovery;
- turn a conversation into a reviewable scope;
- build or adapt the prototype;
- coordinate deployment;
- monitor use and collect feedback;
- triage bugs and communicate status;
- escalate security, data, legal, or reliability issues.

### Senior engineer/educator

A small senior layer supports student teams and owns the shared system.

Senior responsibility:

- maintain curriculum and the UofC basecamp;
- approve architecture, credentials, and access controls;
- own production safety and incident response;
- handle escalated bugs;
- maintain reusable AI harnesses and shared modules;
- coach students without silently taking over their client relationship.

The whiteboard suggests one senior engineer supporting three to five students. This, too, is a capacity hypothesis requiring measurement.

## Client-to-production loop

1. **Qualify** — confirm a real pain, reachable user, narrow workflow, and responsible data profile.
2. **Discover** — observe the current process and capture inputs, outputs, exceptions, and time cost.
3. **Scope** — write a one-page problem statement, non-goals, acceptance criteria, data classification, and owner.
4. **Prototype** — create the smallest testable workflow using synthetic or non-sensitive data.
5. **Client review** — watch the client use it; record confusion and missed cases.
6. **Production review** — senior approval for authentication, credentials, data storage, observability, backup, and rollback.
7. **Deploy** — release to a small user group with a support channel and named owner.
8. **Observe** — monitor failures and whether the tool actually saves time or improves a business outcome.
9. **Support** — triage bugs, communicate status, and document changes.
10. **Generalize** — only after multiple similar clients, extract the shared data model or module.

## Communication-to-code system

The envisioned internal platform converts client communication into structured delivery work:

**Calls, texts, email, and meetings → transcript → proposed scope/change request → human approval → repository issue or code change → test → deployment → client-visible status**

Important control: a transcript must never update a production database or deploy code without an explicit human review step. The system should preserve the original request, the interpreted scope, the approving person, the code change, and the release record.

## Shared technical layer

The strategic brief warns that many custom AI apps can recreate the “spreadsheet nightmare” as disconnected software. UofC should therefore standardize beneath the user interface:

- identity, organizations, and user roles;
- audit logs and client approvals;
- secrets and credential handling;
- event and activity history;
- file and record provenance;
- deployment status and rollback;
- monitoring and client-facing status;
- reusable vertical modules such as inventory, intake, scheduling, CRM, or bookkeeping.

The specific backend technology is not yet decided. OpenEHR appears in the healthcare discussion as a research lead, not an approved foundation for general small-business software.

## Curriculum sequence

The authoritative teaching specification is the [12-week Tactical AI Skills Core Curriculum](curriculum/tactical-ai-skills-core.md). The stages below are its higher-level relationship to client delivery, not a competing syllabus.

| Curriculum weeks | Client-delivery stage |
|---|---|
| 1–4 | apprenticeship in command line, repository systems, collaboration, and responsible AI operation |
| 5–8 | discovery, scope, development harnesses, implementation, data, and retrieval |
| 9–11 | security, authorization, deployment, and operations |
| 12 | capstone release, production evidence, handoff, and improvement |

### Stage 1: tools and mental models

- local files versus cloud services;
- terminal navigation and safe command use;
- Git repositories, commits, pull, push, and collaboration;
- IDE and coding-agent basics;
- asking AI to explain, test, and critique rather than only generate.

### Stage 2: client discovery

- interviewing without leading;
- mapping a workflow;
- writing a problem statement and non-goals;
- estimating value in time, errors, delay, or revenue;
- protecting confidential information.

### Stage 3: prototype delivery

- simple data models and interfaces;
- acceptance criteria;
- testing with realistic examples;
- presenting a prototype and receiving feedback.

### Stage 4: production responsibility

- authentication and permissions;
- credential and secret ownership;
- deployment, observability, backup, and rollback;
- bug triage and incident communication;
- documentation and handoff.

### Stage 5: productization

- comparing workflows across clients;
- separating configuration from reusable code;
- measuring adoption and value;
- pricing, service levels, and referral-driven growth.

## Safety gates

Because students are minors and client data may be sensitive, the program needs written controls before production work:

- guardian consent and student conduct expectations;
- no private one-to-one adult/minor communication outside approved channels;
- an adult supervisor visible on client accounts and communications;
- least-privilege access and no shared credentials;
- no production secrets stored on student laptops or in repositories;
- prohibited or separately supervised data classes, especially health, financial, identity, and payment data;
- client consent for recording or transcription;
- required senior review before any production deployment;
- a documented incident, removal-of-access, and offboarding process.

Healthcare work requires a separate compliance and professional-governance track and should not be used as an early unsupervised student project.

## Capacity ramp

Use evidence, not the whiteboard ratio alone:

| Phase | Suggested load | Exit signal |
|---|---:|---|
| Apprenticeship | 1 student to 1 client | one narrow tool deployed with supervision |
| Supported ownership | 1 student to 2–3 clients | predictable weekly support and clean documentation |
| Portfolio ownership | 1 student to 4–6 similar clients | shared module, low incident rate, measured value |
| Scale test | up to 10 clients | only after support demand and supervision data justify it |

## Core metrics

- time from discovery to first client test;
- percentage of prototypes reaching production;
- weekly active users and repeat use;
- client time saved or delay reduced;
- unresolved bugs by severity and age;
- deployments rolled back;
- student work completed without senior takeover;
- number of clients sharing a reusable module;
- client and student retention;
- security or privacy incidents.
