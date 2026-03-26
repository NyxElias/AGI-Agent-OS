# AGI Agent OS 模版栈 v1.0.0

状态：稳定版
版本：1.0.0
语言：简体中文
日期：2026-03-26

## 1. 本版意图

`v1.0.0` 是面向公开发布的首个受治理工作区基线版本。

## 2. 核心模型

本栈定义四种运行 profile：

- `native`
- `governed`
- `controlled`
- `longrun`

## 3. Controlled 基线

受治理工作区至少包含：

- `POLICY.md`
- `CHANGE-CONTROL.md`
- `STACK-MANIFEST.yaml`
- `AUDIT/index.md`
- `MEMORY/index.md`

## 4. 校验与运行建议

按最高严重级别建议运行模式：

- `V0`：`load-ok`
- `V1`：`load-with-warnings`
- `V2`：`advisory-only`
- `V3`：阻断受保护工作流
- `V4`：`reject-load`

## 5. 示例包

本版附带：

- `examples/v1.0.0-openclaw-controlled/`

其中包含：

- 精简示例（`*.example.*`）
- 可运行夹具（`workspace-template/`）
- 故意失败夹具（`workspace-template-invalid/`）
- 校验断言基线（`VALIDATION-EXPECTATIONS.md`）

## 6. 修改记录

### 2026-03-26

- 创建 `v1.0.0` 中文基线规范
- 增加版本对齐的 controlled 示例包
