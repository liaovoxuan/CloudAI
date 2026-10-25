# CloudAI

CloudAI är en plattformsoberoende AI-assistent.

> **Status för version 1.0.1:** Agent-läget stöder uppgifter med flera steg och applikationspaketen använder ZIP som standardformat. De tidigare 1.0.0-paketen bevaras i [arkivet](../Releases/Legacy/v1.0.0/). Se [Agent-läget](../docs/AGENT_MODE.md) och [begränsningarna för HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Version 1.0.1 använder ett Universal-bygge för Intel och Apple Silicon, medan det arkiverade 1.0.0-paketet endast stöder Apple Silicon (`arm64`).

## Funktioner

-   AI-konversation
-   Agentläge för uppgifter i flera steg
-   Integrering med Cloud AI API
-   Skrivbordsprogram för flera plattformar
-   Byggen för flera arkitekturer
-   Grafiskt gränssnitt
-   Stöd för flera språk

## Agentläge

Agentläget kan dela upp ett mål i steg, använda verktyg som användaren har aktiverat, utföra godkända ändringar och kontrollera resultatet när det är möjligt. Läget ger inte ytterligare behörigheter och bör begära bekräftelse före känsliga eller destruktiva åtgärder. Se [guiden för Agentläget](../docs/AGENT_MODE.md).

## Plattformar som stöds

### Skrivbord

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Andra plattformar

-   HarmonyOS
-   OpenHarmony

## Plattformsdetaljer

| Plattform | Arkitektur och paketstatus | Installation och begränsningar |
| --- | --- | --- |
| Windows | Version 1.0.1 riktar sig mot x64 och ARM64 och använder ZIP som standard. Arkivet innehåller den äldre 1.0.0-ZIP-filen för x64. | Packa upp ZIP helt före körning. |
| Linux | Version 1.0.1 riktar sig mot x86_64 och ARM64 och använder ZIP som standard. 1.0.0-paket för båda arkitekturerna är arkiverade. | ZIP kan innehålla AppImage, DEB, RPM eller TAR.GZ. AppImage kräver körbehörighet; DEB och RPM installeras med pakethanteraren. |
| macOS | Version 1.0.1 använder ett Universal-bygge för Intel och Apple Silicon och distribueras som ZIP som standard; 1.0.0 stöder endast Apple Silicon (`arm64`). | Packa upp ZIP för att hämta programmet. Det är inte signerat och kan behöva tillåtas manuellt i macOS. |
| HarmonyOS | 1.0.1-distributionen använder ZIP som standard; installera den kompatibla signerade HAP-filen i paketet. Arkiverade 1.0.0-HAP är debug-byggen endast för `2in1`. | Äldre HAP riktar sig mot API `60101024`. Kompatibelt system och giltig signatur krävs. Se [HarmonyOS-kommentarerna](../docs/HARMONYOS.md). |
| OpenHarmony | 1.0.1-distributionen använder ZIP som standard; installation kräver den OpenHarmony-kompatibla HAP-filen i paketet. | Kompatibel signatur och enhetstest krävs. Använd inte arkiverad HarmonyOS 1.0.0-HAP som OpenHarmony-paket. |

## Installation

### Linux

AppImage:

1.  Ladda ner och packa upp standard-ZIP-paketet för Linux och välj sedan AppImage-filen för din arkitektur.
2.  Lägg till körbehörighet:

``` bash
chmod +x CloudAI.AppImage
```

3.  Kör programmet:

``` bash
./CloudAI.AppImage
```

Deb-paket kan installeras med:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS-versionen är för närvarande inte signerad med ett Apple Developer-certifikat.

Första gången programmet öppnas kan användarna behöva tillåta det manuellt i säkerhetsinställningarna i macOS.

### HarmonyOS

HarmonyOS-versionen är byggd med den officiella utvecklingsverktygskedjan för HarmonyOS.

DevEco Studio används för utveckling och paketering. HarmonyOS-program byggs som HAP/App-paket och kräver korrekt signeringskonfiguration före distribution.

## Licens

[MIT-licens](../LICENSE).

## Filer för projektet med öppen källkod

Se [informationen om projektet med öppen källkod](../docs/OPEN_SOURCE.md) för licens, källkodens tillgänglighet, bidragsguide och projektpolicyer.

En kopia av källkodsträdet för CloudAI 1.0.1 finns nu i [`Source/CloudAI`](../Source/CloudAI/) och omfattar skrivbordsprogrammet, stöd för Agenter och insticksprogram, paketeringsresurser samt HarmonyOS-projektet. Ett separat HAP-projekt för OpenHarmony, koppling mellan utgåvor och källkod, låsta beroendeversioner och verifierad reproducerbar paketering saknas fortfarande; se [granskningen av statusen för öppen källkod](../docs/OPEN_SOURCE_STATUS.md).

## Utvecklare

Liao Boxuan

## Datum

2026-09-13
