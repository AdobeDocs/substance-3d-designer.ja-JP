---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: '[エッジの斑点]ノードを使用して、メッシュエッジに斑点のある摩耗パターンを生成し、リアルなエッジのダメージ効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジの斑点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# エッジの斑点

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## エッジの斑点

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、エッジを分割するためのわずかな斑点が追加されたエッジを表します。 [エッジDirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)も参照してください。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  エッジのハイライトに使用するベイク済みマップ。 必須！
* **バリエーションマスク**: *グレースケール入力*\
  ノードのエフェクトをマスクするために使用するオプションのマスクスロット。 「バリエーションマスクを上書き」で有効にします。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  エッジのハイライト表示の合計量を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **エッジの選択**: *0.0 ～ 1.0*&#x200B;凸状エッジの影響を設定します。
* **バリエーション**: *0.0 ～ 1.0*&#x200B;バリエーションマスクが効果を分割する範囲を設定します。
* **バリエーションマスクの上書き**: *False/True*&#x200B;組み込みのマスクをカスタム入力スロットで上書きします。

## サンプル画像

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
