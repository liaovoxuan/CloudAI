# Third-Party Notices

CloudAI's original repository content is licensed under the
[MIT License](LICENSE). That license does not replace or override licenses that
apply to third-party software, services, trademarks or other materials.

## Bundled software

Application packages may include language runtimes, cryptographic libraries,
GUI toolkits, HTTP clients, certificate bundles and other dependencies. An
inspection of the archived 1.0.0 macOS package identifies components including
Python, Tcl/Tk, OpenSSL, Requests, urllib3, certifi, idna, charset-normalizer,
packaging, setuptools and py-cpuinfo. This list is informational and is not a
complete software bill of materials.

Each third-party component remains subject to its own copyright notice and
license. Redistributors must preserve every notice and license required by
those components.

## Current limitation

The copied source declares Requests, psutil, py-cpuinfo, PyInstaller and Pillow
for the desktop build. It also uses the Python and C++ standard libraries, an
optional libcurl backend, the HarmonyOS platform SDK and the HarmonyOS Hvigor
plugin. The dependency file does not pin exact Python package versions, and the
project does not yet provide a complete transitive lock or SBOM.

This repository does not currently contain a complete dependency manifest,
software bill of materials, or a verified collection of all third-party license
texts for the application packages. The legacy binaries should therefore not be
treated as a complete third-party compliance bundle.

The archive review also did not establish that every legacy package embeds the
CloudAI MIT License and all notices required by its bundled dependencies. Do
not redistribute an archived package as a self-contained compliance bundle;
include the repository [MIT License](LICENSE) and complete the dependency
license review first.

Before the next release, generate an SBOM from the corresponding source and
build environment, verify each dependency license, and place all required
notices and license texts in both the repository and distributed package. See
the [Release Checklist](docs/RELEASE_CHECKLIST.md).

Third-party product names and trademarks belong to their respective owners and
are used only for identification.
