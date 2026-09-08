---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: '[反応拡散高速]ノードを使用すると、プロシージャルのテクスチャに対して高速の反応拡散アルゴリズムを使用して有機的なパターンを生成できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拡散反応（速い）
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# 拡散反応（速い）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![リアクション拡散ノードアイコン](../../../../../../assets/reaction-diffusion.png "リアクション拡散ノードアイコン")

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、入力グレースケールイメージに対してリアクション拡散効果を行います。

反応 – 拡散とは、物質が広がって（拡散して）他の物質と相互作用する（反応する）過程のことです。 これは、例えば、動物の皮膚に特定のパターンが形成されたときに自然に何が起こるかをシミュレートする数学モデルです。

このノードはパフォーマンス用に最適化されており、速度に関していくつかの精度のトレードオフを行います。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール</i> | リアクション拡散効果を適用するグレースケールイメージです。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 入力画像に適用される拡散効果を表すグレースケールイメージです。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>半径</b> *浮動小数* | 効果が広がる範囲。 |
| <b>コントラスト</b> *浮動小数* | 入力のコントラストを調整します。一種の閾値として機能します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![例1](../../../../../../assets/reactdiff03.png "例1")

</td>
<td style="border: 0;" valign="top">

![例2](../../../../../../assets/reactdiff02.png "例2")

</td>
<td style="border: 0;" valign="top">

![例3](../../../../../../assets/reactdiff01.gif "例3")

</td>
</tr>
</table>
