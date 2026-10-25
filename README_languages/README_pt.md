# CloudAI

CloudAI é um assistente de IA multiplataforma.

> **Estado da versão 1.0.1:** O modo Agent suporta tarefas com várias etapas e os pacotes da aplicação utilizam ZIP por predefinição. Os pacotes 1.0.0 anteriores são mantidos no [arquivo](../Releases/Legacy/v1.0.0/). Consulte o [modo Agent](../docs/AGENT_MODE.md) e as [limitações do HarmonyOS](../docs/HARMONYOS.md).

> **macOS:** A versão 1.0.1 utiliza uma compilação Universal para Intel e Apple Silicon, enquanto o pacote 1.0.0 arquivado suporta apenas Apple Silicon (`arm64`).

## Funcionalidades

-   Conversa com IA
-   Modo Agent para tarefas com vários passos
-   Integração com a API Cloud AI
-   Aplicação desktop multiplataforma
-   Compilações multi-arquitetura
-   Interface gráfica
-   Suporte para vários idiomas

## Modo Agent

O modo Agent pode dividir um objetivo em passos, utilizar as ferramentas ativadas pelo utilizador, efetuar alterações autorizadas e verificar o resultado sempre que possível. Não concede permissões adicionais e deve pedir confirmação antes de ações sensíveis ou destrutivas. Consulte o [guia do modo Agent](../docs/AGENT_MODE.md).

## Plataformas suportadas

### Desktop

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### Outras plataformas

-   HarmonyOS
-   OpenHarmony

## Detalhes das plataformas

| Plataforma | Arquitetura e estado dos pacotes | Instalação e limitações |
| --- | --- | --- |
| Windows | A versão 1.0.1 destina-se a x64 e ARM64 e utiliza ZIP por predefinição. O arquivo mantém o ZIP 1.0.0 antigo para x64. | Extraia totalmente o ZIP antes de executar. |
| Linux | A versão 1.0.1 destina-se a x86_64 e ARM64 e utiliza ZIP por predefinição. Os pacotes 1.0.0 de ambas as arquiteturas estão arquivados. | O ZIP pode conter AppImage, DEB, RPM ou TAR.GZ. AppImage requer permissão de execução; DEB e RPM são instalados com o gestor de pacotes. |
| macOS | A versão 1.0.1 utiliza uma compilação Universal para Intel e Apple Silicon e é distribuída como ZIP por predefinição; 1.0.0 suporta apenas Apple Silicon (`arm64`). | Extraia o ZIP para obter a aplicação. Não está assinada e poderá exigir autorização manual no macOS. |
| HarmonyOS | A distribuição 1.0.1 utiliza ZIP por predefinição; instale o HAP compatível e assinado incluído. Os HAP 1.0.0 arquivados são compilações debug apenas para `2in1`. | Os HAP antigos destinam-se à API `60101024`. São necessários sistema compatível e assinatura válida. Consulte as [notas HarmonyOS](../docs/HARMONYOS.md). |
| OpenHarmony | A distribuição 1.0.1 utiliza ZIP por predefinição; a instalação exige o HAP compatível com OpenHarmony incluído. | São necessários assinatura compatível e teste do dispositivo. Não utilize o HAP HarmonyOS 1.0.0 arquivado como pacote OpenHarmony. |

## Instalação

### Linux

AppImage:

1.  Transfira e extraia o pacote ZIP predefinido para Linux e selecione o AppImage correspondente à sua arquitetura.
2.  Adicione a permissão de execução:

``` bash
chmod +x CloudAI.AppImage
```

3.  Execute a aplicação:

``` bash
./CloudAI.AppImage
```

Os pacotes .deb podem ser instalados com:

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

A versão para macOS atualmente não está assinada com um certificado Apple Developer.

Ao abrir pela primeira vez, os utilizadores podem precisar de permitir a aplicação manualmente nas definições de segurança do macOS.

### HarmonyOS

A versão HarmonyOS é compilada com a cadeia de ferramentas de desenvolvimento oficial do HarmonyOS.

O desenvolvimento e o empacotamento utilizam o DevEco Studio. As aplicações HarmonyOS são criadas como pacotes HAP/App e exigem uma configuração de assinatura adequada antes da distribuição.

## Licença

[Licença MIT](../LICENSE).

## Ficheiros do projeto de código aberto

Consulte as [informações do projeto de código aberto](../docs/OPEN_SOURCE.md) para conhecer a licença, o estado de disponibilidade do código-fonte, o guia de contribuição e as políticas do projeto.

Uma cópia da árvore de código-fonte do CloudAI 1.0.1 está agora disponível em [`Source/CloudAI`](../Source/CloudAI/) e inclui a aplicação para computador, o suporte a Agentes e plug-ins, os recursos de empacotamento e o projeto HarmonyOS. Continuam em falta um projeto HAP separado para OpenHarmony, a correspondência entre versões e código-fonte, versões de dependências bloqueadas e um processo de empacotamento reprodutível verificado; consulte a [análise do estado do código aberto](../docs/OPEN_SOURCE_STATUS.md).

## Programador

Liao Boxuan

## Data

2026-09-13
