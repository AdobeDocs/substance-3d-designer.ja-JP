---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: ambient occlusion HBAO フィルターノードを使用すると、ホライズンベースのアルゴリズムを使用してambient occlusionマップを作成し、リアルなシェーディングを実現できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ambient occlusion(HBAO)(フィルターノード)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Ambient occlusion(HBAO)(フィルターノード)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Ambient occlusion(HBAO)

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

Heightmapを入力として取り、そこからAmbient occlusionマップを生成します。 これは、元々スクリーン空間でリアルタイムにAOを生成することを目的としたAmbient occlusionであるHorizon-Based Algorithmを使用しています。 プロシージャルのHeightmapsからプロシージャルのAOマップを作成する場合に非常に便利です。

より高度で低速なAOの別のバージョンについては、[Ambient occlusion (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)を参照してください

## パラメーター

* **ワールド単位の使用**: *偽/真*&#x200B;ワールド単位またはシーンスペース単位の使用を切り替えます。 より正確な制御を可能にする追加のパラメーターを有効にします。
* **深度**: *0.0 ～ 1.0*&#x200B;ワールド単位がFalseに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。
* **サーフェスサイズ**: **0.0 ～ 1000.0**&#x200B;ワールド単位がTrueに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。
* **Heightスケール(cm)**: *0.0 ～ 1000.0*&#x200B;ワールド単位がTrueに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。
* **半径**: *0.0 ～ 1.0* AOの範囲を制御します。
* **品質**: *4サンプル、8サンプル、16サンプル*\
  計算に使用するサンプルの量を決定して品質レベルを設定します。
* **GPU最適化**: *False/True*&#x200B;内部GPU最適化を有効にして、処理を高速化します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
