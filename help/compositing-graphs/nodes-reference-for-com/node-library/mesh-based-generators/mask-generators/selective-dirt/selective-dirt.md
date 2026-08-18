---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: 選択的Dirtノードを使用して、メッシュジオメトリに基づく選択的Dirtのアキュムレーションマスクを生成し、リアルな風化を実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 選択的Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# 選択的Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## 選択的Dirt

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

この[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)マスクは、凸状のエッジに対する単純なDirt効果を表します。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **バリエーションマスク**: *グレースケール入力*\
  オプションのバリエーションマップは、パラメーターを使用して有効にできます。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  エフェクトの合計レベルを設定し、徐々に表示します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **変動**: *0.0 ～ 1.0*&#x200B;効果にブレンドする変動/経年劣化の量を設定します。
* **バリエーションマスクの上書き**: *False/True*&#x200B;カスタム入力スロットでバリエーションを上書きできるようにします。

## サンプル画像

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
