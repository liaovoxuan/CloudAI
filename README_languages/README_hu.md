# CloudAI

CloudAI egy többplatformos AI-asszisztens.

> **Az 1.0.1-es verzió állapota:** Az Agent mód támogatja a többlépéses feladatokat, az alkalmazáscsomagok alapértelmezett formátuma pedig ZIP. A korábbi 1.0.0-s csomagokat a [régi verziók archívuma](../Releases/Legacy/v1.0.0/) őrzi. Lásd az [Agent mód](../docs/AGENT_MODE.md) és a [HarmonyOS korlátozásainak](../docs/HARMONYOS.md) leírását.

> **macOS:** Az 1.0.1-es verzió Intel és Apple Silicon rendszert egyaránt támogató Universal buildet használ, míg az archivált 1.0.0-s csomag csak az Apple Silicon (`arm64`) rendszert támogatja.

## Funkciók

-   AI-beszélgetés
-   Agent mód többlépéses feladatokhoz
-   Cloud AI API-integráció
-   Többplatformos asztali alkalmazás
-   Többarchitektúrás buildek
-   Grafikus felület
-   Többnyelvű támogatás

## Agent mód

Az Agent mód lépésekre bonthatja a célt, használhatja a felhasználó által engedélyezett eszközöket, jogosult módosításokat végezhet, és lehetőség szerint ellenőrizheti az eredményt. Önmagában nem biztosít további jogosultságokat, és érzékeny vagy romboló műveletek előtt megerősítést kell kérnie. Lásd az [Agent mód útmutatóját](../docs/AGENT_MODE.md).

## Támogatott platformok

### Asztali

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Egyéb platformok

-   HarmonyOS
-   OpenHarmony

## Platformrészletek

| Platform | Architektúra és csomagállapot | Telepítés és korlátozások |
| --- | --- | --- |
| Windows | Az 1.0.1 x64 és ARM64 architektúrát céloz, alapértelmezett formátuma ZIP. Az archívum megőrzi a régi x64-es 1.0.0 ZIP-et. | Futtatás előtt teljesen bontsa ki a ZIP-et. |
| Linux | Az 1.0.1 x86_64 és ARM64 architektúrát céloz, alapértelmezett formátuma ZIP. Mindkét architektúra 1.0.0-s csomagja archiválva van. | A ZIP AppImage, DEB, RPM vagy TAR.GZ kiadást tartalmazhat. Az AppImage futtatási jogot igényel; a DEB és RPM csomagkezelővel telepíthető. |
| macOS | Az 1.0.1 Intel és Apple Silicon rendszert támogató Universal build, alapértelmezett ZIP-kiadással; az 1.0.0 csak Apple Silicon (`arm64`) rendszert támogat. | Bontsa ki a ZIP-et az alkalmazás eléréséhez. Az alkalmazás nincs aláírva, ezért kézi engedélyezésre lehet szükség a macOS-ben. |
| HarmonyOS | Az 1.0.1 alapértelmezett kiadása ZIP; telepítéshez a benne lévő kompatibilis, aláírt HAP használható. Az archivált 1.0.0-s HAP-ok csak `2in1` típusra készült debug buildek. | A régi HAP-ok az `60101024` API-t célozzák. Kompatibilis rendszer és érvényes aláírás szükséges. Lásd a [HarmonyOS-megjegyzéseket](../docs/HARMONYOS.md). |
| OpenHarmony | Az 1.0.1 alapértelmezett kiadása ZIP; telepítéshez a benne lévő OpenHarmony-kompatibilis HAP szükséges. | Kompatibilis aláírás és eszközteszt szükséges. Az archivált HarmonyOS 1.0.0 HAP nem használható OpenHarmony-csomagként. |

## Telepítés

### Linux

AppImage:

1.  Töltse le és bontsa ki az alapértelmezett Linux ZIP-csomagot, majd válassza ki az architektúrájának megfelelő AppImage-fájlt.
2.  Adja hozzá a futtatási jogot:

``` bash
chmod +x CloudAI.AppImage
```

3.  Indítsa el az alkalmazást:

``` bash
./CloudAI.AppImage
```

A .deb csomagok így telepíthetők:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

A macOS-verzió jelenleg nincs Apple Developer-tanúsítvánnyal aláírva.

Az első megnyitáskor előfordulhat, hogy a felhasználóknak kézzel kell engedélyezniük az alkalmazást a macOS biztonsági beállításaiban.

### HarmonyOS

A HarmonyOS-verzió a hivatalos HarmonyOS fejlesztői eszközkészlettel készül.

A fejlesztés és a csomagolás a DevEco Studióban történik. A HarmonyOS-alkalmazások HAP/App csomagként épülnek fel, és a terjesztés előtt megfelelő aláírási konfigurációt igényelnek.

## Licenc

[MIT-licenc](../LICENSE).

## A nyílt forráskódú projekt fájljai

A licencet, a forráskód elérhetőségi állapotát, a közreműködési útmutatót és a projekt szabályzatait a [nyílt forráskódú projekt információi](../docs/OPEN_SOURCE.md) ismertetik.

A CloudAI 1.0.1 forrásfájának másolata már elérhető a [`Source/CloudAI`](../Source/CloudAI/) könyvtárban. Tartalmazza az asztali alkalmazást, az Agent- és bővítménytámogatást, a csomagolási erőforrásokat és a HarmonyOS-projektet. Egy külön OpenHarmony HAP-projekt, a kiadások forráshoz rendelése, a zárolt függőségi verziók és az ellenőrzött reprodukálható csomagolás továbbra is hiányzik; lásd a [nyílt forráskódú állapot áttekintését](../docs/OPEN_SOURCE_STATUS.md).

## Fejlesztő

Liao Boxuan

## Dátum

2026-09-13
