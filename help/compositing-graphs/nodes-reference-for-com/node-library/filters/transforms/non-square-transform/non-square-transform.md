---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Non-Square Transformノードを使用して、XおよびYスケールが独立している非正方形テクスチャにトランスフォームを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非正方形の変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# 非正方形の変形

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 非正方形の変形（グレースケール）

**場所：** *フィルター/変換*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

[Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)の非正方形セーフバージョンです。 非正方形の比率を自動的に検出し、正方形の入力画像を非正方形カンバスに変換できます。

このノードを最大限に活用するには、いくつかの設定を正しく設定する必要があるため、[グラフパラメーター](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)を十分に理解してください。

* **グラフ**&#x200B;のサイズは非正方形である必要があります。そうでない場合、このノードは必要ありません。
* 非正方形トランスフォーム&#x200B;**ノード**&#x200B;の出力サイズを「*親に対して相対的*」に設定します。
* 入力を1つの位置に変換するだけの場合は、**ノードの**&#x200B;並べて表示モードを「*並べて表示しない*」に設定します。

## パラメーター

* **タイルモード**: *自動、手動*&#x200B;非正方形の自動補正を有効にするかどうかを指定します。
* **タイル**: *1 - 16*&#x200B;タイルモードが手動に設定されている場合にのみアクセスできます。 タイリングセーフな方法でスケールを変更できます。
* **オフセット**: *0.0 - 1.0*\
  結果を移動または変換します。 負の値を入力するには、スライダーをダブルクリックします。
* **回転**: *0.0 ～ 1.0*&#x200B;入力画像を回転します。
* **安全な回転（正方形のみ）**: *偽/真*&#x200B;安全な値にスナップして、ピクセルのシャープさを維持します。
* **背景色**: *（カラー値）*画像を塗りつぶす背景色。 基本パラメーターの[タイルモードが「*タイル表示なし*」](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)に設定されている場合にのみ表示されます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
