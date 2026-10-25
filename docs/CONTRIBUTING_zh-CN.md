# CloudAI 贡献指南

感谢参与 CloudAI。参与项目即表示同意遵守[行为准则](CODE_OF_CONDUCT_zh-CN.md)。

## 提交 Issue 前

- 先搜索[现有 Issue](https://github.com/liaovoxuan/CloudAI/issues)，避免重复报告。
- 优先使用 Bug 报告或功能建议模板。
- 不要公开 API Key、访问令牌、私密提示词、个人信息或未经脱敏的日志。
- 安全漏洞必须按照[安全政策](SECURITY_zh-CN.md)私下报告，不要提交公开 Issue。

Bug 报告应包括 CloudAI 版本、操作系统、架构、安装包格式、完整复现步骤、预期行为、实际行为，以及脱敏后的日志或截图。

## 提议变更

大型功能、兼容性调整或新增依赖应先提交 Issue 确认范围。小型文档、翻译和边界清晰的 Bug 修复可以直接提交 Pull Request。

## Pull Request

1. Fork 仓库并创建用途明确的分支。
2. 每个 PR 只解决一个问题，并保留无关的现有改动。
3. 同步更新与变更相关的测试和文档。
4. 公共事实发生变化时，同步英文、简体中文、繁体中文及其他语言 README。
5. 检查 Markdown 链接、安装包名称、版本号和平台说明。
6. 填写 PR 模板，并说明验证方式和结果。

除非维护者明确要求，否则不要提交生成的二进制、凭据、本地配置、上传状态文件或个人数据。

## 源码与构建变更

CloudAI 源码位于 [`Source/CloudAI`](../Source/CloudAI/) 中。提交变更前，请运行其 README 中与变更相关的 Python 测试、语法检查和 C++ 构建。桌面端打包还需要目标平台工具链及已声明的 Python 依赖；由于仓库尚未提供完整锁定文件，准备发布时必须记录精确版本。完整 HarmonyOS 应用构建需要兼容的 SDK 和 DevEco Studio。

不得提交 API Key、签名密钥、证书、签名配置文件或口令。单独配置的 OpenHarmony HAP 工程尚未加入，详情参见[开源状态](OPEN_SOURCE_STATUS_zh-CN.md)。

## 贡献许可

除非另有明确说明，被项目接受的贡献均按仓库的 [MIT License](../LICENSE) 提供。请仅提交你有权许可的内容，并保留第三方要求的版权及许可证声明。
