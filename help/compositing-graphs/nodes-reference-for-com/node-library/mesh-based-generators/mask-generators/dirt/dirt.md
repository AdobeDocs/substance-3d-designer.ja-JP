---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Dirtノードを使用して、メッシュの曲率、位置、オクルージョンに基づいてDirtのアキュムレーションマスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 汚れ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# 汚れ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## 汚れ

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、ベイク処理されたAOと曲率に基づいて、隠れたエッジと沈んだエッジおよびコーナーのDirtを表します。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。 必須！
* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。 必須！
* **経年劣化入力**: *グレースケール入力*\
  カスタム経年劣化マップ入力、オプション、パラメーターにより有効化
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **ワールドスペース標準**: *カラー入力*\
  Triplanarにのみ使用されます。
* **位置**: *カラー入力*\
  Triplanarにのみ使用されます。

### パラメーター

* **Dirtレベル**: *0.0 ～ 1.0* Dirt量のメインコントロール。
* **Dirtのコントラスト**: *0.0 ～ 1.0*&#x200B;マスク内のDirtのコントラストを制御します。
* **経年劣化量**: *0.0 ～ 1.0* Dirtのグランジの度合いを設定します。 Dirtを完全に滑らかにするには、0に設定します。
* **エッジのマスク**: *0.0 ～ 1.0*&#x200B;隆起したエッジから取り除くDirtの量（曲線マップに基づく）。
* **カスタム経年劣化の使用**: *False/True*&#x200B;組み込み経年劣化の代わりにカスタム経年劣化マップ入力を使用できるようにします。
* **経年劣化スケール**: *1 ～ 16*&#x200B;経年劣化の詳細のタイリングスケールを設定します。
* **三平面を使用**: *False/True*&#x200B;経年劣化マッピングに[Triplanar projection](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)を使用して、シームを削除します。
* **三平面ブレンドコントラスト**: *0.001 - 1.0*&#x200B;三平面投影のコントラストを設定します。

## サンプル画像

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
