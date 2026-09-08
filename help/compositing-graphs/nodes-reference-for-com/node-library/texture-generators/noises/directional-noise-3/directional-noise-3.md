---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-3.html"
breadcrumb-title: ''
description: 方向性ノイズ3ノードを使用して、3つのオクターブを持つ方向性ノイズパターンを作成し、方向テクスチャを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向性ノイズ 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# 方向性ノイズ 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![方向性ノイズ 3 – アイコン](../../../../../../assets/directional_noise_3.png "方向性ノイズ 3 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>方向性ノイズ</b>のノイズのバリエーション。

参照： [方向性ノイズ 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md)、[方向性ノイズ 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md)、[方向性ノイズ 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>スケール</b> <i>整数</i> | ノイズタイルの生成に使用するグリッドの区画。    値を大きくすると、描かれるタイルの数が増え、ノイズが高くなります。 |
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>異方性の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの方向の範囲を制御します。値を大きくすると、より狭く、より明確な方向になります。    方向は、<b>Disorder異方性角度</b>パラメーターで制御されます。 |
| <b>anisotropy angleの乱れ</b> <i>フロート</i> | &#39;Disorder 異方性&#39;パラメーターが0でない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>角度</b> <i>フロート</i> | ノイズの方向を設定するために使用する角度です。回転の回数で指定し、水平方向の右から開始します。 |
| <b>角度ランダム</b> <i>フロート</i> | <b>角度</b>の値に適用されるランダムな変動の最大量（ターン数）。 |
| <b>タイルのオフセット</b> <i>浮動小数点2</i> | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向性ノイズ 3 – 例1](../../../../../../assets/directional_noise_3_1.png "方向性ノイズ 3 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向性ノイズ 3 – 例2](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso0.gif "方向性ノイズ 3 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向性ノイズ 3 – 例3](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso1.gif "方向性ノイズ 3 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向性ノイズ 3 – 例4](../../../../../../assets/noise_directional_noise_3_v2_speed0.3_aniso0.6.gif "方向性ノイズ 3 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
