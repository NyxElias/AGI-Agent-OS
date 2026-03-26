# workspace-template-invalid

Intentional invalid fixture for validator regression tests.

Expected failure conditions:

- `STACK-MANIFEST.yaml` lists protected files not aligned with `CHANGE-CONTROL.md`
- append-only target mismatch

Suggested expected finding families:

- `MF`
- `CC`
- `OCM`
