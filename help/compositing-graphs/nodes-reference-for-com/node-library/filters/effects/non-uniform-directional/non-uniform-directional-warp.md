---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Non Uniform Directional Warpノードを使用して不均等な方向ワープを適用し、多様なゆがみエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## 非一様方向。 ワープ（グレースケール）

**場所：** *フィルター/効果*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

不均等な方向ワープは、画像入力によってワープの強さと指向性ワープを決定できる[方向](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)の高度なバージョンです。 これにより、[ぼかし(勾配)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)と同様に、より詳細な制御が可能になり、非常に便利で面白い画像ゆがみを作成できます。

[マルチ指向性ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md)とは異なり、カスタムマップ入力を使用して角度を制御できますが、マルチ指向性ワープではパラメーターを使用して方向のみを制御できます。 つまり、それ以外では不可能な、高度なトレーリングエフェクトやカービングエフェクトを作成できます。

## パラメーター

### 入力

* **入力**: *グレースケール入力*\
  ワープが適用されるベースマップ。
* **強度入力**: *グレースケール入力*\
  ワープ効果の強度を制御する必須のマスクマップは、グレースケールにする必要があります。
* **ワープ角度入力**: *グレースケール入力*\
  ワープ効果の角度を制御する必須のマスクマップは、グレースケールにする必要があります。

### パラメーター

* **強度**: *0.0 ～ 20.0*\
  ワープ効果の強度を設定します。ピクセルを押し出す範囲を指定します。
* **ワープ角度**: *0.0 ～ 1.0*\
  ワープ効果を適用する角度または方向を設定します。
* **ワープ角度入力マルチプライヤ**: *0.0 - 1.0*\
  ワープ角度入力マップの効果を設定します。 ワープ角度入力マップは、0からこのパラメーターの値までの補間に使用されます。
* **トレイルモード**: *最小、最大、平均*\
  基準線のブレンド方法を設定します。
* **トレイルの長さ**: *0.0 ～ 1.0*\
  基準線の長さを設定します。
* **トレイルフェード**: *0.0 ～ 1.0*\
  各トレールがフェードを出力する量を設定します
* **基準線カーブ**: *-1.0 - 1.0*&#x200B;基準線フェードが0でない場合にのみ効果があります。 フェード効果の動作を設定します。

## サンプル画像

</td>
</tr>
</table>
