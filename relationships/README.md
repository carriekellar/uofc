# Relationship CRM

This is a lightweight, human-readable CRM for the people and organizations surrounding UofC. It tracks context and next actions without storing secrets, sensitive records, or minors’ personal contact information.

## Relationship stages

- **Named:** appears in the source material; identity may still need verification.
- **Connected:** a relationship owner can make contact.
- **Discovery:** an active conversation is clarifying fit or needs.
- **Active:** participating as a client, student, mentor, operator, or partner.
- **Future:** aspirational relationship without a confirmed introduction.
- **Paused:** no current action.

## Core team and students

| ID | Person | Role/context | Relationship owner | Stage | Next action | Verification |
|---|---|---|---|---|---|---|
| R-001 | Carrie | Instructor, builder, and current central relationship owner | Carrie | Active | Assign explicit program and production-accountability roles | Confirm preferred public title |
| R-002 | Jun | Student owner for Amy and Richard | Carrie | Active | Import original project artifacts and confirm supervision | Name spelling to confirm |
| R-003 | Lydia | Student owner for Jenny | Carrie | Active | Import bookkeeping prototype and discovery notes | Confirm |
| R-004 | JL | Student owner for PRI project and contributor to Basecamp | Carrie | Active | Verify client identity and recover project scope | Full/preferred name to confirm |
| R-005 | AJ | Student owner for Nancy credentialing | Carrie | Active | Confirm safe research-only starting scope | Full/preferred name to confirm |
| R-006 | Keith | Named owner for IVR/“dial monkey” implementation in strategic notes | Team | Named | Confirm whether this remains active and which venture owns it | Role and scope to confirm |

Student contact details belong in an approved guardian/supervisor system, not this repository.

## Clients and close project relationships

| ID | Person | Organization/domain | Connection/context | Relationship owner | Stage | Next action | Verification |
|---|---|---|---|---|---|---|---|
| R-101 | Amy | Real estate | Initial camp participant/client; referred Richard | Carrie | Active | Recover interview, prototype, and current workflow | Business and preferred name to confirm |
| R-102 | Richard | Real estate | Referral from Amy | Carrie / Jun | Connected | Conduct independent discovery before combining workflows | Full identity to confirm |
| R-103 | Jenny | Bookkeeping; transcript may also associate her with PRI | Initial client for Lydia | Carrie | Active | Clarify organization and exact bookkeeping problem | Affiliation to confirm |
| R-104 | Ishmel | Land and Earn / Baxus | Primary program-manager stakeholder in the prototype PRD; likely related to the earlier PRI transcript reference | Carrie | Active | Confirm preferred name, Baxus/PRI relationship, and contact route | Name appears as Ishmel in PRD |
| R-105 | Nancy | Independent practitioner / midwifery | Credentialing client and proposed clinical pilot | Carrie | Active | Verify professional role, entity, jurisdiction, and approved scope | Required |

## Organization prospects

Named Berea businesses and public contact details remain in the [supplied opportunity matrix](../data/berea-small-business-ai-opportunities.csv). Move an organization into this CRM only after:

1. a relationship owner is assigned;
2. the public contact details are verified;
3. outreach or an introduction occurs;
4. the interaction is logged.

## Interaction log

Add brief factual entries to [`interaction-log.md`](interaction-log.md). Record decisions and next actions, not private conversation. Link project-specific discovery material from the relevant [project record](../projects/README.md).

## CRM rules

- one stable ID per person;
- distinguish a confirmed fact from a hypothesis;
- record how UofC knows the person and who owns the relationship;
- assign one next action and owner;
- verify names and affiliations before outreach;
- do not store passwords, private identifiers, health or financial information;
- do not store minors’ emails, phone numbers, addresses, schedules, or guardian details;
- obtain consent before recording or transcribing;
- move regulated or sensitive records into an approved system with appropriate access controls.
