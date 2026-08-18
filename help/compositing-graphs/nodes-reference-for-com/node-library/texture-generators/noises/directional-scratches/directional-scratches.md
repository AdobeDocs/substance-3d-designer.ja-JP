---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: '[方向Scratches]ノードを使用して、マテリアルに磨耗や損傷の効果を加える方向のスクラッチパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方向スクラッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# 方向スクラッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![方向スクラッチ – アイコン](../../../../../../assets/directional_scratches.png "方向スクラッチ – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

角度とサイズを調整できるスクラッチパターンのランダムな散布。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 出力

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
<td style="border: 0;" valign="top">

### 例

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
| <b>角度</b>浮動小数点 | スクラッチの方向を設定するために使用する角度です。ターン数および水平方向の右から始まります。 |
| <b>角度ランダム</b>浮動小数点 | <b>角度</b>の値に適用されるランダムな変動の最大量（ターン数）。 |
| <b>パターン適用量</b>浮動小数点 | 散布されるスクラッチパターンの量の乗数。 |
| <b>パターンサイズ</b>浮動小数点2 | スクラッチパターンの境界ボックスのサイズです。    Y値はスクラッチの最大長を制御します。 |
| <b>パターンサイズランダム</b>浮動小数点2 | スクラッチに適用されるダウンスケーリングのランダム量の乗数。    Y値は、スクラッチの長さに適用されます。 |
| <b>タイルのオフセット</b>浮動小数点2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b>ブール値 | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向の傷 – 例1](../../../../../../assets/directional_scratches_1.png "方向の傷 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向の傷 – 例2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "方向の傷 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向の傷 – 例3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "方向の傷 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向の傷 – 例4](../../../../../../assets/noise-directional-scrat-1.gif "方向の傷 – 例4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向の傷 – 例5](../../../../../../assets/noise-directional-scrat-2.gif "方向の傷 – 例5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
