---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Clothの摩耗ノードを使用して、メッシュの曲率と接触領域に基づいてクロスサーフェスに摩耗マスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 布地の摩耗
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# 布地の摩耗

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## 布地の摩耗

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

マスクは、布地マテリアルのエッジのすり切れを表します。 効果の大部分を決定する布地のディテールの高さマップを使用します。適切なマップがなければ、効果は非常に基本的に見えます。

## パラメーター

### 入力

* **布のHeight**: *グレースケール入力*\
  布パターンのみのHeight。 これは、（ベイク処理された）オブジェクトのHeightではなく、タイリングのディテールパターンです。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **曲率**: *グレースケール入力*\
  ベイク処理/生成された曲率で、起伏のあるエッジを決定します。

### パラメーター

* **ハードエッジの量**: *0.0 - 1.0*
* **柔らかさを適用**: *0.0 ～ 5.0*&#x200B;摩耗したエッジのぼかし/柔らかさを指定します。

## サンプル画像

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>
