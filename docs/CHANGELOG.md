# Changelog

## Repository updates - 2026-09-19

-   Added the sanitized CloudAI 1.0.1 working tree under `Source/CloudAI`,
    including the desktop application, Agent mode, plugin support, Python and
    C++ cores, tests, packaging definitions, shared resources and HarmonyOS.
-   Excluded signing keys, certificates, profiles and passwords; replaced the
    project signing block with an unsigned local configuration.
-   Replaced the stale bundled privacy DOCX with a synchronized multilingual
    Markdown policy and added the MIT License and third-party notice to the
    packaging definitions.
-   Updated HarmonyOS version metadata and device declarations for `phone`,
    `tablet` and `2in1`.
-   Verified both Python test suites, Python syntax, both CMake entry points and
    the C++ smoke test. Full cross-platform packages and a HAP still require
    their target toolchains and device testing.
-   Updated source-availability documentation: release provenance, dependency
    locks, an SBOM and a separately configured OpenHarmony HAP project remain
    unavailable.

## v1.0.1 - 2026-09-13

-   Added documentation for Agent mode.
-   Added detailed Windows, Linux, macOS, HarmonyOS and OpenHarmony status to
    every translated README.
-   Clarified that version 1.0.1 application packages use ZIP as the default
    distribution format.
-   Changed the macOS build target to Universal for Intel and Apple Silicon;
    the legacy 1.0.0 package remains Apple Silicon-only.
-   Corrected HarmonyOS release status and documented the limitations of the
    archived HAP packages.
-   Moved existing 1.0.0 application packages to the legacy archive without
    replacing their binaries.
-   Completed an open-source project-file review: expanded the contribution,
    conduct, security, support and privacy policies; added issue and pull-request
    templates, third-party notices and a release checklist.
-   Documented the source and reproducible-build gaps present at release time.

## v1.0.0 - 2026-08-02

-   Initial CloudAI application package release.
-   Published desktop and HarmonyOS build artifacts.

## v0.8 Beta - 2026-08-02

-   Initial public open-source release preparation.
-   Multi-platform build support.
