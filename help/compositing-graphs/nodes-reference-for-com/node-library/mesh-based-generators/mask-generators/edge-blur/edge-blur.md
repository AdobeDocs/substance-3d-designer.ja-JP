---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: エッジぼかしノードを使用してエッジマスクをぼかし、緩やかな遷移と滑らかなエッジベースの耐候性エフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジぼかし
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# エッジぼかし

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## エッジぼかし

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、ベイク処理された曲率マップに基づいてエッジをハイライトします。 これは、非常に単純なマスクジェネレータの1つです。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  効果の基になるベイク済みマップです。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  エッジのハイライトの度合いを設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **ぼかしの半径**: *0.0 ～ 8.0*&#x200B;ハイライトされたエッジのぼかしの量を設定します。

## サンプル画像

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>
