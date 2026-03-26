---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: MEMORY
template_version: 2
status: active
language: en
owner: system
trust_class: C
review_cycle: review-weekly
last_updated: 2026-03-26
last_updated_by: human:system-owner
change_control: reviewed
provenance:
  source: human-authored
  channel: terminal
  authority: delegated-owner
memory_model: typed
---

# MEMORY/index.md

## Memory Classes

- `commitments`: obligations that must persist until closure
- `decisions`: approved governance decisions with authority reference
- `preferences`: operator preferences with expiry/review date
- `incidents`: safety or policy incidents for retrospective review
- `facts`: stable contextual facts with source attribution

## Entry Contract

Each new memory entry should include:

- `memory_id`
- `class`
- `content`
- `source`
- `confidence`
- `created_at`
- `review_at`
- `status`

## Governance Rules

- low-confidence facts cannot become durable defaults without reinforcement
- conflicting memories must both remain visible until reviewed
- private/sensitive content requires explicit retention reason
- stale preferences should not drive actions before revalidation

## Active Memory Register

| memory_id | class | content | source | confidence | created_at | review_at | status |
|---|---|---|---|---|---|---|---|
| mem-2026-03-26-001 | decisions | controlled profile enabled for this workspace | human:governance-owner | high | 2026-03-26T16:06:00+08:00 | 2026-04-26 | active |
| mem-2026-03-26-002 | commitments | protected-file changes require reviewed activation | CHANGE-CONTROL.md | high | 2026-03-26T16:08:00+08:00 | 2026-04-02 | active |
| mem-2026-03-26-003 | preferences | default uncertain actions to advisory-only mode | POLICY.md | high | 2026-03-26T16:10:00+08:00 | 2026-04-09 | active |
