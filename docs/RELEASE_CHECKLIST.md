# Release Checklist

Complete this checklist before publishing a CloudAI release.

## Source and version

- [ ] The complete source for the release is committed and tagged.
- [ ] `VERSION`, changelogs and all translated README files agree.
- [ ] Build and packaging steps reproduce every artifact from the tag.
- [ ] No credentials, private keys, local paths or personal data are included.

## Dependencies and licensing

- [ ] Dependency manifests and lock files are current.
- [ ] An SBOM is generated for every platform package.
- [ ] Third-party licenses are reviewed for compatibility and obligations.
- [ ] Required copyright notices and license texts are included in packages.
- [ ] The CloudAI MIT License is included in source and binary distributions.

## Security and privacy

- [ ] Supported dependency and toolchain versions are used.
- [ ] Packages are scanned for known vulnerabilities and accidental secrets.
- [ ] Credential storage, network destinations and update behavior are tested.
- [ ] Security and privacy documentation reflects actual behavior.
- [ ] The privacy document bundled with the app matches `docs/PRIVACY.md`.

## Platform verification

- [ ] Windows x64 and ARM64 packages are tested on their advertised systems.
- [ ] Linux x86_64 and ARM64 formats install, run and uninstall correctly.
- [ ] The macOS Universal binary is verified with both `arm64` and `x86_64`
      slices, signed or clearly documented as unsigned, and tested on both.
- [ ] HarmonyOS and OpenHarmony packages use the intended device types, API
      range, release mode, version code and valid signing configuration.
- [ ] Default ZIP archives extract cleanly and contain the documented files.

## Publication

- [ ] SHA-256 checksums are generated and independently verified.
- [ ] Artifact names include version, platform and architecture where useful.
- [ ] Each artifact records its source tag or commit.
- [ ] Previous packages are moved to the versioned legacy archive.
- [ ] Release notes document known limitations and upgrade impact.
