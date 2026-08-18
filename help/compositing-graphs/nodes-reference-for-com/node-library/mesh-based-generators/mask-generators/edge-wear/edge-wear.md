---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Edge Wearノードを使用して、メッシュエッジに摩耗マスクを作成し、リアルなエッジのダメージとウェザリングエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このノードは、オブジェクトのエッジの損耗を表します。 パラメーターは数多くありますが、使い方は簡単ではありません。遊び回って、物事を感じてみることをお勧めします。 このノードは非常に強力ですが、カスタムのオーバーライドマスクは実行できません。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  エフェクトの合計幅を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **しきい値**: *0.0 ～ 1.0*&#x200B;レベルと同様に、効果の全体スプレッドを設定します。
* **エッジの幅**: *0.0 ～ 1.0*&#x200B;ハイライト効果のフルネスを設定します。 下げて、より輝かせます。
* **障害**: *0.0 ～ 1.0*\
  Smoothnessを分解するためにブレンドするノイズの量を設定します。

## サンプル画像

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
