---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: シェイプノードを使用して、Substance 3D Designerでパターンやテクスチャを作成するための基本的な幾何学的シェイプを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# シェイプ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## シェイプ

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

さまざまな手続き型シェイプが生成されます。基本シェイプを変更するオプションもあります。 シェイプは常に完全に補間され、高精度です。

シンプルであるにもかかわらず、これは非常に便利なノードです。これは、最も手続き型のHeightmap生成の構成要素です。 基本的なシェイプとトランスフォームノードを組み合わせることで、ビットマップよりもはるかに正確な、完全に手続き型のハイトマップシェイプを作成できます。

## パラメーター

* **タイル**: *1 - 16*\
  結果をタイルする回数を設定します。
* **パターン**: *正方形、円盤、放物面、ベル、ガウス、イバラ、角錐、レンガ、グラデーション、ウェーブ、ハーフベル、縁の付いたベル、クレスカント、カプセル、コーン*、半球**\
  使用するパターン形状を選択します。
* **パターン固有**: *0.0 ～ 1.0*\
  選択したパターンのシェイプを変更できます。 効果は選択したパターンによって異なります。
* **スケール**: *0.0 ～ 1.0*&#x200B;シェイプ全体をスケールします。
* **サイズ**: *0.0 ～ 1.0* X軸またはY軸に対して不均等な拡大/縮小を許可します。
* **角度**: *0.0 ～ 1.0*&#x200B;シェイプ全体を回転します。
* **回転45°**: *偽/真*&#x200B;あらかじめ設定された45度で回転します。
* **非正方形拡張**: *False/True*\
  スカッシュとストレッチを非正方形の比率で補正できます。
* **非正方形タイリング**&#x200B;**:** *偽/真*非正方形拡張が有効な場合、これによりシェイプが押しつぶされずにタイリングされます。

## サンプル画像

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
