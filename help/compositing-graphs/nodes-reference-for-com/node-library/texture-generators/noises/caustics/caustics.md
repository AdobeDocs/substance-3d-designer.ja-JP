---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: コースティクスノードを使用して、水中および屈折ライティングエフェクトを作成するためのコースティクスライトパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: コースティクス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# コースティクス

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**インチ：** *テクスチャジェネレーター**/ノイズ*

**複合**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

高さマップとライトの方向に基づいて投影されたコースティクスを生成します。グレースケールとカラーの両方のバージョンがありますが、違いは微妙ですが、カラーバージョンでは色分散効果が追加されます。 光は1つの点からキャストされ、環境マップは使用されません。

</td>
</tr>
</table>

## パラメーター

* **出力カラースペース**: *Raw, sRGB*\
  出力カラースペースを設定します。
* **フォトングリッドサイズ**: *自動、512、1024、2048、4096*\
  グリッドサイズを調整して画質を設定しますが、デフォルトでは一致する入力に設定されます。 計算の高速化に使用できます。
* **サーフェスHeightスケール**: *0.0 ～ 1.0*\
  Heightの変換方法を指定する乗数。
* **サーフェスHeightの位置**: *0.0 - 1.0*\
  投影する屈折サーフェスの距離を設定します。
* **サーフェスIOR**: *1.0 ～ 2.0*\
  屈折率を設定します。カラーバージョンでは、これによりカラーの分散が大きくなります。
* **フォトンのサイズ**: *1.0 - 50.0*\
  フォトンサイズは効果の鮮明さに影響します。
* **分散**: *0.0 ～ 0.01 （カラーバージョンのみ）*\
  カラー分散のみに影響します。 IORが低い場合は表示されません。
* **ジッター**: *0.0 ～ 1.0*\
  キャストフォトンのパーティクルに不規則なジッターを加えます。
* **明るい位置**:\
  ライトの位置を移動します。 また、2D ビューのギズモを介して行われます。
* **背景色**: *（カラー値） （カラーバージョンのみ）*\
  背景色を変更します。 グレースケール版では黒に制限されます。
* **非正方形拡張**: *False/True*\
  カボチャの補正を有効にし、非正方形の比率で伸縮します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
