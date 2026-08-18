---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/the-library.html"
breadcrumb-title: ''
description: Substance 3D Designerのライブラリを使用すると、ノードプリセット、マテリアル、カスタムコンテンツにアクセスして管理できます。
helpx_creative_field: ""
helpx_description: Designer > Interface > Library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライブラリ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8cb5aa2a7e1cd668f00808b3cd0e15063990fb8b
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---


# ライブラリ

このページでは、Substance 3D Designerの&#x200B;**ライブラリ**&#x200B;パネル、そのレイアウト、およびコンテンツの検索とフィルタリングに使用できるツールを紹介します。

![ライブラリ](../../assets/library-main.png "ライブラリ")

## 概要

<b>ライブラリ</b>パネルは、グラフで作業する必要のあるすべての&#x200B;*アセット*&#x200B;を見つけて集めることができる、分割ビュー&#x200B;*リソースマネージャー*&#x200B;です。

ハードドライブ上またはネットワーク上の&#x200B;*フォルダー*&#x200B;が監視され、[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)の[ライブラリ監視パス](https://docs.substance3d.com/display/SDDOC/Project+Settings#ProjectSettings-proj-libraryLibrary)の一覧に追加されます。 これらのフォルダーで行われたすべての変更（コンテンツの追加、削除、更新）は、*ライブラリ</b>に*&#x200B;引き継がれます。<b>

>[!WARNING]
>
> **カスタムコンテンツについて**
> 
> カスタムリソースは&#x200B;**ライブラリ**&#x200B;に追加されますが、既存のカテゴリに対して設定されたフィルター処理ルールのため、表示されない可能性があります。 プロジェクトの作業中にコンテンツが確実に見つかるように、フォルダーに整理された独自のフィルターを作成することをお勧めします。\
> 詳細については、ドキュメントの[カスタムコンテンツとフィルターの管理](./managing-custom-content/managing-custom-content-and-filters.md)セクションを参照してください。

**ライブラリ**&#x200B;は、サポートされているすべてのアセットを監視できます[リソース](../../resources/resources.md):

* [Substanceパッケージ](../../getting-started/overview/overview.md) (SBS)および[Substanceアーカイブ](../../getting-started/overview/overview.md) (SBSAR)からのグラフ
* [ビットマップ画像](../../resources/bitmap-resource/bitmap-resource.md)
* [ベクター画像](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [関数グラフ](../../function-graphs/function-graphs.md)
* [AxFファイル](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)
* [フォント](../../resources/font-resource/font-resource.md)
* [3Dシーン](../../resources/3d-scene-resource/3d-scene-resource.md)

パネルは2つの主要な部分に分かれています。

* 左側の「**カテゴリ**」セクション
* 右側の&#x200B;**コンテンツ**&#x200B;セクション

## カテゴリ

<b>ライブラリ</b>パネルの左側にある<b>カテゴリ</b>セクションには、すべてのアセット&#x200B;*カテゴリ* （フォルダー）と&#x200B;*フィルター*&#x200B;がツリービューとして含まれています。\
このツリービューの任意の項目をクリックすると、その項目の内容と&#x200B;*すべての子項目*&#x200B;の内容を表示できます。

### カテゴリ

デフォルトのカテゴリとフィルターには、Designerに付属しているすべてのアセットが含まれています。 これらは編集または削除できません。\
デフォルトのカテゴリは次のとおりです。

* お気に入り：「お気に入り」としてフラグを設定したすべてのアセットを収集します
* [グラフ項目](../../interface/the-graph-view/graph-items/graph-items.md):グラフを整理するための特別なオブジェクトを一覧表示します
* [Atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md): [Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)のatomic nodesを一覧表示します
* [FX-Mapノード](../../function-graphs/fxmaps/fxmaps.md): [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)ノードによって計算されたグラフに固有のノードを含みます
* [関数ノード](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md): [関数グラフ](../../function-graphs/function-graphs.md)のアトミックノードを一覧表示します
* [テクスチャジェネレーター](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/texture-generators.md):コンテンツを自律的に生成する[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)を表すノードが含まれています
* [フィルター](../../compositing-graphs/nodes-reference-for-com/node-library/filters/filters.md)：入力を変更する[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)を表すノードが含まれています
* [スプラインとパスツール](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-paths-tools.md): [スプライン](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)および[パス](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md)ノードのカタログ
* [SDF 関数](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions): [シェイプスプラッタv2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)および[3Dビューア](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)ノードと共に使用する3D SDF 関数を作成するためのノードが含まれます
* [関数](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md): [関数グラフ](../../function-graphs/the-function-graph/the-function-graph.md)を表すノードを含みます
* [3Dビュー](../3d-view/3d-view.md):オーサリング環境マップ用の環境マップやノードなど、[3Dビュー](../../interface/3d-view/3d-view.md)など、3Dシーンで画像ベースのライティングに使用されるマップ関連のコンテンツを提供します
* PBRマテリアル：他のノード、「レシピ」、またはカスタムワークスペース設定をテストするためのプレースホルダーとして使用できる、事前に作成されたマテリアル。 オーサリング資料について学ぶには、専用の[資料サンプル](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)を参照することをお勧めします。
* [値](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md): Substanceグラフに単純な値を生成するためのノードです。

## コンテンツ

<b>ライブラリ</b>のコンテンツは、*ラベル付きサムネール*&#x200B;として表示されます。 これらのサムネールは、次の要因に応じて異なる側面を持ちます。

* [SBS](../../getting-started/overview/overview.md)および[SBSAR](../../getting-started/overview/overview.md)ファイルの[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)は、*最初の出力*&#x200B;で表されます。グラフの作成者が設定した場合は、*カスタムアイコン*&#x200B;で表されます
* [ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)と[ベクターグラフィックス(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)は、ビットマップ自体の&#x200B;*ミニチュアレンダリング*&#x200B;で表されます
* [3Dメッシュ](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)、[関数グラフ](../../function-graphs/the-function-graph/the-function-graph.md)、[フォント](../../resources/font-resource/font-resource.md)および[AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)ファイルは、種類ごとに&#x200B;*汎用アイコン*&#x200B;で表されます

>[!WARNING]
>
> **サムネールに問題がある場合**
> 
> ライブラリサムネールに関連する問題（間違った画像、更新アイコンでレンダリングが止まるなど）のトラブルシューティングに推奨される手順 は、*サムネールの更新*&#x200B;を手動でトリガーします。\
> これを行うには、[環境設定ウィンドウ](../../interface/preferences-window/preferences-window.md)の[ライブラリ](../../interface/preferences-window/preferences-window.md)セクションにある&#x200B;**サムネイルの再構築**&#x200B;ボタンを使用します。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### ライブラリのアセットの使用

ライブラリのアセットを使用するには、目的の場所に&#x200B;*ドラッグ&amp;ドロップ*&#x200B;します。\
<b>Ctrl</b>キーを押しながらアイテムをクリックすると、<b>コンテンツ</b>セクションで&#x200B;*複数*&#x200B;個のアイテムを選択できます。 この場合、ドラッグ&amp;ドロップ操作により、*選択範囲全体*&#x200B;のグラフにノードが配置されます。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![ライブラリからノードを削除しています](../../assets/library-create-node.gif "ライブラリからノードを削除しています")

</td>
</tr>
</table>

### 名前によるアセットの検索

<b>コンテンツ</b>セクションの左上にある<b>検索</b>バーを使用すると、*任意のアセットを名前*&#x200B;で検索できます。 この方法でコンテンツを検索する場合、<b>カテゴリ</b>セクションの現在の選択範囲は無視され、<b>ライブラリ</b>の&#x200B;*コンテンツ全体*&#x200B;が検索されます。\
「<b>検索</b>」バーの横にある「![](../../assets/library-icon-search-filter.png) <b>フィルターの条件…</b>」アイコンを使用して、検索結果を&#x200B;*グラフの種類*&#x200B;でフィルターできます。

>[!NOTE]
>
> 検索バーでは、探しているアセットの名前だけでなく、アセットに含めることができる&#x200B;*タグ*&#x200B;またはアセットが属する&#x200B;*カテゴリ*&#x200B;も考慮されます。\
> 例えば、「*Normal*」と入力すると、通常のマップの生成または変更に使用できるすべてのアセットが一覧表示されます。 これは、新しいノードを発見するための良い方法であり、したがって、新しい可能性があります！

![ライブラリでのアセット検索](../../assets/library-search-2.png "ライブラリでのアセット検索")

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### ライブラリアセットの表示

![](../../assets/library-icon-view-mode.png) <b>表示モード</b>ドロップダウンボタンを使用して、コンテンツ項目の表示サイズを選択できます。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![ライブラリアセット表示モード](../../assets/library-display-modes.png "ライブラリアセット表示モード")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/library-icon-toggle-label.png) **ラベルの切り替え**&#x200B;ボタンを使用すると、ノードのラベルを表示または非表示にできます。

</td>
<td style="border: 0;" valign="top">

![ラベルの切り替え](../../assets/library-toggle-label.png "ラベルの切り替え")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

コンテンツ項目にカーソルを置くと、項目の&#x200B;*説明*&#x200B;が作成者によって指定されている場合は、短時間の後にツールチップが表示されます。\
*アイテムの右クリック*&#x200B;すると、そのアイテムのソースファイルへのパスなどの追加情報が表示されます。

</td>
<td style="border: 0;" valign="top">

![アセット情報のツールヒント](../../assets/library-item-tooltip.png "アセット情報のツールヒント")

</td>
</tr>
</table>

>[!NOTE]
>
> [インスタンスノード](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) – つまり非アトミックノードの場合、このパスは、システムのファイルブラウザーにファイルを表示する&#x200B;*ハイパーリンク*&#x200B;です。\
> アトミックノードは、特殊なエイリアスのパスを使用します（例： `graphatomic://`、`structure://`、...） このライブラリは、内部ライブラリを指しているためクリックできません。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### お気に入り

![](../../assets/library-icon-favoritepng.png) <b>[お気に入りに追加]</b>ボタンを使用すると、<b>コンテンツ</b>セクションの任意のアイテムを<b>お気に入り</b>リストに追加できます。 このボタンを使用すると、このリストにコンテンツが既に追加されている場合は、*削除*&#x200B;することもできます。\
このリストにコンテンツを追加すると、そのコンテンツは<b>ライブラリ</b>の<b>お気に入り</b>カテゴリで利用可能になり、グラフ内のノードを検索する際に<b>ノード</b>メニューリストの&#x200B;*トップ*&#x200B;に表示されます（検索語が一致している場合）。

</td>
<td style="border: 0;" valign="top">

![ライブラリのお気に入り](../../assets/library-favourites.png "ライブラリのお気に入り")

</td>
</tr>
</table>
