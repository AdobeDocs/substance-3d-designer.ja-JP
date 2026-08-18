---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: '[AOキャンセル]ノードを使用して、クリーンなテクスチャ処理のためにスキャンしたマテリアルから環境オクルージョンを取り除きます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AOのキャンセル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
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

このノードは、別のAOマップ入力に基づいて、アルベド（ベースカラー）マップからアンビエントオクルージョンのライティング情報を削除しようとします。 アルベド情報がPBRで正しく、主に（強い）照明情報がないことを確認するために使用できます。

スキャンしたメッシュからベイク処理されたAOマップがある場合や、Heightまたは法線の情報から生成されたAOマップがある場合に便利なノードです。

## パラメーター

* **AOのキャンセル**: *0.0 ～ 1.0*&#x200B;照明情報を削除するための強度。
* **青の彩度**: *0.0 ～ 1.0*（脱）照明が除去された領域の彩度の補正。 このエフェクトは、暗い領域で失われたカラーを返すために使用できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
