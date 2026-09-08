---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# AOのキャンセル

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## AOのキャンセル

**イン：** *マテリアルフィルター/スキャン処理*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、別のAOマップ入力に基づいて、アルベド(Base color)マップからAmbient occlusionの照明情報を削除しようとします。 アルベド情報がPBRで正しく、主に（強い）照明情報がないことを確認するために使用できます。

スキャンしたメッシュからAOマップをベイクする場合や、Heightまたは通常の情報からAOマップを生成する場合に便利です。

## パラメーター

* **AOの取り消し**: *0.0 - 1.0*&#x200B;照度情報を削除する強さ。
* **青の彩度**: *0.0 ～ 1.0*（脱）照明が除去された領域の彩度の補正。 このエフェクトは、暗い領域で失われたカラーを返すために使用できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
