---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: '[サンブリーチ]ノードを使用して、太陽の露出に基づいてマスクを生成し、リアルなサンブリーチ効果と色あせた効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: サンブリーチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# サンブリーチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## サンブリーチ

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは[ライト](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md)に似ていますが、AOもサポートされており、効果の上に明るい白レベルとフェードレベルを表すマスクになります。

## 入力

* **標準のワールドスペース**: *カラー入力*
* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

## パラメーター

* **レベル**: *0.0 ～ 1.0*\
  漂白の総量を設定し、効果をさらに下げます。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **オクルージョン**: *0.0 ～ 1.0*&#x200B;最終結果に対するAOの影響を設定します。

## サンプル画像

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
