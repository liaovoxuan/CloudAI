# CloudAI

CloudAI es un asistente de IA multiplataforma.

> **Estado de la versión 1.0.1:** El modo Agent admite tareas de varios pasos y los paquetes de la aplicación usan ZIP como formato predeterminado. Los paquetes 1.0.0 anteriores se conservan en el [archivo de versiones anteriores](../Releases/Legacy/v1.0.0/). Consulte el [modo Agent](../docs/AGENT_MODE.md) y las [limitaciones de HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** La versión 1.0.1 utiliza una compilación Universal compatible con Intel y Apple Silicon, mientras que el paquete 1.0.0 archivado solo admite Apple Silicon (`arm64`).

## Características

-   Conversación con IA
-   Modo Agent para tareas de varios pasos
-   Integración con la API de Cloud AI
-   Aplicación de escritorio multiplataforma
-   Compilaciones multiarquitectura
-   Interfaz gráfica
-   Soporte para varios idiomas

## Modo Agent

El modo Agent puede dividir un objetivo en pasos, utilizar las herramientas habilitadas por el usuario, realizar cambios autorizados y verificar el resultado cuando sea posible. No concede permisos adicionales y debe solicitar confirmación antes de ejecutar acciones sensibles o destructivas. Consulte la [guía del modo Agent](../docs/AGENT_MODE.md).

## Plataformas compatibles

### Escritorio

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Otras plataformas

-   HarmonyOS
-   OpenHarmony

## Detalles de las plataformas

| Plataforma | Arquitectura y estado de los paquetes | Instalación y limitaciones |
| --- | --- | --- |
| Windows | La versión 1.0.1 se dirige a x64 y ARM64 y usa ZIP de forma predeterminada. El archivo conserva el ZIP 1.0.0 antiguo para x64. | Extraiga completamente el ZIP antes de ejecutar la aplicación. |
| Linux | La versión 1.0.1 se dirige a x86_64 y ARM64 y usa ZIP de forma predeterminada. Los paquetes 1.0.0 de ambas arquitecturas están archivados. | El ZIP puede contener AppImage, DEB, RPM o TAR.GZ. AppImage requiere permiso de ejecución; DEB y RPM se instalan con el gestor de paquetes. |
| macOS | La versión 1.0.1 usa una compilación Universal para Intel y Apple Silicon y se distribuye como ZIP de forma predeterminada; 1.0.0 solo admite Apple Silicon (`arm64`). | Extraiga el ZIP para obtener la aplicación. No está firmada y puede requerir autorización manual en los ajustes de seguridad de macOS. |
| HarmonyOS | La distribución 1.0.1 usa ZIP de forma predeterminada; se instala el HAP compatible y firmado incluido. Los HAP 1.0.0 archivados son compilaciones debug limitadas a `2in1`. | Los HAP antiguos se dirigen a la API `60101024`. Se requieren un sistema compatible y una firma válida. Consulte las [notas de HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | La distribución 1.0.1 usa ZIP de forma predeterminada; la instalación requiere el HAP compatible con OpenHarmony incluido. | Se requieren firma compatible y prueba del dispositivo. No use el HAP HarmonyOS 1.0.0 archivado como paquete OpenHarmony. |

## Instalación

### Linux

AppImage:

1.  Descargue y extraiga el paquete ZIP predeterminado para Linux y seleccione el AppImage correspondiente a su arquitectura.
2.  Añada el permiso de ejecución:

``` bash
chmod +x CloudAI.AppImage
```

3.  Ejecute la aplicación:

``` bash
./CloudAI.AppImage
```

Los paquetes .deb se pueden instalar con:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

La versión para macOS actualmente no está firmada con un certificado de Apple Developer.

La primera vez que se abra, es posible que los usuarios deban permitir la aplicación manualmente en los ajustes de seguridad de macOS.

### HarmonyOS

La versión para HarmonyOS se compila con la cadena de herramientas de desarrollo oficial de HarmonyOS.

El desarrollo y el empaquetado utilizan DevEco Studio. Las aplicaciones HarmonyOS se compilan como paquetes HAP/App y requieren una configuración de firma adecuada antes de su distribución.

## Licencia

[Licencia MIT](../LICENSE).

## Archivos del proyecto de código abierto

Consulta la [información del proyecto de código abierto](../docs/OPEN_SOURCE.md) para conocer la licencia, la disponibilidad del código fuente, la guía de contribución y las políticas del proyecto.

Una copia del árbol de código fuente de CloudAI 1.0.1 ya está disponible en [`Source/CloudAI`](../Source/CloudAI/) e incluye la aplicación de escritorio, compatibilidad con Agent y complementos, recursos de empaquetado y el proyecto HarmonyOS. Aún faltan un proyecto HAP independiente para OpenHarmony, la correspondencia entre versiones publicadas y código fuente, el bloqueo de dependencias y un empaquetado reproducible verificado; consulta la [revisión del estado de código abierto](../docs/OPEN_SOURCE_STATUS.md).

## Desarrollador

Liao Boxuan

## Fecha

2026-09-13
