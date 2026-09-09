---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: マテリアル分析用にテクスチャから高周波数の照明のディテールを取り除くには、「照明キャンセル高周波数」ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライティングで高周波数をキャンセル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# ライティングで高周波数をキャンセル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)と似ていますが、フルカラー画像に適しています（それほど彩度を下げません）。このノードは、高周波数の小さな照明のディテールを取り消そうとします。

[低周波数の照明をキャンセル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)および、より高度な、おすすめの[輝度ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md)も参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 1.0</i> | 照明キャンセル効果の強さ。 |
| <b>半径</b> <i>0.0 - 10.0</i> | キャンセルする光の詳細の半径またはサイズ。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="lighting-cancel-high-frequencies.resources/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
