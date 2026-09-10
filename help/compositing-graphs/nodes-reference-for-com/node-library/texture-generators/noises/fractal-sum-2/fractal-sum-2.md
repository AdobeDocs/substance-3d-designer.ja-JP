---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-2.html"
breadcrumb-title: ''
description: '[フラクタル和 2]ノードを使用して、有機的なテクスチャのバリエーションを作成するために2オクターブのフラクタルノイズを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: フラクタル和 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# フラクタル和 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![フラクタル和 2 – アイコン](fractal-sum-2.resources/fractal_sum_2.png "フラクタル和 2 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>フラクタル和</b>ノイズのバリエーションです。

参照： [フラクタル和ベース](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md)、[フラクタル和 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md)、[フラクタル和 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)、[フラクタル和 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 生成されるノイズをグレースケールビットマップとして指定します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>障害</b> <i>浮動小数</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>浮動小数</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>非正方形の拡張</b> <i>ブーリアン</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![フラクタル和 2 – 例1](fractal-sum-2.resources/fractal_sum_2_1.png "フラクタル和 2 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![フラクタル和 2 – 例2](fractal-sum-2.resources/noise_fractal_sum_2_v2_speed0.6_aniso0.gif "フラクタル和 2 – 例2"){zoomable="yes"}

</td>
</tr>
</table>
