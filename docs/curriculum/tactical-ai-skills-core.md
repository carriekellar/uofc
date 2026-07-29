# Tactical AI Skills Core Curriculum

## Program purpose

The Tactical AI Skills Core Curriculum prepares learners to turn an ambiguous human problem into a secure, tested, deployed, and supportable software system. Learners build with AI, but they remain responsible for every decision and outcome.

The program follows a repeatable delivery loop:

> **Problem → Scope → Architecture → Development Harness → Implement → Test → Secure → Deploy → Operate → Improve**

This is not a survey course and it is not prompt practice in isolation. Each week produces evidence inside a working project. By the end, another person must be able to clone, configure, test, deploy, and operate the learner's capstone without relying on undocumented knowledge.

## Audience and prerequisites

The course is designed for beginning or early-intermediate software builders, including teenagers working with real small-business problems.

Learners should be able to:

- use a computer, browser, and text editor;
- create and organize local files;
- write clear short explanations;
- perform basic arithmetic and reason through a sequence of steps;
- ask for help and describe what they tried;
- use an approved password manager and multi-factor authentication.

Prior programming experience is helpful but not required. Learners need access to:

- a computer with a terminal, code editor, Git, and a modern browser;
- a GitHub account protected with multi-factor authentication;
- an approved AI assistant;
- a sandbox or development environment that does not contain client secrets or production data;
- a mentor who can approve access, security-sensitive changes, and production deployments.

## Guiding principles

1. **AI output is a proposal until verified.** Generated claims, plans, commands, code, tests, and security advice require inspection and evidence.
2. **The task drives model choice.** Use the least costly, fastest model that can meet the needed context, reliability, modality, and risk level.
3. **Learners must explain, inspect, and repair AI-assisted work.** Shipping code that a learner cannot reason about is not completion.
4. **Destructive operations require recovery paths.** Confirm the target, preview the effect, back up material data, and know how to restore it.
5. **Tests are executable requirements.** A passing test is useful evidence, not proof that the entire system is correct or safe.
6. **Documentation is part of the system.** Setup, decisions, operations, and recovery instructions must evolve with the software.
7. **Secrets never go in prompts or repositories.** Use approved secret stores, redacted examples, and least-privilege credentials.
8. **Authentication does not replace authorization.** Knowing who someone is does not establish what they may do.
9. **Deployed systems require owners, logs, and rollback.** A release without accountable operation is an unfinished prototype.
10. **Human impact sets the standard of care.** Privacy, accessibility, safety, and responsible handling take precedence over speed.

## Four kinds of model

Learners must use the word “model” precisely:

| Model type | Meaning | Example | Primary test |
|---|---|---|---|
| Mental model | A person's simplified explanation of how something works | “A Git commit is a recoverable snapshot of selected changes.” | Does it predict behavior accurately enough to guide action? |
| Domain model | The concepts, rules, and relationships in the problem space | A booking has a client, service, time, status, and cancellation policy. | Does it match the language and rules used by real users? |
| Data model | The structures used to persist and relate information | `customers`, `appointments`, and a customer foreign key | Does it preserve integrity and support required queries and retention? |
| AI model | A trained computational system used to generate or classify content | A coding model used to propose a database migration | Is it appropriate for the task, and has its output been verified? |

Confusing these categories causes avoidable errors. An AI model can suggest a domain model, but users must validate the domain. A data model encodes only part of a domain. A mental model helps a learner reason, but it is not the system itself.

## Model-routing matrix

Routing is a judgment process, not a brand leaderboard. Reassess when the task involves sensitive data, irreversible changes, weak evidence, or high consequence.

| Task | Preferred capability | Optimize for | Required context and tools | Verification and escalation |
|---|---|---|---|---|
| Brainstorming | Fast chat/reasoning model | breadth, speed, low cost | problem statement, constraints, audience | Treat ideas as options; cluster and rank them with human criteria. |
| Research | Search-enabled reasoning model | source quality, recency, synthesis | explicit questions, dates, primary-source access | Open cited sources, compare dates, and distinguish fact from inference. |
| Scoping | Strong reasoning model | constraint handling, completeness | discovery notes, users, boundaries, risks | Review scope with users; convert claims into acceptance criteria. |
| Architecture | High-reliability reasoning/coding model | tradeoffs, long context, consistency | requirements, domain/data models, operational constraints | Record alternatives; conduct human architecture and threat review. |
| Coding | Coding model with repository tools | local correctness, edit precision | relevant files, conventions, interfaces, tests | Inspect the diff; run focused and full checks; explain the change. |
| Debugging | Reasoning/coding model with logs and test tools | causal diagnosis, iteration speed | reproducible failure, recent changes, sanitized logs | Reproduce first, test the hypothesis, and add a regression test. |
| UI exploration | Multimodal model | visual reasoning, rapid variation, accessibility | screenshots, design constraints, real content | Test keyboard, contrast, responsiveness, and user tasks in the browser. |
| Extraction | Fast model or deterministic parser | consistency, volume, low cost | schema, examples, source documents | Sample against originals; validate types, required fields, and uncertainty. |
| Security review | High-reliability reasoning model plus scanners | adversarial coverage, precision | data flows, dependencies, auth rules, threat model | Never rely on one model; use checklists, tooling, and qualified human review. |
| Repetitive operations | Small model or deterministic automation | predictability, cost, auditability | strict inputs/outputs, permissions, stop conditions | Prefer scripts for deterministic work; use dry runs, logs, and bounded retries. |

Do not use AI when a deterministic command is simpler, when necessary consent is missing, when data cannot be shared safely, when an accountable expert must make the decision, or when the learner cannot verify the result.

## Learning architecture

Each week combines four modes:

1. **Briefing:** concepts, demonstrations, risks, and vocabulary.
2. **Lab:** guided practice with a visible artifact.
3. **Project application:** the same skill applied to the capstone.
4. **Review:** learner explanation, evidence inspection, and repair.

Every lab should leave durable evidence such as a command transcript, Markdown document, issue, pull request, test, migration, threat model, deployment record, or runbook update. Sensitive values and client data must be redacted or replaced with fixtures.

## Twelve-week sequence

### Week 1 — Command-line fluency

**Focus:** Work safely and deliberately in a shell.

**Core concepts**

- shells, prompts, commands, flags, arguments, help, and manual pages;
- absolute and relative paths, the working directory, and home/project boundaries;
- creating, moving, copying, inspecting, and removing files and directories;
- hidden files, file extensions, permissions, and quoted paths;
- pipes, standard input/output/error, redirection, and command composition;
- environment variables and process-scoped configuration;
- finding files and content with `rg`, `rg --files`, and other search tools;
- reading logs, interpreting exit codes, and distinguishing success from silence;
- safe deletion: exact targets, previews, backups, trash, and recovery.

**Measurable outcomes**

By the end of the week, the learner can:

- navigate an unfamiliar project without a graphical file explorer;
- find every reference to a term while excluding generated directories;
- combine commands with a pipe and redirect output intentionally;
- set and inspect a non-secret environment variable;
- use an exit code and log evidence to explain whether a command succeeded;
- describe and demonstrate a recovery path before deleting or overwriting data.

**Lab**

Create a sandbox directory containing nested, hidden, temporary, and log files. Use commands to inventory it, find a known error in the logs, transform selected output, and save a report. Move a file to a recoverable location, restore it, and document the commands and exit codes in `labs/week-01-cli.md`.

**Evidence:** command transcript, recovered file, search result, and a short safety checklist.

### Week 2 — Directory and Markdown systems

**Focus:** Make a repository navigable to humans and tools.

**Core concepts**

- project conventions, purposeful names, predictable nesting, and shallow structures;
- Markdown headings, paragraphs, lists, code fences, tables, links, images, and diagrams;
- README and index files as navigation and contracts;
- relative links, anchors, file explorers, previewers, and rendered-output checks;
- source files versus generated artifacts, caches, exports, build output, and temporary files;
- co-locating documentation with the decisions or components it explains.

**Measurable outcomes**

The learner can:

- design a directory tree that separates source, tests, documentation, fixtures, and generated output;
- create a useful README that explains purpose, setup, use, verification, and ownership;
- write valid Markdown with working relative links, a table, and a simple diagram;
- identify which files should be versioned, ignored, regenerated, or deleted;
- locate information using both a file explorer and command-line search.

**Lab**

Turn the week-one sandbox into a small documented project. Add a root README, `docs/` index, source/generated boundary, naming rules, and a Mermaid flow showing how an input becomes an output. Preview the rendered Markdown and repair all broken links.

**Evidence:** documented directory tree, link check, and a source/generated classification table.

### Week 3 — Git and GitHub collaboration

**Focus:** Create an auditable, recoverable history and collaborate through review.

**Core concepts**

- repositories, working tree, staging area, commits, diffs, and history;
- focused commits and meaningful commit messages;
- branches, merges, pull requests, review, and protected main branches;
- merge conflicts as competing changes requiring judgment;
- issues, labels, releases, tags, and change summaries;
- `.gitignore` and the difference between untracked, ignored, and removed files;
- safe recovery with restore, revert, reflog awareness, and backup branches;
- GitHub Actions basics: triggers, jobs, checks, logs, and secrets.

**Measurable outcomes**

The learner can:

- explain the state of a file from working change through merged commit;
- stage only intended lines/files and create a focused commit;
- open a branch and pull request linked to an issue;
- review a diff and give specific, respectful, actionable feedback;
- resolve a small merge conflict without discarding either author's intent;
- revert a faulty change and identify the recovery record;
- interpret a failed continuous-integration check.

**Lab**

In pairs, create issues for two documentation changes, implement them on separate branches, review both pull requests, deliberately introduce and resolve a conflict, tag a release, and revert a seeded defect. Add a minimal GitHub Actions workflow that validates Markdown or runs a small test.

**Evidence:** issue, branch history, reviewed pull requests, resolved conflict, tag, revert, and CI log.

### Week 4 — Tactical AI operation

**Focus:** Direct AI systems effectively while retaining human judgment.

**Core concepts**

- chat, reasoning, coding, and multimodal model strengths and limits;
- selection by task, cost, speed, context window, tool access, and reliability;
- task briefs with goal, context, constraints, acceptance criteria, and allowed actions;
- context management: relevant files, examples, source authority, and state summaries;
- tools and agent loops: observe, plan, act, inspect, verify, and stop;
- hallucination and uncertainty management;
- prompt injection, data exposure, excessive permissions, and unsafe tool actions;
- situations where AI is unnecessary, inappropriate, or impossible to verify.

**Measurable outcomes**

The learner can:

- route ten common tasks using the model-routing matrix and defend each choice;
- write a task brief that another person or agent can execute;
- reduce an oversized context to the minimum authoritative material;
- identify unsupported claims and verify them against primary evidence;
- inspect an AI-generated diff, explain it, and repair a seeded error;
- stop an agent loop when permissions, evidence, or recovery is inadequate.

**Lab**

Give two different model classes the same bounded task. Record time, cost proxy, quality, unsupported claims, and repair effort. Then use an AI coding assistant to propose a small change, inspect every changed line, run verification, and write a decision note explaining what was accepted or rejected.

**Evidence:** routing decision, task brief, comparison table, verified diff, and reflection.

### Week 5 — Scope and technical planning

**Focus:** Turn an ambiguous request into a testable delivery agreement.

**Core concepts**

- problem, affected users, current workflow, desired outcome, and baseline;
- in-scope and out-of-scope boundaries;
- user stories and functional requirements;
- nonfunctional requirements: security, privacy, accessibility, performance, reliability, and maintainability;
- domain model, data model, system context, architecture, and dependencies;
- assumptions, constraints, risks, milestones, and decision records;
- acceptance criteria and definition of done.

**Measurable outcomes**

The learner can:

- separate a proposed feature from the underlying user problem;
- identify primary users, owners, affected non-users, and measurable outcomes;
- write testable functional and nonfunctional requirements;
- define explicit exclusions that protect time and safety;
- diagram a system boundary, dependencies, trust boundaries, and major data flows;
- produce acceptance criteria, milestones, risks, and a definition of done.

**Lab**

Interview a stakeholder or use an approved scenario. Produce a one-page scope, user stories, requirements, a domain glossary, initial data model, context/architecture diagram, risk register, milestones, and acceptance checklist. Conduct a scope review in which a peer challenges assumptions and exclusions.

**Evidence:** approved scope and architecture packet with resolved review notes.

### Week 6 — Development harnesses

**Focus:** Build a fast, reproducible feedback system before feature volume grows.

**Core concepts**

- reproducible local setup and pinned dependencies;
- task scripts for setup, development, testing, building, and cleanup;
- unit, integration, and end-to-end tests;
- fixtures, factories, seed data, and isolated test data;
- formatting, linting, type checking, and pre-commit checks;
- continuous integration and failure visibility;
- sandboxes, least-privilege development credentials, and production separation;
- `AGENTS.md`, README, and contributor instructions;
- agent feedback loops that run checks, inspect output, and stop on failure.

**Measurable outcomes**

The learner can:

- set up the project from a clean clone using only documented instructions;
- run one command for each major verification layer;
- create deterministic fixtures that contain no private production data;
- distinguish unit, integration, and end-to-end coverage;
- configure automated formatting, linting, type checking, tests, and CI;
- give an AI coding agent exact project commands and observable stop conditions.

**Lab**

Bootstrap the capstone repository. Add version requirements, dependency locks, example environment configuration, setup/dev/test scripts, fixtures or seed data, formatter, linter, type checker where applicable, pre-commit checks, CI, contributor guidance, and scoped agent instructions. Swap repositories with a peer and repair every undocumented setup step.

**Evidence:** successful clean-clone setup, CI run, test output, and peer setup report.

### Week 7 — Full-stack development

**Focus:** Implement a thin, accessible end-to-end feature.

**Core concepts**

- frontend and backend responsibilities and shared contracts;
- HTTP methods, status codes, headers, request/response flow, and APIs;
- JSON structures, schemas, input validation, and error handling;
- third-party APIs, timeouts, retries, rate limits, and failure isolation;
- background jobs and idempotency;
- configuration across environments;
- responsive interfaces, semantic HTML, keyboard access, labels, focus, contrast, and understandable errors;
- evaluating tools and frameworks by project needs, maintenance, security, team fit, and exit cost.

**Measurable outcomes**

The learner can:

- trace a user action from interface through API, business logic, storage, and response;
- implement and document a validated JSON endpoint;
- return useful errors without exposing internals or sensitive data;
- handle a third-party timeout or failure safely;
- build a keyboard-operable responsive interface;
- justify a tool choice against at least two viable alternatives.

**Lab**

Build one vertical slice of the capstone: accessible input, client validation, server validation, persisted result, success/error states, and an automated test at each relevant boundary. Add a mocked third-party API or background job with explicit timeout, retry, and duplicate-processing behavior.

**Evidence:** working vertical slice, API contract, accessibility check, failure test, and tool decision record.

### Week 8 — Databases and retrieval

**Focus:** Store, query, migrate, retain, and recover data responsibly.

**Core concepts**

- relational tables, rows, columns, primary/foreign keys, cardinality, and relationships;
- normalization and intentional denormalization;
- SQL selection, filtering, aggregation, joins, and parameterization;
- indexes and query-plan tradeoffs;
- transactions, consistency, concurrency, and rollback;
- migrations as reviewed, ordered, reversible production changes;
- local versus hosted databases and safe admin tools;
- backup, restore, integrity checks, and recovery objectives;
- vector databases, embeddings, chunking, retrieval, ranking, and evaluation;
- data classification, retention, export, deletion, and legal/contractual constraints.

**Measurable outcomes**

The learner can:

- translate a validated domain model into tables, keys, constraints, and relationships;
- write a parameterized join query and explain its result;
- choose an index based on an observed query pattern;
- use a transaction for a multi-step integrity requirement;
- create, test, and roll back a migration;
- restore a backup into a non-production environment and verify it;
- explain when vector retrieval is useful and how to evaluate groundedness;
- implement a documented retention and deletion path.

**Lab**

Extend the capstone with a relational schema, constraints, migration, seed data, joined query, and transaction. Measure a query before and after a justified index. Create and restore a backup. If retrieval is relevant, build a small evaluated corpus; otherwise write a decision explaining why conventional search is sufficient.

**Evidence:** schema diagram, migration, query/test results, restoration record, and retention decision.

### Week 9 — Security fundamentals

**Focus:** Reduce risk systematically across design, code, dependencies, and operations.

**Core concepts**

- assets, actors, entry points, trust boundaries, threats, controls, and residual risk;
- least privilege and separation of duties;
- secrets generation, storage, rotation, revocation, and redaction;
- server-side validation, output encoding, and safe file handling;
- injection, cross-site scripting, cross-site request forgery, and insecure direct object references;
- dependency provenance, lockfiles, vulnerability scanning, updates, and supply-chain risk;
- encryption in transit and at rest;
- safe logs that support investigation without exposing secrets or sensitive data;
- secure defaults, review checklists, disclosure, and responsible vulnerability handling.

**Measurable outcomes**

The learner can:

- create a threat model from the capstone architecture and prioritize risks;
- locate and remove a deliberately exposed secret, then rotate the credential;
- prevent a seeded injection or XSS defect and add a regression test;
- identify vulnerable or unnecessary dependencies and document remediation;
- design logs that answer operational questions without leaking protected values;
- follow a responsible escalation and vulnerability-handling process.

**Lab**

Threat-model the capstone using its data-flow diagram. Complete a security review checklist, scan dependencies, test key inputs, inspect logs, and remediate at least two seeded weaknesses. Record risk owner, mitigation, evidence, and residual risk; do not publish exploit details for a live system.

**Evidence:** threat model, security review, remediation diffs/tests, scan record, and risk register.

### Week 10 — Authentication, authorization, and two-factor authentication

**Focus:** Establish identity and enforce permission at every protected action.

**Core concepts**

- identity, authentication, authorization, and accounting/audit;
- password storage using established adaptive password-hashing libraries;
- sessions, secure cookies, tokens, expiration, rotation, and revocation;
- OAuth 2.0 and OpenID Connect roles and flows;
- roles, permissions, ownership rules, policy checks, and deny-by-default design;
- email/phone verification, account recovery, and identity-change safeguards;
- TOTP, passkeys, recovery codes, enrollment, step-up authentication, and reset;
- rate limiting, credential stuffing defenses, lockout tradeoffs, and abuse monitoring;
- privileged/admin access and auditable elevation;
- tenant boundaries and systematic multitenant isolation tests.

**Measurable outcomes**

The learner can:

- explain authentication versus authorization using a concrete capstone action;
- implement or configure a trusted identity system without inventing cryptography;
- enforce server-side authorization on every protected object/action;
- configure secure session or token lifecycle behavior;
- enroll and verify a second factor or passkey and protect recovery codes;
- test rate limits, account recovery, admin access, and cross-tenant denial;
- revoke access and demonstrate that old sessions or credentials stop working.

**Lab**

Add production-appropriate authentication using a vetted library or provider. Implement a permission matrix, server-side policy checks, secure sessions, a second factor (TOTP or passkey), recovery codes, throttling, audit events, and admin safeguards. Attempt horizontal, vertical, and cross-tenant access with automated negative tests.

**Evidence:** identity-flow diagram, permission matrix, auth configuration, negative tests, recovery/revocation demonstration, and audit sample.

### Week 11 — Deployment and operations

**Focus:** Release safely and keep the system healthy, affordable, and recoverable.

**Core concepts**

- development, staging, and production separation;
- build artifacts, containers, images, registries, and provenance;
- hosting and cloud-service selection;
- environment configuration and managed secrets;
- DNS, TLS/HTTPS, certificates, and secure transport;
- deployment migrations, compatibility, and sequencing;
- continuous delivery/deployment with approvals and protected environments;
- health checks, structured logs, metrics, alerts, traces, and ownership;
- rollback, feature flags, incident response, and post-incident learning;
- budgets, quotas, cost alerts, and resource cleanup;
- backups, restoration drills, recovery time, recovery point, and disaster recovery.

**Measurable outcomes**

The learner can:

- produce the same versioned artifact for staging and production;
- configure environments without committing secrets;
- deploy a migration with an explicit compatibility and rollback plan;
- configure HTTPS, health checks, actionable logs, monitoring, and ownership;
- perform and document a rollback;
- set a cost budget/alert and identify the largest cost drivers;
- restore data and service in a timed recovery exercise.

**Lab**

Deploy the capstone to staging, then production through an approved CI/CD path. Configure domains/HTTPS as applicable, health checks, structured logs, an alert, secret injection, migration execution, backup schedule, cost control, and named ownership. Induce a safe staging failure, roll back, restore a backup, and update the runbook with measured recovery results.

**Evidence:** deployment record, artifact/version reference, health evidence, alert, rollback log, restoration drill, cost control, and runbook.

### Week 12 — Capstone release, handoff, and improvement

**Focus:** Demonstrate an end-to-end production system and transfer operational knowledge.

**Required capstone package**

- approved problem statement, users, scope, exclusions, outcomes, and acceptance criteria;
- domain/data models, architecture diagram, decisions, dependencies, and threat model;
- readable Git history with issues, branches, reviews, tags, and release notes;
- reproducible development harness, fixtures, automated checks, and passing CI;
- tested frontend/backend behavior, validation, errors, and accessibility;
- database schema, migrations, backup, restoration evidence, retention, and deletion;
- authentication, authorization, 2FA or passkey support, recovery, and abuse controls;
- secure production deployment with environment separation and managed secrets;
- health checks, logs, monitoring, cost controls, owner, rollback, and backups;
- user documentation, operator runbook, known limitations, and support path;
- live demonstration and retrospective grounded in evidence.

**Measurable outcomes**

The learner can:

- demonstrate each acceptance criterion using a released version;
- explain the architecture, trust boundaries, data lifecycle, and identity controls;
- trace a change from issue through reviewed commit, test, deployment, and monitoring;
- diagnose a seeded operational problem using documented logs and procedures;
- hand the project to a peer who can configure, test, deploy, and operate it;
- identify what to keep, change, stop, and investigate next.

**Lab: capstone verification and handoff**

A peer who has not worked on the project follows only the repository documentation to:

1. clone the repository;
2. configure a safe environment;
3. run the application and all required tests;
4. deploy the version to an approved environment;
5. verify health, logs, monitoring, and backups;
6. perform one routine operation and one rollback or recovery exercise.

The learner repairs documentation or automation gaps, delivers a ten-minute demo, answers architecture/security/operations questions, and publishes a retrospective with prioritized improvements.

**Evidence:** completed handoff checklist, peer sign-off, release, demo, runbook exercise, and retrospective.

## Assessment

Assessment rewards demonstrated capability and durable evidence, not code volume or confident presentation.

| Component | Weight | Evidence |
|---|---:|---|
| Command-line exercises | 20% | safe navigation, search, composition, logs/exit codes, environment use, and recovery |
| GitHub collaboration | 15% | issues, focused history, branches, pull requests, reviews, conflict resolution, release, and safe revert |
| Scope and architecture | 15% | validated problem/outcomes, boundaries, requirements, models, decisions, milestones, risks, and acceptance criteria |
| Security and identity | 15% | threat model, remediation, secrets handling, authorization, 2FA/recovery, isolation, logging, and review evidence |
| Development harness and testing | 15% | clean setup, scripts, fixtures, formatting/lint/type checks, layered tests, contributor/agent guidance, and CI |
| Capstone | 20% | secure production release, handoff, operations, documentation, demo, and retrospective |
| **Total** | **100%** | |

### Shared performance rubric

Each component is scored on a four-level scale.

| Level | Description |
|---|---|
| 4 — Production-capable | Work is correct, reproducible, secure for its stated context, clearly explained, independently verified, and usable by another person. Tradeoffs and residual risks are explicit. |
| 3 — Competent | Required work functions and is documented with meaningful verification. Minor gaps do not block safe use or handoff. |
| 2 — Developing | The main idea is present, but correctness, coverage, explanation, security, or reproducibility has material gaps. Substantial guidance is still required. |
| 1 — Insufficient evidence | Work is missing, cannot be reproduced, is unsafe, or depends on AI output the learner cannot explain and repair. |

For each weighted component, instructors score these dimensions:

- **Correctness and completeness:** Does it satisfy its stated requirements?
- **Verification:** Is there relevant, repeatable evidence rather than assertion?
- **Safety and recovery:** Are permissions, data, destructive actions, failure modes, and recovery handled?
- **Clarity and handoff:** Can another person understand and use the work?
- **Learner ownership:** Can the learner explain decisions, inspect details, and repair failures?

A serious security, privacy, authorization, or recovery failure cannot earn “Production-capable,” even if the feature works.

## Completion criteria

A learner completes the core curriculum when all of the following are true:

- earns at least 70% overall;
- earns at least “Competent” (level 3) for security and identity;
- earns at least “Competent” (level 3) for the capstone;
- completes all required safety, recovery, and peer-handoff exercises;
- has no unresolved critical security issue or undocumented production secret;
- demonstrates that AI-assisted work can be explained, inspected, tested, and repaired;
- meets the operational handoff standard below.

> **Operational handoff standard:** Another person, using only version-controlled documentation and approved credentials, can clone, configure, test, deploy, and operate the capstone.

“Operate” includes identifying the owner and deployed version, checking health and logs, responding to a routine alert, accessing backup/restore instructions, and following a rollback or recovery procedure.

## Instructor and mentor review gates

Mentor approval is required before:

- using real client or personal data;
- connecting a third-party service with write access;
- adding authentication or changing permission rules;
- exposing an application to the public internet;
- running a production migration;
- rotating or revoking shared credentials;
- performing a destructive operation on production data;
- declaring a project ready for handoff or live client use.

Review is not a substitute for learner understanding. The learner should lead the explanation, show the evidence, name uncertainty, and make the repair.

## Recommended repository evidence

A capstone repository should make the following easy to locate:

```text
README.md
AGENTS.md                    # if AI agents are used
docs/
  scope.md
  architecture.md
  threat-model.md
  decisions/
  user-guide.md
  runbook.md
src/
tests/
fixtures/                    # synthetic or approved test data
migrations/
.env.example                 # names and safe examples, never secrets
.gitignore
```

The exact structure may vary by framework. What matters is that source, generated output, private configuration, test data, decisions, and operating instructions have clear and enforceable boundaries.
