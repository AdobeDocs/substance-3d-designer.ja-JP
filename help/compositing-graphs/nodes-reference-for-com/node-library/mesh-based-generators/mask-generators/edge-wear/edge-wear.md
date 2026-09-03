---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Edge Wearノードを使用して、メッシュエッジに摩耗マスクを作成し、リアルなエッジダメージと風化エフェクトを生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 7%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-wear.resources/edge-wear-01.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このノードは、オブジェクトのエッジの損耗を表します。 パラメーターは数多くありますが、使い方は簡単ではありません。遊び回って、物事を感じてみることをお勧めします。 このノードは非常に強力ですが、カスタムのオーバーライドマスクは実行できません。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | エフェクトの合計幅を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>しきい値</b> <i>0.0 - 1.0</i> | 「レベル」と同様に、エフェクトの合計幅を設定します。 |
| <b>エッジの幅</b> <i>0.0 - 1.0</i> | ハイライト効果のフルネスを設定します。 下げて、より輝かせます。 |
| <b>障害</b> <i>0.0 - 1.0</i> | Smoothnessを分解するためにブレンドするノイズの量を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-wear.resources/edge-wear-02.gif" />
        </td>
    </tr>
</table>
