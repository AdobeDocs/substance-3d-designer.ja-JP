---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: ベクトルワープノードは、ベクトルフィールドを使用してテクスチャをワープし、流動的で有機的なゆがみエフェクトを作成する場合に使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベクターワープ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# ベクターワープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp.png){width="128px"}

![](vector-warp.resources/vector-warp-grayscale.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベクターワープは、[ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)や[指向性ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)に似た高度なゆがみ効果ですが、主な違いは、グレースケールマップではなく、（カラー）ベクタービットマップによって操作されることです。 つまり、アトミックノードのいとこよりも強力で汎用性の高い製品です。

ベクトルマップはノーマルマップに似ていますが、正規化する必要はなく、RチャンネルとGreen（XとY）チャンネルのみが使用されます。 ブルーとアルファチャンネルは、必要に応じて黒のままにすることができます。 適切なベクターマップを作成することは、このノードを使用する際に最も大きな課題となることがあります。[グレースケールマップを標準に変換](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)するか、[RGBAマージでチャンネルを組み合わせてマップを作成します。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) または、[「フローマップ」](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting)のような機能も使用できます。

このノードは、標準的なワープノードではカットされない非常に特殊なゆがみを、さまざまな方向で行う場合に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー入力</i> | ゆがみをマップします。 |
| <b>ベクターマップ</b> <i>カラー入力</i> | ゆがみドライバのマップ。 カラーチャンネルには、赤と青が使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 1.0</i> | ベクトルマップの強度の乗数。 |
| <b>ベクター形式</b> <i>DirectX、OpenGL</i> | グリーンチャンネルのアップチャンネルとダウンチャンネルを切り替えます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-ex.png" />
        </td>
    </tr>
</table>
