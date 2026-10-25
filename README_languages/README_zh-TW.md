# CloudAI

CloudAI 是一款跨平台人工智慧助理。

目前專案版本：**1.0.1**。應用程式安裝套件預設使用 ZIP 作為發布格式；現有 1.0.0 安裝套件已保留在[舊版封存](../Releases/Legacy/v1.0.0/)中。

1.0.1 的 macOS 建置採用 Universal 格式，同時支援 Intel 與 Apple Silicon。封存的 1.0.0 macOS 安裝套件僅支援 Apple Silicon（`arm64`）。

## 功能

-   AI 對話
-   適用於多步驟工作的 Agent 模式
-   雲端 AI API 整合
-   跨平台桌面應用程式
-   多架構建置
-   圖形化介面
-   多語言支援

## Agent 模式

Agent 模式可以將目標拆分為多個步驟、使用使用者已啟用的工具、在授權範圍內執行變更，並儘可能驗證結果。此模式本身不會取得額外權限；執行敏感或破壞性操作前應要求使用者確認。詳情請參閱 [Agent 模式說明](../docs/AGENT_MODE_zh-CN.md)。

## 支援平台

### 桌面

-   Windows x64
-   Windows ARM64
-   macOS Universal（Intel + Apple Silicon）— v1.0.1
-   macOS Apple Silicon — 舊版 v1.0.0
-   Linux x86_64
-   Linux ARM64

### 其他平台

-   HarmonyOS（1.0.1 預設提供 ZIP；舊版 1.0.0 HAP 已封存）
-   OpenHarmony（1.0.1 預設提供 ZIP）

## 平台詳細資訊

| 平台 | 架構與安裝套件狀態 | 安裝方式與限制 |
| --- | --- | --- |
| Windows | 1.0.1 面向 x64 和 ARM64，預設提供 ZIP 安裝套件；舊版封存中保留了 1.0.0 x64 ZIP。 | 執行應用程式前必須先完整解壓縮 ZIP。 |
| Linux | 1.0.1 面向 x86_64 和 ARM64，預設提供 ZIP 安裝套件；兩種架構的 1.0.0 套件均已封存。 | ZIP 中可包含 AppImage、DEB、RPM 或 TAR.GZ。AppImage 需要執行權限；DEB 和 RPM 應透過對應的系統套件管理員安裝。 |
| macOS | 1.0.1 使用同時支援 Intel 與 Apple Silicon 的 Universal 建置，預設以 ZIP 發布；舊版 1.0.0 僅支援 Apple Silicon（`arm64`）。 | 解壓縮 ZIP 後可取得應用程式。應用程式目前未簽署，首次執行時可能需要在 macOS 安全性設定中手動允許。 |
| HarmonyOS | 1.0.1 發布套件預設使用 ZIP，安裝時使用套件內相容且已簽署的 HAP；封存的 1.0.0 HAP 是僅支援 `2in1` 的 debug 建置。 | 舊版 HAP 面向 API `60101024`。安裝需要相容系統和有效的簽署設定。詳情請參閱 [HarmonyOS 說明](../docs/HARMONYOS_zh-CN.md)。 |
| OpenHarmony | 1.0.1 發布套件預設使用 ZIP，安裝時需要使用套件內與 OpenHarmony 相容的 HAP。 | 需要相容簽署和裝置測試；不能將封存的 HarmonyOS 1.0.0 HAP 當作 OpenHarmony 安裝套件。 |

## 安裝

### Linux

AppImage：

1.  下載並解壓縮預設的 Linux ZIP 安裝套件，然後選擇符合裝置架構的 AppImage。
2.  加入執行權限：

``` bash
chmod +x CloudAI.AppImage
```

3.  執行應用程式：

``` bash
./CloudAI.AppImage
```

Deb 套件可透過以下指令安裝：

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS 版本目前未使用 Apple Developer 憑證簽署。

首次開啟時，使用者可能需要在 macOS 安全性設定中手動允許應用程式執行。

### HarmonyOS

HarmonyOS 1.0.1 預設以 ZIP 發布。解壓縮後應安裝其中相容且已簽署的 HAP。封存的 1.0.0 HAP 是僅支援 `2in1` 的 debug 建置，詳情請參閱 [HarmonyOS 發布說明](../docs/HARMONYOS_zh-CN.md)。

## 授權條款

[MIT License](../LICENSE)。

## 開源專案文件

授權條款、原始碼可用性狀態、貢獻指南、行為準則、安全與隱私政策、支援資訊及第三方聲明，請參閱[開源專案資訊](../docs/OPEN_SOURCE_zh-CN.md)。

CloudAI 1.0.1 原始碼樹副本現已加入 [`Source/CloudAI`](../Source/CloudAI/)，包含桌面應用程式、Agent 與外掛支援、封裝資源及 HarmonyOS 工程。獨立的 OpenHarmony HAP 工程、發行成品來源對應、相依套件鎖定及經過驗證的可重現封裝流程仍未提供，詳情請參閱[開源狀態檢查](../docs/OPEN_SOURCE_STATUS_zh-CN.md)。

## 開發者

廖博軒

## 日期

2026-09-13
