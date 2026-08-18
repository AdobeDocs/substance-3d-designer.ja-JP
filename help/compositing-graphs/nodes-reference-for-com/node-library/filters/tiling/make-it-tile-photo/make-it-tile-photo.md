---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: 「写真をタイル状にする」ノードを使用すると、素材を作成するために写真をシームレスなタイリングテクスチャに変換できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Make It Tile Photo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Make It Tile Photo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## Make It Tile Photo (Grayscale)

**イン：** *フィルター/タイル*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、エッジが連続していないためにタイリングできない可能性のあるイメージに対して、エッジ修正機能を提供します。 これは、入力画像のエッジ以外には影響しません。 尺度を調整したり、タイルを異なる方法で並べたりする場合は、[タイルパッチを作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)を参照してください。

## パラメーター

* **マスクワープH**: *-100.0 - 100.0*&#x200B;未定義のトランジションを避けるために、横軸にワープを導入します。
* **マスクワープV**: *-100.0 - 100.0*&#x200B;未定義のトランジションを避けるために、縦軸にワープを導入します。
* **マスクサイズH**: *0.0 ～ 1.0*&#x200B;トランジションの端が水平方向に到達する距離を設定します。
* **マスクサイズV**: *0.0 ～ 1.0*&#x200B;トランジションの端が垂直方向に達する範囲を設定します。
* **マスク精度H**: *0.0 ～ 1.0*&#x200B;水平方向の変化の滑らかさを設定します。
* **マスク精度V**: *0.0 ～ 1.0*&#x200B;垂直方向の切り替えの滑らかさを設定します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
