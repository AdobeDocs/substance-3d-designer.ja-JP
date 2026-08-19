---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: '[円弧舗装]ノードを使用して、曲線の道路およびパステクスチャを作成するための円弧状の舗装パターンを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 円弧舗装
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 円弧舗装

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## 円弧舗装

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

パリの円弧舗装パターンを生成します。 この効果は、標準の[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)または[タイルSampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)では実現できないため、この専用ノードです。

## パラメーター

* **尺度**: *1 ～ 8*&#x200B;グローバル尺度/タイルを設定します。
* **パターン適用量**: *1 -* 32\
  各弧で使用するレンガの量を設定します。
* **パターン適用量ランダム**: *0.0 - 1.0*\
  各弧のレンガの量をランダムに変化させます。 レンガに異なるスケールを与えるという追加の効果があります。
* **パターンの最小量**: *1 - 10*\
  円弧をランダム化するときのレンガの最小量をコントロールします。
* **円弧の量**: *0 - 20*\
  上下に積み重ねる円弧の数を設定します。 レンガのHeightを変更します。
* **パターン**: *入力画像、正方形、ディスク、放物面、ベル、ガウス、とげ、ピラミッド、レンガ、グラデーション、ウェーブ、ハーフベル、縁の付いたベル、三日月、カプセル、コーン*\
  使用するパターン形状を選択します。
* **入力画像のフィルター**: *バイリニア+ミップマップ、バイリニア、ニアレスト*
* **パターンスケール**: *0.0 ～ 1.0*&#x200B;各タイルのスケールを設定します。
* **パターン幅**: *0.0 ～ 1.0*\
  タイルの幅を設定します。
* **パターンHeight**: *0.0 - 1.0*\
  各タイルのHeightを設定します。
* **パターン幅ランダム**: *0.0 ～ 1.0*\
  タイルの幅をランダム化します。
* **パターンHeightランダム**: *0.0 - 1.0*\
  タイルのHeightをランダム化します。
* **グローバルパターンの幅のランダム**: *0.0 ～ 1.0*&#x200B;タイルの幅をランダムに変化させます。タイル間のギャップは大きくなりません。
* **パターンのHeightの減少**: *0.0 ～ 1.0*&#x200B;各弧の端でタイルのHeightが押しつぶされるのを制御します。
* **カラーランダム**: *0.0 ～ 1.0*\
  タイルのカラーをランダム化します。
* **非正方形拡張**: *False/True*\
  スカッシュとストレッチを非正方形の比率で補正できます。

## サンプル画像

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
