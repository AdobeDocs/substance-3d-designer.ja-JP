---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: 「HDRマージ」ノードを使用すると、複数のHDR画像を単一のパノラマにマージして、複合環境マップを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HDR 結合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# HDR 結合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge-01.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

複数の写真の露光量を結合して、ハイダイナミックレンジの画像を作成します。 最初の入力は、露光量不足の画像です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力1-16</b> <i>カラー入力</i> | 入力画像。 使用可能な量はパラメーターによって異なります。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力</b> <i>2 - 16</i> | 使用可能な入力量を設定します。 |
| <b>露出デルタ(EV)</b> <i>0.0 - 4.0</i> | イメージ間で解釈する露出の差を設定します。 |
| <b>白色点</b> <i>0.0 - 13.0</i> | 最終結果に対して調整を行う場合は、「白色点」を選択します。 |
