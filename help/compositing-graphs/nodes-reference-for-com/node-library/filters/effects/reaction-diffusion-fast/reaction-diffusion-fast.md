---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: プロシージャテクスチャ用の高速反応拡散アルゴリズムを使用して有機的なパターンを生成するには、反応拡散の高速ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 反応拡散速
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# 拡散反応（速い）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![リアクションディフュージョンノードアイコン](reaction-diffusion-fast.resources/reaction-diffusion-fast-01.png "リアクションディフュージョンノードアイコン")

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、入力グレースケール画像に対して反応拡散効果を実行します。

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
| <b>半径</b> *フロート* | 効果が広がる範囲。 |
| <b>コントラスト</b> *浮動小数* | 入力のコントラストを調整します。一種の閾値として機能します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![例1](reaction-diffusion-fast.resources/reaction-diffusion-fast-02.png "例1")

</td>
<td style="border: 0;" valign="top">

![例2](reaction-diffusion-fast.resources/reaction-diffusion-fast-03.png "例2")

</td>
<td style="border: 0;" valign="top">

![例3](reaction-diffusion-fast.resources/reaction-diffusion-fast-04.gif "例3")

</td>
</tr>
</table>
