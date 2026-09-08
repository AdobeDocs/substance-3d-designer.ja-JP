---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: '[Flood Fillからボックスサイズへ]ノードを使用して、プロシージャスケーリング効果のバウンディングボックスサイズ値で領域を塗りつぶします。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fillのサイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Flood Fillのサイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)を基準として、各タイルの個々のサイズに関連付けられた値を使用してグレースケールマップを作成します。

値はカンバスサイズ全体に対する相対値で表示されます（完全な白いタイルの場合、カンバス全体が引き伸ばされます）。したがって、コントラストは低くなることがよくあります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>出力</b> <i>最大(X, Y), X, Y</i> | 値の基準となるメトリック（幅、長さまたはその両方）を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodbbox-ex1.png" />
        </td>
    </tr>
</table>
