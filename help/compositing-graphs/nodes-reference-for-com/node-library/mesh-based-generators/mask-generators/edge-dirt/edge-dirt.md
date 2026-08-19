---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: エッジDirtノードを使用して、メッシュエッジにDirtのアキュムレーションマスクを作成し、リアルなエッジのウェザリングエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジDirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# エッジDirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## エッジDirt

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、Dirtマップのみに基づいてエッジの周囲に集まる曲率エフェクトを表します。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  エフェクトの配置に使用されるベイク済みマップ。 必須！
* **バリエーションマスク**: *グレースケール入力*\
  ノードのエフェクトをマスクするために使用されるマスクスロット。オーバーライドパラメータが有効な場合にのみ使用されます。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  Dirt量を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **バリエーション**: *0.0 ～ 1.0*&#x200B;大規模なマスクや分割をどの程度行うかをブレンドします。
* **バリエーションマスクの上書き**: *False/True*

## サンプル画像

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
