---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: シェイプドロップシャドウノードを使用してシェイプにドロップシャドウ効果を加え、テクスチャの深度と奥行きを表現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプドロップシャドウ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# シェイプドロップシャドウ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## シェイプドロップシャドウ（グレースケール）

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力された白黒マスク（グレースケール版の場合）または透明画像（カラー版の場合）上で、他の2D画像処理ソフトウェアでよく知られている「ドロップシャドウ」効果を実行します。

[シャドウ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md)効果とは異なり、完全な透明度が適用された画像を返し、他のソフトウェアで期待されるものと同様の完全な効果が得られます。

## パラメーター

* **角度**: *0.0 ～ 1.0*&#x200B;光（フェイク）の入射角度。
* **距離**: *-0.5 - 0.5*&#x200B;影のドロップダウンと図形との間の距離を調整します。
* **サイズ**: *0.0 ～ 1.0*&#x200B;影のぼかしやぼやけを制御します。
* **スプレッド**: *0.0 ～ 1.0*&#x200B;ぼかし効果のカットオフ/トレショルドを設定すると、シャドウがさらに広がります。
* **不透明度**: *0.0 ～ 1.0*\
  シャドウ効果のブレンド不透明度。
* **（シャドウ）カラー**: *（カラー値）*シャドウに適用される色の濃淡。
* **マスクカラー**: *（カラー値） *（グレースケールバージョンのみ）**透明度マップされた出力に使用される単色。
* **入力は事前に乗算されています**: *False/True *（カラーバージョンのみ）**入力を事前に乗算されたものと見なすかどうかを指定します。
* **Pre-Multiply Output**: *False/True*&#x200B;出力を事前に乗算するかどうかを指定します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
