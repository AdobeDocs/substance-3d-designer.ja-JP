---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: ハイパスノードを使用して、テクスチャから高周波数のディテールを取り出し、シャープとディテールの強調の効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ハイパス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# ハイパス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/high-pass-greyscale.png){width="128px"}

![](highpass.resources/high-pass.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

カラーおよびグレースケールバージョンで使用可能なハイパスフィルターを実行します。 同じ名前のPhotoshopアクションに似ています。\
タイリングのためにテクスチャをクリーンアップする場合など、画像の大きな輝度差を取り除く場合に便利です。

重要：入力に適したバージョンを使用してください。 カラー入力には「ハイパス」、グレースケール入力には「ハイパスグレースケール」を使用します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>半径</b> <i>0.0 - 64.0</i> | フィルターの半径：半径を小さくすると小さな違いが除去され、半径を大きくすると大きな領域が除去されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-example.png" />
        </td>
    </tr>
</table>
