# P-XXX — Technical design

Status: **Draft / not approved**

## System purpose

## Users and permissions

| Role | May view | May change | May approve |
|---|---|---|---|
| Client owner | | | |
| Client user | | | |
| Student owner | | | |
| Senior engineer | | | |

## Architecture

Document the user interface, application services, data store, integrations, hosting, and environments. Link to code and diagrams rather than embedding secrets.

## Data inventory

| Data | Source | Classification | Storage | Retention | Deletion/export owner |
|---|---|---|---|---|---|

## Integrations and credentials

| Service | Purpose | Credential owner | Least-privilege scope | Failure behavior |
|---|---|---|---|---|

## AI behavior

Document model/provider, inputs, outputs, human approval points, evaluation cases, and the safe fallback when the AI is unavailable or wrong.

## Testing

- acceptance tests;
- permission tests;
- invalid and missing input;
- integration failures;
- backup and restore;
- rollback;
- representative AI evaluation cases.

## Operations

Document logs, metrics, alerts, backup, recovery, cost limits, support owner, and expected response time.

## Known limitations

- _To be completed._
