---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: セル3ノードを使用して、有機的および生物学的テクスチャ効果を生み出すための中間セルラーパターンを生成する。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セル 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# セル 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![セル 3 – アイコン](cells-3.resources/cells_3.png "セル 3 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>セル</b>の城壁ノイズのバリエーションです。

ディスクの交差は、不均一な柔らかさの薄い壁を持つセルを生成します。

参照： [セル 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[セル 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md)、[セル 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>硬さ</b> <i>浮動小数</i> | セルの壁の定義。値を大きくすると、壁がより鮮明になります。 |
| <b>反転</b> <i>ブーリアン</i> | 出力画像のグレースケール値を反転します。 |
| <b>障害</b> <i>浮動小数</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>異方性の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの方向の範囲を制御します。値を大きくすると、より狭く、より明確な方向になります。    方向は、<b>Disorder異方性角度</b>パラメーターで制御されます。 |
| <b>anisotropy angleの乱れ</b> <i>フロート</i> | &#39;Disorder 異方性&#39;パラメーターが0でない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>パターンサイズ</b> <i>浮動小数点2</i> | セル内の分散ディスクのサイズの乗数。1.0はセルのフルスパンです。 |
| <b>パターンスケール</b> <i>フロート</i> | <b>パターンサイズ</b>の乗数。1.0は完全なサイズです。 |
| <b>角度</b> <i>フロート</i> | 円盤の方向を設定するために使用する角度です。回転の回数で指定し、水平右から開始します。 |
| <b>角度ランダム</b> <i>フロート</i> | <b>角度</b>の値に適用されるランダムな変動の最大量（ターン数）。 |
| <b>タイルのオフセット</b> <i>浮動小数点2</i> | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の拡張</b> <i>ブーリアン</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![セル 3 – 例1](cells-3.resources/cells_3_1.png "セル 3 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![セル 3 – 例2](cells-3.resources/noise_cells_3_v2_speed0.6_aniso0.gif "セル 3 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![セル 3 – 例3](cells-3.resources/noise_cells_3_v2_speed0.6_aniso1.gif "セル 3 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![セル 3 – 例4](cells-3.resources/noise_cells_3_v2_speed0.3_aniso0.6.gif "セル 3 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
