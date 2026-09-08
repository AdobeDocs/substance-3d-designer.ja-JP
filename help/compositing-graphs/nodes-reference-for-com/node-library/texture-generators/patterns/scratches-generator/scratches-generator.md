---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: '[Scratchesジェネレータ]ノードを使用して、マテリアルに磨耗や損傷を加えるための手続き型のスクラッチパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scratchesジェネレータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Scratchesジェネレータ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Scratchesジェネレータ（通常）

**イン：** *テクスチャジェネレーター**/パターン*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

これにより、ランダムスクラッチが配置されます。例えば、方向、スプレッド、ゆがみを設定することができます。

特別なバージョンのScratchesジェネレーター、Scratchesジェネレーター法線があり、これらの傷の深度に基づいてノーマルマップを生成します。 ほとんどのオプションはまったく同じですが、いくつかの追加のパラメーターがあり、これらは通常設定ではっきりとマークされています（以下を参照）。

## パラメーター

* **スプライン番号**: *1 - 512*&#x200B;配置するスクラッチ（スプライン）の量。
* **スプラインあたりの最大セグメント数**: *2 ～ 256*&#x200B;スクラッチの長さに対するセグメント/サブディビジョンの量。 より滑らかなカーブとゆがみが得られます。 この効果は、ゆがみの値が大きいほど目立ちます。
* **スプラインの回転**: *0.0 ～ 1.0*&#x200B;すべてのスプラインを一方向に向けるために均一に回転させます。
* **スプラインの回転ランダム**: *0.0 ～ 1.0*&#x200B;角度の変化。すべてのスプラインをランダムに回転します。
* **スプラインのスケール**: *0.0 ～ 1.0*&#x200B;すべてのスプラインを均一にスケールします。
* **スプラインスケールランダム**: *0.0 ～ 1.0*&#x200B;各スプラインを個別にランダムにスケールします。
* **スプラインのゆがみ**: *0.0 ～ 1.0*&#x200B;すべてのスプラインで均一なゆがみレベルです。
* **スプラインゆがみランダム**: *0.0 ～ 1.0*&#x200B;各スプラインのゆがみレベルを個別にランダム化します。
* **スプラインゆがみの頻度**: *0.0 ～ 1.0*&#x200B;ゆがみの頻度を設定し、ゆがみの詳細のスケールを制御します。
* **スプラインの幅**: *0.0 ～ 2.0*&#x200B;すべてのスプラインの幅を均一に設定します。
* **スプライン幅ランダム**: *0.0 ～ 1.0*&#x200B;各スプラインのスプライン幅を個別にランダム化します。
* **スプラインの位置のランダム**: *0.0 ～ 1.0*&#x200B;各スプラインの位置を個別にランダム化します。 この値を小さくすると、より多くのスプラインがキャンバスの中心に集まります。 キズの斑点の作成に使用できます。
* **pxのスプライン幅を設定**: *偽/真*&#x200B;スプライン幅の設定に使用される単位を決定します。
* **輝度ランダム（グレースケール版のみ）**: *0.0 ～ 1.0*&#x200B;各スプラインの輝度を個別にランダム化します。
* **法線の強さ（法線バージョンのみ）**: *0.0 ～ 1.0*&#x200B;各スプラインの法線エフェクトの強さをグローバルに設定します。
* **&#x200B;法線の強さランダム**（標準版のみ）**&#x200B;**: *0.0 ～ 1.0*各スプラインの法線強さを個別にランダム化します。
* **&#x200B;標準形式**（標準版のみ）**&#x200B;**: *DirectX、OpenGL*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。
* **フェードモード**: *なし、開始、終了、開始+終了*&#x200B;スプラインフェードの有無とその方向を設定します。
* **フェードの長さ**: *0.0 ～ 1.0*&#x200B;上で有効になっている場合に、フェード効果の長さを設定します。
* **非正方形拡張**: *False/True*\
  カボチャと伸縮の補正を非正方形の比率で有効にします。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
