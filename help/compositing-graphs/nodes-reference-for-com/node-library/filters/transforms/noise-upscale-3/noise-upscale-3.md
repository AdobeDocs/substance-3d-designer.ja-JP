---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: ノイズアップスケール3ノードを使用すると、高解像度でディテールを保持するための高度なノイズベースのアルゴリズムを使用して、テクスチャをアップスケールすることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ノイズアップスケール3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# ノイズアップスケール3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## ノイズアップスケール3

**場所：** *フィルター/変形*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力ノイズの手続きを取り、ディテールを維持しながらタイリングをあまり発生させずに、2倍の解像度までスケールします。 ユーザー定義のマスクを使用して、元のスケールの上にノイズをブレンドします。

このノードは、主に重くて大きなノイズを使用する遅いグラフの最適化を目的としています。 これにより、計算時間をあまり長くすることなく、より高い解像度を使用できます。

[ノイズアップスケール1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md)と[ノイズアップスケール2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)も参照してください。ほとんどの場合、タイルを非表示にする方がわずかに優れています。

## パラメーター

### 入力

* **グレースケール**: *グレースケール入力*\
  ターゲットノイズの画像。
* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

*パラメーターがありません。*

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
