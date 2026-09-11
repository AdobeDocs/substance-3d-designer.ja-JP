---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/incorrect-image-output.html"
breadcrumb-title: ''
description: Substance 3D Designerの誤った出力画像のトラブルシューティングと、レンダリングの問題を解決する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Incorrect image output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 画像出力が正しくない
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---


# 画像出力が正しくない

このページでは、Substance 3D Designerで発生する予期しない誤った出力画像という技術的な問題の一覧を示し、それぞれのトラブルシューティング手順を示します。

## ステッピング/バンディングを表示

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（エラー）](../../assets/error.svg)問題**

出力画像のグラデーションは、滑らかではなく段階的です。 ステッピングの原因は、画像で使用される&#x200B;*値の範囲が狭すぎることです*。\
つまり、グラデーションの1つのステップから次のステップにスムーズに移行するのに十分な値がありません。

輝度/RGBA値は、整数または浮動小数点値を使用してエンコードでき、*精度*&#x200B;に影響します。

* **整数**&#x200B;は、0 ～ 1の範囲の値を格納するために、8ビットの精度（0 ～ 255、256の可能な値）と16ビットの精度（0 ～ 65535、65536の可能な値）を提供します。
* **浮動小数点**&#x200B;は、16ビット(HDR 16F)および32ビット(HDR 32F)の精度を提供し、負の値を含む0 ～ 1の範囲外の値を格納できます。 これにより、輝度度の値が1.0を大きく上回る可能性があるハイダイナミックレンジ(HDR)画像を操作できます。

HDR画像を使用する必要がない場合、ほとんどのノードでは、整数でエンコードされた0 ～ 1の範囲の値が出力されます。 画像の出力形式が8ビットの場合、画像で使用できる値は256ですが、多くの場合、グラデーションのステッピングが目に見えるようになります。 これは、特にNormalノードの出力に影響を与える可能性があります。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/demo-stepping-8-bit.png){width="256px"}![](../../assets/demo-stepping-8-bit-2.png){width="256px"}![](../../assets/demo-stepping-8-bit-3.png){width="256px"}

</td>
</tr>
</table>

**![（ティック）](../../assets/check.svg)推奨ステップ**

ノードとすべてのノードの&#x200B;**出力形式** （ビット深度）を確認し、これらのノードが&#x200B;*少なくとも16ビットの整数精度*&#x200B;を使用していることを確認してください。

Output formatパラメーターは、通常、*入力に対する相対* [継承方式](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定され、グラフ全体に精度の低さを伝達できます。 理想的には、グラフの上流に行くことによって、問題の根本的な原因を見つけることができます。

ノードの出力の精度は、ノードの下に表示されるテキスト情報を見ればすばやく識別できます。

* **L/C**&#x200B;は、グレースケール（輝度など）またはカラーの画像を参照しています
* **8/16**&#x200B;は整数エンコーディングを意味します
* **16F/32F**&#x200B;は浮動小数点エンコーディングを意味します

例：

* L8：グレースケール8ビット整数
* C16:カラー16ビット整数
* C32F:カラー32ビット浮動小数点(HDR)

## 公開されたSBSARの品質低下

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

<b>![（エラー）](../../assets/error.svg)問題</b>

右側の図に示すように、Substance 3Dアーカイブ(SBSAR)から出力されるイメージの画質は、パブリッシュされるSubstance 3Dファイルのグラフよりも著しく低くなります。\
出力の解像度が低く見えます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/issues-sbsar-bitmap-relative-to.jpg){width="256px"}

</td>
</tr>
</table>

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

すべての[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードの[出力サイズ](../../compositing-graphs/output-size/output-size.md)プロパティが&#x200B;*絶対* [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されていることを確認してください。

そうでない場合は、参照されている[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)が、公開されているSubstance 3Dアーカイブでデフォルトの256\*256解像度で保存されます。これにより、* 1つ以上の出力の品質に影響します*。

## 画像がぼやけている

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![（エラー）](../../assets/error.svg)問題**

[変形2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)または[ブレンド](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)などの一部のノードを使用すると、シェイプがわずかにぼやけます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/issues-bilinear.jpg){width="256px"}

</td>
</tr>
</table>

**![（ティック）](../../assets/check.svg)推奨ステップ**

画像内のピクセルを再配置する場合、例えばシェイプのサイズ変更や画像の解像度の変更を行う場合、ソースのピクセルを宛先に&#x200B;*マップ*&#x200B;する方法を決定するには2つの方法があります。

* **最も近い**:ピクセルは、一致する座標でターゲット&#x200B;*そのまま*&#x200B;にマップされます。 ターゲットの解像度が低い場合は、ピクセルが完全に無視されることがあります。 ターゲットの解像度が高い場合は、スパンをカバーするすべてのピクセルにマップされます。 出力は&#x200B;*鮮明*&#x200B;で、わずかに&#x200B;*エイリアスが発生*&#x200B;しているように見えます。
* **バイリニアフィルター**:フィルター処理が元画像に適用され、そのピクセルがターゲット解像度にマップされ、ピクセル間のトランジションが&#x200B;*滑らかになります*。 出力は&#x200B;*より滑らか*&#x200B;で、わずかに&#x200B;*ぼやけて*&#x200B;見えます。

[Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)ノードには、**Filteringメソッド**&#x200B;オプションが用意されており、この2つのマッピングメソッドのうち、どちらを使用するかを選択できます。

ほとんどのノード（例： [ブレンド](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)） – 解像度の異なる入力テクスチャをサンプリングする場合は、デフォルトで&#x200B;*バイリニアフィルタリング*&#x200B;が使用されます。これにより、望ましくないブラーが発生する場合があります。\
変形2Dノードは&#x200B;*atomic*&#x200B;であるため非常に軽量です。テクスチャを別のノードに送信する前に[出力サイズ](../../compositing-graphs/output-size/output-size.md)プロパティを使用して、テクスチャ解像度を変更するために&#x200B;*変形を必要としない場合でも*&#x200B;使用できるため、このサイズ変更による影響を&#x200B;*制御*&#x200B;できます。

[ピクセルプロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)ノードの[関数グラフ](../../function-graphs/function-graphs.md)で、**サンプル**&#x200B;ノードには&#x200B;*同じオプション*&#x200B;が含まれており、サンプリングされたテクスチャをノードの解像度にマップする方法を制御できます。
