# AGI Agent OS

Governance-first template stack for controlled AI agent workspaces.

中文说明请见: [`README.zh-CN.md`](README.zh-CN.md)

## Overview

This repository provides a versioned governance specification and practical fixtures for building controlled agent workspaces.

It is designed for teams that need:

- explicit policy and change-control contracts
- auditable mutation and activation behavior
- validator-friendly fixtures for pass/fail regression
- commercially usable repository governance workflows

## Current Release

- Version: `v1.0.0`
- Default branch: `main`
- Index: `INDEX.md`
- Release notes: `RELEASE-NOTES.md`

## Repository Contents

- Specs:
  - `AGI-Agent-OS-Template-Stack-v1.0.0.en.md`
  - `AGI-Agent-OS-Template-Stack-v1.0.0.zh-CN.md`
- Changelog:
  - `CHANGELOG-v1.0.0.md`
  - `CHANGELOG-v1.0.0.zh-CN.md`
- Controlled example pack:
  - `examples/v1.0.0-openclaw-controlled/`

## OpenClaw Quick Start

1. Copy `examples/v1.0.0-openclaw-controlled/workspace-template/` into your OpenClaw workspace.
2. Confirm `POLICY.md`, `CHANGE-CONTROL.md`, `STACK-MANIFEST.yaml`, `AUDIT/index.md`, `MEMORY/index.md` exist.
3. Validate manifest consistency before protected activation.
4. Use `workspace-template-invalid/` and `VALIDATION-EXPECTATIONS.md` for validator regression checks.

## About Metadata

- English: `ABOUT.md`
- Chinese: `ABOUT.zh-CN.md`

## Commercial Repository Guidance

For business-facing use, review:

- `COMMERCIAL-GUIDELINES.md`
- `COPYRIGHT.md`
- `NOTICE`
- `LICENSE`
- `REFERENCES.md`

## Privacy Baseline

This public baseline excludes local machine identifiers and private local environment metadata.

## License

Licensed under Apache License 2.0. See `LICENSE`.
