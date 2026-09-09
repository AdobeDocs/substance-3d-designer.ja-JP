---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: サーフェスの照明と詳細な方向を調整するために法線マップベクトルを回転するには、 Normal Vector Rotationノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線のベクトル回転
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# 法線のベクトル回転

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

正接空間で入力Normalmapのすべてのベクトルを回転させる法線ユーティリティノード。 ピクセルを変形するのではなく、ピクセルが表す値を変更します。 オプションのマップを使用して、グレースケールのファセットにランダムな回転を追加できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>標準</b> <i>カラー入力</i> | 回転を実行するベースマップ。 必須。 |
| <b>回転マップ （オプション）</b> <i>グレースケール入力</i> | 回転強さを変調するグレースケールマップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>回転角度</b> <i>0.0 - 1.0</i> | 法線マップを回転する角度を設定します |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 法線マップ形式を切り替える（グリーンチャンネルを反転する） |
