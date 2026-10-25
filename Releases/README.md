# Releases

Public downloads are hosted in [GitHub Releases](https://github.com/liaovoxuan/CloudAI/releases).
[CloudAI 1.0.1](https://github.com/liaovoxuan/CloudAI/releases/tag/v1.0.1) includes the packages available in this local project: Windows x64, macOS, Linux x86_64 / ARM64 / RISC-V 64, and HarmonyOS. No Windows ARM64 or separate OpenHarmony binary is included in this publication.

ZIP bundles and individual Linux package formats are provided. ARM64 / RISC-V 64 bundles include architecture reports, checksums and upstream build manifests. They require glibc >= 2.39 and a Linux desktop with X11 / XWayland.

The original compiled packages are uploaded without rebuilding or claiming that they were produced from the newly published source copy. Linux ARM64 / RISC-V 64 manifests identify LocalAI commit `2b9e415c54b8bd422058c9e76008e715f16ce31d`; other existing binaries have no equally precise source mapping. macOS and HarmonyOS installation/signing limitations still apply; see the release notes and [HarmonyOS documentation](../docs/HARMONYOS.md).

Local application bundles, installers and historical binaries remain on disk and are ignored by Git. The documentation and legacy checksum list remain in this source repository. Historical binaries already hosted in the [existing v0.8.0-beta release](https://github.com/liaovoxuan/CloudAI/releases/tag/v0.8.0-beta) are preserved; the old tag and assets are not rewritten.

CloudAI original code is provided under the [MIT License](../LICENSE). Bundled third-party software retains its own licenses; review [third-party notices](../THIRD_PARTY_NOTICES.md) and the [open-source status review](../docs/OPEN_SOURCE_STATUS.md).
