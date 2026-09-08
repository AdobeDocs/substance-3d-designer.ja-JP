---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-1.html"
breadcrumb-title: ''
description: 「BnWスポット1」ノードを使用して、白黒のスポットパターンを生成し、テクスチャバリエーションとディテールマスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BnWスポット1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# BnWスポット1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![BnW個のスポット1 – アイコン](../../../../../../assets/bnw_spots_1.png "BnW個のスポット1 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

粗い<b>白黒(BnW)スポット</b>のノイズのバリエーション。

参照： [BnW個の場所2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md)、[BnW個の場所3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

</td>
</tr>
</table>

## 出力

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 生成されるノイズをグレースケールビットマップとして表します。 |

## パラメーター

|  |  |
| --- | --- |
| <b>スケール</b>整数 | ノイズタイルの生成に使用するグリッドの区画。    値を大きくすると、描かれるタイルの数が増え、ノイズが高くなります。 |
| <b>障害</b>浮動小数点 | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b>浮動小数点 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>異方性の乱れ</b>浮動小数点 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの方向の範囲を制御します。値を大きくすると、より狭く、より明確な方向になります。    方向は、<b>Disorder異方性角度</b>パラメーターで制御されます。 |
| <b>乱雑な異方性角度</b>浮動小数点 | <b>Disorder 異方性</b>パラメーターが0ではない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>粗さ</b>浮動小数点 | ノイズオクターブのバランスです。オクターブの値を大きくすると、周波数が高いオクターブがより目立つようになります。 |
| <b>タイルのオフセット</b>浮動小数2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b> ブーリアン | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnWスポット1 – 例1](../../../../../../assets/bnw_spots_1_1.png "BnWスポット1 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnWスポット1 – 例2](../../../../../../assets/noise_bnw_spots_1_v2_speed0.6_aniso0.gif "BnWスポット1 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![BnWスポット1 – 例3](../../../../../../assets/noise_bnw_spots_1_v2_speed0.6_aniso1.gif "BnWスポット1 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![BnWスポット1 – 例4](../../../../../../assets/noise_bnw_spots_1_v2_speed0.3_aniso0.6.gif "BnWスポット1 – 例4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
