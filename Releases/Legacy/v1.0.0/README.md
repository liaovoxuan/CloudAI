# CloudAI 1.0.0 Legacy Packages

These packages are retained for historical reference. They have not been
replaced or relabeled as version 1.0.1.

The archived macOS application is an Apple Silicon-only (`arm64`) build. It is
not Universal and does not support Intel Macs. Version 1.0.1 uses a Universal
macOS build, but that package is not stored in this archive.

The two HarmonyOS files are separate 1.0.0 builds. The earlier build was renamed
from `CloudAI(2).hap` to `CloudAI-early-build.hap` to make its status explicit.
Both HAP files have the limitations documented in
[`docs/HARMONYOS.md`](../../../docs/HARMONYOS.md).

These compiled packages may include separately licensed components. Review the
[third-party notices](../../../THIRD_PARTY_NOTICES.md) and the documented
[open-source status](../../../docs/OPEN_SOURCE_STATUS.md) before redistribution.
The complete set of repository policies is listed in the
[open-source project information](../../../docs/OPEN_SOURCE.md).

Verify the archived files against [`SHA256SUMS`](SHA256SUMS) before use. On
macOS, run `shasum -a 256 -c SHA256SUMS` from this directory; on Linux, run
`sha256sum -c SHA256SUMS`.

## Public downloads

The same historical binaries are already hosted in the existing
[v0.8.0-beta release](https://github.com/liaovoxuan/CloudAI/releases/tag/v0.8.0-beta).
That historical tag and its assets are preserved. Local archive files remain
on disk and are not stored in the Git source tree. The checksum list in this
directory refers to the local archive filenames; hosted asset names can differ.
