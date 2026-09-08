---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# Scratchesジェネレータ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これにより、ランダムスクラッチが配置されます。例えば、方向、スプレッド、ゆがみを設定することができます。

特別なバージョンのScratchesジェネレーター、Scratchesジェネレーター法線があり、これらの傷の深度に基づいてノーマルマップを生成します。 ほとんどのオプションはまったく同じですが、いくつかの追加のパラメーターがあり、これらは通常設定ではっきりとマークされています（以下を参照）。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スプライン番号</b> <i>1 - 512</i> | 配置するスクラッチ（スプライン）の量。 |
| <b>スプラインあたりの最大セグメント数</b> <i>2 - 256</i> | スクラッチの長さに対するセグメント/サブディビジョンの量。 より滑らかなカーブとゆがみが得られます。 この効果は、ゆがみの値が大きいほど目立ちます。 |
| <b>スプラインの回転</b> <i>0.0 - 1.0</i> | すべてのスプラインを一定の方向に回転します。 |
| <b>スプライン回転ランダム</b> <i>0.0 - 1.0</i> | 角度の変化。すべてのスプラインをランダムに回転します。 |
| <b>スプラインのスケール</b> <i>0.0 - 1.0</i> | すべてのスプラインを均一にスケールします。 |
| <b>スプラインスケールランダム</b> <i>0.0 - 1.0</i> | 各スプラインを個別にランダムにスケールします。 |
| <b>スプラインゆがみ</b> <i>0.0 - 1.0</i> | すべてのスプラインにわたって均一なゆがみレベル。 |
| <b>スプラインゆがみランダム</b> <i>0.0 - 1.0</i> | 各スプラインのゆがみレベルを個別にランダム化します。 |
| <b>スプラインゆがみの頻度</b> <i>0.0 - 1.0</i> | ゆがみの頻度を設定し、ゆがみの詳細のスケールを制御します。 |
| <b>スプラインの幅</b> <i>0.0 - 2.0</i> | すべてのスプラインの幅を均一に設定します。 |
| <b>スプライン幅ランダム</b> <i>0.0 - 1.0</i> | 各スプラインのスプライン幅を個別にランダム化します。 |
| <b>スプライン位置ランダム</b> <i>0.0 - 1.0</i> | 各スプラインの位置を個別にランダム化します。 この値を小さくすると、より多くのスプラインがキャンバスの中心に集まります。 キズの斑点の作成に使用できます。 |
| <b>pxのスプライン幅を設定</b> <i>False/True</i> | スプラインの幅設定に使用する単位を指定します。 |
| <b>輝度ランダム（グレースケール版のみ）</b> <i>0.0 - 1.0</i> | 各スプラインの輝度を個別にランダム化します。 |
| <b>標準の強度（標準バージョンのみ）</b> <i>0.0 - 1.0</i> | すべてのスプラインに対してグローバルに法線エフェクトの強さを設定します。 |
| <b>法線の強度ランダム（通常バージョンのみ）</b> <i>0.0 - 1.0</i> | 各スプラインの法線強さを個別にランダム化します。 |
| <b>標準の形式（標準バージョンのみ）</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>フェードモード</b> <i>なし、開始、終了、開始+終了</i> | スプラインのフェードを指定します。 |
| <b>フェード長</b> <i>0.0 - 1.0</i> | フェード効果の長さを設定します（上記で有効になっている場合）。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/scratches-ex1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/scratches-ex2.png" />
        </td>
    </tr>
</table>
