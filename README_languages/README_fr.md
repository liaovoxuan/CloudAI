# CloudAI

CloudAI est un assistant IA multiplateforme.

> **État de la version 1.0.1 :** le mode Agent prend en charge les tâches en plusieurs étapes et les paquets utilisent ZIP par défaut. Les anciens paquets 1.0.0 sont conservés dans les [archives](../Releases/Legacy/v1.0.0/). Consultez le [mode Agent](../docs/AGENT_MODE.md) et les [limitations de HarmonyOS](../docs/HARMONYOS.md).

> **macOS :** la version 1.0.1 utilise une compilation Universal compatible avec Intel et Apple Silicon, tandis que le paquet 1.0.0 archivé prend uniquement en charge Apple Silicon (`arm64`).

## Fonctionnalités

-   Conversation IA
-   Mode Agent pour les tâches en plusieurs étapes
-   Intégration à l’API Cloud AI
-   Application de bureau multiplateforme
-   Compilations multi-architectures
-   Interface graphique
-   Prise en charge de plusieurs langues

## Mode Agent

Le mode Agent peut décomposer un objectif en étapes, utiliser les outils activés par l’utilisateur, effectuer des modifications autorisées et vérifier le résultat lorsque cela est possible. Il n’accorde aucune autorisation supplémentaire et doit demander une confirmation avant toute action sensible ou destructive. Consultez le [guide du mode Agent](../docs/AGENT_MODE.md).

## Plateformes prises en charge

### Bureau

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Autres plateformes

-   HarmonyOS
-   OpenHarmony

## Détails des plateformes

| Plateforme | Architecture et état des paquets | Installation et limitations |
| --- | --- | --- |
| Windows | La version 1.0.1 cible x64 et ARM64 et utilise ZIP par défaut. L’archive conserve l’ancien ZIP 1.0.0 pour x64. | Extrayez complètement le ZIP avant l’exécution. |
| Linux | La version 1.0.1 cible x86_64 et ARM64 et utilise ZIP par défaut. Les paquets 1.0.0 des deux architectures sont archivés. | Le ZIP peut contenir AppImage, DEB, RPM ou TAR.GZ. AppImage nécessite le droit d’exécution ; DEB et RPM s’installent avec le gestionnaire de paquets. |
| macOS | La version 1.0.1 utilise une compilation Universal pour Intel et Apple Silicon, distribuée par défaut en ZIP ; la 1.0.0 prend uniquement en charge Apple Silicon (`arm64`). | Extrayez le ZIP pour obtenir l’application. Elle n’est pas signée et peut nécessiter une autorisation manuelle dans macOS. |
| HarmonyOS | La distribution 1.0.1 utilise ZIP par défaut ; l’installation emploie le HAP compatible et signé inclus. Les HAP 1.0.0 archivés sont des builds debug limités à `2in1`. | Les anciens HAP ciblent l’API `60101024`. Un système compatible et une signature valide sont requis. Consultez les [notes HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | La distribution 1.0.1 utilise ZIP par défaut ; l’installation nécessite le HAP compatible avec OpenHarmony inclus. | Une signature compatible et un test sur appareil sont requis. N’utilisez pas le HAP HarmonyOS 1.0.0 archivé comme paquet OpenHarmony. |

## Installation

### Linux

AppImage :

1.  Téléchargez et extrayez le paquet ZIP Linux par défaut, puis sélectionnez l’AppImage correspondant à votre architecture.
2.  Ajoutez le droit d'exécution :

``` bash
chmod +x CloudAI.AppImage
```

3.  Exécutez l'application :

``` bash
./CloudAI.AppImage
```

Les paquets .deb peuvent être installés avec :

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

La version macOS n'est actuellement pas signée avec un certificat Apple Developer.

Lors de la première ouverture, les utilisateurs peuvent avoir besoin d'autoriser manuellement l'application dans les réglages de sécurité de macOS.

### HarmonyOS

La version HarmonyOS est compilée avec la chaîne d'outils de développement officielle d'HarmonyOS.

Le développement et l'empaquetage utilisent DevEco Studio. Les applications HarmonyOS sont générées sous forme de paquets HAP/App et nécessitent une configuration de signature appropriée avant la distribution.

## Licence

[Licence MIT](../LICENSE).

## Fichiers du projet open source

Consultez les [informations sur le projet open source](../docs/OPEN_SOURCE.md) pour la licence, l'état de disponibilité du code source, le guide de contribution et les règles du projet.

Une copie de l'arborescence source de CloudAI 1.0.1 est désormais disponible dans [`Source/CloudAI`](../Source/CloudAI/). Elle comprend l'application de bureau, la prise en charge du mode Agent et des extensions, les ressources d'empaquetage et le projet HarmonyOS. Il manque encore un projet HAP OpenHarmony distinct, la correspondance entre versions publiées et source, le verrouillage des dépendances et un empaquetage reproductible vérifié ; consultez l'[état des lieux open source](../docs/OPEN_SOURCE_STATUS.md).

## Développeur

Liao Boxuan

## Date

2026-09-13
