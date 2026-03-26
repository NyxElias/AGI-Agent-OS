---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: CHANGE-CONTROL
template_version: 2
status: active
language: en
owner: governance
trust_class: A
review_cycle: review-monthly
last_updated: 2026-03-26
last_updated_by: human:governance-owner
change_control: controlled
provenance:
  source: human-authored
  channel: terminal
  authority: direct-owner
control_mode: constitutional
activation_model: reviewed-activation
---

# CHANGE-CONTROL.md

## Scope

This process governs all protected files and all policy-impacting operational changes.

## Protected Files

- `IDENTITY.md`
- `SOUL.md`
- `POLICY.md`
- `CHANGE-CONTROL.md`
- `STACK-MANIFEST.yaml`

## Change Record Requirements

Every protected change must have a unique `change_id` and include:

- proposer
- target files
- rationale and risk
- reviewer/approver
- planned activation time
- rollback snapshot reference
- linked audit event id

## Lifecycle

Allowed transitions:

- `proposed -> reviewed`
- `reviewed -> approved`
- `reviewed -> rejected`
- `approved -> activated`
- `activated -> superseded`
- `activated -> rolled_back`

Forbidden transitions:

- `proposed -> activated`
- `proposed -> approved`
- `reviewed -> activated`
- `rejected -> activated`

## Separation of Duties

- proposer and approver must be different identities when feasible
- self-approval for protected changes requires explicit human override log

## Activation Rules

- protected changes require `approved` state
- activation must write a new audit event in `AUDIT/index.md`
- manifest consistency must be re-validated before activation

## Rollback Rules

- rollback never deletes history
- rollback must create a new audit event and reference previous `change_id`
- emergency rollback may execute before full review but must be reviewed after stabilization
