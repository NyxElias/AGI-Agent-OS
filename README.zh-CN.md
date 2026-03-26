# AGI Agent OS

English first: [`README.md`](README.md)

这是一个面向受治理 AI Agent 工作区的规范化模板栈仓库。

## 当前版本

- 版本：`v1.0.0`
- 主分支：`main`
- 索引：`INDEX.md`
- 发布说明：`RELEASE-NOTES.md`

## 核心内容

- 规范（中英双语）
- 变更日志（中英双语）
- OpenClaw 受治理示例包（含通过/失败夹具）

## OpenClaw 快速应用

1. 将 `examples/v1.0.0-openclaw-controlled/workspace-template/` 复制到 OpenClaw 工作区。
2. 确认治理核心文件齐全（`POLICY.md`、`CHANGE-CONTROL.md`、`STACK-MANIFEST.yaml`、`AUDIT/index.md`、`MEMORY/index.md`）。
3. 在受保护激活前执行 manifest 一致性校验。
4. 使用 `workspace-template-invalid/` 与 `VALIDATION-EXPECTATIONS.md` 做校验器回归。

## About 信息

- 英文：`ABOUT.md`
- 中文：`ABOUT.zh-CN.md`

## 商业化使用建议

请先阅读：

- `COMMERCIAL-GUIDELINES.md`
- `COPYRIGHT.md`
- `NOTICE`
- `LICENSE`
- `REFERENCES.md`
