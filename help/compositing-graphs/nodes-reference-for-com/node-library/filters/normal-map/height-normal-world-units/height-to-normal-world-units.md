---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: 精度の高い詳細を得るには、[標準ワールド単位にHeight]ノードを使用して、ワールド単位のスケーリングを使用して高さマップを法線マップに変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通常のワールドユニットへのHeight
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# 通常のワールドユニットへのHeight

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

変換中に実際のユニットを使用する、高度なHeightから通常への変換ノード。

ソースのHeightmapのサイズがわかっていて、スキャンしたマテリアルを操作する場合など、最も正確な変換を行いたい場合に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>表面のサイズ(cm)</b> <i>0.0 - 1000.0</i> | 入力HeightmapのDimension。 |
| <b>深度 (cm)</b> <i>0.0 - 100.0</i> | Heightmapディテールの最大深度。 |
| <b>標準の形式</b> <i>OpenGL, DirectX</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>サンプリング</b> <i>標準、ソベル</i> | 精度を決定する2つのサンプリングモードを切り替えます。 |
