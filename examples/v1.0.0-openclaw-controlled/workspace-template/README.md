# v1.0.0 OpenClaw Controlled Workspace Template

This folder is a runnable governance starter set for a controlled OpenClaw workspace.

Included files:
- `AGENTS.md`
- `BOOTSTRAP.md`
- `POLICY.md`
- `CHANGE-CONTROL.md`
- `STACK-MANIFEST.yaml`
- `CHANGE-RECORD.example.yaml`
- `AUDIT/index.md`
- `MEMORY/index.md`

How to use:
1. Keep `USER.md` plus constitutional files (`PRINCIPAL.md`, `GOALS.md`, `STATE.md`, `RISKS.md`, `IDENTITY.md`, `SOUL.md`).
2. Use included `AGENTS.md` and `BOOTSTRAP.md` as startup defaults or merge into existing ones.
3. Validate that `STACK-MANIFEST.yaml` matches actual paths before allowing protected activation.
4. Treat `AUDIT/index.md` as append-only and bind every protected activation to an audit event.
5. Use `CHANGE-RECORD.example.yaml` as the approval/activation data contract starter.
6. Keep `MEMORY/index.md` as governance memory registry; retain OpenClaw runtime short-term memory separately if needed.

Reference alignment:
- OpenClaw bootstrapping: `AGENTS.md` and `BOOTSTRAP.md` drive startup/loading behavior.
- OpenClaw default agent behavior: this pack adds constitutional control, activation gates, and audit/memory discipline on top of that baseline.
