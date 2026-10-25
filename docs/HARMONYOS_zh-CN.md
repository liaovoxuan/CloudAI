# HarmonyOS 发布说明

1.0.1 应用安装包默认使用 ZIP 作为发布格式。在 HarmonyOS 上，应先解压发布包，再安装其中兼容且已签名的 HAP。现有的 1.0.0 HAP 文件已移入旧版归档，避免被误认为当前版本。

## 已归档安装包的已知限制

- 安装包仅声明了 `2in1` 设备类型。
- 元数据将其标记为 debug 构建。
- 安装包面向 HarmonyOS API 版本 `60101024`，可能无法安装在不兼容的系统上。
- 分发时可能需要目标设备认可的签名配置。

未来发布 HarmonyOS 版本时，应基于源码使用 release 模式重新构建，设置预期的设备类型和 API 兼容范围，配置正确的版本号与签名，并在所声明支持的每类设备上完成测试。

## 源码工程

经过清理的 CloudAI 1.0.1 HarmonyOS 工程位于 [`Source/CloudAI/harmonyos`](../Source/CloudAI/harmonyos/) 中，包含 ArkTS 外壳、NAPI 桥接层、资源文件及共享 C++ 核心。工程元数据声明版本为 `1.0.1`、HarmonyOS 6.1.1（API 24）、`arm64-v8a`，设备类型包括 `phone`、`tablet` 和 `2in1`。

C++ 核心及其冒烟测试已通过 CMake 构建。由于完整构建 HAP 并进行设备测试需要兼容的 HarmonyOS SDK、DevEco Studio 和本地签名配置，本次未在仓库环境中执行这些步骤。当前也没有建立该源码与已有 ZIP 或 HAP 产物之间的对应关系，因此不能据此证明已有二进制可复现。

原工程旁的全部私有签名材料和口令均未复制进仓库。请在本地配置新的或已获授权的签名身份。当前 API Key 文件使用可逆编码而非平台密钥库；在使用生产凭据前，请阅读[源码安全说明](../Source/CloudAI/harmonyos/README.md#security-note)。
