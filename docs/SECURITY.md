# Security Policy

## Supported versions

| Version | Security support |
| --- | --- |
| 1.0.1 | Supported |
| 1.0.0 and earlier | Legacy; no routine security fixes |

Only the latest release line is supported. Legacy packages are retained for
historical reference and should not be used where current security support is
required.

## Known credential-storage limitation

The included CloudAI 1.0.1 desktop, Python and C++ implementations store API
keys separately from public provider settings and mask them in status output,
but the compatible on-disk format uses reversible obfuscation rather than a
platform-backed keystore. Treat the local secret file as sensitive and avoid
production credentials until each application uses an appropriate operating-
system credential store.

## Reporting a vulnerability

Do not report vulnerabilities in a public issue. Submit a
[private vulnerability report](https://github.com/liaovoxuan/CloudAI/security/advisories/new)
with:

- affected version, operating system, architecture and package format;
- a description of the impact and affected component;
- reproducible steps or a minimal proof of concept;
- relevant sanitized logs, screenshots or crash information;
- any known mitigations; and
- your preferred credit, if any.

Do not include real API keys, access tokens, private prompts or personal data.
Use placeholders or test credentials.

If GitHub private vulnerability reporting is unavailable, open a minimal public
issue asking for a private security contact. Do not include vulnerability
details in that issue.

## Response and disclosure

Maintainers aim to acknowledge a report within seven calendar days and provide
a status update within 30 days. These are targets, not a service-level
guarantee. Please allow a reasonable remediation period before public
disclosure. The project will coordinate disclosure and credit with the reporter
when practical.

## Scope

Reports about CloudAI code, packaging, credential handling, update mechanisms
and bundled dependencies are in scope. Vulnerabilities solely in a third-party
AI provider or operating system should be reported to that vendor, but CloudAI
integration issues that expose users remain in scope.
