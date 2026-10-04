# 项目进度

## 进行中

- Windows 和 Apple 芯片 Mac 尚未完成本次改动的运行回归；Intel Mac 的具体业务测试项未逐项记录。

## 最近完成

- 2026-10-04 09:12：完成 macOS 构建适配：Mac 专用 APP/DMG 配置、Cargo 路径识别、非交互 DMG 打包、`.app` 路径支持、客户端真实版本读取及 DMG 分发。使用入口见 [README.md](README.md)。

## 最近验证

- 2026-10-04 10:50：用户确认当前 macOS 13.7.8 Intel 环境可正常使用；提交前重新检查国际化键、Node 脚本语法和补丁空白，均通过；生成产物已被 Git 忽略。
- 2026-10-04 09:12：在 macOS 13.7.8 Intel 上运行 `npm run dist`（包含 `npm run tauri build`）成功，生成 APP 和 x64 DMG；`hdiutil verify` 校验通过，打包临时磁盘已全部卸载。
- 2026-10-04 09:12：`cargo test --release --lib --locked --manifest-path src-tauri/Cargo.toml` 通过 1 项路径回归测试；隔离目录中的 CLI `state` 启动成功并识别本机 ZCode 路径；脚本语法及 `git diff --check` 通过。未验证 GUI 交互与真实账号业务流程。
- 2026-10-04 08:32：前端 `npm run build`、`npm run check:i18n`、分发脚本语法检查及 `git diff --check` 通过；系统 PlistBuddy 成功读取已安装 ZCode 版本 `3.14.4`。
