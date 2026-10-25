# HarmonyOS Release Notes

The version 1.0.1 application package uses ZIP as its default distribution
format. For HarmonyOS, extract the archive and install its compatible, signed
HAP. The existing 1.0.0 HAP files have been moved to the legacy archive so that
they are not presented as current releases.

## Known limitations of the archived packages

- The packages declare only the `2in1` device type.
- Their metadata identifies them as debug builds.
- They target HarmonyOS API version `60101024` and may not install on
  incompatible systems.
- Distribution may require a signing configuration accepted by the target
  device.

A future HarmonyOS release should be rebuilt from source in release mode, use
the intended device types and API compatibility range, receive a valid version
code and signature, and be tested on each advertised device category.

## Source project

The sanitized CloudAI 1.0.1 HarmonyOS project is available under
[`Source/CloudAI/harmonyos`](../Source/CloudAI/harmonyos/). It contains the ArkTS shell, NAPI
bridge, resources and shared C++ core. Its metadata declares version `1.0.1`,
HarmonyOS 6.1.1 (API 24), `arm64-v8a`, and the `phone`, `tablet` and `2in1`
device types.

The C++ core and smoke test build successfully with CMake. A full HAP build and
device test were not run in this repository environment because they require a
compatible HarmonyOS SDK, DevEco Studio and local signing configuration. The
source has not been mapped to an existing ZIP or HAP artifact, so it must not be
used as proof that an existing binary is reproducible.

All private signing material and passwords found beside the original project
were excluded. Configure a new or authorized signing identity locally. The
current API-key file uses reversible encoding rather than a platform-backed
keystore; read the [source security note](../Source/CloudAI/harmonyos/README.md#security-note)
before using it with production credentials.
