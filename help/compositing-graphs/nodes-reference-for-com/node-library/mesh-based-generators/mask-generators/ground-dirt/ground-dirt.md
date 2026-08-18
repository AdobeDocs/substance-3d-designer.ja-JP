---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: 地面Dirtノードを使用して、地面に対するメッシュの位置と方向に基づいてDirtのアキュムレーションマスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 地面Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# 地面Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## 地面Dirt

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、[下から上へ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md)または[Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md)の反対に、最初から積み上げられたDustを表します。 カスタムマップは上書きされません。

## 入力

* **位置**: *グレースケール入力*\
  効果のベースにするベイクした位置マップ。 必須！
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

## パラメーター

* **レベル**: *0.0 ～ 1.0*\
  Dirtの全体的な外観レベルを設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **DirtのHeight**: *0.0 ～ 1.0* Dirtを表示するHeight（縦横比固定）を設定します。

## サンプル画像

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
