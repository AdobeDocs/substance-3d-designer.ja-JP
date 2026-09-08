---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: 湿潤ノイズノードを使用して、湿潤面の効果を生み出すための湿潤パターンと凝縮パターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水分ノイズ1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---


# 水分ノイズ1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![水分ノイズ 1 – アイコン](../../../../../../assets/moisture_noise_1.png "水分ノイズ 1 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

深みのあるスポンジのような<b>湿気</b>ノイズのバリエーションです。

様々な硬さとサイズの円盤で、ベースグレーから始まり、以下のカラーに分散され、追加または削除されます。

参照： [水分ノイズ2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

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
| <b>パターンサイズ</b> 浮動小数2 | スキャッタパターンのサイズの乗数。1.0は元のスキャタリングサイズです。 |
| <b>パターン角度</b>浮動小数 | 散布パターンの方向を指定する角度です。指定する角度はパターンが水平から右に向かって回転する回数です。 |
| <b>パターン角度ランダム</b>浮動小数 | <b>パターン角度</b>の値に適用されるランダムな変動の最大量（ターン数）。 |
| <b>グローバルの不透明度</b>浮動小数 | ノイズのすべての成分の不透明度。0.0の場合は基本が平坦なグレーになり、1.0の場合は成分によって適用される完全な加算または減算の結果です。 |
| <b>タイルのオフセット</b>浮動小数2 | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の展開</b> ブーリアン | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水分ノイズ1 – 例1](../../../../../../assets/moisture_noise_1_1.png "水分ノイズ1 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水分ノイズ1 – 例2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "水分ノイズ1 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![水分ノイズ1 – 例3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "水分ノイズ1 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![水分ノイズ1 – 例4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "水分ノイズ1 – 例4"){zoomable="yes"}

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
