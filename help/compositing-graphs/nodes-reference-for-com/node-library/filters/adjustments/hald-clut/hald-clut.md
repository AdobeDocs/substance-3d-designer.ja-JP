---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: 「Hald CLUT」ノードを使用すると、カラーグレーディングと補正にHald CLUT形式を使用してカラールックアップテーブルを適用できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ハルト・クラット
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# ハルト・クラット

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力画像にLUTを適用します。 LUTは4096\*4096の解像度でHald形式である必要があります。 詳細については、<http://www.quelsolaar.com/technology/clut.html>を参照してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー入力</i> | LUTを適用する画像。 |
| <b>lut</b> <i>カラー入力</i> | Lut入力スロット。 4096 x 4096でなければなりません。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>AlphaごとのLUT強度</b> <i>False/True</i> | LUT効果をアルファチャンネルでウェイト付けするかどうかを定義します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
