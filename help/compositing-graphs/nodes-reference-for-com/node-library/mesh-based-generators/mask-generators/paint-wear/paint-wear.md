---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: ペイントの摩耗ノードを使用して、メッシュジオメトリに基づいてペイントの摩耗マスクを生成し、リアルなペイントのチッピングエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ペイントの摩耗
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# ペイントの摩耗

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## ペイントの摩耗

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、ペイントが剥がれ落ちて、エッジがすり減っていることを表します。

## パラメーター

### 入力

* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **バリエーションマスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  ペイントの摩耗量の合計を設定し、徐々に表示します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **オクルージョン**: *0.0 ～ 1.0*&#x200B;焼き上げた青が暗い領域の摩耗を防ぐ効果の量を設定します。
* **半径**: *0.0 ～ 2.0*&#x200B;チッピング効果が凸状のエッジからどの程度広がるかを設定します。
* **バリエーション**: *0.0 ～ 1.0*&#x200B;効果にブレンドするバリエーション(経年劣化)の量を設定します。
* **バリエーションマスクの上書き**: *False/True*&#x200B;カスタムバリエーション(経年劣化)マップ入力スロットを有効にします。

## サンプル画像

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
