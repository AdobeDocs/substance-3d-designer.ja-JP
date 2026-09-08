---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: セル2ノードを使用して、有機的および生物学的テクスチャ効果を生み出すための中間セルラーパターンを生成する。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セル 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# セル 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![セル 2 – アイコン](../../../../../../assets/cells_2.png "セル 2 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>セル</b>の城壁ノイズのバリエーションです。

調整可能な壁Thicknessを備えたセルのバイナリマスク。

参照： [セル 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[セル 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)、[セル 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>エッジの幅</b>浮動小数 | セル間の壁のThicknessを、グリッドの比率で補正します。 （解像度に依存しない） |
| <b>ブーリアンの反転</b> | 出力画像の黒と白を切り替えます。 |
| <b>障害</b>浮動小数 | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b>浮動小数 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>非正方形の展開</b> ブーリアン | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成量を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![セル 2 – 例1](../../../../../../assets/cells_2_1.png "セル 2 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![セル 2 – 例2](../../../../../../assets/noise_cells_2_v2_speed0.3_aniso0.6.gif "セル 2 – 例2"){zoomable="yes"}

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
