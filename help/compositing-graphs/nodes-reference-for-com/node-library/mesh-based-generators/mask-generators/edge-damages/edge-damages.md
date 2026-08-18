---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: エッジの損傷ノードを使用して、メッシュのエッジに損傷マスクを生成し、エッジの磨耗や破損をリアルに表現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジの損害賠償
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# エッジの損害賠償

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## エッジの損害賠償

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、曲率とベイク処理されたAOに基づいて、隆起した凸状のエッジに加えられたダメージを表します。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  エフェクトの配置に使用されるベイク済みマップ。 必須！
* **環境オクルージョン**: *グレースケール入力*\
  エフェクトの配置に使用されるベイク済みマップ。 必須！
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  適用するエッジのダメージ量。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **ダメージの強さ**: *0.0 ～ 1.0*&#x200B;欠けた一貫性のある外観と、カオスで傷だらけで大きなダメージを受けた外観との間で変化します。

## サンプル画像

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
