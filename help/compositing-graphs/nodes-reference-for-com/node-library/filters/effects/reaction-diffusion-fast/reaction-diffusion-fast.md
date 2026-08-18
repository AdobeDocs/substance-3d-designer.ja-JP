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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# 反応拡散速

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![リアクションディフュージョンノードアイコン](../../../../../../assets/reaction-diffusion.png "リアクションディフュージョンノードアイコン")

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、入力グレースケール画像に対して反応拡散効果を実行します。

反応拡散とは、物質が広がって（拡散して）他の物質と相互作用する（反応する）過程のことです。 これは、例えば、動物の皮膚に特定のパターンが形成されたときに自然に何が起こるかをシミュレートする数学モデルです。

このノードはパフォーマンス用に最適化されており、速度に関していくつかの精度のトレードオフを行います。

</td>
</tr>
</table>

## 入力コネクタ

<b>入力</b> *グレースケール*&#x200B;反応拡散効果を適用するグレースケール画像です。

## 出力コネクタ

<b>出力&#x200B;</b>*グレースケール*&#x200B;入力画像に適用された反応拡散効果を表すグレースケール画像です。

## パラメーター

<b>半径</b> *浮動小数点*&#x200B;効果の範囲。

<b>コントラスト</b> *浮動小数点*\
入力のコントラストを調整します。一種の閾値として機能します。

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
