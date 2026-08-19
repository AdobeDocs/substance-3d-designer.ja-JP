---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Metal Edge Wearノードを使用して、メッシュの曲率と位置に基づいてメタルエッジに摩耗マスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 金属Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## 金属Edge Wear

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、金属物体のエッジの摩耗を表現し、凸状の隆起エッジにスクラッチや切り屑が表示され、ベイク処理されたAOの暗部によってマスクされる可能性があります。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **経年劣化入力**: *グレースケール入力*
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **ワールドスペース標準**: *カラー入力*
* **位置**: *カラー入力*

### パラメーター

* **磨耗のレベル**: *0.0 ～ 1.0*&#x200B;磨耗の総量を設定し、徐々に明らかになります。
* **磨耗のコントラスト**: *0.0 ～ 1.0*&#x200B;最終結果のコントラストを設定します。
* **エッジのSmoothness**: *0.0 ～ 16.0*&#x200B;曲率からのエッジからのフォールオフのSmoothnessを設定します。
* **経年劣化量**: *0.0 ～ 1.0*&#x200B;エッジ間でブレンドする経年劣化量を設定します。
* **経年劣化スケール**: *1 - 16*&#x200B;経年劣化のスケールを設定します。
* **周囲オクルージョンのマスク**: *0.0 ～ 1.0*&#x200B;最終的な効果に対するAOの効果の量を設定します。暗い領域はマスクされます。
* **曲率の重み**: *0.0 ～ 1.0*&#x200B;曲率の凸状のエッジが最終効果に与える効果の量を設定します。
* **カスタム経年劣化を使用**: *False/True*&#x200B;カスタム経年劣化マップ入力スロットを有効にします。
* **三平面を使用**: *偽/真*[三平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)プロジェクションを有効にして縫い目を隠します。
* **3平面のブレンドコントラスト**: *0.0 ～ 1.0* 3平面投影のブレンドコントラストを設定します。

## サンプル画像

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
