---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: 「BaseColorメタリック粗さコンバーター」ノードを使用して、様々なPBRマテリアル形式とワークフローを変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベースカラーメタリックの粗さコンバーター
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# ベースカラー/メタリック/粗さコンバーター

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## ベースカラー/メタリック/粗さコンバーター

**場所：** *マテリアルフィルター/PBRユーティリティ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、ベースカラー、メタリック、および粗さのマップを、Specular/光沢モデルなどの異なるPBRモデル出力に変換します。 付属の出力ターゲットには、Vray、Corona、Redshift、Renderman、Arnoldなどのよく知られたレンダリングエンジンがあります。

これは、PBRの1つのモデルで作成されたグラフやマテリアルがあり、ターゲットには別のモデルが必要な場合に便利です。

## パラメーター

* **SpecularLevel入力を使用**: *False/True*&#x200B;余分な入力スロットをSpecularLevel入力に公開します。 これは変換時にも考慮されます。
* ***Target**: *PBR拡散/Specular/グロス、Vray (GGX)、コロナ、コロナ1.6+、Redshift 1.x、Arnold 4 (AiStandard)、Arnold 4 (AlSurface)、RenderMan (PxrSurface)**変換対象モデルを設定します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
