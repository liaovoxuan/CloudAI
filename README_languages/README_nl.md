# CloudAI

CloudAI is een platformonafhankelijke AI-assistent.

> **Status van versie 1.0.1:** De Agent-modus ondersteunt taken met meerdere stappen en de applicatiepakketten gebruiken standaard ZIP. De eerdere 1.0.0-pakketten worden bewaard in het [archief](../Releases/Legacy/v1.0.0/). Zie de [Agent-modus](../docs/AGENT_MODE.md) en de [HarmonyOS-beperkingen](../docs/HARMONYOS.md).

> **macOS:** Versie 1.0.1 gebruikt een Universal-build voor Intel en Apple Silicon, terwijl het gearchiveerde pakket van versie 1.0.0 alleen Apple Silicon (`arm64`) ondersteunt.

## Functies

-   AI-gesprek
-   Agent-modus voor taken met meerdere stappen
-   Integratie met de Cloud AI API
-   Platformonafhankelijke desktopapplicatie
-   Builds voor meerdere architecturen
-   Grafische interface
-   Ondersteuning voor meerdere talen

## Agent-modus

De Agent-modus kan een doel in stappen opdelen, door de gebruiker ingeschakelde hulpmiddelen gebruiken, toegestane wijzigingen uitvoeren en het resultaat waar mogelijk verifiëren. De modus verleent geen extra bevoegdheden en moet om bevestiging vragen vóór gevoelige of destructieve handelingen. Zie de [handleiding voor de Agent-modus](../docs/AGENT_MODE.md).

## Ondersteunde platforms

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Andere platforms

-   HarmonyOS
-   OpenHarmony

## Platformdetails

| Platform | Architectuur en pakketstatus | Installatie en beperkingen |
| --- | --- | --- |
| Windows | Versie 1.0.1 is gericht op x64 en ARM64 en gebruikt standaard ZIP. Het archief bevat de oudere 1.0.0-ZIP voor x64. | Pak de ZIP volledig uit voordat u de applicatie start. |
| Linux | Versie 1.0.1 is gericht op x86_64 en ARM64 en gebruikt standaard ZIP. 1.0.0-pakketten voor beide architecturen zijn gearchiveerd. | De ZIP kan AppImage, DEB, RPM of TAR.GZ bevatten. AppImage vereist uitvoerrechten; DEB en RPM worden met pakketbeheer geïnstalleerd. |
| macOS | Versie 1.0.1 gebruikt een Universal-build voor Intel en Apple Silicon en wordt standaard als ZIP verspreid; 1.0.0 ondersteunt alleen Apple Silicon (`arm64`). | Pak de ZIP uit om de applicatie te verkrijgen. Deze is niet ondertekend en moet mogelijk handmatig worden toegestaan in macOS. |
| HarmonyOS | De 1.0.1-distributie gebruikt standaard ZIP; installeer de compatibele ondertekende HAP uit het pakket. De gearchiveerde 1.0.0-HAP's zijn debug-builds voor alleen `2in1`. | De oudere HAP's zijn gericht op API `60101024`. Een compatibel systeem en geldige ondertekening zijn vereist. Zie de [HarmonyOS-opmerkingen](../docs/HARMONYOS.md). |
| OpenHarmony | De 1.0.1-distributie gebruikt standaard ZIP; installatie vereist de OpenHarmony-compatibele HAP uit het pakket. | Compatibele ondertekening en een apparaattest zijn vereist. Gebruik de gearchiveerde HarmonyOS 1.0.0-HAP niet als OpenHarmony-pakket. |

## Installatie

### Linux

AppImage:

1.  Download en pak het standaard Linux-ZIP-pakket uit en kies vervolgens de AppImage voor uw architectuur.
2.  Voeg uitvoerrechten toe:

``` bash
chmod +x CloudAI.AppImage
```

3.  Start de applicatie:

``` bash
./CloudAI.AppImage
```

Deb-pakketten kunnen worden geïnstalleerd met:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

De macOS-versie is momenteel niet ondertekend met een Apple Developer-certificaat.

Bij de eerste keer openen moeten gebruikers de applicatie mogelijk handmatig toestaan in de beveiligingsinstellingen van macOS.

### HarmonyOS

De HarmonyOS-versie is gebouwd met de officiële HarmonyOS-ontwikkeltoolchain.

Voor de ontwikkeling en het maken van pakketten wordt DevEco Studio gebruikt. HarmonyOS-applicaties worden gebouwd als HAP/App-pakketten en vereisen een juiste ondertekeningsconfiguratie vóór distributie.

## Licentie

[MIT-licentie](../LICENSE).

## Open-sourceprojectbestanden

Raadpleeg de [informatie over het open-sourceproject](../docs/OPEN_SOURCE.md) voor de licentie, de beschikbaarheid van de broncode, de bijdragehandleiding en het projectbeleid.

Een kopie van de CloudAI 1.0.1-bronboom is nu beschikbaar in [`Source/CloudAI`](../Source/CloudAI/) en bevat de desktoptoepassing, Agent- en pluginondersteuning, pakketbronnen en het HarmonyOS-project. Een afzonderlijk OpenHarmony HAP-project, de koppeling tussen releases en broncode, vergrendelde afhankelijkheidsversies en geverifieerde reproduceerbare pakketbouw ontbreken nog; zie de [beoordeling van de open-sourcestatus](../docs/OPEN_SOURCE_STATUS.md).

## Ontwikkelaar

Liao Boxuan

## Datum

2026-09-13
