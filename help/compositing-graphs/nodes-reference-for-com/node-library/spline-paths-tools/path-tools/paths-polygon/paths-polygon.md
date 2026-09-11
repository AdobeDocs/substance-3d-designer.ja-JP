---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-polygon.html"
breadcrumb-title: ''
description: Pathsポリゴンノードを使用して、ジオメトリパターンを生成するための頂点データからポリゴンパスを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Polygon
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角形のパス
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# 多角形のパス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](paths-polygon.resources/paths-polygon-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

パス形式でプリミティブ（多角形）を生成します。

プリミティブを正確に配置するには、[Path 2D 変形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md)ノードを使用します。

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | 1つのエンコードされたパスのリストが含まれ、エンコードされたセグメントのリストが記述されます。<br>これは直接使用または変更するためにインデントされていません。 互換性のあるノードを見つけるためのパスを検索します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>辺の数</b> <i>整数</i> | ヒント： 100 ～ 1000の数値を入力して、円を生成します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](paths-polygon.resources/PathsPolygon_Variant1_1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](paths-polygon.resources/PathsPolygon_Variant2.jpg "ノードの例2")

</td>
</tr>
</table>
