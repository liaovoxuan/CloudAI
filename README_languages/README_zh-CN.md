# CloudAI

CloudAI 是一款轻量级跨平台桌面 AI 助手，支持智能问答、识图和 OCR。应用无需注册 CloudAI 账户，仅在用户主动发起 AI 请求时发送数据。

> **仓库状态：**本仓库目前用于存放 CloudAI 文档与发行信息，源码及可复现构建说明尚未发布。因此在源码发布前，它应被视为提供公开下载的软件，而不是可复现构建的完整开源项目。

[English](README.md)

## 功能

- AI 对话
- 图片理解与 OCR
- 用户自行配置云端 AI 服务
- 图形化、多语言桌面界面
- QEMU/UTM 指令转换插件

## 支持平台

- Windows x64
- macOS
- Linux x86_64 与 ARM64
- HarmonyOS / OpenHarmony

## 下载

请从 [GitHub Releases](https://github.com/liaovoxuan/CloudAI/releases) 下载适合当前平台的软件包。

不同版本提供的软件包格式可能不同，下载前请查看对应版本说明；上方列出的平台不一定在每个版本中都提供安装包。

macOS 版本目前尚未通过 Apple Developer 证书公证，首次打开时可能需要在“隐私与安全性”中手动允许。

HarmonyOS 软件包使用 DevEco Studio 构建并在发布时签名；签名凭据不会存放在本仓库中。

## 隐私

CloudAI 本身不要求账户，也不收集分析数据。发送给用户所配置 AI 服务商的请求和附件，受对应服务商隐私政策约束。详见[隐私政策](docs/PRIVACY_zh-CN.md)。

## 文档

- [更新日志](docs/CHANGELOG_zh-CN.md)
- [参与贡献](docs/CONTRIBUTING_zh-CN.md)
- [安全政策](docs/SECURITY_zh-CN.md)
- [支持](docs/SUPPORT_zh-CN.md)

## 许可证

本仓库目前包含 MIT 许可声明；对应源码发布时将一并明确完整许可范围。

## 开发者

廖博轩
