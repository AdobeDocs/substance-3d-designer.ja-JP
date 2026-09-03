---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: 輝度ハイパスノードを使用して、テクスチャから高周波輝度のディテールを取り出し、サーフェスのディテールを強調します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 輝度ハイパス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 輝度ハイパス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass-01.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)を入力の輝度値に対して実行して、照明情報を取り消します。 撮影したテクスチャを照明情報で修正する場合に便利です。 [Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)で複数のパスを組み合わせて、様々な周波数の光のディテールを取り除くことができます。

[低周波数の照明をキャンセル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)よりも、色の保持に関して少し優れています。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>半径</b> <i>0.0 - 64.0</i> | ハイパス効果の半径です。 半径を小さくすると、小さな照明がキャンセルされ、入力画像に合わせて調整されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-02.png" />
        </td>
    </tr>
</table>
