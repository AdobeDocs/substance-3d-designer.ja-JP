---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 曲率のSobelノードを使用して、エッジベースのマスクを作成するためのSobel演算子を使用して曲率のエッジを検出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率ソベル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 曲率ソベル

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## 曲率ソベル

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力[Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)に対して、単純で過酷なシングルパス曲率変換を行います。 作成されるマップには、凸状の領域に白い色合いがあり、凹状の領域に黒い色合いがあります。 曲率を行うと、常に線が太くなり、変化がシャープになります。

このノードは、特定のエッジをすばやくハイライト表示したり暗くしたりする場合に便利です。 これは、[曲率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)とは少し異なります。画質は向上しますが、シャープで粗い印象を与えます。

## パラメーター

* **適用度**: *0.0 ～ 1.0*&#x200B;効果の適用度で、コントラストを調整します。
* **通常の型**: *DirectX、OpenGL*

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
