---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: エッジ選択ノードを使用して、エッジベースのウェザリングおよび摩耗効果を作成するためのメッシュエッジを選択するマスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジ選択
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# エッジ選択

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## エッジ選択

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、曲率に基づいて任意の種類のエッジを選択する最適な方法です。 [レベルノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)を使用して手動で行う必要がない場合は、任意のレベルまたはコントラストの凸型と凹型を分離できます。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  エッジのハイライト表示に使用するベイク済みマップ。 必須！
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  [凸状]と[凹状]の両方のエッジハイライトの合計量を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  ハイライトのコントラストを[凸状]と[凹状]の両方で調整します。
* **凸型**
  * **凸状のエッジの幅**: *0.0 ～ 1.0*&#x200B;凸状のエッジのハイライトの幅を設定します。 「柔らかさ」を少し上げると、エッジが薄くなる可能性があることに注意してください。
  * **凸状の柔らかさ**: *0.0 ～ 1.0*&#x200B;凸状のエッジのトランジションの柔らかさを設定します。
  * **凸状の強度**: *0.0 ～ 1.0*&#x200B;凸状エッジのエッジハイライトの最大強度を設定します。 0に設定すると、ハイライト表示されません。
* **凹型**
  * **凹型エッジの幅**: *0.0 ～ 1.0*&#x200B;凹型エッジのハイライトの幅を設定します。 「柔らかさ」を少し上げると、エッジが薄くなる可能性があることに注意してください。
  * **凹状の柔らかさ**: *0.0 ～ 1.0*&#x200B;凹状のエッジの変化の柔らかさを設定します。
  * **凹状の強さ**: *0.0 ～ 1.0*&#x200B;凹状のエッジのエッジハイライトの最大強さを設定します。 0に設定すると、ハイライト表示されません。

## サンプル画像

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
