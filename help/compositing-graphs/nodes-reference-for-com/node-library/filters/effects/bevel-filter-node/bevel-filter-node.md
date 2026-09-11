---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: ベベルフィルターノードを使用して、シェイプやパターンに深度や立体感を加えるためのベベルエッジを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベベル（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# ベベル（フィルタノード）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bevel-filter-node.resources/bevel.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力グレースケールのハイトマップにエッジの面取り効果を適用します。 ベベルのHeightmapと、そのHeightmapに基づくNormalmapの両方を返します。

このノードは、理想的にはバイナリ（高契約の白黒）の基本的なハイトマップに正確なカーブプロファイルを適用するのに便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール入力</i> | 変換するマップを高くします。 |
| <b>カスタム曲線</b> <i>グレースケール入力</i> | 正確なカーブ/勾配を決定するグラデーション。 [レベル](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)や[トーンカーブ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)など、あらゆる種類の調整を実行できるグラデーション線形ノードが理想的です。 [カスタムカーブを使用]がTrueの場合にのみアクティブになります。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>距離</b> <i>-1.0 - 1.0</i> | ベベル効果の範囲 |
| <b>角の種類</b> <i>ラウンド、Angular</i> | ベベルのプロファイルを丸めるか直線にするかを指定します。 |
| <b>滑らかさ</b> <i>0.0 - 5.0</i> | ベベルの後に追加で実行するスムージング（ぼかし）の量。 |
| <b>均一でないブラーを使用</b> <i>False/True</i> | スムージングを不均等に行うかどうか。 |
| <b>カスタム曲線を使用</b> <i>False/True</i> | カスタムHeightカーブの使用を切り替えます。 詳しくは、上記を参照してください。 |
| <b>法線の強度</b> <i>0.0 - 50.0</i> | 生成されたNormalmapの強度。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 別のノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bevel-filter-node.resources/bevel-example.png" />
        </td>
    </tr>
</table>
