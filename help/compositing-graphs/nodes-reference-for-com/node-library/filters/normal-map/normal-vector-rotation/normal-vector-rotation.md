---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: 法線ベクトルの回転ノードを使用して、法線マップベクトルを回転し、サーフェスの照明と詳細の方向を調整します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線のベクトル回転
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 法線のベクトル回転

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## 法線のベクトル回転

**場所：** *フィルター/標準マップ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

接線空間で入力Normalmapのすべてのベクトルを回転する法線ユーティリティノード。 ピクセルを変形するのではなく、ピクセルが表す値を変更します。 オプションのマップを使用して、グレースケールのファセットにランダムな回転を追加できます。

## 入力

* **標準**: *カラー入力*\
  回転を実行するベースマップ。 必須。
* **回転マップ（オプション）**: *グレースケール入力*\
  回転の強さを調整するグレースケールマップ。

## パラメーター

* **回転角度**: *0.0 ～ 1.0*\
  法線マップを回転する角度を設定します
* **標準の形式**: *DirectX、OpenGL*\
  法線マップ形式を切り替える（グリーンチャンネルを反転する）

## 例

</td>
</tr>
</table>
