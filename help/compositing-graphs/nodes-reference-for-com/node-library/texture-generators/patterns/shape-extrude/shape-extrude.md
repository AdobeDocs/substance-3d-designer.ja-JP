---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: シェイプの押し出しノードを使用してシェイプを押し出し、Substance 3D Designerテクスチャに3Dのような深度効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプの押し出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# シェイプの押し出し

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## シェイプの押し出し

**イン：** *テクスチャジェネレーター**/パターン*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

2Dのバイナリ「シェイプ」入力を3D回転のハイトマップにレンダリングできる高度なノード。 3Dパッケージでシェイプをその軸に沿って押し出し、ボリュームを作成する場合の押し出しと同様に機能します。 プロファイルグラデーションマスクと組み合わせて、回転/レイズタイプのボディも作成できます。 ハイトマップの複雑な人為的シェイプを作成する場合に非常に便利です。

## パラメーター

### 入力

* **押し出しシェイプの入力**: *グレースケールの入力*&#x200B;押し出しシェイプがカスタムに設定されている場合、ここで独自の（できれば）バイナリシェイプマスクをプラグインします。
* **プロファイルグラデーション**: *グレースケール入力\
  [プロファイルの種類]が[垂直グラデーション]に設定されている場合、回転ボディの軸に沿ったシェイプのスケールを定義するために使用できます。*
* **プロファイルマスク**: *グレースケール入力*\
  押し出しシェイプをその軸に沿って非表示または表示するために使用されるマスクスロット。 軸に沿ってシェイプの連続性を解除するために使用できます。 バイナリとしてのみ解釈されます：グレースケールのput値は0または1に丸められます。

### パラメーター

* **押し出しHeight**: *0.0 -* 1.0\
  シェイプを中心から上に押し出す量。
* **押し出し深度**: *0.0 ～ 1.0*&#x200B;押し出しシェイプの中心からの下げ幅です。
* **シェイプの押し出し**: *立方体、円柱、カスタム入力*&#x200B;組み込みのシェイプを使用するか、独自のカスタムシェイプを外部に入力してください。
* **シェイプの押し出しサイズ**: *0.0 ～ 1.0*&#x200B;組み込みの立方体と円柱でのみ使用され、基本シェイプのサイズを決定します。不均等にスケーリングできます。
* **スケール**: *0.0 ～ 1.0*\
  エフェクトのグローバルスケールを設定します。 組み込みシェイプでは、これは均一なベースシェイプのスケールであり、Heightや深度には影響しません。\
  カスタム入力では、最終的な結果全体が均一にスケールされます。
* **プロファイルの種類**: *直線、垂直グラデーション、マスク*&#x200B;効果の動作を決定し、オプションの追加入力マップを使用するためのメインコントロール。\
  「直線」は標準の「押し出し」動作、「垂直グラデーション」は軸全体に沿ったカスタムスケール値、「マスク」はマスクごとの軸に沿ったセクションを非表示にできます。
* **ベベルのHeight**: *0.0 ～ 1.0*&#x200B;押し出し軸に沿ってベベルが到達する距離を設定します。
* **ベベルの強さ**: *0.0 ～ 1.0*&#x200B;ベベルが元の形状からどれだけリトラクトするかを設定します。
* **ベベル曲線**: *-1.0 ～ 1.0*&#x200B;ベベル効果の凸曲線または凹曲線を設定します。 値を0に設定すると、直線になり、曲線はなくなります。
* **ミラーベベル**: *偽/真*&#x200B;切り替えて、ベベルをシェイプの上と下に適用します。
* **マルチプライヤーのダウンスケール**: *0 ～ 2*&#x200B;組み込みの簡単なダウンスケールコントロールです。 これを使用すると、アンチエイリアスをすばやく追加できます。ノードの解像度も上げることを確認してください。
* **位置**:\
  3D空間で結果を回転するためのメインコントロール。 2D ビュー内のインタラクティブギズモと相関します。
* **出力範囲**: *[0, 1], [-1, 1]*出力の最小値と最大値を設定します。 rangeが[-1,1]に設定されている場合、負の値は黒で表示されます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
