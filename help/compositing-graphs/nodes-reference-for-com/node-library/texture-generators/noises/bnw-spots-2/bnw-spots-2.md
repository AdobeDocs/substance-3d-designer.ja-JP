---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-2.html"
breadcrumb-title: ''
description: 「BnWスポット2」ノードを使用して、テクスチャバリエーションのコントロールを強化した白黒のスポットパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BnWスポット2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# BnWスポット2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![BnW個のスポット2 – アイコン](../../../../../../assets/bnw_spots_2.png "BnW個のスポット2 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

粗い<b>白黒(BnW)スポット</b>のノイズのバリエーション。

参照： [BnW個の場所1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-1/bnw-spots-1.md)、[BnW個の場所3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

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
| <b>anisotropy angleの乱れ</b> <i>フロート</i> | <b>Disorder 異方性</b>パラメーターが0ではない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>タイルのオフセット</b> <i>浮動小数点2</i> | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnWスポット2 – 例1](../../../../../../assets/bnw_spots_2_1.png "BnWスポット2 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnWスポット2 – 例2](../../../../../../assets/noise_bnw_spots_2_v2_speed0.6_aniso0.gif "BnWスポット2 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnWスポット2 – 例3](../../../../../../assets/noise_bnw_spots_2_v2_speed0.6_aniso1.gif "BnWスポット2 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnWスポット2 – 例4](../../../../../../assets/noise_bnw_spots_2_v2_speed0.3_aniso0.6.gif "BnWスポット2 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
