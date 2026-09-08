---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: '[法線からHeightへ] HQノードを使用して、サーフェスの詳細を抽出するために法線マップを高品質の高さマップに変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HeightHQに標準
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# HeightHQに標準

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## HeightHQに標準

**場所：** *フィルター/法線マップ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

正接空間のノーマルマップを再びハイトマップに変換しようとする逆変換ノード。 これは、より高度なノードです。[Heightに対して標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md)では、選択肢が少なく、異なる計算を使用します。

ノーマルマップソースしかなくても、ハイトマップと組み合わせて操作を実行したい場合に便利です。 Heightを通常に変換すると情報が失われるため、100%正しい結果を得ることはできないことに注意してください。 正しく生成されたHeightmapを置き換えることはできません。

## パラメーター

* **標準の形式**: *DirectX、OpenGL*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。
* **リリーフバランス**: *0.0 ～ 1.0*&#x200B;低周波バイアスと高周波バイアスのブレンド。
* **Heightの強さ**: *0.0 ～ 1.0* Heightmapの強さまたは乗数。グローバルな不透明度に少し似ています。
* **Heightの正規化**: *偽/真* Heightmapの範囲を自動的に拡大・縮小して、完全なコントラストを使用します（[自動レベル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)など）。
* **品質**: *通常、高*&#x200B;速度と品質を切り替えます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
