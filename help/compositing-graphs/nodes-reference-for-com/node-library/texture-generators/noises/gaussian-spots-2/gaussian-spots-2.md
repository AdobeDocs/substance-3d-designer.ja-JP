---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-2.html"
breadcrumb-title: ''
description: 「ガウスの斑点2」ノードを使用して、有機的なテクスチャのバリエーションを生み出すための高度なガウスのスポットパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ガウス斑2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# ガウス斑2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ガウスのスポット2 – アイコン](../../../../../../assets/gaussian_spots_2.png "ガウスのスポット2 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

滑らかな<b>ガウスの斑点</b>のノイズのバリエーションです。\
[ガウスノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)ノードに基づいて、グラデーションの幅を狭くし、周波数を高くします。

関連項目： [ガウススポット1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md)

</td>
</tr>
</table>

## 出力

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 生成されるノイズをグレースケールビットマップとして指定します。 |

## パラメーター

|  |  |
| --- | --- |
| <b>スケール</b> 整数 | ノイズタイルの作成に使用するグリッドの区画。    値を大きくすると、より多くのタイルが描画され、ノイズが濃くなります。 |
| <b>障害</b>浮動小数 | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b>浮動小数 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>異方性の障害</b>浮動小数 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの方向の範囲を制御します。値を大きくすると、より狭く、より明確な方向になります。    方向は、<b>Disorder anisotropy angle</b>パラメーターによって制御されます。 |
| <b>anisotropy angleの障害</b>浮動小数 | <b>Disorder 異方性</b>パラメーターが0ではない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>タイルのオフセット</b>浮動小数2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b> ブーリアン | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ガウスのスポット2 – 例1](../../../../../../assets/gaussian_spots_2_1.png "ガウスのスポット2 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ガウスのスポット2 – 例2](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso0.gif "ガウスのスポット2 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ガウスのスポット2 – 例3](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.6_aniso1.gif "ガウスのスポット2 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ガウスのスポット2 – 例4](../../../../../../assets/noise_gaussian_spots_2_v2_speed0.3_aniso0.6.gif "ガウスのスポット2 – 例4"){zoomable="yes"}

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
