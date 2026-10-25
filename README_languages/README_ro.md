# CloudAI

CloudAI este un asistent AI pentru mai multe platforme.

> **Starea versiunii 1.0.1:** Modul Agent acceptă activități cu mai mulți pași, iar pachetele aplicației folosesc implicit formatul ZIP. Pachetele 1.0.0 anterioare sunt păstrate în [arhivă](../Releases/Legacy/v1.0.0/). Consultați [modul Agent](../docs/AGENT_MODE.md) și [limitările HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** Versiunea 1.0.1 folosește un build Universal pentru Intel și Apple Silicon, în timp ce pachetul 1.0.0 arhivat acceptă numai Apple Silicon (`arm64`).

## Caracteristici

-   Conversație cu AI
-   Mod Agent pentru sarcini în mai mulți pași
-   Integrare cu API-ul Cloud AI
-   Aplicație desktop multiplatformă
-   Build-uri pentru mai multe arhitecturi
-   Interfață grafică
-   Suport pentru mai multe limbi

## Mod Agent

Modul Agent poate împărți un obiectiv în pași, poate utiliza instrumentele activate de utilizator, poate efectua modificări autorizate și poate verifica rezultatul atunci când este posibil. Nu acordă permisiuni suplimentare și trebuie să solicite confirmare înainte de acțiuni sensibile sau distructive. Consultați [ghidul modului Agent](../docs/AGENT_MODE.md).

## Platforme acceptate

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Alte platforme

-   HarmonyOS
-   OpenHarmony

## Detalii despre platforme

| Platformă | Arhitectură și starea pachetelor | Instalare și limitări |
| --- | --- | --- |
| Windows | Versiunea 1.0.1 vizează x64 și ARM64 și folosește implicit ZIP. Arhiva păstrează vechiul ZIP 1.0.0 pentru x64. | Extrageți complet ZIP-ul înainte de rulare. |
| Linux | Versiunea 1.0.1 vizează x86_64 și ARM64 și folosește implicit ZIP. Pachetele 1.0.0 pentru ambele arhitecturi sunt arhivate. | ZIP-ul poate conține AppImage, DEB, RPM sau TAR.GZ. AppImage necesită permisiune de executare; DEB și RPM se instalează cu managerul de pachete. |
| macOS | Versiunea 1.0.1 folosește un build Universal pentru Intel și Apple Silicon și este distribuită implicit ca ZIP; 1.0.0 acceptă doar Apple Silicon (`arm64`). | Extrageți ZIP-ul pentru a obține aplicația. Nu este semnată și poate necesita autorizare manuală în macOS. |
| HarmonyOS | Distribuția 1.0.1 folosește implicit ZIP; instalați HAP-ul compatibil și semnat inclus. HAP-urile 1.0.0 arhivate sunt build-uri debug doar pentru `2in1`. | HAP-urile vechi vizează API-ul `60101024`. Sunt necesare un sistem compatibil și o semnătură validă. Consultați [notele HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | Distribuția 1.0.1 folosește implicit ZIP; instalarea necesită HAP-ul compatibil cu OpenHarmony inclus. | Sunt necesare o semnătură compatibilă și testarea dispozitivului. Nu utilizați HAP-ul HarmonyOS 1.0.0 arhivat ca pachet OpenHarmony. |

## Instalare

### Linux

AppImage:

1.  Descărcați și extrageți pachetul ZIP implicit pentru Linux, apoi selectați AppImage-ul corespunzător arhitecturii dvs.
2.  Adăugați permisiunea de executare:

``` bash
chmod +x CloudAI.AppImage
```

3.  Rulați aplicația:

``` bash
./CloudAI.AppImage
```

Pachetele .deb pot fi instalate cu:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

Versiunea pentru macOS nu este momentan semnată cu un certificat Apple Developer.

La prima deschidere, utilizatorii ar putea fi nevoiți să permită manual aplicația în setările de securitate din macOS.

### HarmonyOS

Versiunea pentru HarmonyOS este construită cu lanțul oficial de instrumente de dezvoltare HarmonyOS.

Dezvoltarea și împachetarea folosesc DevEco Studio. Aplicațiile HarmonyOS sunt construite ca pachete HAP/App și necesită o configurație corectă de semnare înainte de distribuire.

## Licență

[Licență MIT](../LICENSE).

## Fișierele proiectului cu sursă deschisă

Consultați [informațiile proiectului cu sursă deschisă](../docs/OPEN_SOURCE.md) pentru licență, starea disponibilității codului sursă, ghidul de contribuție și politicile proiectului.

O copie a arborelui sursă CloudAI 1.0.1 este acum disponibilă în [`Source/CloudAI`](../Source/CloudAI/) și include aplicația desktop, suportul pentru Agenți și extensii, resursele de împachetare și proiectul HarmonyOS. Un proiect HAP separat pentru OpenHarmony, asocierea versiunilor publicate cu sursa, versiunile blocate ale dependențelor și împachetarea reproductibilă verificată lipsesc în continuare; consultați [evaluarea stării sursei deschise](../docs/OPEN_SOURCE_STATUS.md).

## Dezvoltator

Liao Boxuan

## Data

2026-09-13
