# CloudAI

CloudAI to wieloplatformowy asystent AI.

> **Stan wersji 1.0.1:** Tryb Agent obsługuje zadania wieloetapowe, a pakiety aplikacji domyślnie korzystają z formatu ZIP. Poprzednie pakiety 1.0.0 są przechowywane w [archiwum](../Releases/Legacy/v1.0.0/). Zobacz opis [trybu Agent](../docs/AGENT_MODE.md) i [ograniczeń HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Wersja 1.0.1 korzysta z kompilacji Universal dla procesorów Intel i Apple Silicon, natomiast zarchiwizowany pakiet 1.0.0 obsługuje wyłącznie Apple Silicon (`arm64`).

## Funkcje

-   Rozmowa z AI
-   Tryb Agent do zadań wieloetapowych
-   Integracja z Cloud AI API
-   Wieloplatformowa aplikacja desktopowa
-   Kompilacje dla wielu architektur
-   Interfejs graficzny
-   Obsługa wielu języków

## Tryb Agent

Tryb Agent może podzielić cel na kroki, korzystać z narzędzi włączonych przez użytkownika, wprowadzać autoryzowane zmiany i w miarę możliwości weryfikować wynik. Sam w sobie nie nadaje dodatkowych uprawnień i powinien prosić o potwierdzenie przed działaniami wrażliwymi lub destrukcyjnymi. Zobacz [przewodnik po trybie Agent](../docs/AGENT_MODE.md).

## Obsługiwane platformy

### Komputery stacjonarne

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Inne platformy

-   HarmonyOS
-   OpenHarmony

## Szczegóły platform

| Platforma | Architektura i stan pakietów | Instalacja i ograniczenia |
| --- | --- | --- |
| Windows | Wersja 1.0.1 jest przeznaczona dla x64 i ARM64 i domyślnie używa ZIP. Archiwum zawiera starszy ZIP 1.0.0 dla x64. | Przed uruchomieniem całkowicie rozpakuj ZIP. |
| Linux | Wersja 1.0.1 jest przeznaczona dla x86_64 i ARM64 i domyślnie używa ZIP. Pakiety 1.0.0 dla obu architektur są zarchiwizowane. | ZIP może zawierać AppImage, DEB, RPM lub TAR.GZ. AppImage wymaga prawa do wykonywania; DEB i RPM instaluje się menedżerem pakietów. |
| macOS | Wersja 1.0.1 korzysta z kompilacji Universal dla Intel i Apple Silicon i domyślnie jest dystrybuowana jako ZIP; 1.0.0 obsługuje tylko Apple Silicon (`arm64`). | Rozpakuj ZIP, aby uzyskać aplikację. Nie jest podpisana i może wymagać ręcznego zezwolenia w macOS. |
| HarmonyOS | Dystrybucja 1.0.1 domyślnie używa ZIP; instaluje się zawarty w nim zgodny i podpisany HAP. Zarchiwizowane HAP 1.0.0 to kompilacje debug tylko dla `2in1`. | Starsze HAP są przeznaczone dla API `60101024`. Wymagane są zgodny system i prawidłowy podpis. Zobacz [uwagi HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Dystrybucja 1.0.1 domyślnie używa ZIP; instalacja wymaga zawartego w nim HAP zgodnego z OpenHarmony. | Wymagane są zgodny podpis i test urządzenia. Nie używaj zarchiwizowanego HAP HarmonyOS 1.0.0 jako pakietu OpenHarmony. |

## Instalacja

### Linux

AppImage:

1.  Pobierz i rozpakuj domyślny pakiet ZIP dla systemu Linux, a następnie wybierz AppImage odpowiedni dla swojej architektury.
2.  Dodaj prawo do wykonywania:

``` bash
chmod +x CloudAI.AppImage
```

3.  Uruchom aplikację:

``` bash
./CloudAI.AppImage
```

Pakiety .deb można zainstalować za pomocą:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Wersja na macOS nie jest obecnie podpisana certyfikatem Apple Developer.

Przy pierwszym uruchomieniu może być konieczne ręczne zezwolenie aplikacji w ustawieniach zabezpieczeń systemu macOS.

### HarmonyOS

Wersja na HarmonyOS jest budowana za pomocą oficjalnego zestawu narzędzi deweloperskich HarmonyOS.

Do tworzenia i pakowania służy DevEco Studio. Aplikacje HarmonyOS są budowane jako pakiety HAP/App i wymagają prawidłowej konfiguracji podpisu przed dystrybucją.

## Licencja

[Licencja MIT](../LICENSE).

## Pliki projektu open source

Informacje o licencji, dostępności kodu źródłowego, zasadach współtworzenia i politykach projektu znajdują się w [informacjach o projekcie open source](../docs/OPEN_SOURCE.md).

Kopia drzewa źródłowego CloudAI 1.0.1 jest teraz dostępna w [`Source/CloudAI`](../Source/CloudAI/) i obejmuje aplikację komputerową, obsługę Agentów i wtyczek, zasoby do pakowania oraz projekt HarmonyOS. Nadal brakuje oddzielnego projektu HAP dla OpenHarmony, powiązania wydań ze źródłem, zablokowanych wersji zależności oraz zweryfikowanego, powtarzalnego procesu pakowania; zobacz [przegląd stanu open source](../docs/OPEN_SOURCE_STATUS.md).

## Deweloper

Liao Boxuan

## Data

2026-09-13
