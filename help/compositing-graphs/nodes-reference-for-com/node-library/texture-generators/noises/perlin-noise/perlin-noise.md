---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: パーリンノイズノードを使用して、自然なテクスチャやバリエーションを生み出すための滑らかな自然な外観のノイズパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パーリンノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# パーリンノイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![パーリンのノイズ – アイコン](perlin-noise.resources/perlin_noise.png "パーリンのノイズ – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

パーリンノイズ（グレースケール値の分布で広く使用されている）を生成します。

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
| <b>スケール</b> <i>整数</i> | ノイズタイルの作成に使用するグリッドの区画。    値を大きくすると、より多くのタイルが描画され、ノイズが濃くなります。 |
| <b>障害</b> <i>浮動小数</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>浮動小数</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>タイルのオフセット</b> <i>浮動小数2</i> | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の拡張</b> <i>ブーリアン</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Perlinのノイズ – 例1](perlin-noise.resources/perlin_noise_1.png "Perlinのノイズ – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Perlinのノイズ – 例2](perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif "Perlinのノイズ – 例2"){zoomable="yes"}

</td>
</tr>
</table>
