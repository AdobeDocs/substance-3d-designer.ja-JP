---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: マテリアルセレクタノードを使用して、マルチマテリアルテクスチャ効果を作成するためのメッシュデータに基づいてマテリアルを選択します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルセレクター
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# マテリアルセレクター

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## マテリアルセレクター

**In:** *メッシュベースのジェネレーター**/Utilities*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

フルカラーのIDマップを、白黒のバイナリマスクに変換します。 異なるカラーをブレンドして1つのマスクに結合できます。

これは、[マルチマテリアルのブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)を使用せずにマスクを手動で使用する場合や、同じマスクを他の場所で手動で使用する場合に便利です。

## パラメーター

* **マテリアル**: 1 ～ 16\
  結合が有効になっているマテリアルの数を設定します。
* **マテリアル#1-16を有効にする**: False/True\
  最終的な出力マスクへのカラーのブレンドと合成を切り替えます。 結合するカラーの数に応じて有効にできます。
* **マテリアル#1-16**: （カラー値）\
  白黒に変換されるマテリアルカラーのカラーピッカー。
* **カラーピッカーパラメーター**\
  カラーのブレンドと、カラーの白黒への変換を変更します。
  * **ぼやけ**: 0.01 ～ 1.0\
    隣接するカラーとどれだけブレンドするかを指定します。
  * **パディング**: 0.0 ～ 1.0\
    コントラストなど、変化のシャープさ。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
