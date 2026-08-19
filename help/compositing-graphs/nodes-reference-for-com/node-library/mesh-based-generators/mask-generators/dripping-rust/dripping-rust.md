---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: '[滴下錆]ノードを使用して、メッシュジオメトリと重力の向きに基づいて錆の滴下パターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴下錆
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# 滴下錆

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## 滴下錆

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、錆のフレークと斑点を表し、漏れが伝わります。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  錆の配置に役立つベイク処理または生成されたマップ。
* **環境オクルージョン**: *グレースケール入力*\
  錆の配置に役立つベイク処理または生成されたマップ。
* **位置**: *グレースケール入力*\
  点滴方向のベイク処理または生成されたマップ。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **錆の分散**: *0.0 ～ 1.0*&#x200B;錆量のメインコントロール。
* **錆のコントラスト**: *0.0 ～ 1.0*&#x200B;生成される錆の斑点のコントラストの量を設定します（点滴には影響しません）。
* **Smoothnessの拡散**: *0.0 ～ 1.0*&#x200B;錆の斑点に適用するぼかし/にじみの量。
* **しずくの強さ**: *0.0 ～ 1.0*&#x200B;斑点からのしずくの強さと長さを設定します。
* **しずくのSmoothness**: *0.0 ～ 1.0*&#x200B;しずくに適用するぼかしと滑らかさの量。
* **滴のサンプル量**: *0 ～ 32*&#x200B;滴の効果の品質レベル（ステップ）を設定します。 速度にわずかな影響を与えます。

## サンプル画像

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
