---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# BaseColor/メタリック/ラフネスコンバーター

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/pbr-convert.png){width="128px"}

<b>イン：</b> マテリアルフィルター > PBRユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、ベースカラー、メタリックマップ、およびラフネスマップを、Specular/光沢度モデルなどの異なるPBRモデル出力に変換します。 含まれる出力ターゲットには、Vray、Corona、Redshift、Renderman、Arnoldなどのよく知られたレンダリングエンジンがあります。

この機能は、PBRの1つのモデルで作成されたグラフまたはマテリアルがあり、かつ対象として別のモデルが必要な場合に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>SpecularLevel入力を使用する</b> <i>False/True</i> | スペキュラレベル入力に追加の入力スロットを表示します。 これは変換時にも考慮されます。 |
| <b>ターゲット</b> <i>PBR Diffuse/Specular/グロス、Vray(GGX)、Corona、Corona 1.6+、Redshift 1.x、Arnold 4(AiStandard)、Arnold 4(AlSurface)、RenderMan(PxrSurface)</i> | 変換対象モデルを設定します。 |
