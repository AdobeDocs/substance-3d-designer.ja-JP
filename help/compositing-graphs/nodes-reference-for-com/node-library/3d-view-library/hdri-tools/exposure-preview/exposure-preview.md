---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 最終レンダリングの前に、露光量プレビューノードを使用して、HDRI環境での露光量調整をプレビューします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 露光量プレビュー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# 露光量プレビュー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/exposure-preview-01.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

露出ステップをプレビューするためのヘルパーノード。 ユーザが最小値と最大値を設定すると、ノードはオリジナルの入力の公開されたバージョンが異なるより大きなイメージを生成します。 異なるバージョンは常に水平方向に積み重ねられます。量はノードまたはグラフの解像度によって異なります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>最大露光量(EV)</b> <i>-8.0 - 8.0</i> | 一番上の最も明るい画像の最大露光量。 |
| <b>最小露出(EV)</b> <i>-8.0 - 8.0</i> | 最も暗い画像（下部）の最小露光量。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exposure-preview-02.png" />
        </td>
    </tr>
</table>
