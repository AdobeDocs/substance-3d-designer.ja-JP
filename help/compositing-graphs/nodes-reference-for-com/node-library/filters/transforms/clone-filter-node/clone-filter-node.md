---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: コピーフィルターノードを使用して、テクスチャ領域を複製およびオフセットし、シームレスなパターン作成およびタイリング効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: クローン（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# クローン（フィルタノード）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## クローン

**場所：** *フィルター/変換*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

指定した場所に入力画像のクローンを1回作成します。 単純な「コピースタンプ」ツールとして機能できます。

意図した結果を得るには、ある程度の注意が必要です。

* 理想的には、ブレンドは直線コピーにすぎないため、入力画像には（デカールのような）アルファチャンネルが含まれています。
* マスクはデフォルトで黒に設定されているので、すべての結果を確認するには、少なくとも均一な白のグレースケール値を挿入する必要があります。
* オフセットは、画像の外側を簡単にクリップするので、小さい値を使用します。

## パラメーター

### 入力

* **ソース**: *カラー入力*\
  コピーする画像。 重要：画像にアルファチャンネルが含まれていることが理想的です。
* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 デフォルトは黒です。

### パラメーター

* **オフセット**: *-*\
  結果を移動または変換します。 正の値は左と上、負の値は右と下です。 小さい値1.0以上を使用すると、画像の外側に移動します。
* **ぼかしマスク**: *0.0 ～ 10.0\
  ぼかしフィルターをマスクに適用して、エッジをソフトにします。*

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
