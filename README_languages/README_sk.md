# CloudAI

CloudAI je multiplatformový AI asistent.

> **Stav verzie 1.0.1:** Režim Agent podporuje viackrokové úlohy a balíky aplikácie štandardne používajú formát ZIP. Predchádzajúce balíky 1.0.0 sú uložené v [archíve](../Releases/Legacy/v1.0.0/). Pozrite si [režim Agent](../docs/AGENT_MODE.md) a [obmedzenia HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Verzia 1.0.1 používa zostavenie Universal pre Intel aj Apple Silicon, zatiaľ čo archivovaný balík 1.0.0 podporuje iba Apple Silicon (`arm64`).

## Funkcie

-   AI konverzácia
-   Režim Agent pre viackrokové úlohy
-   Integrácia s Cloud AI API
-   Multiplatformová desktopová aplikácia
-   Zostavenia pre viacero architektúr
-   Grafické rozhranie
-   Podpora viacerých jazykov

## Režim Agent

Režim Agent dokáže rozdeliť cieľ na kroky, používať nástroje povolené používateľom, vykonávať autorizované zmeny a podľa možností overiť výsledok. Sám osebe neposkytuje ďalšie oprávnenia a pred citlivými alebo deštruktívnymi akciami by mal vyžiadať potvrdenie. Pozrite si [príručku režimu Agent](../docs/AGENT_MODE.md).

## Podporované platformy

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Ďalšie platformy

-   HarmonyOS
-   OpenHarmony

## Podrobnosti o platformách

| Platforma | Architektúra a stav balíkov | Inštalácia a obmedzenia |
| --- | --- | --- |
| Windows | Verzia 1.0.1 je určená pre x64 a ARM64 a štandardne používa ZIP. Archív obsahuje starší ZIP 1.0.0 pre x64. | Pred spustením ZIP úplne rozbaľte. |
| Linux | Verzia 1.0.1 je určená pre x86_64 a ARM64 a štandardne používa ZIP. Balíky 1.0.0 pre obe architektúry sú archivované. | ZIP môže obsahovať AppImage, DEB, RPM alebo TAR.GZ. AppImage vyžaduje právo na spustenie; DEB a RPM sa inštalujú správcom balíkov. |
| macOS | Verzia 1.0.1 používa Universal zostavenie pre Intel a Apple Silicon a štandardne sa distribuuje ako ZIP; 1.0.0 podporuje iba Apple Silicon (`arm64`). | Rozbaľte ZIP a získate aplikáciu. Nie je podpísaná a môže vyžadovať ručné povolenie v macOS. |
| HarmonyOS | Distribúcia 1.0.1 štandardne používa ZIP; nainštalujte kompatibilný podpísaný HAP vnútri. Archivované HAP 1.0.0 sú debug zostavenia iba pre `2in1`. | Staršie HAP sú určené pre API `60101024`. Potrebný je kompatibilný systém a platný podpis. Pozrite si [poznámky HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Distribúcia 1.0.1 štandardne používa ZIP; inštalácia vyžaduje HAP kompatibilný s OpenHarmony vnútri. | Potrebný je kompatibilný podpis a test zariadenia. Archivovaný HarmonyOS HAP 1.0.0 nepoužívajte ako balík OpenHarmony. |

## Inštalácia

### Linux

AppImage:

1.  Stiahnite a rozbaľte predvolený ZIP pre Linux a potom vyberte AppImage pre svoju architektúru.
2.  Pridajte právo na spustenie:

``` bash
chmod +x CloudAI.AppImage
```

3.  Spustite aplikáciu:

``` bash
./CloudAI.AppImage
```

Balíky .deb môžete nainštalovať pomocou:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Verzia pre macOS momentálne nie je podpísaná certifikátom Apple Developer.

Pri prvom otvorení môžu používatelia musieť aplikáciu ručne povoliť v nastaveniach zabezpečenia macOS.

### HarmonyOS

Verzia pre HarmonyOS je zostavená s oficiálnym vývojovým nástrojovým reťazcom HarmonyOS.

Vývoj a balenie prebiehajú v DevEco Studiu. Aplikácie HarmonyOS sa zostavujú ako balíky HAP/App a pred distribúciou vyžadujú správnu konfiguráciu podpisu.

## Licencia

[Licencia MIT](../LICENSE).

## Súbory open-source projektu

Informácie o licencii, dostupnosti zdrojového kódu, prispievaní a pravidlách projektu nájdete v [informáciách o open-source projekte](../docs/OPEN_SOURCE.md).

Kópia stromu zdrojového kódu CloudAI 1.0.1 je teraz dostupná v [`Source/CloudAI`](../Source/CloudAI/) a obsahuje desktopovú aplikáciu, podporu Agentov a doplnkov, baliace prostriedky a projekt HarmonyOS. Samostatný projekt HAP pre OpenHarmony, prepojenie vydaní so zdrojom, uzamknuté verzie závislostí a overené reprodukovateľné balenie stále chýbajú; podrobnosti uvádza [kontrola stavu open source](../docs/OPEN_SOURCE_STATUS.md).

## Vývojár

Liao Boxuan

## Dátum

2026-09-13
