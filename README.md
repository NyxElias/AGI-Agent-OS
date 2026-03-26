# AGI Agent OS

Governance-first template stack for controlled AI agent workspaces.

中文说明请见: [`README.zh-CN.md`](README.zh-CN.md)

## Project Philosophy

AGI Agent OS is built on one core idea: **agent capability must be paired with explicit governance**.

The stack treats a workspace as an operational system, not just a prompt folder. It defines clear authority boundaries, policy gates, mutation controls, and accountability artifacts so teams can run agents in a controllable way.

Core principles:

- explicit authority before action
- policy-first execution
- controlled mutation for high-trust files
- append-oriented audit discipline
- typed memory with provenance and staleness checks
- validator-friendly contracts over ambiguous prose

## What This Repository Contains

- Bilingual specs (English + Chinese)
- Versioned release artifacts
- Controlled OpenClaw example pack
- Pass/fail fixtures for validator regression
- Commercial usage guidance and legal baseline files

## Why It Exists

Most agent projects fail operationally at three points:

- policy is implicit and inconsistently enforced
- protected changes happen without robust review/traceability
- runtime validation is ad hoc and difficult to automate

This repository addresses those gaps by combining specification, fixtures, and operational release discipline.

## Versioning & Evolution

The public baseline starts at `v1.0.0`, derived from iterative local development history (`v0.0.1` -> `v0.1.2`).

Evolution focus across those iterations:

- governance model foundations
- activation-gate semantics
- validator matrices and finding families
- OpenClaw controlled workspace templates
- runnable + invalid fixtures for CI assertions

Entry points:

- Specs index: `INDEX.md`
- Current spec (EN): `docs/specs/AGI-Agent-OS-Template-Stack-v1.0.0.en.md`
- Current spec (ZH): `docs/specs/AGI-Agent-OS-Template-Stack-v1.0.0.zh-CN.md`
- Release notes: `docs/RELEASE-NOTES.md`
- Changelog: `CHANGELOG-v1.0.0.md`

## OpenClaw Quick Start

1. Copy `examples/v1.0.0-openclaw-controlled/workspace-template/` into your OpenClaw workspace.
2. Confirm governance core files exist (`POLICY.md`, `CHANGE-CONTROL.md`, `STACK-MANIFEST.yaml`, `AUDIT/index.md`, `MEMORY/index.md`).
3. Validate manifest consistency before protected activation.
4. Use `workspace-template-invalid/` with `VALIDATION-EXPECTATIONS.md` to test failure-path behavior.

## Commercial Use Notes

For business use, review these files first:

- `docs/COMMERCIAL-GUIDELINES.md`
- `docs/COPYRIGHT.md`
- `NOTICE`
- `LICENSE`
- `docs/REFERENCES.md`

Recommended production controls:

- protected branch and mandatory PR review
- CI validator checks before merge/release
- versioned release tags (`vX.Y.Z`)
- immutable audit-chain conventions in deployed workspaces

## References & Citation

External interoperability references are tracked in `docs/REFERENCES.md`.

Citation policy:

- keep references attributable
- avoid large verbatim copy from third-party docs
- refresh reference links at each significant release

## Privacy Baseline

This public repository excludes local machine paths and local environment identifiers.

## License

Licensed under Apache License 2.0. See `LICENSE`.
