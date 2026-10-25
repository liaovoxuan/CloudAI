# CloudAI

CloudAI is a cross-platform AI assistant.

Current project version: **1.0.1**. Its application packages use ZIP as the
default distribution format. The existing 1.0.0 packages are retained in the
[legacy archive](../Releases/Legacy/v1.0.0/).

The macOS build for 1.0.1 uses Universal format and supports both Intel and
Apple Silicon. The archived 1.0.0 macOS package is Apple Silicon (`arm64`) only.

## Downloads and source

- [CloudAI 1.0.1 public downloads](https://github.com/liaovoxuan/CloudAI/releases/tag/v1.0.1), with no GitHub sign-in required.
- Linux ARM64 and RISC-V 64 ZIPs contain DEB, RPM, portable packages and architecture verification reports; both require glibc >= 2.39.
- Current downloads also include Windows x64, macOS and HarmonyOS. This publication does not include a Windows ARM64 or separate OpenHarmony package.
- [All releases and historical packages](https://github.com/liaovoxuan/CloudAI/releases).
- The full source tree is in `Source/CloudAI`, including the desktop app, Python/C++ cores, plugins, shared resources and HarmonyOS project.

Binaries are distributed through GitHub Releases; local installers and application bundles under `Releases/` are not stored in the source tree. See the release notes and bundled manifests for binary provenance. Publishing the source copy does not establish reproducibility of existing binaries.

## Features

-   AI conversation
-   Agent mode for multi-step tasks
-   Cloud AI API integration
-   Multi-platform desktop application
-   Multi-architecture builds
-   Graphical interface
-   Multi-language support

## Agent Mode

Agent mode can break a goal into steps, use tools enabled by the user, make
authorized changes and verify the result where possible. It does not grant
additional permissions and should request confirmation before sensitive or
destructive actions. See the [Agent mode guide](../docs/AGENT_MODE.md).

## Supported Platforms

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Other Platforms

-   HarmonyOS (1.0.1 ZIP distribution; legacy 1.0.0 HAP archived)
-   OpenHarmony (1.0.1 ZIP distribution)

## Platform Details

| Platform | Architecture and package status | Installation and limitations |
| --- | --- | --- |
| Windows | Version 1.0.1 targets x64 and ARM64 and uses ZIP as the default package. The legacy archive contains the 1.0.0 x64 ZIP. | Extract the ZIP completely before running the application. |
| Linux | Version 1.0.1 targets x86_64 and ARM64 and uses ZIP as the default package. Legacy 1.0.0 packages for both architectures are archived. | The ZIP may contain AppImage, DEB, RPM or TAR.GZ distributions. AppImage requires execution permission; DEB and RPM use their system package managers. |
| macOS | Version 1.0.1 uses a Universal build for Intel and Apple Silicon and is distributed as ZIP by default. The legacy 1.0.0 package is Apple Silicon (`arm64`) only. | Extract the ZIP to obtain the application. The application is currently unsigned and may require manual approval in macOS Security settings. |
| HarmonyOS | The 1.0.1 release bundle uses ZIP by default; installation uses the compatible signed HAP contained in the bundle. The archived 1.0.0 HAP files are debug builds limited to `2in1`. | The legacy HAPs target API `60101024`. Installation requires a compatible system and valid signing configuration. See the [HarmonyOS notes](../docs/HARMONYOS.md). |
| OpenHarmony | The 1.0.1 release bundle uses ZIP by default; installation requires an OpenHarmony-compatible HAP from that bundle. | A compatible signature and device test are required. Do not use the archived HarmonyOS 1.0.0 HAP as an OpenHarmony package. |

## Installation

### Linux

AppImage:

1.  Download and extract the default Linux ZIP package, then select the AppImage for your architecture.
2.  Add execution permission:

``` bash
chmod +x CloudAI.AppImage
```

3.  Run the application:

``` bash
./CloudAI.AppImage
```

Deb packages can be installed with:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

The macOS version is currently not signed with an Apple Developer
certificate.

When opening for the first time, users may need to allow the application
manually in macOS Security settings.

### HarmonyOS

The HarmonyOS 1.0.1 distribution uses ZIP by default. Extract it and install
the compatible signed HAP inside. The archived 1.0.0 HAP packages are debug
builds limited to `2in1`; see the [HarmonyOS release notes](../docs/HARMONYOS.md).

## License

[MIT License](../LICENSE).

## Open-source project files

See the [open-source project information](../docs/OPEN_SOURCE.md) for the
license, source-availability status, contribution guide, code of conduct,
security and privacy policies, support information and third-party notices.

The copied CloudAI 1.0.1 source tree is available in
[`Source/CloudAI`](../Source/CloudAI/), including the desktop application,
Agent and plugin support, packaging resources and HarmonyOS. A separate
OpenHarmony HAP project, release provenance, dependency locks and verified
reproducible packaging remain unavailable; see the
[open-source status review](../docs/OPEN_SOURCE_STATUS.md).

## Developer

Liao Boxuan

## Date

2026-09-13
