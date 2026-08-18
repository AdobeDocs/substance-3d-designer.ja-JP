---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: '[法線の変換]ノードを使用すると、ベクトル方向を正しく維持しながら、法線マップに変換を適用できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線の変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 法線の変形

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## 法線の変形

**場所：** *フィルター/標準マップ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

アトミックトランスフォーム2Dノードと同様に、接線空間を分割せずにノーマルマップを変換できます。その代わりに、その場で再計算が行われます。その結果、常に正しいノーマルマップが生成されます。

## パラメーター

* **Matrix2x2**: *（変換マトリックス）:*\
  入力を回転またはスケールします。
* **オフセット**: *-0.5 - 0.5*\
  結果を移動または変換します。 変形コントロールがある場合は、カンバスと直接対話することで結果を変更できます。
* **標準の形式**: *DirectX、OpenGL*\
  法線マップ形式を切り替える（グリーンチャンネルを反転する）

</td>
</tr>
</table>
