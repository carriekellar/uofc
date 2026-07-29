# Project portfolio

This section is the operating index for UofC client work. It answers four questions for every project:

1. What business problem are we trying to solve?
2. Who owns the relationship and the build?
3. Which product and technical artifacts exist?
4. Has the project passed production review?

## Status language

- **Source-mentioned:** the project appears in supplied notes or transcripts.
- **Discovery:** the workflow and success criteria are being verified.
- **Prototype:** a testable version exists, but it is not approved for production.
- **Production review:** security, privacy, reliability, ownership, and support are being evaluated.
- **Live:** approved users are relying on the tool in a real workflow.
- **Paused/closed:** work has stopped, with access and data disposition documented.

“A prototype exists” does not mean it is present in this repository or ready for production.

## Portfolio

| ID | Project | Client/domain | Student owner | Current evidence | Project record | Technical document | Production review |
|---|---|---|---|---|---|---|---|
| P-001 | Real-estate workflow tools | Amy and referral Richard | Jun | Existing prototypes are mentioned; files not supplied | [Record](amy-richard-real-estate/project.md) | [Technical](amy-richard-real-estate/technical-design.md) | [Review](amy-richard-real-estate/production-review.md) |
| P-002 | Bookkeeping workflow tool | Jenny | Lydia | Existing prototype is mentioned; files not supplied | [Record](jenny-bookkeeping/project.md) | [Technical](jenny-bookkeeping/technical-design.md) | [Review](jenny-bookkeeping/production-review.md) |
| P-003 | Land and Earn Grant Operations Assistant | Ishmel / Baxus; PRI relationship to confirm | JL | Clean prototype handoff at commit `168f897`; synthetic-data verification documented | [Record](ismailia-pri/project.md) | [Technical](ismailia-pri/technical-design.md) | [Review](ismailia-pri/production-review.md) |
| P-004 | Independent-practitioner credentialing | Nancy | AJ | Credentialing project is described; clinical venture remains separately governed | [Record](nancy-credentialing/project.md) | [Technical](nancy-credentialing/technical-design.md) | [Review](nancy-credentialing/production-review.md) |

## Internal platform

| ID | Project | Purpose | Record |
|---|---|---|---|
| I-001 | UofC Basecamp | curriculum, client context, communication-to-scope workflow, project oversight, and shared production controls | [Record](uofc-basecamp.md) |

## Prospect pipeline

The supplied Berea matrix contains five opportunity categories that have not yet been confirmed as client projects. They remain in [the Berea opportunity map](../docs/04-berea-opportunity-map.md) and [source CSV](../data/berea-small-business-ai-opportunities.csv) until discovery produces a named client, agreed scope, and project owner.

## Required artifacts for every client

| Artifact | Purpose | Required before |
|---|---|---|
| Project record | relationship owner, problem, outcomes, scope, and status | work begins |
| Discovery evidence | workflow notes, examples, baseline, users, and constraints | prototype |
| Technical design | architecture, data, integrations, access, testing, and operations | production review |
| Acceptance checklist | observable client-approved outcomes | production review |
| Production review | security, privacy, reliability, rollback, ownership, and support decision | launch |
| Change log | approved changes and releases | first production change |
| Closure record | export/retention, credential revocation, and handoff | pause or closure |

## Adding a project

Copy the three files under [`_templates/`](./_templates/), assign the next project ID, add the project to this index, and add every person involved to the [relationship CRM](../relationships/README.md). Never place passwords, API keys, private health information, financial records, or minors’ personal contact information in these documents.
