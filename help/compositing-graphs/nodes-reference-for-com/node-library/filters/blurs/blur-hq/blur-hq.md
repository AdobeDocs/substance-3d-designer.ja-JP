---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: ぼかしHQノードを使用して、高品質のぼかし効果をテクスチャに適用し、滑らかでプロフェッショナルな外観のぼかしを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ブラー HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# ブラー HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-01.png){width="128px"}

![](blur-hq.resources/blur-hq-02.png){width="128px"}

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高品質ガウスぼかしを結果に対して実行します。 [標準のアトミックボックスぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [よりも画質が大幅に向上しました。](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

重要：入力に適したバージョンを使用してください。 カラー入力には「ブラーHQ」を使用し、グレースケール入力には「ブラーHQグレースケール」を使用します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 16.0</i> | ブラーの強さ（半径）。 この値が大きいほど、ぼかしは先に達します。 |
| <b>クォリティ</b> <i>0 - 1</i> | 内部サンプリング量を増やして高品質を実現し、計算速度を低下させます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/blur-hq-03.gif" />
        </td>
    </tr>
</table>
