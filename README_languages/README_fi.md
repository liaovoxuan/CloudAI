# CloudAI

CloudAI on monialustainen tekoälyavustaja.

> **Version 1.0.1 tila:** Agent-tila tukee monivaiheisia tehtäviä, ja sovelluspakettien oletusmuoto on ZIP. Aiemmat 1.0.0-paketit säilytetään [vanhojen versioiden arkistossa](../Releases/Legacy/v1.0.0/). Katso [Agent-tila](../docs/AGENT_MODE.md) ja [HarmonyOS-rajoitukset](../docs/HARMONYOS.md).

> **macOS:** Versio 1.0.1 käyttää sekä Inteliä että Apple Siliconia tukevaa Universal-koontiversiota, kun taas arkistoitu 1.0.0-paketti tukee vain Apple Siliconia (`arm64`).

## Ominaisuudet

-   Tekoälykeskustelu
-   Agent-tila monivaiheisiin tehtäviin
-   Cloud AI API -integraatio
-   Monialustainen työpöytäsovellus
-   Usean arkkitehtuurin koontiversiot
-   Graafinen käyttöliittymä
-   Monikielinen tuki

## Agent-tila

Agent-tila voi jakaa tavoitteen vaiheisiin, käyttää käyttäjän käyttöön ottamia työkaluja, tehdä valtuutettuja muutoksia ja tarkistaa tuloksen mahdollisuuksien mukaan. Tila ei itsessään anna lisäoikeuksia, ja sen tulee pyytää vahvistus ennen arkaluonteisia tai tuhoavia toimia. Katso [Agent-tilan opas](../docs/AGENT_MODE.md).

## Tuetut alustat

### Työpöytä

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Muut alustat

-   HarmonyOS
-   OpenHarmony

## Alustojen tiedot

| Alusta | Arkkitehtuuri ja pakettien tila | Asennus ja rajoitukset |
| --- | --- | --- |
| Windows | Versio 1.0.1 kohdistuu x64- ja ARM64-arkkitehtuureihin ja käyttää oletuksena ZIP-muotoa. Arkistossa on vanha x64-version 1.0.0 ZIP. | Pura ZIP kokonaan ennen sovelluksen käynnistämistä. |
| Linux | Versio 1.0.1 kohdistuu x86_64- ja ARM64-arkkitehtuureihin ja käyttää oletuksena ZIP-muotoa. Molempien arkkitehtuurien 1.0.0-paketit on arkistoitu. | ZIP voi sisältää AppImage-, DEB-, RPM- tai TAR.GZ-jakelun. AppImage tarvitsee suoritusoikeuden; DEB ja RPM asennetaan paketinhallinnalla. |
| macOS | Versio 1.0.1 käyttää Intel- ja Apple Silicon -järjestelmiä tukevaa Universal-koontiversiota ja oletuksena ZIP-jakelua; 1.0.0 tukee vain Apple Siliconia (`arm64`). | Pura ZIP saadaksesi sovelluksen. Sitä ei ole allekirjoitettu, joten se voidaan joutua sallimaan macOS:n tietoturva-asetuksissa. |
| HarmonyOS | Version 1.0.1 jakelu käyttää oletuksena ZIP-muotoa; asennukseen käytetään paketin yhteensopivaa allekirjoitettua HAP-tiedostoa. Arkistoidut 1.0.0-HAPit ovat vain `2in1`-laitteille tarkoitettuja debug-koonteja. | Vanhat HAPit kohdistuvat API-versioon `60101024`. Asennus vaatii yhteensopivan järjestelmän ja kelvollisen allekirjoituksen. Katso [HarmonyOS-huomautukset](../docs/HARMONYOS.md). |
| OpenHarmony | Version 1.0.1 jakelu käyttää oletuksena ZIP-muotoa; asennus vaatii paketin OpenHarmony-yhteensopivan HAP-tiedoston. | Yhteensopiva allekirjoitus ja laitetestaus ovat tarpeen. Älä käytä arkistoitua HarmonyOS 1.0.0 HAP -tiedostoa OpenHarmony-pakettina. |

## Asennus

### Linux

AppImage:

1.  Lataa ja pura Linuxin oletusarvoinen ZIP-paketti ja valitse sitten arkkitehtuurillesi sopiva AppImage.
2.  Lisää suoritusoikeus:

``` bash
chmod +x CloudAI.AppImage
```

3.  Käynnistä sovellus:

``` bash
./CloudAI.AppImage
```

Deb-paketit voi asentaa komennolla:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS-versiota ei tällä hetkellä ole allekirjoitettu Apple Developer -varmenteella.

Ensimmäisellä avauskerralla käyttäjän on ehkä sallittava sovellus manuaalisesti macOS:n tietoturva-asetuksissa.

### HarmonyOS

HarmonyOS-versio on rakennettu HarmonyOS:n virallisilla kehitystyökaluilla.

Kehityksessä ja paketoinnissa käytetään DevEco Studiota. HarmonyOS-sovellukset rakennetaan HAP/App-paketeiksi, ja ne edellyttävät asianmukaista allekirjoitusmääritystä ennen jakelua.

## Lisenssi

[MIT-lisenssi](../LICENSE).

## Avoimen lähdekoodin projektitiedostot

[Avoimen lähdekoodin projektitiedoissa](../docs/OPEN_SOURCE.md) kuvataan lisenssi, lähdekoodin saatavuus, osallistumisohjeet ja projektin käytännöt.

CloudAI 1.0.1:n lähdekoodipuun kopio on nyt hakemistossa [`Source/CloudAI`](../Source/CloudAI/). Se sisältää työpöytäsovelluksen, Agent- ja liitännäistuen, paketointiresurssit sekä HarmonyOS-projektin. Erillinen OpenHarmony HAP -projekti, julkaisujen yhdistäminen lähdekoodiin, lukitut riippuvuusversiot ja varmennettu toistettava paketointi puuttuvat edelleen; katso [avoimen lähdekoodin tilan tarkistus](../docs/OPEN_SOURCE_STATUS.md).

## Kehittäjä

Liao Boxuan

## Päivämäärä

2026-09-13
