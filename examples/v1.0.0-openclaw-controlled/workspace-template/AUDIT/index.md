---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: AUDIT
template_version: 2
status: active
language: en
owner: governance
trust_class: D
review_cycle: stable
last_updated: 2026-03-26
last_updated_by: system:bootstrap
change_control: append-only
provenance:
  source: human-authored
  channel: terminal
  authority: governance-system
mutability: append-only
---

# AUDIT/index.md

## Logging Contract

- append new entries only; do not rewrite prior entries
- every protected activation must include `change_id`
- every denial or override must include reason and authority basis

## Event Fields

- `event_id`
- `timestamp`
- `actor`
- `event_type`
- `target`
- `result`
- `authority_basis`
- `change_id` (if applicable)
- `notes`

## Audit Ledger

| event_id | timestamp | actor | event_type | target | result | authority_basis | change_id | notes |
|---|---|---|---|---|---|---|---|---|
| aud-2026-03-26-001 | 2026-03-26T16:05:00+08:00 | human:governance-owner | bootstrap | workspace-template | success | owner-directive | n/a | initialized controlled template pack |
| aud-2026-03-26-002 | 2026-03-26T16:12:00+08:00 | human:governance-owner | approval | POLICY.md | approved | change-control-reviewed | cc-2026-03-26-001 | initial policy ratified |
| aud-2026-03-26-003 | 2026-03-26T16:14:00+08:00 | system:validator | validation | STACK-MANIFEST.yaml | pass | profile-openclaw-controlled | cc-2026-03-26-001 | manifest consistency verified |
