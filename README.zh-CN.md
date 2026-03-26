# AGI Agent OS

English first: [`README.md`](README.md)

这是一个面向受治理 AI Agent 工作区的规范化模板栈项目。

## 项目理念

AGI Agent OS 的核心理念是：**能力必须与治理同时存在**。

它把工作区视为“可运行的治理系统”，而非单纯提示词集合，强调授权边界、策略门禁、受保护变更流程、审计可追踪与可校验运行。

核心原则：

- 先授权，后动作
- 先策略，后执行
- 高信任文件变更必须受控
- 审计采用 append-only 纪律
- 记忆必须有类型、来源与时效规则
- 用可校验契约替代模糊叙述

## 仓库内容

- 中英双语规范
- 版本化发布工件
- OpenClaw controlled 示例包
- 校验器通过/失败回归夹具
- 商业化使用与法律基线文件

## 版本演进

公开发布从 `v1.0.0` 开始，源自本地迭代演进（`v0.0.1` -> `v0.1.2`）。

历次迭代重点：

- 治理模型基础
- 激活门禁语义
- validator 查表矩阵与 finding 家族
- OpenClaw 受治理工作区模板
- 可运行与故障夹具（用于 CI 断言）

入口文件：

- 规范索引：`INDEX.md`
- 当前英文规范：`AGI-Agent-OS-Template-Stack-v1.0.0.en.md`
- 当前中文规范：`AGI-Agent-OS-Template-Stack-v1.0.0.zh-CN.md`
- 发布说明：`RELEASE-NOTES.md`
- 变更日志：`CHANGELOG-v1.0.0.zh-CN.md`

## OpenClaw 快速应用

1. 将 `examples/v1.0.0-openclaw-controlled/workspace-template/` 复制到 OpenClaw 工作区。
2. 确认治理核心文件齐全（`POLICY.md`、`CHANGE-CONTROL.md`、`STACK-MANIFEST.yaml`、`AUDIT/index.md`、`MEMORY/index.md`）。
3. 在受保护激活前执行 manifest 一致性校验。
4. 使用 `workspace-template-invalid/` 与 `VALIDATION-EXPECTATIONS.md` 做失败路径回归测试。

## 商业化使用说明

请优先阅读：

- `COMMERCIAL-GUIDELINES.md`
- `COPYRIGHT.md`
- `NOTICE`
- `LICENSE`
- `REFERENCES.md`

建议的生产治理控制：

- `main` 分支保护 + 强制 PR 评审
- 合并与发布前执行校验器 CI
- 版本标签化发布（`vX.Y.Z`）
- 在实际工作区中坚持审计链不可回写

## 引用与标注

外部参考统一记录于 `REFERENCES.md`。

引用策略：

- 保持可追溯来源
- 避免大段复制第三方文档
- 在重要版本发布时复核链接与兼容性假设

## 隐私基线

公开仓库不包含本机路径与本地环境标识。

## 许可证

采用 Apache License 2.0，详见 `LICENSE`。
