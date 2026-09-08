---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: 「Flood Fillからグラデーションへ」ノードを使用すると、滑らかなカラー効果を作成するために、領域をグラデーション値で塗りつぶすことができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fillからグラデーション
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Flood Fillからグラデーション

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## Flood Fillからグラデーション

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)ベースを（ランダムな方向の）グラデーションに変換します。 タイルがランダムに傾いたり傾斜したりしているハイトマップを作成するのに非常に便利です。

## パラメーター

### 入力

* **Flood Fill**: *色入力*&#x200B;基本Flood Fillデータ。
* **角度入力**: *グレースケール入力*\
  外部マップを使用してセルごとの角度を決定するオプションマップ。
* **勾配入力**: *グレースケール入力*&#x200B;セルごとのグラデーションの勾配強さを決定するオプションのマップ。

### *パラメーター*

* **角度**: *0.0 ～ 1.0*&#x200B;すべてのタイルに均等なグローバル角度/方向を設定します。
* **角度のバリエーション**: *0.0 ～ 1.0*&#x200B;各タイルの角度を個別にランダム化します。 これは最も便利で強力なパラメーターです。
* **バウンディングボックスのサイズで乗算**: *0.0 ～ 1.0*&#x200B;タイルの個々のバウンディングボックスのサイズに合わせて、線形効果全体のサイズを調整します。 つまり、小さなタイルは大きなタイルよりも暗くなります。
* **角度画像入力マルチプライヤ**: *0.0 - 1.0*&#x200B;生成されるグラデーションの方向に対するオプションの角度入力マップの影響を設定します
* **勾配イメージ入力マルチプライヤ**: *0.0 - 1.0*\
  生成されるグラデーションの勾配強度に対する、オプションの勾配入力マップの影響を設定します。
* **勾配強度で乗算**: *0.0 ～ 1.0*
* **平坦な勾配の色**: *（グレースケール値）*平坦な勾配に対して単色の値を設定できます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
