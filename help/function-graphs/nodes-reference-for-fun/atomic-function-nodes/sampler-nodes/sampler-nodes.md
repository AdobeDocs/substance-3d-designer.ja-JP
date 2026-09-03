---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer機能グラフのサンプラーノードにアクセスして、テクスチャをサンプリングし、カラー値を抽出します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: サンプラ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Samplerノード

![Samplerノード](sampler-nodes.resources/sampler-nodes-01.png "Samplerノード")

これらのノードは、指定された2D座標で入力イメージの値をサンプリングします。

<b>サンプルグレー</b>は、グレースケール画像の入力<b>位置</b>で輝度値をサンプリングし、<b>浮動小数点</b>値として出力します。

<b>サンプルカラー</b>は、カラー画像の入力<b>位置</b>でRGBA値をサンプリングし、<b>Float4</b>値として出力します。R、G、B、Aコンポーネントは、それぞれX、Y、Z、Wコンポーネントにマップされます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

座標は入力の左上隅から始まり、水平および垂直に0 ～ 1の範囲です。

この範囲外の位置は、選択した<b>アドレス指定モード</b>に従って処理されます（以下を参照）。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![ピクセル座標](sampler-nodes.resources/sampler-nodes-02.png "ピクセル座標")

</td>
</tr>
</table>

>[!NOTE]
>
> <b>位置</b>の入力は、画像のX座標とY座標が値のX要素とY要素にそれぞれマップされるFloat2値である必要があります

## パラメーター

+++入力画像
サンプリングに使用するノード入力を選択できます。

リストは、現在接続されている入力に動的に適応します。 つまり、ノード入力を接続する際にエントリが追加されます。

入力の番号付けは0から始まるので、ノードの最初の入力に接続されている画像は&#x200B;*入力画像0*&#x200B;として表示されます。

+++

+++フィルタリングモード
解像度の違いによりサンプル画像のピクセルが出力画像に正確にマッピングされない場合の補間方法を定義できます。

<b>最も近い</b>\
ピクセルは、一致する座標でターゲット&#x200B;*をそのまま*&#x200B;にマップされます。 ターゲットの解像度が低い場合は、ピクセルが完全に無視されることがあります。 ターゲットの解像度が高い場合は、スパンをカバーするすべてのピクセルにマップされます。 出力は&#x200B;*鮮明*&#x200B;で、わずかに&#x200B;*エイリアスが発生*&#x200B;しているように見えます。

<b>バイリニアフィルター</b>\
ソース画像にフィルター処理が適用され、そのピクセルがターゲット解像度にマッピングされて、ピクセル間のトランジションが&#x200B;*滑らかになります*。 出力は&#x200B;*より滑らか*&#x200B;で、わずかに&#x200B;*ぼやけて*&#x200B;見えます。

+++

+++アドレス指定モード
[0;1]範囲外の位置の値の処理方法をコントロールします。

<b>繰り返し</b>\
値が大きくなるにつれて[0;1]の範囲をループします。\
例： 3.4は0.4、-1.7は0.3です。

<b>エッジにクランプ</b>\
[0;1]の範囲外の値を最も近い制限値にクランプします。\
例： .3.4は1、-1.7は0です。

+++
