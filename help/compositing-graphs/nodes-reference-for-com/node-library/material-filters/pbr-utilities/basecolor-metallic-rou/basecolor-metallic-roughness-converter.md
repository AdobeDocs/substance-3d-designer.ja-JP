---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: BaseColor メタリックラフネスコンバーターノードを使用して、異なるPBR マテリアル形式およびワークフロー間で変換を行います。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BaseColor メタリックラフネスコンバータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
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

このノードは、ベースカラー、メタリックマップ、およびラフネスマップを、Specular/光沢度モデルなどの異なるPBRモデル出力に変換します。 含まれる出力ターゲットには、Vray、Corona、Redshift、Renderman、Arnoldなどのよく知られたレンダリングエンジンがあります。

この機能は、PBRの1つのモデルで作成されたグラフまたはマテリアルがあり、かつ対象として別のモデルが必要な場合に便利です。

## パラメーター

* **SpecularLevel入力を使用**: *False/True* SpecularLevel入力に追加の入力スロットを表示します。 これは変換時にも考慮されます。
* ***Target**: *PBR Diffuse/Specular/グロス、Vray (GGX)、Corona、Corona 1.6+、Redshift 1.x、Arnold 4 (AiStandard)、Arnold 4 (AlSurface)、RenderMan (PxrSurface)**変換対象モデルを設定します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
