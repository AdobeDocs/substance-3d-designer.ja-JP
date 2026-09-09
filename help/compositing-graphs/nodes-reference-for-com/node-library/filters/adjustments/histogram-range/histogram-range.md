---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: '[ヒストグラム範囲]ノードを使用して、カラー補正と調整のヒストグラム範囲に基づいてテクスチャ値を再マップします。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラム範囲
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# ヒストグラム範囲

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-1.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケール入力の範囲を縮小または移動します。 これは[コントラストの輝度](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)と似ていますが、状況によっては異なるコントロールを使用して、トランジションを再マップできます。\
また、範囲を再マップするためのより便利な方法については、[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)を参照してください。

[ここをクリックして、ヒストグラムの範囲に関するSubstanceアカデミーのビデオを視聴します。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>範囲</b> <i>0.0 - 1.0</i> | 範囲を縮小する範囲。 これは、最小レベルと最大レベルの両方のスライダーを内側に移動することと似ています。 |
| <b>位置</b> <i>0.0 - 1.0</i> | 「オフセット」では、範囲を縮小するために別の中心点を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range.gif" />
        </td>
    </tr>
</table>
