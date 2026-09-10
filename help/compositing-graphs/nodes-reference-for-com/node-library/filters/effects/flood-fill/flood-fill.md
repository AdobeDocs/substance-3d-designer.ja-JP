---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
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
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill.resources/floodfill.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Flood Fillは、基本的なバイナリタイルテクスチャにバリエーションを加えることができる高度なエフェクトのセットの一部です。 このエフェクトは、単独で使用することを目的としたものではなく、他のFlood Fillエフェクトを使用する場合の出発点として使用します。 この分割された個別のデータにより、より動的で最適化された、破壊的でないワークフローが可能になります。

その他のFlood Fill効果は、[グラデーションへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)、[カラー/グレースケールへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md)、[ランダムなFlood FillへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)、[ランダムなカラーへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md)、[ボックスのサイズへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md)、[位置へのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md)、[グレーマッパー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md)および[インデックスへのFlood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)です

>[!WARNING]
>
> 入力マップは、動作するFlood Fillに適している必要があります。 これは、各タイルが各ピクセルについて完全な黒(0,0,0)の境界によって他の行から分離されるバイナリマップ（白黒のみ、グレースケールなし）であることが理想的です。 これに最適な候補の例は、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)です。
> 
> タイルが完全な黒のピクセルで区切られていない場合、問題が発生します。通常は、グレースケールの傾斜値が使用されている場合です。 結果に赤い値が含まれていないことや、奇妙な人工的な線を使用している可能性があることから、この問題を特定できます。 このような場合は、入力マップのコントラストを調整するか、入力マップを切り替えます。 「安全性/速度」のトレードオフ設定を変更して、改善された点がないか確認してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>安全性/速度のトレードオフ</b> <i>単純または小さい図形、複雑または大きい図形、エラーなしモード。</i> | 入力シェイプに最適になるように計算モードを設定します。 正しいモードが選択されている場合、より正確な結果が得られます。 |
| <b>高度なオプション</b> <i>詳細パラメーターの表示と出力/詳細パラメーターおよび出力の非表示</i> |  |
| <b>安全性/速度のトレードオフを上書き</b> <i>-1 - 100</i> | 詳細オプションがオンの場合にのみ表示されます。 内部フィーチャをオーバーライドできます。 非常に高度で、独自のエフェクトやデバッグを作成するのに役立ちます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-ex1.png" />
        </td>
    </tr>
</table>

良い例も悪い例もFlood Fillの結果です。
