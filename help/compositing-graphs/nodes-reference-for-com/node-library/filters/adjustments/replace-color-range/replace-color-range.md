---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: カラー範囲の置き換えノードを使用して、指定した範囲内のカラーをカラー補正のために新しいカラーに置き換えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラー範囲を置換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# カラー範囲を置換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range-01.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ソースカラーをターゲットカラーに置き換えます。追加のコントロールがあります。 例えば、ID マップ(烘焙)の一部に色を付け直すときなどに使用できます。

より詳細なバージョンについては、[カラーマッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ソースカラー</b> <i>（カラー値）</i> | 置き換えるカラー。 |
| <b>ターゲットの色</b> <i>（カラー値）</i> | 置き換えるカラー。 |
| <b>ソース範囲</b> <i>0.0 - 1.0</i> | 選択したソースの範囲または許容値。 隣接するカラーの色相もシフトされるように、色相を大きくすることができます。 |
| <b>しきい値</b> <i>0.0 - 1.0</i> | 範囲の減衰/コントラスト。 ソースカラーのみを置き換えるには低く、ソースカラーにブレンドするカラーを置き換えるには高く設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-02.png" />
        </td>
    </tr>
</table>
