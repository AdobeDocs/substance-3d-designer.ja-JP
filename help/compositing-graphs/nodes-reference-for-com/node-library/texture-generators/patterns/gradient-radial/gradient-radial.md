---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: 円形グラデーションの中心点から放射状に広がる円形グラデーションを作成するには、グラデーション円形ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 円形グラデーション
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# 円形グラデーション

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/gradient-radial.png){width="128px"}

## 円形グラデーション

**イン：** *テクスチャジェネレーター**/パターン*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

[円形グラデーション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)と同様に、2つのカスタムポイントによって放射状に定義されたグレースケールグラデーションのトランジションを作成します。 変換はaからbの間で行われ、中心点と半径で定義されます。 結果が常に並ぶとは限らない点に注意してください。

## パラメーター

* **シェイプ: *円錐、半球***トランジションのプロファイルを決定します。 円錐はシャープで線形の変化で、半球はソフトで中央が丸くなっています。
* **ポイント1**:\
  グラデーションの中心点。 白から始まります。
* **ポイント2**:\
  グラデーションの範囲を決定する半径ポイント。 黒で終わります。
* **非正方形拡張**: *False/True*\
  カボチャの補正を有効にし、非正方形の比率で伸縮します。

</td>
</tr>
</table>
