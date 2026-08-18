---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Greaseノードを使用して、メッシュジオメトリと接触領域に基づいてグリース蓄積マスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グリース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# グリース

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## グリース

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、特にキャラクターの顔やその他の特定の領域を対象としています。 Thicknessの低い領域にスキングリースタイプのマスクを生成します。

## パラメーター

### 入力

* **Thickness**: *グレースケール入力*\
  エフェクト全体のベースとなるベイク処理されたThicknessマップ。 必須！
* **ノイズ**: *グレースケール入力*\
  グリースデータを上書きするためのノイズ経年劣化マップ（オプション）。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  表示するエフェクトの総量を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **Thicknessのしきい値**: *0.0 ～ 1.0*&#x200B;効果が現れる最小のThicknessを設定します。 レベルも同様に重要です。Thicknessマップに合わせて調整してください。
* **ノイズを上書き**: *False/True*&#x200B;カスタム入力スロットで内部グリース経年劣化マップを上書きするように設定します。

## サンプル画像

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
