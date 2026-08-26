---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: '[カラーパレットを適用]ノードを使用すると、スタイル設定された色効果のカラーパレットを使用してテクスチャを再マップできます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーパレットを適用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# カラーパレットを適用

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![色の量子化アイコン](../../../../../../assets/ApplyColorPalette.png "色の量子化アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

IDマップを使用して、順序付けされたパレットのカラーを画像に適用します。

IDマップ内のインデックスをパレット内のカラーのインデックスに一致させることで、カラーが配分されます。

例えば、パレットのカラー#2は、ID値が2のIDマップ内のすべてのピクセルに適用されます。

このノードは、次のノードと組み合わせて使用できます： [色のクオンタイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[カラーパレットの作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、[カラーパレットの変更](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)、[カラーパレットの表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 入力コネクタ

|  |  |
| --- | --- |
| <b>ID</b> *グレースケール*&#x200B;プライマリ | 入力パレットの色を配布するために使用される入力IDマップ。   IDマップは、全体（例えば、シェイプ）の一部であるピクセルがすべて同じ一意の識別値を保持する画像です。 この場合、値は整数です。   IDマップは、[クオンタイズカラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)ノードを使用して作成できます。 |
| <b>パレット</b> *色* | ピクセルの行としてエンコードされたRGBカラーの順序付けされたリスト。 パレットには、最大256色を保持できます。 これは、ノードがIDマップのインデックスにマップするパレットです。   パレットは、[色の量子化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)ノードで生成し、[色のパレットを変更](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)ノードで変更できます。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *色* | パレットのカラーをIDマップのインデックスにマッピングした結果。 |

## 例

![カラーパレットの適用：例1](../../../../../../assets/apply_color_palette_example_2.png "カラーパレットの適用：例1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![カラーパレットの適用：例3](../../../../../../assets/apply_color_palette_example_4.png "カラーパレットの適用：例3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>後</i>
    </td>
  </tr>
</table>
