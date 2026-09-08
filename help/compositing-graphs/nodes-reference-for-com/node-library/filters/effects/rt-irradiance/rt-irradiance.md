---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: RT放射ノードを使用して、ジオメトリからリアルタイムの放射照度情報を計算し、リアルなライティングを計算します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT放射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# RT放射

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**場所：** *フィルター/効果*

**複合**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

環境マップとemissiveマップから生成された高さマップ入力に対してレイトレース照射を生成します。 グラフ内のテクスチャに照明を「ベイク」するために使用できます。 偽物のグローバルイルミネーションとグローに使用します。計算時間があるため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。 2つのマップを返します。1つは放射がマテリアル入力に適用される放射照度出力で、もう1つは計算された放射照度値のみを含む未処理の放射照度マップです。

</td>
</tr>
</table>

## パラメーター

### 入力

* **Height:** *グレースケール入力* Heightは、マテリアルスロットからの必要な入力です。 これがないと、ノードが正常に機能しません。
* **Emissive:** *カラー入力* Emissiveは、純粋な黒は光を放たず、その他の色の値は光を放つフォーマットにする必要があります。 Alphaは無視されます。 結果を確認するには、このスロットへの接続または環境スロットが必要です。
* **環境**: *カラー入力*\
  放射を計算するためのHDR Lighting environment。 結果を確認するには、このスロットへの接続またはEmissiveスロットが必要です。

### パラメーター

* **Heightスケール**: *0.0 ～ 1.0*\
  Heightを変換するスケール。 シーン全体の外観に影響します。
* **画質**: *32光線、64光線、128光線*\
  結果の品質を決定しますが、パフォーマンスにも影響します。 光線が少ないほど、ノイズが高くなります。
* **バウンスの計算**: *False/True*\
  バウンスの計算を切り替えます。 品質と速度に影響します。
* **環境回転**: *0.0 ～ 1.0*\
  環境を回転させます。
* **環境露出(EV)**: *-4.0 - 4.0*\
  環境に使用する露光量の値は、エフェクトの合計輝度に影響します。
* **Emissiveの適用度**: *0.0 ～ 20.0*\
  emissive入力の乗数。emissiveからの放射の強さに影響します。
* **Emissiveカラースペース**: *sRGB、リニア*\
  Enissive入力の解釈に使用されるカラースペース。
* **Raw照射AlphaのIBLシャドウ**: *False/True*\
  ぼかしを切り替えて、
* **Emissive LOD バイアス**: *-1.0 - 1.0* emissive放射照度の質を調整します。 値が小さいほどノイズが高くなります。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
