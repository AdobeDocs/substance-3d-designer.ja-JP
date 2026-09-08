---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: '[曲率]フィルタノードを使用して、凸状サーフェスと凹状サーフェスを検出するためのHeightマップから曲率マップを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲率（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# 曲率（フィルタノード）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## 曲率

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力[Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)に対して、単純で過酷なシングルパス曲率変換を実行します。 作成されるマップには、凸状の領域に白い色合いがあり、凹状の領域に黒い色合いがあります。 曲率は、常にピクセルの細い線とシャープなトランジションを生成します。

このノードは、特定のエッジをすばやくハイライト表示したり暗くしたりする場合に便利です。 [曲線の滑らかさ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) （高品質の結果を生成）および[曲線の粗さ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) （多くのオプションを含む）と比較すると、この値に制限があります。

## パラメーター

* **適用度**: *0.0 ～ 10.0*&#x200B;効果の適用度。 結果のコントラストを上げます。
* **標準の形式**: *DirectX、OpenGL*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
