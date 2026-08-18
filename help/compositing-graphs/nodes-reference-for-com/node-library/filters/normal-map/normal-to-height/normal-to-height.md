---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: '[法線からHeight]ノードを使用して、サーフェスの深度情報を抽出するために法線マップをHeightマップに変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Heightに垂直
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Heightに垂直

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Heightに垂直

**場所：** *フィルター/標準マップ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

接線空間の法線マップを再び高さマップに変換しようとする逆変換ノード。 これは少しシンプルなバージョンです。[Height本部への通常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md)には、他のオプションがあります。

ノーマルマップソースしかなくても、ハイトマップと組み合わせて操作を実行したい場合に便利です。 Heightを通常に変換すると情報が失われるため、100%正しい結果を得ることはできないことに注意してください。 必要に応じて設定を調整すると、この非HQバージョンでは単純なディテールを適切に変換できます。

## パラメーター

* **リリーフバランス**: *0.0 ～ 1.0*&#x200B;周波数の違いが最終結果に与える影響の度合いを調整します。 これは入力マップに大きく依存し、かなりの微調整が必要です。
* **標準の形式**: *DirectX、OpenGL*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。
* **グローバルの不透明度**: *0.0 ～ 1.0*&#x200B;効果のグローバルの不透明度を調整します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
