---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: 3D シーンからマテリアルプロパティを抽出し、マテリアル作成ワークフローのSubstanceグラフで使用します。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルの値とテクスチャの抽出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# マテリアルの値とテクスチャの抽出

マテリアルのプロパティを抽出して、Substanceグラフで使用できます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## テクスチャからの新しいグラフ

</td>
<td style="border: 0;" valign="top">

### テクスチャを抽出

</td>
<td style="border: 0;" valign="top">

### 値を抽出

</td>
</tr>
</table>

## テクスチャからの新しいグラフ

「テクスチャ入力からグラフを作成」アクションは、マテリアルが使用するすべてのテクスチャを使用して新しいSubstanceグラフを作成します

このアクションを使用すると、いくつかの処理が行われます。

* 選択した場所に、マテリアルにちなんだ名前の付いたSubstanceグラフーが作成されます。
* [ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)は、マテリアルが使用するすべてのテクスチャに対して作成され、&#39;Resources&#39;フォルダーの下の、マテリアルの名前の付いたフォルダーに配置されます。
* グラフでは、これらのビットマップリソースごとに[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)個のノードが作成され、テクスチャを使用して、マテリアルプロパティの後に構成された[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)個のノードに自動的に接続されます。
* 同じテクスチャの各チャンネルを使用して異なるマテリアルプロパティを制御する場合（[チャンネルパッキング](../../glossary/glossary.md)と呼ばれます）、[グレースケール変換](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md)のノードが自動的に追加され、適切なチャンネルが選択されます。
* グラフはマテリアルに自動的に接続されます。グラフを編集するまで、その外観は変わりません。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![テクスチャ入力からグラフを作成 – &#39;3D ビュー&#39; ビューポートの操作](../../assets/createGraphFromTexturesActionViewport.png "テクスチャ入力からグラフを作成 – &#39;3D ビュー&#39; ビューポートの操作"){zoomable="yes"}

*3D ビュー ビューポートの操作*

</td>
<td style="border: 0;" valign="top">

![テクスチャ入力からグラフを作成 – [マテリアル]メニューの操作](../../assets/createGraphFromTexturesActionMaterials.png "テクスチャ入力からグラフを作成 – [マテリアル]メニューの操作"){zoomable="yes"}

*マテリアルメニューの操作*

</td>
<td style="border: 0;" valign="top">

![テクスチャ入力からグラフを作成 – &#39;プロパティ&#39;ドックの操作](../../assets/createGraphFromTexturesActionProps.png "テクスチャ入力からグラフを作成 – &#39;プロパティ&#39;ドックの操作"){zoomable="yes"}

*プロパティドックのアクション*

</td>
</tr>
</table>

![テクスチャからグラフが作成された結果](../../assets/createGraphFromTexturesResult.png "マテリアルテクスチャからグラフが作成された結果"){zoomable="yes"}

*テクスチャからグラフを作成した結果*

+++デモンストレーション
![テクスチャ入力からグラフを作成 – デモ](../../assets/createGraphFromTextures.gif "テクスチャ入力からグラフを作成 – デモ"){zoomable="yes"}



+++

>[!TIP]
>
> オブジェクトにカーソルを置き<b>Shift + LMB</b>を押して選択すると、3D ビュー ビューポートですばやく直接アクションにアクセスできます。 次に、RMBをクリックして、アクションをホストしているコンテキストメニューにアクセスします。

>[!NOTE]
>
> *埋め込みテクスチャ*&#x200B;を使用する形式（例： USDZ）の場合、テクスチャを抽出してディスクにコピーする必要があります。 これにより、テクスチャを抽出する場所を選択するための追加ステップが実行されます。

## テクスチャを抽出

「テクスチャをグラフに抽出」アクションは、マテリアルで使用されるテクスチャの既存のグラフに新しいビットマップノードを作成します。

このアクションを使用すると、いくつかの処理が行われます。

* [ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)は、マテリアルで使用されるテクスチャ用に作成され、&#39;Resources&#39;フォルダーの下の、マテリアルにちなんだ名前のフォルダーに配置されます。
* 選択したグラフで、[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードがそのビットマップリソース用に作成され、そのテクスチャを使用して、マテリアルプロパティの後に構成された[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードに自動的に接続されます。

マテリアルプロパティ&#x200B;*に対して構成された出力がグラフに既に存在する*&#x200B;場合、*ノードは作成されず*&#x200B;ビットマップリソースの作成のみが実行されます。

例： 「ベースカラー」プロパティのテクスチャを、「ベースカラー」用に構成された出力ノードを既にホストしているグラフに抽出すると、グラフにノードが作成されなくなります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![グラフにテクスチャを抽出 – プロパティドックの動作](../../assets/extractTextureAction.png "グラフにテクスチャを抽出 – プロパティドックの動作"){zoomable="yes"}

プロパティドックのマテリアルプロパティのアクション

</td>
<td style="border: 0;" valign="top">

![グラフにテクスチャを抽出 – 「出力先グラフの選択」ダイアログ](../../assets/extractTextureSelectGraph.png "グラフにテクスチャを抽出 – 「出力先グラフの選択」ダイアログ"){zoomable="yes"}

「宛先グラフを選択」ダイアログ

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![テクスチャ抽出結果](../../assets/extractTextureResult.png "テクスチャ抽出結果"){zoomable="yes"}

テクスチャ抽出結果

+++デモンストレーション
![グラフにテクスチャを抽出 – デモ](../../assets/extractTextureToGraph.gif "グラフにテクスチャを抽出 – デモ"){zoomable="yes"}



+++

「テクスチャをリソースとして抽出」アクションでは、マテリアルで使用されるテクスチャのビットマップリソースのみが作成され、「Resources」フォルダの下の、マテリアルにちなんだ名前のフォルダに配置されます。

>[!NOTE]
>
> *埋め込みテクスチャ*&#x200B;を使用する形式（例： USDZ）の場合、テクスチャを抽出してディスクにコピーする必要があります。 その結果、テクスチャを抽出する場所を選択するための追加の手順が必要になります。

## 値を抽出

&#39;値をグラフに抽出&#39;アクションは、マテリアルプロパティ値の既存のグラフに新しい[値プロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)ノードを作成します。

このアクションを使用すると、いくつかの処理が行われます。

* 選択したグラフで、そのプロパティ値に対して[Value processor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)ノードが作成され、そのマテリアルプロパティの後に構成される[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードに自動的に接続されます。
* 値プロセッサノードの[Substance関数グラフ](../../function-graphs/function-graphs.md)で、値の種類に一致する[定数ノード](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)が作成され、グラフの出力として設定された抽出値に設定されます。

マテリアルプロパティ&#x200B;*に対して構成された出力がグラフに既に存在する*&#x200B;場合、*ノードは作成されません*。

例： 「異方性レベル」プロパティの値を、「異方性レベル」用に設定された出力ノードを既にホストしているグラフに抽出すると、グラフにノードが作成されなくなります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![値をグラフに抽出 – プロパティドックのアクション](../../assets/extractValueAction.png "値をグラフに抽出 – プロパティドックのアクション"){zoomable="yes"}

プロパティドックのマテリアルプロパティのアクション

</td>
<td style="border: 0;" valign="top">

![グラフに値を抽出 – 「グラフ先の選択」ダイアログ](../../assets/extractValueSelectGraph.png "グラフに値を抽出 – 「グラフ先の選択」ダイアログ"){zoomable="yes"}

「宛先グラフを選択」ダイアログ

</td>
<td style="border: 0;" valign="top">

![値をグラフに抽出 – 値プロセッサノードの関数の定数ノード](../../assets/extractValueResult2.png "値をグラフに抽出 – 値プロセッサノードの関数の定数ノード"){zoomable="yes"}

値プロセッサノードの関数の定数ノード

</td>
</tr>
</table>

![値の抽出結果](../../assets/extractValueResult.png "値の抽出結果"){zoomable="yes"}

値の抽出結果

+++デモンストレーション
![値をグラフに抽出 – デモ](../../assets/extractValueToGraph.gif "値をグラフに抽出 – デモ"){zoomable="yes"}



+++
