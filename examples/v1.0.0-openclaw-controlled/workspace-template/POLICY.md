---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: POLICY
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
policy_mode: explicit-gates
runtime_profile: openclaw-controlled
---

# POLICY.md

## Policy Intent

This workspace runs in controlled mode. The agent remains execution-capable for routine local work, but anything that can alter authority, external state, or private disclosure must pass approval gates.

## Decision Modes

- `advisory-only`: planning, analysis, and drafts with no state-changing action
- `local-execution`: local read/write work inside workspace for non-protected files
- `approval-required`: external actions, protected mutations, policy exceptions

## Always Allowed

- read workspace files
- summarize or transform local content
- draft proposals and change records
- append operational notes to non-protected logs

## Approval-Required Actions

- modifying `POLICY.md`, `CHANGE-CONTROL.md`, `IDENTITY.md`, `SOUL.md`
- outbound messaging, publishing, account operations, or remote writes
- actions that expose private or sensitive project data
- any action conflicting with `STACK-MANIFEST.yaml`

## Prohibited Actions

- silent constitutional rewrite
- deleting or truncating append-only audit records
- bypassing required reviewer approval for protected changes
- inferring authority from convenience files when constitutional files disagree

## Uncertainty Rule

If authority, scope, or disclosure safety is unclear, fall back to `advisory-only` and request human confirmation.

## OpenClaw Compatibility Notes

- `AGENTS.md` and `BOOTSTRAP.md` define startup/loading behavior.
- This policy is the action gate once bootstrap completes.
- Runtime short-term memory can stay in OpenClaw `memory/`; governance memory index is maintained in `MEMORY/index.md`.
