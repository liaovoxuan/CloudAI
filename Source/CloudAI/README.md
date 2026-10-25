# CloudAI 1.0.1 Source

This directory is a sanitized copy of the CloudAI source working tree. It
was copied from the `projects/CloudAI` subproject of the LocalAI monorepo; the
monorepo's unrelated `shared/native` LocalAI C++ implementations are not part
of CloudAI. It contains:

- `desktop/`: the Python/Tk desktop application, Agent mode and plugin host;
- `source/python/`: the headless standard-library Python implementation and
  tests;
- `source/cpp/`: the C++17 core, CLI and CTest smoke test;
- `harmonyos/`: the ArkTS application, NAPI bridge and HarmonyOS resources;
- `packaging/`: PyInstaller definitions for Windows, Linux and macOS;
- `plugin_examples/`: a minimal third-party plugin example; and
- `shared/`: default configuration, version metadata and icons required by the
  packaging definitions.

The packaging definitions also include this directory's MIT `LICENSE`,
`THIRD_PARTY_NOTICES.md` and the multilingual `resources/PRIVACY.md` policy.

## Python and C++ boundaries

| Path | Language | Responsibility |
| --- | --- | --- |
| `desktop/*.py` | Python | Tk desktop GUI, Agent runner and plugin host; this is the desktop packaging entry point. |
| `source/python/` | Python | Dependency-free headless CloudAI core, CLI behavior and Python tests. It is separate from the Tk desktop application. |
| `source/cpp/` | C++17 | Canonical native core, CLI and CTest smoke test. |
| `harmonyos/entry/src/main/ets/` | ArkTS | HarmonyOS UI and HTTP lifecycle. |
| `harmonyos/entry/src/main/cpp/` | C++/NAPI | HarmonyOS bridge; it links the canonical C++ core from `source/cpp/`. |

Do not substitute the Python implementation for the C++ core, or copy the
LocalAI monorepo's other native libraries into this project. The two CloudAI
core implementations intentionally have separate source and test directories.

## Quick verification

Run the dependency-free Python and C++ core tests from this directory:

```bash
PYTHONPATH=source/python python3 -m unittest source/python/test_cloudai.py
PYTHONPATH=desktop python3 -m unittest desktop/test_cloudai_plugins.py
cmake -S source/cpp -B /tmp/cloudai-cpp-build
cmake --build /tmp/cloudai-cpp-build
ctest --test-dir /tmp/cloudai-cpp-build --output-on-failure
```

The desktop GUI and PyInstaller packaging require the packages listed in
`requirements.txt`. The HarmonyOS application requires a compatible HarmonyOS
SDK and DevEco Studio; see [`harmonyos/README.md`](harmonyos/README.md).

## Credentials and signing

No API keys, release signing keys, certificates, profiles or passwords are
included. The HarmonyOS build profile is deliberately unsigned. Configure
signing only in your local environment and never commit signing material.

The current API-key stores use reversible obfuscation for compatibility; this
is not platform-backed encryption. Do not use production credentials until the
storage implementation has been migrated to an appropriate operating-system
credential store.

The bundled multilingual privacy policy is synchronized with the repository
policy and documents network AI providers, Agent web search, third-party
plugins and reversible credential storage. Review it again whenever application
data flows change.

All original CloudAI source in this directory is provided under the repository
[MIT License](LICENSE).
