---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 異方性反射ブラーノードを使用して方向ブラーエフェクトを適用し、モーションブラーや筋の効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 異方性反射ブラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# 異方性反射ブラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[方向のぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)の高品質を実行します。外観をカスタマイズするいくつかの設定があります。 「モーションブラー」とも呼ばれます。

重要：入力に適したバージョンを使用してください。 カラー入力には「異方性ブラー」を使用し、グレースケール入力には「異方性ブラーグレースケール」を使用します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 16.0</i> | ぼかしの強さ（半径）。 この値が大きいほど、ぼかしは先に達します。 |
| <b>異方性</b> <i>0.0 - 1.0</i> | ぼかしの方向性。 0.0に設定することは、通常のぼかしを実行することと同じです。 |
| <b>角度</b> <i>0.0 - 1.0</i> | ぼかし方向の角度を設定します。 |
| <b>クォリティ</b> <i>0 - 1</i> | 内部的に[ボックスぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)とHQブラーを切り替えます。 品質のための速度の貿易。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
