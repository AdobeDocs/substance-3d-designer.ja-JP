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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---


# 通常のワールドユニットへのHeight

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-hq.png){width="128px"}

## 通常のワールドユニットへのHeight

**場所：** *フィルター/法線マップ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

変換中に実際のユニットを使用する、高度なHeightから通常への変換ノード。

ソースのHeightmapのサイズがわかっていて、スキャンしたマテリアルを操作する場合など、最も正確な変換を行いたい場合に便利です。

## パラメーター

* **表面サイズ(cm)**: *0.0 ～ 1000.0*&#x200B;入力HeightmapのDimension。
* **Heightの深度(cm)**: *0.0 ～ 100.0* Heightmapの詳細の最大深度。
* **標準の形式**: *OpenGL、DirectX*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。
* **サンプリング**: *標準、Sobel*&#x200B;精度を決定する2つのサンプリングモードを切り替えます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
