# CloudAI

CloudAI is a lightweight, cross-platform desktop AI assistant for chat, image
understanding, and OCR. It does not require a CloudAI account and only sends
data when the user explicitly makes an AI request.

> **Repository status:** this repository currently hosts CloudAI documentation
> and release information. The source code and reproducible build instructions
> have not yet been published here. Until then, treat CloudAI as downloadable
> software rather than a fully reproducible open-source project.

[简体中文](README_zh-CN.md)

## Features

- AI chat
- Image understanding and OCR
- User-configured cloud AI services
- Graphical, multilingual desktop interface
- QEMU/UTM command conversion plugin

## Supported platforms

- Windows x64
- macOS
- Linux x86_64 and ARM64
- HarmonyOS / OpenHarmony

## Download

Download the package matching your platform from
[GitHub Releases](https://github.com/liaovoxuan/CloudAI/releases).

Published package formats may vary by version. Check the release notes before
downloading; a platform listed above may not be available in every release.

The macOS build is not currently notarized with an Apple Developer certificate.
macOS may require manual approval in Privacy & Security.

HarmonyOS packages are built with DevEco Studio and signed during the release
process. Signing credentials are not stored in this repository.

## Privacy

CloudAI itself does not require an account or collect analytics. Requests and
attachments sent to a configured AI provider are subject to that provider's
privacy policy. See the [Privacy Policy](docs/PRIVACY.md).

## Documentation

- [Changelog](docs/CHANGELOG.md)
- [Contributing](docs/CONTRIBUTING.md)
- [Security Policy](docs/SECURITY.md)
- [Support](docs/SUPPORT.md)

## License

The repository currently includes an MIT license notice. The licensing status
will be clarified alongside publication of the corresponding source code.

## Developer

Liao Boxuan
