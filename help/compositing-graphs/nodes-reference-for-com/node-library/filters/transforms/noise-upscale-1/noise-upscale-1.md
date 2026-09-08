---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: テクスチャ解像度を上げるときにディテールを保持するノイズベースのアルゴリズムを使用してテクスチャをアップスケールするには、ノイズアップスケール1ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ノイズアップスケール1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# ノイズアップスケール1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## ノイズアップスケール1

**場所：** *フィルター/変形*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力ノイズの手続きを取り、ディテールを維持しながらタイリングをあまり発生させずに、2倍の解像度までスケールします。 「X」タイプのマスクを使用し、元の入力と同様のコントラストでブレンドします（内部ブレンドモードはコピー）。

このノードは、主に重くて大きなノイズを使用する遅いグラフの最適化を目的としています。 これにより、計算時間をあまり長くすることなく、より高い解像度を使用できます。

このプロセスのバリエーションについては、[ノイズアップスケール2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)および[ノイズアップスケール3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)も参照してください。

## パラメーター

* **オフセット1X**: *0.0 ～ 1.0*&#x200B;上と下のパーツをX軸に沿ってスライドします。
* **オフセット1Y**: *0.0 - 1.0*\
  上部と下部をY軸に沿ってスライドします。
* **オフセット2X**: *0.0 ～ 1.0*&#x200B;左右のパーツをX軸にスライドします。
* **オフセット2Y**: *0.0 ～ 1.0* Y軸の左右の部分をスライドします。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise1ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
