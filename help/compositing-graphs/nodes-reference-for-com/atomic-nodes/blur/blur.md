---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: ぼかしノードを使用して、テクスチャにぼかし効果を適用し、ディテールを滑らかにしてソフトフォーカス効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ブラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---


# ブラー

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![ぼかしノードアイコン](blur.resources/blur-9.png){width="200px"}

**In:**&#x200B;個のアトミックノード

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

ぼかしノードは、「ボックスぼかし」操作を実行します。つまり、設定された距離のピクセルの値を平均し、ぼやけた、シャープでない外観を作成します。 [Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)で利用できる最も簡単、最速、かつ最も基本的なブラー操作を提供します。

ぼかしは、いくつかのエッジをわずかにソフトにするなど、高速でシンプルな操作ではよく機能しますが、より要求の厳しいシナリオでは[ぼかし（最高画質）](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)を選択することをお勧めします。これは、品質を考慮してパフォーマンスを落とすことになります。

</td>
</tr>
</table>

## パラメーター

* **強さ** : 0 – 無制限\
  ぼかしの強度または距離を設定します。 この数に上限はありませんが、値を大きくすると、画像全体が平均化されたカラーに変わります。

次の例は、高い値（この場合は50）を使用する場合の、左側にあるこのノードのぼかし、右側にある[ぼかし(HQ)](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)を示しています。 1 ～ 2程度の値にすると、この違いは目立ちません。

| ブラー（アトミック） | ブラー HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
