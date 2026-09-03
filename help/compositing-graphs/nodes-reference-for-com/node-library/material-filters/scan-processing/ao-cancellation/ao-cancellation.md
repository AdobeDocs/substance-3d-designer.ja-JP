---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: 「AOキャンセル」ノードを使用して、スキャンしたマテリアルからambient occlusionを取り除き、クリーンなテクスチャ処理を行います。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AOのキャンセル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# AOのキャンセル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、別のAOマップ入力に基づいて、アルベド(Base color)マップからAmbient occlusionの照明情報を削除しようとします。 アルベド情報がPBRで正しく、主に（強い）照明情報がないことを確認するために使用できます。

スキャンしたメッシュからAOマップをベイクする場合や、Heightまたは通常の情報からAOマップを生成する場合に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>AOのキャンセル</b> <i>0.0 - 1.0</i> | 照明情報を削除する強さです。 |
| <b>青の彩度</b> <i>0.0 - 1.0</i> | (De)照明が除去される領域の彩度の補正。 このエフェクトは、暗い領域で失われたカラーを返すために使用できます。 |
