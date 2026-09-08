---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-4.html"
breadcrumb-title: ''
description: 「フラクタル和 4」ノードを使用して、4オクターブのフラクタルノイズを生成し、細かい有機的なテクスチャを作り出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: フラクタル和 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# フラクタル和 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![フラクタル和 4 – アイコン](../../../../../../assets/fractal_sum_4.png "フラクタル和 4 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>フラクタル和</b>のノイズのバリエーション。

参照： [フラクタル和ベース](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md)、[フラクタル和 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md)、[フラクタル和 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md)、[フラクタル和 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 生成されるノイズをグレースケールビットマップとして表します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![フラクタル和 4 – 例1](../../../../../../assets/fractal_sum_4_1.png "フラクタル和 4 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![フラクタル和 4 – 例2](../../../../../../assets/noise_fractal_sum_4_v2_speed0.6_aniso0.gif "フラクタル和 4 – 例2"){zoomable="yes"}

</td>
</tr>
</table>
