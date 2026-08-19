---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Dustノードを使用して、メッシュジオメトリに基づいてDustのアキュムレーションマスクを作成し、リアルなDustと汚れのエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、上に向いている領域だけでなく、閉塞した領域や下がっている領域にも蓄積されているDustを表します。 適切なベイク処理されたAOおよびワールド空間法線が動作する必要があります。

## パラメーター

### 入力

* **環境オクルージョン**: *グレースケール入力*\
  Dustの配置に使用するベイク済みマップ。 必須！
* **ワールドスペース標準**: *カラー入力*\
  Dustの配置に使用するベイク済みマップ。 必須！
* **ノイズ**: *グレースケール入力*\
  カスタムDustマップ（オプション）。[ノイズのオーバーライド]が[True]に設定されている場合にのみ表示されます。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  Dustの合計量を設定します。
* **コントラスト**: *0.0 ～ 1.0*\
  Dustのコントラストを調整します。
* **オクルージョン量**: *0.0 ～ 1.0* AOの影響を設定します。閉塞した領域により多くのDustが表示されます。
* **ノイズの不透明度**: *0.0 ～ 1.0*&#x200B;ほこりの多い領域に表示されるノイズの量を設定します。
* **ノイズを上書き**: *False/True*&#x200B;カスタムのDustマップ入力を使用するように設定します。

## サンプル画像

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
