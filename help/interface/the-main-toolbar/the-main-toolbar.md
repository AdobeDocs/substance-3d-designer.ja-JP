---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: Substance 3D Designerのメインツールバーについて説明します。このメインツールバーから、一般的なワークフローのツールやコマンドにアクセスできます。
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: メインツールバー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# メインツールバー

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

メインウィンドウの左上に表示される[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)のメインツールバーとメニューについて説明します。ドロップダウンメインメニューとクイックアクセスボタンの2つの部分で構成されています。 すべてのクイックアクセスボタン機能には、<b>ファイル</b>および<b>編集</b>メニューからもアクセスできます。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![メインツールバー](../../assets/mainmenu.png "メインツールバー")

</td>
</tr>
</table>

## クイックアクセスボタン

![](../../assets/newsubstance.png) <b>新しいSubstanceグラフ…:</b> (Ctrl + N) [新しいグラフ](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)ウィンドウを表示し、[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)で新しいパッケージを作成します。

![](../../assets/open.png) <b>開く…:</b> (Ctrl+O)既存の[Substanceパッケージ(.SBS、.SBSAR、.SBSASM)](../../getting-started/overview/overview.md)を開きます。

![](../../assets/saveall.png) <b>すべて保存：</b> (Ctrl+⇧+S) [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)に一覧表示されているすべてのパッケージを保存します。

![](../../assets/undo.png) <b>取り消し：</b> (Ctrl+Z)最後に行った操作を取り消します。

![](../../assets/redo.png) <b>やり直し：</b> (Ctrl + Y)最後に取り消した操作をやり直します。

## ファイル

<b>新規：</b>は、グラフまたはパッケージを作成するためのサブメニューを開きます。

* <b>新しいグラフ...:</b>(Ctrl+N) [新しいグラフ](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)ウィンドウが表示され、新しい[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)を設定できます。
* <b>新しいSubstance関数グラフ:</b> [Substance関数グラフ](../../function-graphs/function-graphs.md)を使用して新しいパッケージを作成します；
* <b>空：</b>空のパッケージを作成します。

<b>開く…:</b> (Ctrl+O)既存の[Substanceパッケージ(.SBS、.SBSAR、.SBSASM)](../../getting-started/overview/overview.md)を開きます。

<b>最近使用したパッケージ：</b>最近使用したパッケージの一覧を表示します。 エントリをクリックして開きます。

<b>最後のセッションパッケージ(#)を開く</b>：最後のセッションが終了したとき、または終了したときに開いていたすべてのパッケージを開きます。

<b>すべてを保存：</b> (Ctrl + ⇧ + S)バックグラウンドで読み込まれたパッケージを含め、開いているすべてのパッケージを保存します。

<b>すべて閉じる：</b>開いているすべてのパッケージを閉じます。

<b>リソースの再読み込み：</b> Designerで[ビットマップやSVGデータを含むすべてのリソースを強制的に再読み込みします](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)。

<b>Exit:</b> (Ctrl+Q) - Substance 3D Designerを閉じます。

## 編集

<b>取り消し：</b> (Ctrl+Z)最後の操作を取り消します。

<b>やり直し：</b> (Ctrl + Y)最後に取り消した操作をやり直します。

<b>環境設定…:</b>環境設定ウィンドウを開きます。

>[!NOTE]
>
> このダイアログには、macOSのタスクバーのSubstance 3D Designerメニューからアクセスできます。

## ツール

<b>レンダリングのキャンセル：</b> (Esc) Substance engineの現在の処理を停止します。 不要で負荷の高いオペレーションを中断するために使用できます。

<b>中断エンジン:</b> (⇧+Esc) レンダリングエンジンを中断します。 これにより、複雑な[グラフ](../../compositing-graphs/substance-compositing-graphs.md)の編集を高速化できます。

<b>スイッチエンジン...: </b>(F9) GPU エンジン （Windowsの&#39;DirectX&#39;、macOSの&#39;OpenGL&#39;）およびCPU エンジン （Appleシリコンの&#39;NEON&#39;、その他すべての&#39;SSE&#39;）を含むレンダリングエンジンを選択できます。

<b>Substance Player:</b> DesignerとSubstance Playerの連携を管理する：

* <b>Locate Player...:</b> Playerがインストールされている場所をDesignerに知らせます。
* <b>Playerをダウンロード…:</b> Substance Playerドキュメントの[ランディングページ](https://helpx.adobe.com/substance-3d-player/home.html)を開きます。このページでは、Playerをダウンロードできます。

<b>Plugin Manager...</b>: [Plugin Manager]ウィンドウを開きます。このウィンドウでは、Substance 3D Designer用の[Pythonプラグインをインストール、ロード、およびアンロードできます。](../../scripting/scripting.md)

## Windows

<b>新しいエクスプローラー:</b>新しいエクスプローラードックを開きます。 複数のエクスプローラーのドックを開くことができます。

<b>新しい3D ビュー:</b>新しい3D ビュードックを開きます。 複数の3D ビュードックを開くことができます。

<b>新しいライブラリビュー：</b>新しいライブラリドックを開きます。 複数のライブラリドックを開くことができます。

<b>Python Editor:</b>スクリプトの評価と作成[に使用するPython Editorを開きます。](../../scripting/scripting.md)

<b>レイアウトのリセット：</b>ワークスペースを既定のレイアウトにリセットします。 すべてのウィンドウが再配置され、一部のウィンドウが再び非表示になる可能性があります。 プログラムレイアウトに問題がある場合に使用します。

<b>ウィンドウの最大化を解除：</b>任意のパネルが&#x200B;*最大化*&#x200B;されている場合、このオプションはウィンドウの最大化を解除し、レイアウトを&#x200B;*最大化の前*&#x200B;と同じ状態に復元します

<b>エクスプローラー:</b> [エクスプローラー](../the-explorer-window/the-explorer-window.md)を表示/非表示にします。

<b>グラフ：</b> [グラフウィンドウ](../../interface/the-graph-view/the-graph-view.md)の表示/非表示を切り替えます。

<b>パラメーター：</b> [プロパティ](../properties/properties.md)を表示/非表示にします。

<b>コンソール：</b>コンソールウィンドウの表示/非表示を切り替えます。

<b>3Dビュー：</b> [3Dビュー](../../interface/3d-view/3d-view.md)を表示/非表示にします。

<b>依存関係マネージャー：</b> [依存関係マネージャー](../../interface/dependency-manager/dependency-manager.md)の表示/非表示を切り替えます。

<b>2Dビュー：</b> [2D ビュー](../2d-view/2d-view.md)を表示/非表示にします。

<b>ライブラリ：</b> [ライブラリウィンドウの表示/非表示を切り替えます。](../../interface/the-library/the-library.md)

<b>メインツールバー：</b>メインツールバーの表示/非表示を切り替えます（クイックアクセスボタンのみ）。

>[!NOTE]
>
> Designerのパネル管理、カスタマイズ、およびワークフロー拡張機能について詳しくは、このドキュメントの[ワークスペースのカスタマイズ](../../interface/customizing-your-wor/customizing-your-workspace.md)を参照してください。

## ヘルプ

<b>Tutorials:</b> [Substance 3Dチュートリアル](https://substance3d.adobe.com/tutorials/)のWebサイト（以前のSubstanceアカデミー）を開きます。<b>\
</b>

<b>リリースノート：</b>最新バージョンの更新履歴ログを表示するウィンドウを開きます。

<b>技術要件：</b>アプリケーションを実行するための技術要件を表示します。

<b>ドキュメント：</b> [このドキュメント](https://www.adobe.com/go/Substance-3D-doc-Designer_jp)で既定のWebブラウザーを開きます。

<b>スクリプトドキュメント：</b> WebブラウザーをローカルのPython APIドキュメントで開きます。

<b>フォーラム…:</b> Webブラウザーを[サポートコミュニティ](https://forum.substance3d.com/)フォーラムで開き、コミュニティに連絡して質問します。

<b>バグの報告…:</b>バグレポートウィンドウを開きます。

<b>ログのエクスポート…:</b>現在のログファイルを圧縮(.zip)ファイルにエクスポートし、テクニカルサポートに提供します。

<b>フィードバックを送信…:</b> Adobeの[サポートコミュニティ](https://www.adobe.com/go/Substance-3D-feedback-Designer_jp)のホームページでWebブラウザーを開きます。

<b>Substance 3Dアセット：</b>サブスクライバー（以前のSubstance Source）は、[プレミアム3Dコンテンツ](https://substance3d.adobe.com/assets)を参照してください。

<b>Substance 3Dコミュニティアセット:</b> [無料のコミュニティアセット](https://substance3d.adobe.com/community-assets/) （以前のSubstance share）を参照できます。

<b>アカウントの管理\*:</b> AdobeアカウントのWebページを開きます。

<b>サインイン/サインアウト…\*:</b> Adobeアカウントにサインインまたはサインアウトできます。

<b>ホーム画面…:</b> [ホーム画面](../../interface/home-screen/home-screen.md)ダイアログを表示します。

<b>新機能…:</b> Designerの最新リリースに追加された機能を示す画面が表示されます

<b>ようこそ画面…\*:</b>新しいユーザーにDesignerの目的と[Substance 3Dエコシステム](https://helpx.adobe.com/substance-3d.html)での場所を案内する画面を表示します

<b>パートナー：</b> Designerのパートナーが提供するサードパーティ統合に関する免責事項および通知にアクセスできます。

<b>Substance 3D Designerについて…:</b>アプリケーションとそのコンポーネントに関するバージョン番号などの情報を表示します。

\*：これらのオプションは、[Adobe Creative Cloudデスクトップ](https://creativecloud.adobe.com/en/apps/download/creative-cloud)からインストールされたバージョンのDesignerでのみ使用できます。この場合、[Substance 3Dサブスクリプション](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar)が必要です。
