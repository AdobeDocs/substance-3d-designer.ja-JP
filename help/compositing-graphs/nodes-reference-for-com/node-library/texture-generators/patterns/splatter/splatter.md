---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: スプラッタノードを使用して、テクスチャ間でシェイプを散乱化し、ランダムなパターンや有機的なテクスチャディテールを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラッタ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# スプラッタ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## はね（カラー）

**イン：** *テクスチャジェネレーター**/パターン*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

スプラッタは、マップ入力をランダムに配置するためのパターンジェネレータです。 幾何学的にパターン化された配置のための多くのコントロールがあり、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)よりも使いやすくなっています。 後者の場合も同様の結果を得ることができますが、はるかに複雑です。

スプラッタは、何度も微調整しなくても、一部のシェイプをすばやく型抜きするのに適しています。

デフォルトのスプラッタパラメータは全くランダムに表示されないことに注意してください。ランダム化を行うには、一部を微調整する必要があります（主にディセーションパラメータ）。 また、スプラッタを使用するにはマップ入力が必要です。

## パラメーター

* **パターンサイズの幅**: *0.0 ～ 1000.0* X軸で使用するパターンの数。
* **パターンサイズHeight**: *0.0 ～ 1000.0* Y軸で使用するパターンの数。
* **回転**: *-360.0 - 360.0*&#x200B;すべてのパターンを設定された量だけ回転します。
* **回転のバリエーション**: *0.0 ～ 360.0*&#x200B;個々のシェイプごとにランダムな回転を導入します。
* **ズーム**: *100.0 - 10000.0*&#x200B;最終結果を拡大します。 タイリングが壊れていることに注意してください。
* **ゲイン**: *0.0 ～ 10.0*&#x200B;すべてのパターンの描画ゲインを調整します。 より目立つようになります。
* **パンX**: *-100.0 - 100.0* X軸で結果をパンします。
* **パンY**: *-100.0 - 100.0* Y軸に結果全体をパンします。
* **障害**: *0.0 ～ 100.0*\
  シェイプをランダムにシフトします。
* **グリッド番号**: *0 ～ 8*&#x200B;結果のスケールを調整するために、さまざまなグリッドサイズにジャンプします。 タイルを維持します。
* **乱雑な角度**: *0.0 - 360.0*&#x200B;乱雑な角度の変化を制御します。
* **無秩序なランダム**: *偽/真*&#x200B;無秩序な角度をランダム化し、さらに混乱を加えます。
* **パターンサイズ**: *5 - 12*
* **サイズのバリエーション**: *0.0 ～ 100.0*&#x200B;すべてのシェイプにランダムな拡大/縮小を導入します。
* **画像入力フィルタリング （エンジン > v4のみ）**: *バイリニア+ミップマップ、バイリニア、最も近い*&#x200B;入力画像に適用するフィルタリング。
* **出力レベルの最小値**: *0.0 ～ 1.0*&#x200B;最小レベル調整を出力します。
* **出力レベルの最大値**: *0.0 ～ 1.0*&#x200B;最大レベル調整を出力します。
* **背景色**: *（グレースケール値）*べた塗りの背景色を設定します。
* **輝度のバリエーション**: *0.0 ～ 1.0 （グレースケール版のみ）*輝度のバリエーションを導入します。
* **カラーバリエーション**: *0.0 ～ 1.0 （カラーバージョンのみ）*カラーバリエーションを導入

## サンプル画像

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
