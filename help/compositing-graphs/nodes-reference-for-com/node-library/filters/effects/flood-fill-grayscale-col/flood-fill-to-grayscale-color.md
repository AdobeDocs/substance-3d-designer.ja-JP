---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Flood Fillからグレースケールへのカラーノードを使用して、接続された領域をグレースケールで塗りつぶし、モノクロパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GrayscaleColorへのFlood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Flood Fillからグレースケール/カラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fillからランダムなグレースケール/カラー

**場所：** *フィルター/効果*

**&#x200B;**&#x200B;単純&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## 説明

Flood Fillデータを使用して、グレースケールまたはカラー値のスウォッチを生成します。 [Flood Fillからランダムグレースケールへ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)とは異なり、これらの2つのノードでは、セルごとにランダム化する基本値を決定する追加の入力マップを使用することで、正確なバリエーションとトーンをより詳細に制御できます。

これは、すべてのセルに独自の値や色を与えながら、制御を維持し、事前に決定された入力をベースとする強力なシステムです。

## パラメーター

### 入力

* **Flood Fill**: *カラー入力*
* **グレースケール/色入力**: *グレースケール/色入力*

### パラメーター

* **輝度/カラー調整**: *-1.0 - 1.0*&#x200B;ノードのバイアスまたはベース値を設定します。 グレースケールまたはカラー入力を使用する場合は、開始点としてその初期値を変更するために使用されます。
* **輝度/カラーランダム**: *-1.0 - 1.0*&#x200B;変化の量を設定します。

</td>
</tr>
</table>
