---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: セル 2ノードを使用して、有機的および生物学的なテクスチャ効果を生み出すための中間のセルラーパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セル 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# セル 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![セル 2 – アイコン](cells-2.resources/cells-2-01.png "セル 2 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>セル</b>の壁面雑音のバリエーションです。

調整可能な壁Thicknessを備えたセルのバイナリマスク。

参照： [セル 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)、[セル 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)、[セル 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>エッジの幅</b> <i>フロート</i> | セル間の壁のThicknessをグリッドの比率で調整します。 （解像度に依存しない） |
| <b>反転</b> <i>ブール値</i> | 出力画像の黒と白を切り替えます。 |
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![セル 2 – 例1](cells-2.resources/cells-2-02.png "セル 2 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![セル 2 – 例2](cells-2.resources/cells-2-03.gif "セル 2 – 例2"){zoomable="yes"}

</td>
</tr>
</table>
