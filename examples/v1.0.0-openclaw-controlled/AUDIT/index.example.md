---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: AUDIT
template_version: 1
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

# AUDIT/index.md Example

## Audit Scope

- protected changes
- significant outbound actions
- human overrides
- denied actions

## Decision Logging

- Decisions should be recorded with authority basis and timestamp

## Action Logging

- Actions should record actor, target, result, and linked change if applicable

## Override Logging

- Human override should include reason and affected operation

## Deletion Attempt Policy

- Audit records are append-only
- Deletion attempts are themselves audit events
