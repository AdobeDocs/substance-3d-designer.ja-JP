---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-switch.html"
breadcrumb-title: ''
description: マテリアル切り替えノードを使用して、入力マスクまたは条件に基づいて複数のマテリアルを切り替えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルスイッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---


# マテリアルスイッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-switch.resources/material-switch.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、[Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)のマルチチャンネル、フルマテリアルのバージョンです。 入力として2つのマテリアルを受け取り、switchパラメーターに基づいて1つのみを返します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>切り替え</b> <i>False/True</i> | 切り替えると、マテリアル 1または2が返されます。 |
