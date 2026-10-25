# CloudAI

CloudAI er en tværplatforms AI-assistent.

> **Status for version 1.0.1:** Agent-tilstand understøtter opgaver med flere trin, og applikationspakkerne bruger ZIP som standardformat. De tidligere 1.0.0-pakker opbevares i [arkivet over ældre versioner](../Releases/Legacy/v1.0.0/). Se [Agent-tilstand](../docs/AGENT_MODE.md) og [begrænsninger for HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Version 1.0.1 bruger et Universal-build til både Intel og Apple Silicon, mens den arkiverede 1.0.0-pakke kun understøtter Apple Silicon (`arm64`).

## Funktioner

-   AI-samtale
-   Agent-tilstand til opgaver med flere trin
-   Integration med Cloud AI API
-   Desktopapplikation til flere platforme
-   Builds til flere arkitekturer
-   Grafisk brugergrænseflade
-   Understøttelse af flere sprog

## Agent-tilstand

Agent-tilstand kan opdele et mål i trin, bruge de værktøjer, som brugeren har aktiveret, foretage godkendte ændringer og så vidt muligt kontrollere resultatet. Tilstanden giver ikke i sig selv yderligere rettigheder og bør anmode om bekræftelse før følsomme eller destruktive handlinger. Se [vejledningen til Agent-tilstand](../docs/AGENT_MODE.md).

## Understøttede platforme

### Skrivebord

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Andre platforme

-   HarmonyOS
-   OpenHarmony

## Platformdetaljer

| Platform | Arkitektur og pakkestatus | Installation og begrænsninger |
| --- | --- | --- |
| Windows | Version 1.0.1 er målrettet x64 og ARM64 og bruger ZIP som standard. Arkivet indeholder den ældre 1.0.0-ZIP til x64. | Pak ZIP helt ud, før applikationen køres. |
| Linux | Version 1.0.1 er målrettet x86_64 og ARM64 og bruger ZIP som standard. 1.0.0-pakker til begge arkitekturer er arkiveret. | ZIP kan indeholde AppImage, DEB, RPM eller TAR.GZ. AppImage kræver køretilladelse; DEB og RPM installeres med systemets pakkehåndtering. |
| macOS | Version 1.0.1 bruger et Universal-build til Intel og Apple Silicon og distribueres som standard som ZIP; den ældre 1.0.0 understøtter kun Apple Silicon (`arm64`). | Pak ZIP ud for at få applikationen. Den er ikke signeret og kan kræve manuel tilladelse i macOS' sikkerhedsindstillinger. |
| HarmonyOS | 1.0.1-distributionen bruger ZIP som standard; installationen bruger den kompatible signerede HAP i pakken. De arkiverede 1.0.0-HAP'er er debug-builds begrænset til `2in1`. | De ældre HAP'er er målrettet API `60101024`. Installation kræver et kompatibelt system og en gyldig signatur. Se [HarmonyOS-noterne](../docs/HARMONYOS.md). |
| OpenHarmony | 1.0.1-distributionen bruger ZIP som standard; installation kræver en OpenHarmony-kompatibel HAP fra pakken. | En kompatibel signatur og enhedstest er påkrævet. Brug ikke den arkiverede HarmonyOS 1.0.0-HAP som OpenHarmony-pakke. |

## Installation

### Linux

AppImage:

1.  Download og udpak standard-ZIP-pakken til Linux, og vælg derefter AppImage-filen til din arkitektur.
2.  Tilføj køretilladelse:

``` bash
chmod +x CloudAI.AppImage
```

3.  Kør applikationen:

``` bash
./CloudAI.AppImage
```

Deb-pakker kan installeres med:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS-versionen er i øjeblikket ikke signeret med et Apple Developer-certifikat.

Første gang applikationen åbnes, kan brugerne være nødt til at tillade den manuelt i sikkerhedsindstillingerne i macOS.

### HarmonyOS

HarmonyOS-versionen er bygget med det officielle HarmonyOS-udviklingsværktøjssæt.

Udvikling og pakning foregår i DevEco Studio. HarmonyOS-applikationer bygges som HAP/App-pakker og kræver en korrekt signeringskonfiguration før distribution.

## Licens

[MIT-licens](../LICENSE).

## Filer til open source-projektet

Se [oplysninger om open source-projektet](../docs/OPEN_SOURCE.md) for licens, status for kildekodens tilgængelighed, bidragsvejledning og projektpolitikker.

En kopi af CloudAI 1.0.1-kildetræet findes nu i [`Source/CloudAI`](../Source/CloudAI/) og omfatter skrivebordsprogrammet, Agent- og pluginunderstøttelse, pakkeressourcer og HarmonyOS-projektet. Et særskilt OpenHarmony HAP-projekt, kobling mellem udgivelser og kildekode, låste afhængigheder og verificeret reproducerbar pakning mangler stadig; se [gennemgangen af open source-status](../docs/OPEN_SOURCE_STATUS.md).

## Udvikler

Liao Boxuan

## Dato

2026-09-13
