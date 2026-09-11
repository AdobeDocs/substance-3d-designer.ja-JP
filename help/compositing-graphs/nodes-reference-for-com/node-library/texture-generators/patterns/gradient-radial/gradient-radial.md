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
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# 円形グラデーション

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[円形グラデーション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)と同様に、2つのカスタムポイントによって放射状に定義されたグレースケールグラデーションのトランジションを作成します。 変換はaからbの間で行われ、中心点と半径で定義されます。 結果が常に並ぶとは限らない点に注意してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>図形</b> <i>円錐、半球</i> | トランジションプロファイルを決定します。 円錐は鋭い直線的な変化で、半球はソフトで中心が丸くなっています。 |
| <b>ポイント1</b> | グラデーションの中心点。 白から始まります。 |
| <b>ポイント2</b> | グラデーションの範囲を決定する半径ポイント。 黒で終わります。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチの非正方形の比率での補正を有効にします。 |
