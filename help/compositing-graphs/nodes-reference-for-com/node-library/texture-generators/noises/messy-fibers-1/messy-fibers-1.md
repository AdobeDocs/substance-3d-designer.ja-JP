---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-1.html"
breadcrumb-title: ''
description: 「乱雑な繊維1」ノードを使用して、生地や繊維のテクスチャディテールを作成するための基本的な繊維パターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 乱雑な繊維1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# 乱雑な繊維1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![乱雑な繊維1 – アイコン](../../../../../../assets/messy_fibers_1.png "乱雑な繊維1 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>乱雑な繊維</b>構造のノイズのバリエーションです。

参照： [乱雑な繊維2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)、[乱雑な繊維3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>乱雑な異方性角度</b>浮動小数点 | &#39;Disorder 異方性&#39;パラメーターが0でない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>角度</b>浮動小数点 | ねじの方向の設定に使用する角度です。回転の回数で指定し、横方向右から開始します。 |
| <b>角度ランダム</b>浮動小数点 | <b>角度</b>の値に適用されるランダムな変動の最大量（ターン数）。 |
| <b>行番号</b>浮動小数点 | 基本スレッドに適用されるタイリングの量。値が大きいほど、スレッドの密度が高く、細くなります。 |
| <b>タイルのオフセット</b>浮動小数点2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b>ブール値 | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![乱雑な繊維1 – アイコン](../../../../../../assets/messy_fibers_1_1.png "乱雑な繊維1 – アイコン"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![乱雑な繊維1 – 例2](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.gif "乱雑な繊維1 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![乱雑な繊維1 – 例3](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso1.gif "乱雑な繊維1 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![乱雑な繊維1 – 例4](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.6.gif "乱雑な繊維1 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
