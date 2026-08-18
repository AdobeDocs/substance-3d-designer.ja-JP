---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: カラー範囲の置き換えノードを使用して、指定した範囲内のカラーをカラー補正のために新しいカラーに置き換えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラー範囲を置換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# カラー範囲を置換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## カラー範囲を置換

**イン：** *フィルター/調整*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ソースカラーをターゲットカラーに置き換えます。追加のコントロールがあります。 たとえば、マテリアルIDマップ（ベイク）のパーツの色を変更するために使用できます。

より詳細なバージョンについては、[カラーマッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)を参照してください。

## パラメーター

* **ソースカラー**: *（カラー値）*置き換える色。
* **ターゲットの色**: *（色の値）*置き換える色。
* **ソース範囲**: *0.0 -* 1.0\
  選択したソースの範囲または許容値。 隣接するカラーの色相もシフトされるように、色相を大きくすることができます。
* **しきい値**: *0.0 ～ 1.0*&#x200B;範囲のフォールオフ/コントラスト。 ソースカラーのみを置き換えるには低く、ソースカラーにブレンドするカラーを置き換えるには高く設定します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
