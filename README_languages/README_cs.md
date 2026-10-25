# CloudAI

CloudAI je multiplatformní AI asistent.

> **Stav verze 1.0.1:** Režim Agent podporuje vícekrokové úlohy a balíčky aplikace jsou standardně distribuovány jako ZIP. Předchozí balíčky 1.0.0 jsou uloženy v [archivu starších verzí](../Releases/Legacy/v1.0.0/). Viz [režim Agent](../docs/AGENT_MODE.md) a [omezení HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Verze 1.0.1 používá sestavení Universal pro Intel i Apple Silicon, zatímco archivovaný balíček verze 1.0.0 podporuje pouze Apple Silicon (`arm64`).

## Funkce

-   AI konverzace
-   Režim Agent pro vícekrokové úlohy
-   Integrace s Cloud AI API
-   Multiplatformní desktopová aplikace
-   Sestavení pro více architektur
-   Grafické uživatelské rozhraní
-   Podpora více jazyků

## Režim Agent

Režim Agent dokáže rozdělit cíl do jednotlivých kroků, používat nástroje povolené uživatelem, provádět autorizované změny a podle možností ověřit výsledek. Sám o sobě neposkytuje další oprávnění a před citlivými nebo destruktivními akcemi by měl vyžádat potvrzení. Viz [průvodce režimem Agent](../docs/AGENT_MODE.md).

## Podporované platformy

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Další platformy

-   HarmonyOS
-   OpenHarmony

## Podrobnosti o platformách

| Platforma | Architektura a stav balíčků | Instalace a omezení |
| --- | --- | --- |
| Windows | Verze 1.0.1 cílí na x64 a ARM64 a standardně používá ZIP. Archiv obsahuje starší ZIP 1.0.0 pro x64. | ZIP je nutné před spuštěním aplikace úplně rozbalit. |
| Linux | Verze 1.0.1 cílí na x86_64 a ARM64 a standardně používá ZIP. Balíčky 1.0.0 pro obě architektury jsou archivovány. | ZIP může obsahovat AppImage, DEB, RPM nebo TAR.GZ. AppImage vyžaduje právo ke spuštění; DEB a RPM se instalují správcem balíčků systému. |
| macOS | Verze 1.0.1 používá Universal sestavení pro Intel a Apple Silicon a standardně se distribuuje jako ZIP; starší 1.0.0 podporuje pouze Apple Silicon (`arm64`). | Rozbalením ZIP získáte aplikaci. Aplikace není podepsaná a může vyžadovat ruční povolení v nastavení zabezpečení macOS. |
| HarmonyOS | Distribuce 1.0.1 standardně používá ZIP; instalace používá kompatibilní podepsaný HAP uvnitř balíčku. Archivované HAP 1.0.0 jsou debug sestavení omezená na `2in1`. | Starší HAP cílí na API `60101024`. Instalace vyžaduje kompatibilní systém a platný podpis. Viz [poznámky k HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Distribuce 1.0.1 standardně používá ZIP; instalace vyžaduje HAP kompatibilní s OpenHarmony uvnitř balíčku. | Je nutný kompatibilní podpis a test zařízení. Archivovaný HarmonyOS HAP 1.0.0 nepoužívejte jako balíček OpenHarmony. |

## Instalace

### Linux

AppImage:

1.  Stáhněte a rozbalte výchozí ZIP pro Linux a poté vyberte AppImage pro svou architekturu.
2.  Přidejte právo na spuštění:

``` bash
chmod +x CloudAI.AppImage
```

3.  Spusťte aplikaci:

``` bash
./CloudAI.AppImage
```

Balíčky .deb lze nainstalovat pomocí:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Verze pro macOS momentálně není podepsána certifikátem Apple Developer.

Při prvním otevření mohou uživatelé muset aplikaci ručně povolit v nastavení zabezpečení macOS.

### HarmonyOS

Verze pro HarmonyOS je sestavena s oficiální vývojovou sadou nástrojů HarmonyOS.

Vývoj a balení probíhají v DevEco Studiu. Aplikace HarmonyOS se sestavují jako balíčky HAP/App a před distribucí vyžadují správnou konfiguraci podpisu.

## Licence

[Licence MIT](../LICENSE).

## Soubory open-source projektu

Informace o licenci, dostupnosti zdrojového kódu, přispívání a pravidlech projektu najdete v [informacích o open-source projektu](../docs/OPEN_SOURCE.md).

Kopie stromu zdrojového kódu CloudAI 1.0.1 je nyní dostupná v [`Source/CloudAI`](../Source/CloudAI/) a zahrnuje desktopovou aplikaci, podporu režimu Agent a pluginů, prostředky pro balení a projekt HarmonyOS. Stále chybí samostatný projekt HAP pro OpenHarmony, vazba vydaných artefaktů na zdroj, uzamčené verze závislostí a ověřené reprodukovatelné balení; podrobnosti uvádí [kontrola stavu open source](../docs/OPEN_SOURCE_STATUS.md).

## Vývojář

Liao Boxuan

## Datum

2026-09-13
