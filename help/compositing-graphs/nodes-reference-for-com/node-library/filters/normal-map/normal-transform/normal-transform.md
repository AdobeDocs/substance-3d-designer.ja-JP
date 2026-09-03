---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: ベクトル方向を正しく維持しながら法線マップに変換を適用するには、法線変形ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 法線の変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform-01.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

アトミックトランスフォーム2Dノードと同様に、接線空間を分割せずにノーマルマップを変換できます。その代わりに、その場で再計算が行われます。その結果、常に正しいノーマルマップが生成されます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>（変換行列）:</i> | 入力を回転またはスケールします。 |
| <b>オフセット</b> <i>-0.5 - 0.5</i> | 結果を移動または変換します。 変形コントロールがある場合は、カンバスと直接対話することで結果を変更できます。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 法線マップ形式を切り替える（グリーンチャンネルを反転する） |
