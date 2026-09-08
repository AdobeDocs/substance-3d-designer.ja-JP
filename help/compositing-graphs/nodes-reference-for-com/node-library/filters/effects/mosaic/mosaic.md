---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: モザイクノードを使用して、ピクセルをピクセル化されたブロックとパターンに分割することで、モザイク状のタイル効果をテクスチャします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: モザイク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# モザイク

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

## モザイク（グレースケール）

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

マルチパス[ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)効果を実行して、既存の滑らかな傾斜したグラデーションマップを「多面的に」します。 両方の入力に同じマップを使用すると、基本的に明るい領域が大きくなり、強調されます。

これは、Heightmapなどのグレースケールマップに多くの定義を追加する場合に便利です。シェイプにさらなる定義を加えることができます。

## パラメーター

### 入力

* **カラー**: *カラー/グレースケール入力*
* **モザイクマップ**: *グレースケール入力*\
  ワープドライバーマップ。 最初の入力と同じにすることができます。

### パラメーター

* **サンプル**: *0 ～ 16*&#x200B;マルチサンプルの品質を決定します。
* **適用度**: *0.0 ～ 1.0*&#x200B;効果の強さ。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mosaci-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
