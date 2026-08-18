---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/the-explorer-window.html"
breadcrumb-title: ''
description: Substance 3D Designerのエクスプローラーウィンドウを使用して、プロジェクトのファイルやリソースを参照、整理、管理します。
helpx_creative_field: ""
helpx_description: Designer > Interface > Explorer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エクスプローラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 2%

---


# エクスプローラー

[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)のエクスプローラーのドックについて説明します。 このドックを使用すると、パッケージとそのリソースを管理できます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概要

エクスプローラーのドックでは、Substance 3D Designerで現在開いているファイルやリソースを管理できます。 現在開いているすべてのパッケージのリストが表示されます。各パッケージは階層として展開され、その中に[リソース](../../resources/resources.md)が表示されます。

エクスプローラーでは、あらゆる種類のリソースを作成、保存、書き出しできるため、プロジェクトを開始および終了できます。

</td>
<td style="border: 0;" valign="top">

![エクスプローラーのドック](../../assets/explorer-3.jpg "エクスプローラーのドック")

</td>
</tr>
</table>

エクスプローラーのドックを使用して、いくつかの重要なアクションを実行できます。

* 新しいパッケージとグラフの作成
* 既存のパッケージの読み込み
* 読み込まれたパッケージを保存して閉じる
* [リソースの読み込みとリンク](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)
* [グラフ結果のテクスチャへの書き出し](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)
* [Substance 3Dアセット(SBSAR)へのパッケージのPublish](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)
* [他のSubstance 3Dアプリケーションへのパッケージの送信](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html)
* [メッシュからマップをベイクする](../../bakers/bakers.md)

## 上ツールバー

このツールバーを使用すると、ワークフロー全体に関連する機能をすばやく実行できます。 すべてのボタンは&#x200B;*コンテキストに応じた*&#x200B;です。つまり、エクスプローラーでの現在の選択に基づいて、ボタンをアクティブにし、動作を変更します。

![](../../assets/save.png) <b>選択したパッケージを保存</b>します。

![](../../assets/sendto-icon.jpg) <b>Publishまたは[送信](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)</b>選択した要素：

* [選択したパッケージをSubstance 3Dアセット(SBSAR)にPublish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md);
* 選択したパッケージを[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)さん、[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)さん、または[Substance 3D Stager](https://www.adobe.com/jp/products/substance3d-stager.html)に送信します。

![](../../assets/republish.png) <b>Publishまたは以前と同じ形式で送信： </b>選択したアイテムをPublishするか、以前と同じ設定で送信します。 このオプションは、*現在*&#x200B;セッションで既に&#x200B;*少なくとも1回*&#x200B;公開されているパッケージでのみ使用できます。

![](../../assets/graph-cleaner.jpg) <b>選択したグラフの未使用ノードを削除します</b>。 ツールは次の規則に従います。

* このツールは、選択した項目が&#x200B;*同じ種類*:グラフ、フォルダー、またはパッケージのみ)の場合にのみ使用できます。
* 選択範囲にフォルダーまたはパッケージが含まれている場合、ツールはその中のすべてのグラフを&#x200B;*再帰的に*&#x200B;消去します。
* ターゲットグラフの1つが[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)の場合、2番目のオプションを使用して、そのグラフ内のノード上のすべてのパラメーター関数をクリーンアップできます。

ツールの詳細については、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)ページの[未使用ノードの削除]セクションを参照してください。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Publish/送信ドロップダウンメニュー](../../assets/explorer-sendto-displayed.jpg "Publish/送信ドロップダウンメニュー")

*Publish/送信*

</td>
<td style="border: 0;" valign="top">

![使用されていないノードの削除ドロップダウンメニュー](../../assets/explorer-graph-cleaner.jpg "使用されていないノードの削除ドロップダウンメニュー")

*未使用のノードを削除する*

</td>
</tr>
</table>

## コンテキストメニュー

エクスプローラを使用する操作の大部分は、コンテキストメニューを使用して行われます。このコンテキストメニューは、エクスプローラのツリービューにある項目のRMBをクリックすると表示されます。

使用できるオプションは、選択またはクリックしたアイテムによって異なります。

+++空のスペース

空の容量は、現在開いているパッケージの下でのみ利用可能です。 既存のアイテムの横にあるをクリックしても、空きスペースとはみなされません。

<b>新しいパッケージ</b>：新しい空のパッケージを作成します；

<b>パッケージを開く</b>: SBSファイルを開くためのファイルダイアログボックスを開きます。

+++

+++パッケージ

<b>新規</b>を使用すると、コンテンツの並べ替えに使用する&#x200B;*フォルダー*&#x200B;に加えて、新しいグラフ([Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)、[ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)および[ベクターグラフィックス](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)のリソースを作成できます

<b>読み込み</b>と<b>リンク</b>[のリソースを取り込む](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

<b>再読み込み</b>、<b>保存、別名で保存</b>および<b>コピーを別名で保存</b>を使用すると、ディスクに保存したり、以前に保存したバージョンのパッケージをディスクから取り消したりできます。

<b>Publish .sbsarファイル</b>および<b> .sbsarファイル</b>を再パブリッシュすると、[最適化されていないコンパイルされていないSubstanceグラフを効率的でポータブルなSBSARファイルにPublishして、他のSubstanceアプリケーションや統合で使用できるようになります](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)。 「前と同じPublish」を選択すると、同じオプションを使用して前のPublishの操作が繰り返され、オプションダイアログをスキップすることで、繰り返し操作を高速化できます。 ツールバーには、同じ機能を持つボタンが含まれています。

<b>依存関係のあるエクスポート</b>は、保存および発行とは異なります。 SBSファイルを取得し、参照されているすべてのリソースと依存関係を収集して、自己完結型のパッケージを作成します。 このダイアログでは、収集するライブラリと、ファイルを圧縮アーカイブ(7-zip)にするかどうかを選択できます。 これは、依存関係の欠落を気にすることなく、SBSファイルを他のユーザーと共有する場合に適しています。

<b>送信先…</b>では、サブメニューが開き、[&#128279;](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html)パッケージを直接[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)に送信するか、[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)に送信するか、[Substance 3D Stager](https://www.adobe.com/jp/products/substance3d-stager.html)に送信するか、[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)にするかを選択できます。

<b>コピー</b>選択したパッケージをコピーします。

<b>貼り付け</b>選択したパッケージにコピーしたグラフやリソース&#x200B;*を*&#x200B;に貼り付けます。

<b>パッケージを閉じる</b>選択したすべてのパッケージを閉じます

<b>出力を計算</b>パッケージ内のすべてのグラフの出力をすべてDesignerが強制的に計算します。

<b>エクスプローラーで表示…</b>パッケージの場所をOSのエクスプローラーのウィンドウで開きます

<b>依存関係マネージャー</b>は、選択したパッケージの依存関係マネージャーウィンドウを開きます。

<b>依存関係を開く</b>では、エクスプローラーのすべての依存関係を開きます（*[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)のみ*）。

+++

+++Substance グラフ

<b>開く：</b> （戻る）このグラフを[グラフビュー](../../interface/the-graph-view/the-graph-view.md)で開きます。

<b>コピー：</b> *(Ctrl-C)*&#x200B;現在のグラフをクリップボードにコピーします。

<b>削除：</b> （削除）このパッケージからグラフを削除します。

<b>名前の変更：</b> (F2)このグラフの名前を変更します。

<b>3Dビューで出力を表示：</b>このグラフの出力を[3Dビュー](../../interface/3d-view/3d-view.md)に送信し、マテリアルとして表示します。

<b>出力の計算：</b>このグラフの出力を計算し、メモリに保持します。

<b>出力のエクスポート…:</b> [ビットマップにエクスポートするためのダイアログを開きます。](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

+++

+++3D シーンリソース

<b>開く：</b> （戻る）この3Dメッシュを[3Dビュー](../../interface/3d-view/3d-view.md)で使用し、標準の立方体または平面を置き換えます。

<b>コピー：</b> (Ctrl-C)このリソースをクリップボードにコピーします。

<b>貼り付け：</b> (Ctrl-V)クリップボードからリソースを貼り付けます。

<b>削除：</b> (Del)このパッケージからリソースを削除します。

<b>名前の変更：</b> (F2)このリソースの名前を変更します。

<b>再読み込み：</b>このメッシュをディスクから強制的に再読み込みします。

<b>エクスプローラーで表示：</b>ディスク上のリソースの場所で、システムファイルブラウザーウィンドウを開きます。

<b>場所の変更：</b>このリソースを別のファイルにリンクするように変更します。

<b>モデル情報のベイク処理…:</b> [ベイク処理ダイアログを開きます。](../../bakers/bakers.md)

+++

+++フォルダー

<b>新規：</b>新しいグラフ([Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)、[Substance関数グラフ](../../function-graphs/function-graphs.md)、[ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)および[ベクターグラフィックス](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)リソースと、コンテンツの並べ替えに使用する&#x200B;*フォルダー*&#x200B;をフォルダー内に作成できます。

<b>読み込み</b>と<b>リンク： </b>[リソース](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)を取り込んで、フォルダーに配置します。

<b>コピー：</b> (Ctrl-C)フォルダーとすべての内容をクリップボードにコピーします。

<b>貼り付け：</b> (Ctrl-V)クリップボードからフォルダーとそのすべての内容を貼り付けます。

<b>名前の変更：</b> (F2)このフォルダーの名前を変更します。

<b>削除：</b> *(Del)*&#x200B;フォルダーとそのすべてのコンテンツをパッケージから削除します。

<b>出力の計算：</b>フォルダーに含まれるすべてのグラフの出力を計算し、メモリに保持します。

+++

## 下部ツールバー

エクスプローラドックの下部にあるツールバーには、パッケージまたはパッケージリソースに関する次の情報が表示されます。

<b>![](../../assets/explorer-dependencies.jpg)依存関係：</b>パッケージを選択すると、そのパッケージの依存関係が専用パネルに一覧表示されます。

<b>![](../../assets/explorer-information.jpg)情報：</b>現在選択されているパッケージまたはリソースに関連するメタデータを提供します：

* パッケージ：パッケージの完全なファイルパス
* [ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md):リソースの完全なファイルパス、その[ICCプロファイル](../../color-management/color-management.md)、画像サイズおよび[インポートメソッド](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) （例： *リンク*&#x200B;または&#x200B;*インポート*）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![依存関係パネル](../../assets/explorer-dependencies-displayed.jpg "依存関係パネル")

*依存関係*

</td>
<td style="border: 0;" valign="top">

![情報パネル](../../assets/explorer-information-displayed.jpg "情報パネル")

*情報*

</td>
</tr>
</table>
