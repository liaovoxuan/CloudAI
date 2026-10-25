# Open Source Status

Last reviewed: 2026-09-19

## License

The repository contains the complete OSI-approved MIT License with the
copyright holder and year filled in. Unless a file states otherwise, original
CloudAI content in this repository is offered under that license.

## Source availability

The repository now contains the copied CloudAI 1.0.1 working tree under
[`Source/CloudAI`](../Source/CloudAI/), including the Python/Tk desktop
application, Agent mode, plugin host and example, headless Python and C++
implementations, tests, Windows/Linux/macOS PyInstaller definitions, required
shared resources and the HarmonyOS ArkTS/NAPI project. Private signing keys,
certificates, profiles, passwords, generated files and local runtime data were
intentionally excluded. The stale binary privacy document was replaced with a
reviewable multilingual Markdown policy, and the packaging definitions now
include the MIT License and third-party notice.

The dependency-free Python tests, desktop Agent/plugin tests, Python syntax
checks, C++ CMake build, CTest smoke test and HarmonyOS project-level CMake
entry all pass in the current environment. The full desktop GUI and packaged
artifacts were not built on every target system, and a complete HAP build still
requires a compatible HarmonyOS SDK, DevEco Studio and local signing.

A separately configured OpenHarmony HAP project is not included. More
importantly, the copied working tree has not been mapped to the commit or exact
toolchain used for any existing release artifact, so those binaries cannot yet
be described as reproducible builds of this source.

To complete release-source verification, add or verify:

- a dedicated OpenHarmony HAP project, or correct the advertised support;
- locked dependency versions and exact build-toolchain versions;
- full Windows, Linux, macOS Universal and HarmonyOS package builds from a tag;
- installation and device tests for every advertised platform and architecture;
- required third-party license texts and a generated SBOM; and
- a mapping from each release artifact to its source revision.

## Binary and dependency status

The existing 1.0.0 packages are retained as legacy binaries. Their third-party
license inventory has not been fully verified; see
[Third-Party Notices](../THIRD_PARTY_NOTICES.md). Version 1.0.1 packages should
not be represented as reproducible source builds until their corresponding
source revision, dependency lock data and verified packaging instructions are
available.

The legacy archive includes SHA-256 checksums for file-integrity verification,
but checksums do not establish source reproducibility, authenticity or license
compliance.

## Community files

The repository includes contribution guidelines, a code of conduct, a security
policy, support guidance, a privacy policy, issue forms and a pull-request
template. These files describe project process; they do not cure missing
artifact provenance, dependency locks or third-party attribution.
