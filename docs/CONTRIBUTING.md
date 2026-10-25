# Contributing to CloudAI

Thank you for helping improve CloudAI. By participating, you agree to follow
the [Code of Conduct](CODE_OF_CONDUCT.md).

## Before opening an issue

- Search [existing issues](https://github.com/liaovoxuan/CloudAI/issues) to
  avoid duplicates.
- Use the bug-report or feature-request form when available.
- Do not post API keys, access tokens, private prompts, personal data or
  unredacted logs.
- Report security vulnerabilities through the private process in
  [SECURITY.md](SECURITY.md), not through a public issue.

Bug reports should include the CloudAI version, operating system, architecture,
package format, exact reproduction steps, expected behavior, actual behavior
and sanitized logs or screenshots.

## Proposing a change

For a large feature, compatibility change or new dependency, open an issue
before implementation so the scope can be agreed upon. Small documentation,
translation and clearly scoped bug fixes may be submitted directly.

## Pull requests

1. Fork the repository and create a focused branch.
2. Keep the change limited to one purpose and preserve unrelated work.
3. Update tests and documentation relevant to the change.
4. Keep the English, Simplified Chinese, Traditional Chinese and other
   translated README files consistent when shared facts change.
5. Verify Markdown links, package names, version numbers and platform claims.
6. Complete the pull-request template and explain how the change was tested.

Do not add generated binaries, credentials, local configuration, upload state
files or personal data unless a maintainer has explicitly requested them.

## Source and build changes

CloudAI source is available in [`Source/CloudAI`](../Source/CloudAI/). Run the
relevant Python tests, syntax checks and C++ build documented in its README
before submitting a change. Desktop packaging additionally requires the
target-platform toolchain and declared Python dependencies; record exact
versions when preparing a release because the repository does not yet provide
a complete lock. A full HarmonyOS application build requires a compatible SDK
and DevEco Studio.

Never submit API keys, signing keys, certificates, profiles or passwords. A
separately configured OpenHarmony HAP project is not yet present; see
[Open Source Status](OPEN_SOURCE_STATUS.md).

## Licensing of contributions

Unless explicitly stated otherwise, contributions accepted into this
repository are provided under the repository's [MIT License](../LICENSE). Only
submit work that you have the right to license, and preserve required
third-party copyright and license notices.
