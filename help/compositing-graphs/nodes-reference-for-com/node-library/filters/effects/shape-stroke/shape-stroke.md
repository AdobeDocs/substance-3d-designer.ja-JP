---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: シェイプの線ノードを使用して、線のアウトラインをシェイプに追加し、境界線やエッジ効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプの線
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# シェイプの線

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-stroke.png){width="128px"}

![](../../../../../../assets/shape-stroke-grayscale.png){width="128px"}

## シェイプストローク（グレースケール）

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

他の2D画像編集アプリケーションで使い慣れている黒と白のマスク（グレースケール版の場合）またはアルファチャンネル付きシェイプ（カラー版の場合）の周囲に、線やアウトラインを追加します。 [エッジ検出](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)のより完全なバージョンと見なすことができます。

様々な画像編集効果に非常に便利です。

## パラメーター

* **幅**: *-1.0 ～ 1.0*&#x200B;線効果の幅です。
* **不透明度**: *0.0 ～ 1.0*\
  エフェクトのグローバル不透明度。
* **（アウトライン）カラー**: *（カラー値）*アウトライン効果に使用されるカラー。
* **マスクカラー**: *（カラー値） *（グレースケールバージョンのみ）**透明度マップされた出力に使用される単色。
* **入力は事前に乗算されています**: *False/True *（カラーバージョンのみ）**入力を事前に乗算されたものと見なすかどうかを指定します。
* **Pre-Multiply Output**: *False/True*&#x200B;出力を事前に乗算するかどうかを指定します。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapestroke-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
