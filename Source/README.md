# CloudAI Source Code

The complete copied CloudAI working tree is available under
[`CloudAI/`](CloudAI/). It includes the cross-platform Python desktop
application, Agent mode, plugin support, Python and C++ cores, tests,
PyInstaller definitions, required shared resources and the HarmonyOS project.

The language implementations remain separate: `CloudAI/desktop` is the Python
desktop application, `CloudAI/source/python` is the headless Python core, and
`CloudAI/source/cpp` is the canonical C++17 core used by the HarmonyOS NAPI
bridge. They are not interchangeable with the LocalAI monorepo's other native
C++ components.

| Platform | Included source |
| --- | --- |
| Windows | Python/Tk desktop application and PyInstaller definition |
| Linux | Python/Tk desktop application and PyInstaller definition |
| macOS | Python/Tk desktop application and Universal PyInstaller definition |
| HarmonyOS | ArkTS application, C++ NAPI bridge, canonical C++ core and resources |
| OpenHarmony | Desktop compatibility detection is present, but no separately configured OpenHarmony HAP project is included |

Private signing material, passwords, generated files and local runtime data
were excluded. See the [source build and security notes](CloudAI/README.md) and
the repository's [open-source status review](../docs/OPEN_SOURCE_STATUS.md).

All original CloudAI source in this directory is provided under the repository
[MIT License](../LICENSE).
