---
spec: agi-agent-os-template-stack
spec_version: 1.0.0
template: MEMORY
template_version: 1
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

# MEMORY/index.md Example

## Memory Types

- events
- semantic
- commitments
- preferences
- incidents

## Retention Rules

- commitments persist until fulfilled or cancelled
- incidents persist for governance review
- low-confidence observations should not become permanent semantic memory without reinforcement

## Provenance Rules

- memory entries should record whether they are human-authored, agent-derived, or imported

## Conflict Handling

- contradictory memory should be marked, not silently merged

## Staleness Handling

- stale preferences or assumptions should be reviewed before operational reuse
