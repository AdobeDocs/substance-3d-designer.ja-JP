---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: '[カラーパレットを表示]ノードを使用して、解析用にテクスチャから抽出されたカラーパレットデータを表示します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーパレットを表示
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# カラーパレットを表示

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![色の量子化アイコン](view-color-palette.resources/ViewColorPalette.png "色の量子化アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

カラーパレットを正方形または長方形にパックして、グラフビューや2Dビューで見やすくします。\
そのパッキングは、できるだけ少ない空きスロットを残すことを目指している。

</td>
</tr>
</table>

パレット内のカラーの順序は保持され、テキストの折り返しと同様に、カラーは左から右、上から下に向かって流れます。

このノードは、次のノードによって生成されたパレットを視覚化するために使用できます： [色の量子化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[色パレットを作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、[色パレットを変更](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パレット</b> <i>色</i>プライマリ | ピクセルの行としてエンコードされたRGBカラーの順序付けされたリスト。 パレットには、最大256色を保持できます。   これは、ノードがパックおよびレンダリングするパレットです。 |
| <b>パレットの色の適用量</b> <i>整数</i> | パレットに格納される色の量。   この数が「パレット」画像入力の実際のカラー数と一致しない場合は、ビジュアライゼーションが不完全であるか、絶対に必要な数よりも多くの空きスロットがある可能性があります。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>色</i> | パックされたパレットの表示。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![カラーパレットの表示：例1](view-color-palette.resources/view_color_palette_example_1.png "カラーパレットの表示：例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![カラーパレットの表示：例2](view-color-palette.resources/view_color_palette_example_2.png "カラーパレットの表示：例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![カラーパレットの表示：例3](view-color-palette.resources/view_color_palette_example_3.png "カラーパレットの表示：例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![カラーパレットの表示：例4](view-color-palette.resources/view_color_palette_example_4.png "カラーパレットの表示：例4"){zoomable="yes"}

</td>
</tr>
</table>
