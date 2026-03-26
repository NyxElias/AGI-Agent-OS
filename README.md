# AGI Agent OS

Governance-first template stack for controlled AI agent workspaces.

## Repository Identity

- Owner: `NyxElias`
- Canonical branch: `main`
- Public baseline version: `v1.0.0`
- Scope: specification + example packs + validation fixtures

## What This Repository Provides

- Versioned stack specifications (EN / zh-CN)
- Controlled workspace governance baseline
- OpenClaw-oriented controlled example pack
- Pass/fail validation fixtures for regression testing

## Quick Links

- Specs index: `INDEX.md`
- English spec: `AGI-Agent-OS-Template-Stack-v1.0.0.en.md`
- Chinese spec: `AGI-Agent-OS-Template-Stack-v1.0.0.zh-CN.md`
- Release notes: `RELEASE-NOTES.md`
- Changelog (EN): `CHANGELOG-v1.0.0.md`
- Changelog (ZH): `CHANGELOG-v1.0.0.zh-CN.md`
- About metadata: `ABOUT.md`

## Directory Structure

```text
.
├── AGI-Agent-OS-Template-Stack-v1.0.0.en.md
├── AGI-Agent-OS-Template-Stack-v1.0.0.zh-CN.md
├── CHANGELOG-v1.0.0.md
├── CHANGELOG-v1.0.0.zh-CN.md
├── INDEX.md
├── RELEASE-NOTES.md
├── VERSION
└── examples/
    └── v1.0.0-openclaw-controlled/
        ├── *.example.*
        ├── workspace-template/
        ├── workspace-template-invalid/
        └── VALIDATION-EXPECTATIONS.md
```

## OpenClaw Application Flow

1. Copy `examples/v1.0.0-openclaw-controlled/workspace-template/` into your OpenClaw workspace.
2. Ensure required governance files exist (`POLICY.md`, `CHANGE-CONTROL.md`, `STACK-MANIFEST.yaml`, `AUDIT/index.md`, `MEMORY/index.md`).
3. Validate manifest consistency before protected activation.
4. Use `workspace-template-invalid/` + `VALIDATION-EXPECTATIONS.md` for validator regression checks.

## Privacy & Sanitization

This public repository is sanitized for open sharing:

- no local absolute machine paths
- no local personal identity details
- no model-provider branding metadata in release docs

## Release Policy

- Every release must create new versioned files.
- English and Chinese specs must stay version-aligned.
- `INDEX.md` and changelog files must be updated per release.

## License

No license file is included yet. Add `LICENSE` before broader external reuse.
