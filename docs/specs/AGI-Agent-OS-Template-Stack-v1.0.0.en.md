# AGI Agent OS Template Stack v1.0.0

Status: Stable
Version: 1.0.0
Language: English
Date: 2026-03-26

## 1. Intent

`v1.0.0` is the first public baseline release for controlled workspace governance.

## 2. Core Model

The stack defines four operating profiles:

- `native`
- `governed`
- `controlled`
- `longrun`

## 3. Controlled Baseline

A controlled workspace must include:

- `POLICY.md`
- `CHANGE-CONTROL.md`
- `STACK-MANIFEST.yaml`
- `AUDIT/index.md`
- `MEMORY/index.md`

## 4. Validation Behavior

Recommended runtime responses by highest severity:

- `V0`: `load-ok`
- `V1`: `load-with-warnings`
- `V2`: `advisory-only`
- `V3`: block protected workflows
- `V4`: `reject-load`

## 5. Example Pack

This release includes:

- `examples/v1.0.0-openclaw-controlled/`

The pack provides:

- concise examples (`*.example.*`)
- runnable fixture (`workspace-template/`)
- intentional failure fixture (`workspace-template-invalid/`)
- expected validator assertions (`VALIDATION-EXPECTATIONS.md`)

## 6. Modification Record

### 2026-03-26

- Created `v1.0.0` English baseline spec
- Added version-aligned controlled example pack
