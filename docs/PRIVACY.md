# Privacy Policy

Last updated: 2026-09-19

## Scope

This policy describes privacy considerations for the CloudAI application and
this repository. CloudAI is a client that can communicate with AI services
selected and configured by the user.

## Data sent to AI services

When a network AI provider is configured, CloudAI may send prompts, conversation
content, attachments and technical request metadata needed to process a request.
That provider processes data under its own privacy policy, retention rules and
account settings. Review those terms before sending confidential information.

Balance checks may contact account or usage endpoints operated by the selected
AI provider. When the Agent web-search action is used, the search query is sent
to DuckDuckGo. Opening an external URL connects to that destination through the
system browser. These third parties may receive ordinary network metadata such
as the user's IP address.

Agent mode may process additional files or command output that the user places
within the task's scope. Review requested actions and permissions before
allowing access to sensitive data.

Third-party plugins execute locally with the permissions of the application
process. Install only plugins you trust and review their own network and data
practices.

## Credentials and local data

API keys and service credentials are sensitive. Users should protect local
configuration and backups, avoid sharing credentials, and revoke any credential
that may have been exposed. The exact storage behavior can vary by application
version and platform.

In the included CloudAI 1.0.1 desktop, Python and C++ source, API keys are
masked in status output but stored on disk with reversible obfuscation rather
than platform-backed encryption. Anyone who can read that local file may be
able to recover the key.

Logs, crash reports and screenshots may contain prompts, paths, system details
or identifiers. Review and redact them before submitting an issue.

## Repository interactions

Information submitted to public issues, pull requests or discussions is public
and retained according to GitHub's policies. Use the private process in
[SECURITY.md](SECURITY.md) for security-sensitive information.

## Third parties

CloudAI packages may include third-party components, and users may configure
third-party AI providers. Those parties have their own terms and privacy
practices. See [Third-Party Notices](../THIRD_PARTY_NOTICES.md) for licensing
information.

## Changes and questions

Material changes to this policy should be recorded in version control. For a
non-sensitive privacy question, open a
[GitHub issue](https://github.com/liaovoxuan/CloudAI/issues). Do not place
personal or security-sensitive information in a public issue.
