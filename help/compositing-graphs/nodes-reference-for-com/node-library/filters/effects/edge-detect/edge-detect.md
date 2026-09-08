---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: エッジ検出ノードを使用して、テクスチャのエッジを検出し、アウトラインやエッジベースのマスク効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジ検出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# エッジ検出

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## エッジ検出

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

白黒画像のコントラストを検出し、そのコントラストを強調する白黒マスクを作成します。

エッジに対して何らかのマスクが必要な場合に便利です。 コントラストの強い入力では最適に機能することに注意してください。必要に応じて、コントラストを調整してから、このノードに値を渡してください。

## パラメーター

* **エッジの幅**: *1.0 ～ 16.0*&#x200B;エッジの周囲で検出された領域の幅。
* **エッジの丸み**: *0.0 ～ 16.0*&#x200B;生成されたマスクを丸め、ぼかし、滑らかにします。
* **反転**: *False/True*\
  結果を反転します。
* **許容値**: *0.0 ～ 1.0*&#x200B;エッジが表示される場所の許容値トレッシュホールド係数。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
