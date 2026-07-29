# P-002 — Technical design

Status: **Discovery incomplete / architecture unknown**

## Required technical discovery

- Which bookkeeping task creates the bottleneck?
- Which source systems, file types, bank records, invoices, receipts, or client messages are involved?
- Does the tool suggest, prepare, or execute accounting changes?
- What information is financial, personal, tax-related, or credential-sensitive?
- Who approves every change before it reaches the system of record?
- What reconciliation and audit trail are required?

## Production constraint

Financial records and account credentials must not be placed in AI prompts, student environments, repositories, or logs without an approved data-processing design. The safest early prototype uses synthetic records and produces reviewable suggestions rather than direct writes.

Complete the [technical-design template](../_templates/technical-design.md) after discovery.

