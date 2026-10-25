# CloudAI

CloudAI ist ein plattformübergreifender KI-Assistent.

> **Versionsstatus 1.0.1:** Der Agent-Modus unterstützt mehrstufige Aufgaben; Anwendungspakete verwenden standardmäßig ZIP. Die bisherigen 1.0.0-Pakete befinden sich im [Archiv älterer Versionen](../Releases/Legacy/v1.0.0/). Siehe [Agent-Modus](../docs/AGENT_MODE.md) und [HarmonyOS-Einschränkungen](../docs/HARMONYOS.md).

> **macOS:** Version 1.0.1 verwendet einen Universal-Build für Intel und Apple Silicon, während das archivierte Paket der Version 1.0.0 nur Apple Silicon (`arm64`) unterstützt.

## Funktionen

-   KI-Konversation
-   Agent-Modus für mehrstufige Aufgaben
-   Integration der Cloud-AI-API
-   Plattformübergreifende Desktop-Anwendung
-   Builds für mehrere Architekturen
-   Grafische Benutzeroberfläche
-   Unterstützung mehrerer Sprachen

## Agent-Modus

Der Agent-Modus kann ein Ziel in Schritte aufteilen, vom Benutzer aktivierte Werkzeuge verwenden, autorisierte Änderungen durchführen und das Ergebnis nach Möglichkeit überprüfen. Er gewährt keine zusätzlichen Berechtigungen und sollte vor sensiblen oder destruktiven Aktionen eine Bestätigung anfordern. Weitere Informationen enthält der [Leitfaden zum Agent-Modus](../docs/AGENT_MODE.md).

## Unterstützte Plattformen

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Andere Plattformen

-   HarmonyOS
-   OpenHarmony

## Plattformdetails

| Plattform | Architektur- und Paketstatus | Installation und Einschränkungen |
| --- | --- | --- |
| Windows | Version 1.0.1 zielt auf x64 und ARM64 und verwendet standardmäßig ZIP. Das Archiv enthält die ältere 1.0.0-ZIP für x64. | Das ZIP muss vor dem Start vollständig entpackt werden. |
| Linux | Version 1.0.1 zielt auf x86_64 und ARM64 und verwendet standardmäßig ZIP. 1.0.0-Pakete für beide Architekturen sind archiviert. | Das ZIP kann AppImage-, DEB-, RPM- oder TAR.GZ-Distributionen enthalten. AppImage benötigt Ausführungsrechte; DEB und RPM werden mit der Paketverwaltung installiert. |
| macOS | Version 1.0.1 verwendet einen Universal-Build für Intel und Apple Silicon und wird standardmäßig als ZIP verteilt; Version 1.0.0 unterstützt nur Apple Silicon (`arm64`). | Durch Entpacken des ZIP erhält man die Anwendung. Sie ist nicht signiert und muss möglicherweise in den macOS-Sicherheitseinstellungen manuell zugelassen werden. |
| HarmonyOS | Die 1.0.1-Ausgabe verwendet standardmäßig ZIP; installiert wird das kompatible signierte HAP aus dem Paket. Die archivierten 1.0.0-HAPs sind auf `2in1` beschränkte Debug-Builds. | Die älteren HAPs zielen auf API `60101024`. Installation erfordert ein kompatibles System und eine gültige Signatur. Siehe [HarmonyOS-Hinweise](../docs/HARMONYOS.md). |
| OpenHarmony | Die 1.0.1-Ausgabe verwendet standardmäßig ZIP; installiert wird ein OpenHarmony-kompatibles HAP aus dem Paket. | Eine kompatible Signatur und ein Gerätetest sind erforderlich. Das archivierte HarmonyOS-1.0.0-HAP darf nicht als OpenHarmony-Paket verwendet werden. |

## Installation

### Linux

AppImage:

1.  Laden Sie das standardmäßige Linux-ZIP-Paket herunter, entpacken Sie es und wählen Sie das AppImage für Ihre Architektur aus.
2.  Fügen Sie die Ausführungsberechtigung hinzu:

``` bash
chmod +x CloudAI.AppImage
```

3.  Starten Sie die Anwendung:

``` bash
./CloudAI.AppImage
```

Deb-Pakete lassen sich so installieren:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Die macOS-Version ist derzeit nicht mit einem Apple-Developer-Zertifikat signiert.

Beim ersten Öffnen müssen Benutzer die Anwendung möglicherweise in den Sicherheitseinstellungen von macOS manuell zulassen.

### HarmonyOS

Die HarmonyOS-Version wird mit der offiziellen HarmonyOS-Entwicklungstoolchain erstellt.

Für Entwicklung und Paketierung wird DevEco Studio verwendet. HarmonyOS-Anwendungen werden als HAP/App-Pakete erstellt und erfordern vor der Verteilung eine ordnungsgemäße Signaturkonfiguration.

## Lizenz

[MIT-Lizenz](../LICENSE).

## Open-Source-Projektdateien

Die [Open-Source-Projektinformationen](../docs/OPEN_SOURCE.md) enthalten die Lizenz, den Status der Quellcodeverfügbarkeit, den Beitragsleitfaden und die Projektrichtlinien.

Eine Kopie des CloudAI-1.0.1-Quellbaums ist jetzt unter [`Source/CloudAI`](../Source/CloudAI/) verfügbar und enthält die Desktop-Anwendung, Agent- und Plugin-Unterstützung, Paketierungsressourcen sowie das HarmonyOS-Projekt. Ein separates OpenHarmony-HAP-Projekt, die Zuordnung von Veröffentlichungen zum Quellcode, gesperrte Abhängigkeitsversionen und eine verifizierte reproduzierbare Paketierung fehlen weiterhin; siehe [Open-Source-Statusprüfung](../docs/OPEN_SOURCE_STATUS.md).

## Entwickler

Liao Boxuan

## Datum

2026-09-13
