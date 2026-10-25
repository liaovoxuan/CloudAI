# CloudAI

CloudAI è un assistente IA multipiattaforma.

> **Stato della versione 1.0.1:** la modalità Agent supporta attività in più passaggi e i pacchetti dell’applicazione usano ZIP come formato predefinito. I precedenti pacchetti 1.0.0 sono conservati nell’[archivio](../Releases/Legacy/v1.0.0/). Consultate la [modalità Agent](../docs/AGENT_MODE.md) e le [limitazioni di HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** La versione 1.0.1 utilizza una build Universal per Intel e Apple Silicon, mentre il pacchetto 1.0.0 archiviato supporta solo Apple Silicon (`arm64`).

## Funzionalità

-   Conversazione IA
-   Modalità Agent per attività in più passaggi
-   Integrazione con l'API Cloud AI
-   Applicazione desktop multipiattaforma
-   Compilazioni multi-architettura
-   Interfaccia grafica
-   Supporto per più lingue

## Modalità Agent

La modalità Agent può suddividere un obiettivo in più passaggi, utilizzare gli strumenti abilitati dall’utente, apportare modifiche autorizzate e verificare il risultato quando possibile. Non concede autorizzazioni aggiuntive e deve chiedere conferma prima di eseguire azioni sensibili o distruttive. Consultate la [guida alla modalità Agent](../docs/AGENT_MODE.md).

## Piattaforme supportate

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Altre piattaforme

-   HarmonyOS
-   OpenHarmony

## Dettagli delle piattaforme

| Piattaforma | Architettura e stato dei pacchetti | Installazione e limitazioni |
| --- | --- | --- |
| Windows | La versione 1.0.1 è destinata a x64 e ARM64 e usa ZIP per impostazione predefinita. L’archivio conserva il vecchio ZIP 1.0.0 per x64. | Estraete completamente lo ZIP prima dell’avvio. |
| Linux | La versione 1.0.1 è destinata a x86_64 e ARM64 e usa ZIP per impostazione predefinita. I pacchetti 1.0.0 per entrambe le architetture sono archiviati. | Lo ZIP può contenere AppImage, DEB, RPM o TAR.GZ. AppImage richiede il permesso di esecuzione; DEB e RPM si installano con il gestore pacchetti. |
| macOS | La versione 1.0.1 usa una build Universal per Intel e Apple Silicon, distribuita in ZIP per impostazione predefinita; 1.0.0 supporta solo Apple Silicon (`arm64`). | Estraete lo ZIP per ottenere l’applicazione. Non è firmata e può richiedere l’autorizzazione manuale in macOS. |
| HarmonyOS | La distribuzione 1.0.1 usa ZIP per impostazione predefinita; l’installazione usa l’HAP compatibile e firmato incluso. Gli HAP 1.0.0 archiviati sono build debug limitate a `2in1`. | I vecchi HAP sono destinati all’API `60101024`. Sono necessari un sistema compatibile e una firma valida. Consultate le [note HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | La distribuzione 1.0.1 usa ZIP per impostazione predefinita; l’installazione richiede l’HAP compatibile con OpenHarmony incluso. | Sono necessari firma compatibile e test del dispositivo. Non usate l’HAP HarmonyOS 1.0.0 archiviato come pacchetto OpenHarmony. |

## Installazione

### Linux

AppImage:

1.  Scaricate ed estraete il pacchetto ZIP predefinito per Linux, quindi selezionate l’AppImage adatto alla vostra architettura.
2.  Aggiungete il permesso di esecuzione:

``` bash
chmod +x CloudAI.AppImage
```

3.  Avviate l'applicazione:

``` bash
./CloudAI.AppImage
```

I pacchetti .deb possono essere installati con:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

La versione per macOS al momento non è firmata con un certificato Apple Developer.

Al primo avvio, gli utenti potrebbero dover autorizzare manualmente l'applicazione nelle impostazioni di sicurezza di macOS.

### HarmonyOS

La versione per HarmonyOS è compilata con la toolchain di sviluppo ufficiale di HarmonyOS.

Lo sviluppo e il confezionamento utilizzano DevEco Studio. Le applicazioni HarmonyOS vengono compilate come pacchetti HAP/App e richiedono una corretta configurazione della firma prima della distribuzione.

## Licenza

[Licenza MIT](../LICENSE).

## File del progetto open source

Consulta le [informazioni sul progetto open source](../docs/OPEN_SOURCE.md) per la licenza, lo stato di disponibilità del codice sorgente, la guida per contribuire e le norme del progetto.

Una copia dell'albero dei sorgenti di CloudAI 1.0.1 è ora disponibile in [`Source/CloudAI`](../Source/CloudAI/) e include l'applicazione desktop, il supporto per Agent e plugin, le risorse di pacchettizzazione e il progetto HarmonyOS. Mancano ancora un progetto HAP OpenHarmony separato, la corrispondenza tra release e sorgente, le versioni bloccate delle dipendenze e una pacchettizzazione riproducibile verificata; consulta la [verifica dello stato open source](../docs/OPEN_SOURCE_STATUS.md).

## Sviluppatore

Liao Boxuan

## Data

2026-09-13
