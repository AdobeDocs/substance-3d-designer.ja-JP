---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ''
description: 「乱雑な繊維3」ノードを使用すると、複雑な繊維パターンを作成して、布地や繊維のテクスチャ効果を生み出すことができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 乱雑な繊維3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# 乱雑な繊維3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![乱雑な繊維3 – アイコン](../../../../../../assets/messy_fibers_3.png "乱雑な繊維3 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>乱雑な繊維</b>構造のノイズのバリエーションです。

参照： [乱雑な繊維1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md)、[乱雑な繊維2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>輝度ランダム</b>浮動小数点 | スレッドからランダムに差し引かれた輝度の範囲です。1は全範囲です。 |
| <b>タイルのオフセット</b>浮動小数点2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b>ブール値 | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![乱雑な繊維3 – 例1](../../../../../../assets/messy_fibers_3_1.png "乱雑な繊維3 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![乱雑な繊維3 – 例2](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.gif "乱雑な繊維3 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![乱雑な繊維3 – 例3](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso1.gif "乱雑な繊維3 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![乱雑な繊維3 – 例4](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif "乱雑な繊維3 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
