# CloudAI

CloudAI 是一个跨平台 AI 助手。

当前项目版本：**1.0.1**。应用安装包默认使用 ZIP 作为发布格式；现有 1.0.0 安装包已保留在[旧版归档](Releases/Legacy/v1.0.0/)中。

1.0.1 的 macOS 构建采用 Universal 格式，同时支持 Intel 与 Apple Silicon。归档的 1.0.0 macOS 安装包仅支持 Apple Silicon（`arm64`）。

## 下载与源码

- [CloudAI 1.0.1 公开下载](https://github.com/liaovoxuan/CloudAI/releases/tag/v1.0.1)：无需 GitHub 登录。
- Linux ARM64 和 RISC-V 64 的 ZIP 内含 DEB、RPM、便携包及架构验证报告；两版要求 glibc ≥ 2.39。
- 当前下载包还包括 Windows x64、macOS 和 HarmonyOS；本次未提供 Windows ARM64 或单独的 OpenHarmony 安装包。
- [全部发布版本及旧版安装包](https://github.com/liaovoxuan/CloudAI/releases)。
- 完整源码位于本仓库的 `Source/CloudAI`，包含桌面端、Python/C++ 核心、插件、共享资源和 HarmonyOS 工程。

构建产物保存在 GitHub Releases，本地 `Releases/` 中的安装包和应用目录不直接纳入 Git。已有二进制与当前源码副本的精确对应关系见 Release 说明及包内 manifest，不将源码上传等同于二进制可复现构建。

## 功能

-   AI 对话
-   用于多步骤任务的 Agent 模式
-   云端 AI API 接入
-   多平台桌面应用
-   多架构构建
-   图形化界面
-   多语言支持

## Agent 模式

Agent 模式可以将目标拆分为多个步骤，使用用户已启用的工具，在授权范围内执行变更，并尽可能验证结果。该模式本身不会获得额外权限；执行敏感或破坏性操作前应请求用户确认。详情参见 [Agent 模式说明](docs/AGENT_MODE_zh-CN.md)。

## 支持平台

桌面：

-   Windows x64
-   Windows ARM64
-   macOS Universal（Intel + Apple Silicon）— v1.0.1
-   macOS Apple Silicon — 旧版 v1.0.0
-   Linux x86_64
-   Linux ARM64

其他：

-   HarmonyOS（1.0.1 默认提供 ZIP；旧版 1.0.0 HAP 已归档）
-   OpenHarmony（1.0.1 默认提供 ZIP）

## 平台详情

| 平台 | 架构与安装包状态 | 安装方式与限制 |
| --- | --- | --- |
| Windows | 1.0.1 面向 x64 和 ARM64，默认提供 ZIP 安装包；旧版归档中保留了 1.0.0 x64 ZIP。 | 运行应用前需要先完整解压 ZIP。 |
| Linux | 1.0.1 面向 x86_64 和 ARM64，默认提供 ZIP 安装包；两种架构的 1.0.0 包均已归档。 | ZIP 中可包含 AppImage、DEB、RPM 或 TAR.GZ。AppImage 需要执行权限；DEB 和 RPM 应通过对应的系统包管理器安装。 |
| macOS | 1.0.1 使用同时支持 Intel 与 Apple Silicon 的 Universal 构建，默认以 ZIP 发布；旧版 1.0.0 仅支持 Apple Silicon（`arm64`）。 | 解压 ZIP 后可获得应用。应用目前没有签名，首次运行时可能需要在 macOS 安全设置中手动允许。 |
| HarmonyOS | 1.0.1 发布包默认使用 ZIP，安装时使用包内兼容且已签名的 HAP；归档的 1.0.0 HAP 是仅支持 `2in1` 的 debug 构建。 | 旧版 HAP 面向 API `60101024`。安装需要兼容系统和有效签名配置。详情参见 [HarmonyOS 说明](docs/HARMONYOS_zh-CN.md)。 |
| OpenHarmony | 1.0.1 发布包默认使用 ZIP，安装时需要使用包内与 OpenHarmony 兼容的 HAP。 | 需要兼容签名和设备测试；不能将归档的 HarmonyOS 1.0.0 HAP 当作 OpenHarmony 安装包。 |

## 安装

### Linux

AppImage：

下载并解压默认的 Linux ZIP 安装包，然后选择与设备架构匹配的 AppImage：

``` bash
chmod +x CloudAI.AppImage
./CloudAI.AppImage
```

Deb：

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS 版本目前未使用 Apple Developer 证书签名。

首次打开时，需要在系统安全设置中手动允许应用运行。

### HarmonyOS

HarmonyOS 1.0.1 默认以 ZIP 发布。解压后应安装其中兼容且已签名的 HAP。归档的 1.0.0 HAP 是仅支持 `2in1` 的 debug 构建，详情参见 [HarmonyOS 发布说明](docs/HARMONYOS_zh-CN.md)。

## 开源协议

[MIT License](LICENSE)。

## 开源项目文件

许可证、源码可用性状态、贡献指南、行为准则、安全与隐私政策、支持信息及第三方声明，请参见[开源项目信息](docs/OPEN_SOURCE_zh-CN.md)。

CloudAI 1.0.1 源码树副本现已加入 [`Source/CloudAI`](Source/CloudAI/)，包含桌面应用、Agent 与插件支持、打包资源及 HarmonyOS 工程。单独的 OpenHarmony HAP 工程、发布产物来源映射、依赖锁定及经过验证的可复现打包流程仍未提供，详情参见[开源状态检查](docs/OPEN_SOURCE_STATUS_zh-CN.md)。

## 开发者

廖博轩

## 日期

2026-09-13
