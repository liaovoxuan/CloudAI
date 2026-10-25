# CloudAI

CloudAI はクロスプラットフォームの AI アシスタントです。

> **バージョン 1.0.1 の状況：** Agent モードは複数ステップのタスクに対応し、アプリケーションパッケージは既定で ZIP 形式を使用します。以前の 1.0.0 パッケージは[旧バージョンのアーカイブ](../Releases/Legacy/v1.0.0/)に保存されています。[Agent モード](../docs/AGENT_MODE.md)および [HarmonyOS の制限事項](../docs/HARMONYOS.md)を参照してください。

> **macOS：** バージョン 1.0.1 は Intel と Apple Silicon の両方に対応する Universal ビルドを使用します。アーカイブされた 1.0.0 パッケージは Apple Silicon（`arm64`）のみに対応しています。

## 機能

-   AI 対話
-   複数ステップのタスクに対応する Agent モード
-   クラウド AI API 連携
-   マルチプラットフォーム対応のデスクトップアプリケーション
-   複数アーキテクチャ向けビルド
-   グラフィカルインターフェース
-   多言語対応

## Agent モード

Agent モードは、目標を複数のステップに分け、ユーザーが有効にしたツールを使用し、許可された範囲で変更を行い、可能な場合は結果を検証できます。このモード自体が追加の権限を与えることはなく、機密性の高い操作や破壊的な操作の前には確認を求める必要があります。詳しくは [Agent モードガイド](../docs/AGENT_MODE.md)を参照してください。

## 対応プラットフォーム

### デスクトップ

-   Windows x64
-   Windows ARM64
-   macOS Universal (Intel + Apple Silicon) — v1.0.1
-   macOS Apple Silicon — legacy v1.0.0
-   Linux x86_64
-   Linux ARM64

### その他のプラットフォーム

-   HarmonyOS
-   OpenHarmony

## プラットフォームの詳細

| プラットフォーム | アーキテクチャとパッケージの状況 | インストール方法と制限事項 |
| --- | --- | --- |
| Windows | 1.0.1 は x64 と ARM64 を対象とし、既定で ZIP を使用します。アーカイブには旧版 1.0.0 の x64 ZIP が保存されています。 | 実行前に ZIP を完全に展開してください。 |
| Linux | 1.0.1 は x86_64 と ARM64 を対象とし、既定で ZIP を使用します。両アーキテクチャの 1.0.0 パッケージがアーカイブされています。 | ZIP には AppImage、DEB、RPM、TAR.GZ のいずれかが含まれます。AppImage には実行権限が必要で、DEB と RPM はパッケージマネージャーでインストールします。 |
| macOS | 1.0.1 は Intel と Apple Silicon 用の Universal ビルドで、既定で ZIP 配布です。1.0.0 は Apple Silicon（`arm64`）のみに対応します。 | ZIP を展開してアプリケーションを取得します。未署名のため、macOS で手動の許可が必要になる場合があります。 |
| HarmonyOS | 1.0.1 は既定で ZIP 配布され、同梱の互換性がある署名済み HAP をインストールします。アーカイブされた 1.0.0 HAP は `2in1` 専用の debug ビルドです。 | 旧版 HAP は API `60101024` を対象とします。互換システムと有効な署名が必要です。[HarmonyOS の注意事項](../docs/HARMONYOS.md)を参照してください。 |
| OpenHarmony | 1.0.1 は既定で ZIP 配布され、同梱の OpenHarmony 対応 HAP をインストールします。 | 対応する署名と実機テストが必要です。アーカイブされた HarmonyOS 1.0.0 HAP は使用しないでください。 |

## インストール

### Linux

AppImage:

1.  既定の Linux 用 ZIP パッケージをダウンロードして展開し、使用するアーキテクチャに合う AppImage を選択します。
2.  実行権限を付与します：

``` bash
chmod +x CloudAI.AppImage
```

3.  アプリケーションを起動します：

``` bash
./CloudAI.AppImage
```

Deb パッケージは次のコマンドでインストールできます：

``` bash
sudo apt install ./CloudAI.deb
```

### macOS

macOS 版は現在、Apple Developer の証明書による署名が行われていません。

初回起動時には、macOS のセキュリティ設定でアプリケーションを手動で許可する必要がある場合があります。

### HarmonyOS

HarmonyOS 版は公式の HarmonyOS 開発ツールチェーンでビルドされています。

開発とパッケージングには DevEco Studio を使用します。HarmonyOS アプリケーションは HAP/App パッケージとしてビルドされ、配布前に適切な署名設定が必要です。

## ライセンス

[MIT ライセンス](../LICENSE)。

## オープンソースプロジェクトのファイル

ライセンス、ソースコードの公開状況、コントリビューションガイドおよびプロジェクトポリシーについては、[オープンソースプロジェクト情報](../docs/OPEN_SOURCE.md)を参照してください。

CloudAI 1.0.1 のソースツリー一式を [`Source/CloudAI`](../Source/CloudAI/) に追加しました。デスクトップアプリケーション、Agent とプラグインのサポート、パッケージ用リソース、HarmonyOS プロジェクトが含まれます。独立した OpenHarmony HAP プロジェクト、リリース成果物とソースの対応付け、依存関係のバージョン固定、検証済みの再現可能なパッケージ手順はまだありません。詳細は[オープンソース状況の確認結果](../docs/OPEN_SOURCE_STATUS.md)を参照してください。

## 開発者

Liao Boxuan

## 日付

2026-09-13
