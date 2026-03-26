---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: CHANGE-CONTROL
template_version: 1
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
protected_file_rules:
  class_a: controlled
  class_b: reviewed
  class_c: open
  class_d: append-only
---

# CHANGE-CONTROL.md Example

## Protected Files

- `IDENTITY.md`
- `SOUL.md`
- `POLICY.md`
- `CHANGE-CONTROL.md`

## Proposal Rules

- Human owner may propose protected changes
- Agent may draft protected changes but may not activate them

## Approval Rules

- Protected-file changes require human approval
- Proposer and approver should be distinct when possible

## Activation Rules

- Reviewed or delayed activation only
- Silent self-activation is forbidden

## Rollback Rules

- Every protected change must reference a rollback snapshot
- Every protected change must reference an audit record

## Audit Requirements

- All protected changes write to `AUDIT/index.md`
