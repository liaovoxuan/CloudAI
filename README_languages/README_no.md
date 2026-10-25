# CloudAI

CloudAI er en plattformuavhengig AI-assistent.

> **Status for versjon 1.0.1:** Agent-modus støtter oppgaver med flere trinn, og applikasjonspakkene bruker ZIP som standardformat. De tidligere 1.0.0-pakkene oppbevares i [arkivet](../Releases/Legacy/v1.0.0/). Se [Agent-modus](../docs/AGENT_MODE.md) og [begrensninger for HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Versjon 1.0.1 bruker et Universal-bygg for både Intel og Apple Silicon, mens den arkiverte 1.0.0-pakken bare støtter Apple Silicon (`arm64`).

## Funksjoner

-   AI-samtale
-   Agent-modus for oppgaver med flere trinn
-   Integrasjon med Cloud AI API
-   Desktopapplikasjon for flere plattformer
-   Bygg for flere arkitekturer
-   Grafisk grensesnitt
-   Støtte for flere språk

## Agent-modus

Agent-modus kan dele et mål inn i trinn, bruke verktøy som brukeren har aktivert, utføre godkjente endringer og kontrollere resultatet når det er mulig. Modusen gir ikke ekstra tillatelser og bør be om bekreftelse før sensitive eller destruktive handlinger. Se [veiledningen for Agent-modus](../docs/AGENT_MODE.md).

## Støttede plattformer

### Stasjonær

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Andre plattformer

-   HarmonyOS
-   OpenHarmony

## Plattformdetaljer

| Plattform | Arkitektur og pakkestatus | Installasjon og begrensninger |
| --- | --- | --- |
| Windows | Versjon 1.0.1 retter seg mot x64 og ARM64 og bruker ZIP som standard. Arkivet inneholder den eldre 1.0.0-ZIP-en for x64. | Pakk ZIP helt ut før applikasjonen kjøres. |
| Linux | Versjon 1.0.1 retter seg mot x86_64 og ARM64 og bruker ZIP som standard. 1.0.0-pakker for begge arkitekturer er arkivert. | ZIP kan inneholde AppImage, DEB, RPM eller TAR.GZ. AppImage krever kjøretillatelse; DEB og RPM installeres med pakkebehandleren. |
| macOS | Versjon 1.0.1 bruker et Universal-bygg for Intel og Apple Silicon og distribueres som ZIP som standard; 1.0.0 støtter bare Apple Silicon (`arm64`). | Pakk ut ZIP for å hente applikasjonen. Den er ikke signert og kan kreve manuell tillatelse i macOS. |
| HarmonyOS | 1.0.1-distribusjonen bruker ZIP som standard; installer den kompatible signerte HAP-en i pakken. De arkiverte 1.0.0-HAP-ene er debug-bygg bare for `2in1`. | De eldre HAP-ene retter seg mot API `60101024`. Kompatibelt system og gyldig signatur kreves. Se [HarmonyOS-merknadene](../docs/HARMONYOS.md). |
| OpenHarmony | 1.0.1-distribusjonen bruker ZIP som standard; installasjon krever den OpenHarmony-kompatible HAP-en i pakken. | Kompatibel signatur og enhetstest kreves. Ikke bruk den arkiverte HarmonyOS 1.0.0-HAP-en som OpenHarmony-pakke. |

## Installasjon

### Linux

AppImage:

1.  Last ned og pakk ut standard-ZIP-pakken for Linux, og velg deretter AppImage-filen for arkitekturen din.
2.  Legg til kjøretillatelse:

``` bash
chmod +x CloudAI.AppImage
```

3.  Kjør applikasjonen:

``` bash
./CloudAI.AppImage
```

Deb-pakker kan installeres med:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS-versjonen er foreløpig ikke signert med et Apple Developer-sertifikat.

Første gang applikasjonen åpnes, kan brukerne måtte tillate den manuelt i sikkerhetsinnstillingene i macOS.

### HarmonyOS

HarmonyOS-versjonen er bygget med det offisielle HarmonyOS-utviklingsverktøysettet.

DevEco Studio brukes til utvikling og pakking. HarmonyOS-applikasjoner bygges som HAP/App-pakker og krever riktig signeringskonfigurasjon før distribusjon.

## Lisens

[MIT-lisens](../LICENSE).

## Filer for prosjektet med åpen kildekode

Se [informasjonen om prosjektet med åpen kildekode](../docs/OPEN_SOURCE.md) for lisens, status for kildekodens tilgjengelighet, bidragsveiledning og prosjektregler.

En kopi av kildetreet for CloudAI 1.0.1 er nå tilgjengelig i [`Source/CloudAI`](../Source/CloudAI/) og omfatter skrivebordsprogrammet, Agent- og programtilleggstøtte, pakkeressurser og HarmonyOS-prosjektet. Et separat OpenHarmony HAP-prosjekt, kobling mellom utgivelser og kildekode, låste avhengighetsversjoner og verifisert reproduserbar pakking mangler fortsatt; se [gjennomgangen av statusen for åpen kildekode](../docs/OPEN_SOURCE_STATUS.md).

## Utvikler

Liao Boxuan

## Dato

2026-09-13
