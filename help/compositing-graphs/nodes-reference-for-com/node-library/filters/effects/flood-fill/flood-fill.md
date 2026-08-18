---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Flood Fillノードを使用して、マスクおよびテクスチャ処理効果を作成するために、同色の接続された領域を塗りつぶします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill.png){width="128px"}

## Flood Fill

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

Flood Fillは、基本的なバイナリタイルテクスチャにバリエーションを加えることができる高度なエフェクトのセットの一部です。 このエフェクトは、単独で使用することを目的としたものではなく、他のFlood Fillエフェクトを使用する場合の出発点として使用します。 この分割された個別のデータにより、より動的で最適化された、破壊的でないワークフローが可能になります。

その他のFlood Fill効果は、[グラデーションへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)、[カラー/グレースケールへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md)、[ランダムなFlood FillへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)、[ランダムなカラーへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md)、[ボックスのサイズへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md)、[位置へのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md)、[グレーマッパー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md)および[インデックスへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)です

>[!WARNING]
>
> 入力マップは、動作するFlood Fillに適している必要があります。 これは、各タイルが各ピクセルについて完全な黒(0,0,0)の境界によって他の行から分離されるバイナリマップ（白黒のみ、グレースケールなし）であることが理想的です。 これに最適な候補の例は、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)です。
> 
> タイルが完全な黒のピクセルで区切られていない場合、問題が発生します。通常は、グレースケールの傾斜値が使用されている場合です。 結果に赤い値が含まれていないことや、奇妙な人工的な線を使用している可能性があることから、この問題を特定できます。 このような場合は、入力マップのコントラストを調整するか、入力マップを切り替えます。 「安全性/速度」のトレードオフ設定を変更して、改善された点がないか確認してください。

## パラメーター

* **安全性/速度のトレードオフ**: *単純または小さな図形、複雑または大きな図形、エラーなし*入力図形に最適な計算モードを設定します。 正しいモードが選択されている場合、より正確な結果が得られます。
* **詳細オプション**: *詳細パラメーターを表示し、出力/詳細パラメーターおよび出力を非表示にする*
* **安全性/速度のトレードオフを上書き**: *-1 - 100*&#x200B;詳細オプションがオンの場合にのみ表示されます。 内部フィーチャをオーバーライドできます。 非常に高度で、独自のエフェクトやデバッグを作成するのに役立ちます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/flood-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/flood-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

良い例も悪い例もFlood Fillの結果です。

</td>
</tr>
</table>
