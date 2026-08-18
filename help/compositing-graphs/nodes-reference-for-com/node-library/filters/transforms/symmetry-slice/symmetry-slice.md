---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 対称スライスノードを使用すると、対称軸に沿ってテクスチャをスライスし、ミラーされたパターンやエフェクトを作成することができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 対称スライス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# 対称スライス

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## 対称スライス

**場所：** *フィルター/変換*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

複雑なシンメトリ/ミラーリング操作ノード。 フルコントロールで様々な幾何演算が可能ですが、多少の実験が必要です。

[ミラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)および[対称](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)と比較すると、このノードにはさらに多くのオプションがあります。

## パラメーター

* **対称モード**: *0 ～ 6*&#x200B;対称ジオメトリまたは対称線を選択してください。 オプションには、「水平方向」、「垂直方向」、「左右斜め」、「左右斜め」、「左右斜め」、「垂直反転」、「コーナー」、「対角角コーナー」があります。
* **転送モード**: *0 ～ 6\
  描画モード。 オプション： *
* **ブレンド**: *0.0 ～ 1.0*&#x200B;元の画像をブレンドして結果に戻します。
* **辺の反転**: *False/True*&#x200B;原点を反転します。つまり、操作の原点が反転します。 たとえば、左から右への対称は右から左になります。
* **Flip Side2**: *False/True*&#x200B;対称モードが5または6の場合にのみ使用されます。 コーナーの原点を反転します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
