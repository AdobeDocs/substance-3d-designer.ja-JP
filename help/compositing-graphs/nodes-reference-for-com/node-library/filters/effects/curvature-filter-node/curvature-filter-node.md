---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: フィルターノードを使用して、高さマップから曲率マップを作成し、凸状および凹状のサーフェスを検出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率(フィルターノード)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 曲率(フィルターノード)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-1.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力[Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)に対して、単純で過酷なシングルパス曲率変換を行います。 作成されるマップには、凸状の領域に白い色合いがあり、凹状の領域に黒い色合いがあります。 曲率を使用すると、常にピクセルの細い線とシャープな効果が得られます。

このノードは、特定のエッジをすばやくハイライト表示したり暗くしたりする場合に便利です。 [曲率スムーズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) （高品質の結果が得られます）および[曲率ソフベル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) （より多くの選択肢があります）と比較すると、制限があります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 10.0</i> | エフェクトの強さ。 結果のコントラストを上げます。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-ex.png" />
        </td>
    </tr>
</table>
