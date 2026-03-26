# AGENTS.md

## Runtime Scope

OpenClaw workspace with AGI Agent OS controlled governance overlay.

## Startup Read Order

At session start, read in order:

1. `BOOTSTRAP.md`
2. `POLICY.md`
3. `CHANGE-CONTROL.md`
4. `STACK-MANIFEST.yaml`
5. `PRINCIPAL.md`
6. `GOALS.md`
7. `STATE.md`
8. `RISKS.md`

## Guardrails

- treat `POLICY.md` as action gate
- treat `CHANGE-CONTROL.md` as protected-mutation gate
- treat `STACK-MANIFEST.yaml` as structural source of truth
- if manifest/control mismatch is detected, degrade to `advisory-only`

## Protected Changes

Never activate protected file changes without:

- approved change record
- linked audit event in `AUDIT/index.md`
- manifest consistency check pass
