---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# 光沢入りエンボス

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/emboss-with-gloss.png){width="128px"}

## 光沢入りエンボス

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

色とHeightの入力に光沢（Specular反射）を加えたエンボス効果を与えます。 Height情報に基づいて、フェイクのベイク処理されたライティングを画像に加えます。 テクスチャにベイク処理されたライティングを必要とする一部のテクスチャリングスタイルに便利です。

他のオプションを含むバージョンについては、[Uberエンボス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)を参照してください。 [エンボス](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)のよりシンプルでアトミックなバージョンもあります。

## パラメーター

### 入力

* **カラー**: *カラー入力*
* **Height**: *グレースケール入力*

### パラメーター

* **ハイライトの色**: *（色の値）*Specularのハイライトの色。
* **シャドウカラー**: *（カラー値）*影の領域または明るくない領域で使用されるカラー。
* **光沢**: *0.0 ～ 0.5*&#x200B;光沢ハイライトのサイズ。
* **適用度**: *0.0 ～ 10.0*&#x200B;ハイライトの適用度。
* **光源の角度**: *0.0 ～ 1.0*\
  （偽物の）光の入射角度。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
