---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: ベベルフィルターノードを使用して、シェイプとパターンに深度と立体感を加えるためのベベルエッジを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベベル（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# ベベル（フィルタノード）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## ベベル

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力グレースケールのハイトマップにエッジの面取り効果を適用します。 ベベルのHeightmapと、そのHeightmapに基づくNormalmapの両方を返します。

このノードは、理想的にはバイナリ（高契約の白黒）の基本的なハイトマップに正確なカーブプロファイルを適用するのに便利です。

## パラメーター

### 入力

* **入力**: *グレースケール入力*\
  変換するマップを高くします。
* **カスタム曲線**: *グレースケール入力*\
  正確なカーブ/勾配を決定するグラデーション。 [レベル](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)や[トーンカーブ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)など、あらゆる種類の調整を実行できるグラデーション線形ノードが理想的です。 [カスタムカーブを使用]がTrueの場合にのみアクティブになります。

### パラメーター

* **距離**: *-1.0 ～ 1.0*&#x200B;ベベル効果が到達する距離。
* **角の種類**: *丸み、Angular*&#x200B;面取りのプロファイルを丸めるか直線にするかを指定します。
* **スムージング**: *0.0 ～ 5.0*&#x200B;ベベルの後で実行する追加のスムージング（ぼかし）の量。
* **不均一なぼかしを使用**: *偽/真*&#x200B;滑らかさを不均一にするかどうかを指定します。
* **カスタムカーブの使用**: *False/True*&#x200B;独自のカスタムHeightカーブの使用を切り替えます。 詳しくは、上記を参照してください。
* **法線の強度**: *0.0 ～ 50.0*&#x200B;生成された法線マップの強度。
* **標準の形式**: *DirectX、OpenGL*\
  別のノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
