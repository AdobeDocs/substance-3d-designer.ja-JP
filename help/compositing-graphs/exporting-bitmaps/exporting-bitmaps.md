---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: 外部アプリケーションやワークフローで使用するために、Substance合成グラフからテクスチャとビットマップを書き出す方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビットマップの書き出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# ビットマップの書き出し

このページでは、Substance 3D Designerで様々なビットマップファイル形式に書き出す方法と、複数のUVタイルを一括して書き出す方法について説明します。[PSDファイルに書き出し](../exporting-psd-files/exporting-psd-files.md)する場合は、専用のページが別途用意されています。

![簡易化された文書の書き出し](../../assets/exportflow.png "簡易化された文書の書き出し")

## 概念のエクスポート

ビットマップを書き出すときは、次の点に注意してください。

* パッケージではなく、Graph</b>からエクスポートする<b>。 パッケージは画像コンテンツだけを生成するわけではありません。
* 書き出されるビットマップの数（および解像度）は、グラフの<b>出力</b>によって決まります。
* すべての出力/ビットマップに対してファイルタイプが設定されています。
* 書き出しは[公開](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)とは異なります。違いをよく理解してください。

## 書き出し方法

書き出しの準備ができたら、書き出しダイアログにアクセスする方法は2つあります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)ウィンドウで、書き出すグラフを右クリックし、**[出力をビットマップとして書き出し]**&#x200B;を選択します

![](../../assets/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

[グラフビュー](../../interface/the-graph-view/the-graph-view.md)で、[ツール]ボタン![](../../assets/image2019-9-17-14-44-17.png)をクリックし、**[出力のエクスポート…]**&#x200B;を選択します

![](../../assets/export-graph.gif)

</td>
</tr>
</table>

## 書き出しダイアログ

書き出しダイアログには、書き出しをカスタマイズするためのいくつかのオプションが表示されます。

右側に表示されているバージョンは標準ダイアログで、解像度の変更はグラフや出力で行うか、ダイアログを開く前に親解像度を設定することで行われます。

1. <b>保存先： </b>すべてのファイルを保存する場所。
1. <b>形式：</b>ファイルの種類は、エクスポートされたすべてのファイルで使用されます。
1. <b>パターン</b>:メタデータキーワードに基づいてファイルの種類を生成する一般的なメソッドです。 検証のために、最初の出力に基づくファイル名の例を以下に示します。\
   以下に、使用可能なすべてのオプションを示します。
   1. *$(graph)* – 現在のグラフの名前
   1. *$(identifier)* – 現在の出力の識別子
   1. *$(description)* – 現在の出力の説明
   1. *$(label)* – 現在の出力のラベル
   1. *$(user\_data)* – 現在の出力のカスタムユーザーデータ
   1. *$(group)* – 現在の出力の出力グループ
   1. *$（カラースペース）* – 現在の出力のカラースペース（*OCIO*&#x200B;および&#x200B;*Adobe ACE* [カラーマネジメント](../../color-management/color-management.md)モードでのみ使用可能）
1. <b>出力：</b>グラフの特定の出力および出力グループのオンとオフを切り替えます。 ボタンを使用して、すべてのオンとオフを切り替えることができます。 1つのビットマップのみが変更されている場合に便利です。
1. <b>自動書き出し：</b>切り替えボタンを使用すると、変更が行われるとすぐに、グラフ出力の自動再書き出しが有効になります。 現在のグラフのみ。 設定によっては重い場合や遅い場合があります。
1. <b>エクスポートボタン：</b>現在の設定でエクスポートするか、ダイアログを閉じます。

![出力ダイアログのエクスポート](../../assets/fromgraph-1.png "出力ダイアログのエクスポート")

## 書き出しダイアログ（バッチ/UVタイル）

DesignerでUVタイルメッシュを操作する場合は、書き出しダイアログを少し異なる方法で使用して、複数のUVタイルを一度にバッチ書き出しすることができます。 このワークフローを理解し、[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)を1つ以上のUVタイルに適切に割り当てていることを確認してください。\
「バッチ」タブを使用すると、作業中（親）の解像度とは異なる解像度でグラフを書き出すときにも高速です。

エクスプローラー&#x200B;*でUVタイルが割り当てられたグラフ上の*&#x200B;を右クリックするか、[ツール]ボタンを使用して、グラフビューで&#x200B;*特定のUVタイルが割り当てられたグラフを開いたことを確認して、上記と同じ方法でダイアログを開始します。*

1. <b>バッチタブ</b>：標準の<b>グラフから</b>方法の代わりにこのタブを選択してください。選択しない場合、オプション2 ～ 3は使用できません。
1. <b>UVタイル：</b>出力と同様に、特定のUVタイルの書き出しのオンとオフを切り替えることができます。
1. <b>[出力サイズ](../../compositing-graphs/output-size/output-size.md): </b>書き出し解像度を無効にして、最大サイズで書き出しながら、より小さく、より効率的に作業できるようにします。

![バッチ書き出し出力ダイアログ](../../assets/batch.png "バッチ書き出し出力ダイアログ")
