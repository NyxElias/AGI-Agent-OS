# Validation Expectations

Date: 2026-03-26  
Scope: `examples/v1.0.0-openclaw-controlled`

This file defines expected validator outcomes for the two fixture directories.

## Target A: `workspace-template/`

Expected result:

- overall: `pass`
- recommended runtime: `load-ok` (or `load-with-warnings` if validator emits non-blocking notices)

Expected conditions:

- `STACK-MANIFEST.yaml` exists and is structurally consistent with controlled profile
- `CHANGE-CONTROL.md` exists with protected-file lifecycle semantics
- `POLICY.md` exists with explicit action gates
- `AUDIT/index.md` is declared append-only and includes event contract
- `MEMORY/index.md` defines typed memory and provenance/retention rules

Expected finding profile:

- no `V3` or `V4`
- no mandatory failure codes from `MF`, `CC`, `AU`, `OCM`, `AG`

## Target B: `workspace-template-invalid/`

Expected result:

- overall: `fail`
- recommended runtime: `advisory-only` or `reject-load` (implementation-dependent)

Intentional invalid conditions:

- protected-file mismatch between `STACK-MANIFEST.yaml` and `CHANGE-CONTROL.md`
- append-only target mismatch (`AUDIT/log.md` declared but `AUDIT/index.md` used)

Expected finding families:

- `MF` (manifest consistency)
- `CC` (change-control consistency)
- `OCM` (controlled-mode contract)

Suggested representative codes:

- `MF003`: manifest profile/structure conflicts with workspace control declarations
- `OCM004`: `CHANGE-CONTROL.md` and manifest protected-file sets diverge
- `AU` family warning/error for append-only target declaration mismatch

Expected severity floor:

- at least one `V3`
- optionally `V4` in hardened mode

## CI Assertion Hints

Minimal assertions for automated regression:

1. `workspace-template/` returns non-failing status.
2. `workspace-template-invalid/` returns failing status.
3. failing target includes at least one finding from `MF` or `OCM`.
4. failing target runtime recommendation is not `load-ok`.
