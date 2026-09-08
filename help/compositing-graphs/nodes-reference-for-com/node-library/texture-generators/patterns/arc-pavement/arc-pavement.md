---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: '[円弧舗装]ノードを使用して、曲線状の道路やパステクスチャを作成するための円弧状の舗装パターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 円弧舗装
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# 円弧舗装

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

パリの円弧舗装パターンを生成します。 この効果は、標準の[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)または[タイルSampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)では実現できないため、この専用ノードです。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>1 - 8</i> | グローバルスケール/タイリングを設定します。 |
| <b>パターン適用量</b> <i>1 - 32</i> | すべての円弧で使用するレンガの量を設定します。 |
| <b>パターン適用量ランダム</b> <i>0.0 - 1.0</i> | 各弧のレンガの量をランダムに変化させます。 レンガに様々なスケールを設定する効果もあります。 |
| <b>パターンの最小量</b> <i>1 - 10</i> | 円弧をランダム化するときのレンガの最小量をコントロールします。 |
| <b>円弧の量</b> <i>0 - 20</i> | 上下に積み重ねる円弧の数を設定します。 Heightを変更します。 |
| <b>パターン</b> <i>入力画像、正方形、ディスク、放物面、ベル、ガウス、とげ、ピラミッド、レンガ、グラデーション、波、ハーフベル、うね付きベル、三日月、カプセル、円錐</i> | 使用するパターン形状を選択します。 |
| <b>フィルタリング</b> <i>バイリニア+ミップマップ，バイリニア，最も近い</i> |  |
| <b>パターンの拡大・縮小</b> <i>0.0 - 1.0</i> | 各タイルのスケールを設定します。 |
| <b>パターンの幅</b> <i>0.0 - 1.0</i> | タイルの幅を設定します。 |
| <b>パターンHeight</b> <i>0.0 - 1.0</i> | 各タイルのHeightを設定します。 |
| <b>パターン幅ランダム</b> <i>0.0 - 1.0</i> | タイルの幅をランダム化します。 |
| <b>パターンHeightランダム</b> <i>0.0 - 1.0</i> | タイルのHeightをランダム化します。 |
| <b>グローバルパターン幅ランダム</b> <i>0.0 - 1.0</i> | タイル間の隙間を広げずに、タイルの幅をランダムに変化させます。 |
| <b>パターンのHeightを下げる</b> <i>0.0 - 1.0</i> | 各弧の端でタイルのHeightを押し潰すかどうかをコントロールします。 |
| <b>カラーランダム</b> <i>0.0 - 1.0</i> | タイルのカラーをランダム化します。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/arcpavement-ex.png" />
        </td>
    </tr>
</table>
