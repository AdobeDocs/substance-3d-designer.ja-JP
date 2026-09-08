---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: 3Dウォリーノイズノードを使用して、3Dポジションに基づいてウォリーノイズを生成し、ボリュームテクスチャエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dワーリーノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 3Dワーリーノイズ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## 3Dワーリーノイズ

**イン：** *テクスチャジェネレータ**/ノイズ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ライブラリで最も汎用性が高く高度なノイズの1つで、入力ポジションマップに基づいて、3D空間でワーリーノイズを生成します。 標準の[セル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)や[距離](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)に基づくノイズよりもはるかに強力なオプションが多数用意されています。

## パラメーター

* **スケール**: *1 - 64*\
  エフェクトのグローバルスケールを設定します。
* **サイズ**: *0.0 ～ 1.0* X、Y、Z軸に対して個別に不均等なスケーリングを実行します。
* **モード**: *ユークリッド、マンハッタン、チェビシェフ、ミンコフスキー\
  距離メトリックを変更します。 非常に異なる種類のノイズを使用できます。*
* **ミンコフスキー数**: *0.0 ～ 20.0* Minkowski距離指標のみ。 異なる種類のメトリック間のブレンド。
* **スタイル**: *F1、F2、F2-F1、境界線、ランダムな色*&#x200B;メートル法の組み合わせの数式を設定します。 さらに多くの組み合わせを使用できます。
* **境界線の幅**: *0.0 ～ 1.0*&#x200B;境界線の組み合わせ計算がアクティブな場合、境界線の幅を制御します。
* **丸み**: *0.0 ～ 1.0* F1、F2、F2-F1モードでのみ使用できます。 レベルの中間位置を設定します。
* **反転**: *False/True*\
  結果を反転します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
