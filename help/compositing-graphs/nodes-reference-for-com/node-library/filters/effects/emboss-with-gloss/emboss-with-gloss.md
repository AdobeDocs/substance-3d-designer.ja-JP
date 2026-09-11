---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: '[光沢のあるエンボス]ノードを使用して、テクスチャに深度と輝きを加えるための光沢マップを使用したエンボス効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光沢入りエンボス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# 光沢入りエンボス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

色とHeightの入力に光沢（Specular反射）を加えたエンボス効果を与えます。 Height情報に基づいて、偽物のベイクされた照明を画像に加えます。 テクスチャに照明をベイクする必要がある一部のテクスチャリングスタイルに便利です。

他のオプションを含むバージョンについては、[Uber エンボス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)を参照してください。 [エンボス](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)のより単純でアトミックなバージョンもあります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>色</b> <i>カラー入力</i> |  |
| <b>Height</b> <i>グレースケール入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ハイライトの色</b> <i>（カラー値）</i> | Specularハイライトの色。 |
| <b>シャドウの色</b> <i>（カラー値）</i> | 影の領域や明るくない領域で使用するカラー。 |
| <b>光沢</b> <i>0.0 - 0.5</i> | 光沢度ハイライトのサイズ。 |
| <b>適用度</b> <i>0.0 - 10.0</i> | ハイライトの強さ。 |
| <b>光源の角度</b> <i>0.0 - 1.0</i> | （偽物の）光の入射角度。 |
