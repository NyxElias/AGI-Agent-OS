# BOOTSTRAP.md

## Profile

- `profile`: `openclaw-controlled`
- `mode`: `controlled-governance`

## Required Core Files

- `POLICY.md`
- `CHANGE-CONTROL.md`
- `STACK-MANIFEST.yaml`
- `AUDIT/index.md`
- `MEMORY/index.md`

## Load Procedure

1. confirm all required core files exist
2. load policy and change-control gates
3. validate manifest consistency
4. if validation passes, enter normal controlled runtime
5. if validation fails, fall back to `advisory-only`

## Bootstrap Failure Behavior

- missing `POLICY.md` or `CHANGE-CONTROL.md`: block protected workflows
- missing `STACK-MANIFEST.yaml`: advisory-only
- missing `AUDIT/index.md`: advisory-only with audit finding
- missing `MEMORY/index.md`: advisory-only with memory finding
