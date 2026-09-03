---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: 「カラーパレットを作成」ノードを使用して、テクスチャから16色のパレットを抽出し、定型化された効果を得ます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーパレットを作成(16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# カラーパレットを作成(16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![色の量子化アイコン](create-color-palette-16.resources/create-color-palette-16-01.png "色の量子化アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

カラーの順序付けされたリストを作成し、最大16色でパレットとして出力します。

ノードは、「パレット」入力のセットを使用して、既存のパレットに新しい色を追加できます。

このノードは、次のノードと組み合わせて使用できます： [色のクオンタイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[カラーパレットの適用](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)、[カラーパレットの変更](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)、[カラーパレットの表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パレット</b> <i>色</i>プライマリ | ピクセルの行としてエンコードされたRGBカラーの順序付けされたリスト。 パレットには、最大256色を保持できます。   この入力はオプションです。 使用する場合は、ノードによって設定された色がこのパレットに追加されます。   パレットは、[[カラーパレットの表示]](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)ノードで表示できます。 |
| <b>パレットの色の適用量</b> <i>整数</i> | パレットに格納される色の量。   この数が「パレット」画像入力の実際のカラー数と一致しない場合は、ビジュアライゼーションが不完全であるか、絶対に必要な数よりも多くの空きスロットがある可能性があります。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パレット</b> <i>色</i> | 指定した色が追加された、更新されたパレット。 |
| <b>パレットの色の適用量</b> <i>整数</i> | パレットに保存されているカラーの更新量。指定した量のカラーがパレットに追加されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>カラー適用量</b> *整数* | パレットに追加するカラーの量。 |
| <b>色#</b> *浮動小数点3* *&#39;カラーの値&#39;として使用可能なパラメーターの数* | パレットに追加する色。   カラーは、この番号付きリストと同じ順序でパレットに追加されます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![カラーパレットの作成：例1](create-color-palette-16.resources/create-color-palette-16-02.png "カラーパレットの作成：例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![カラーパレットの作成：例2](create-color-palette-16.resources/create-color-palette-16-03.png "カラーパレットの作成：例2"){zoomable="yes"}

</td>
</tr>
</table>

![カラーパレットの作成：例3](create-color-palette-16.resources/create-color-palette-16-04.png "カラーパレットの作成：例3"){zoomable="yes"}
