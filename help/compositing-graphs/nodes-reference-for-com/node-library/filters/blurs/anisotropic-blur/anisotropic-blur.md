---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 異方性反射ブラーノードを使用して、ブラーの方向エフェクトを適用し、モーションブラーと筋エフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 異方性反射ブラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# 異方性反射ブラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## 異方性反射ぼかし（グレースケール）

**場所：** *フィルター/ぼかし*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

[方向のぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)の高品質を実行します。外観をカスタマイズするいくつかの設定があります。 「モーションブラー」とも呼ばれます。

重要：入力に適したバージョンを使用してください。 カラー入力には「異方性ブラー」を使用し、グレースケール入力には「異方性ブラーグレースケール」を使用します。

## パラメーター

* **強度**: *0.0 ～ 16.0*&#x200B;ぼかしの強度（半径）。 この値が大きいほど、ぼかしは先に達します。
* **異方性**: *0.0 ～ 1.0*&#x200B;ぼかしの方向性。 0.0に設定することは、通常のぼかしを実行することと同じです。
* **角度**: *0.0 ～ 1.0*&#x200B;ぼかし方向の角度を設定します。
* **品質**: *0 ～ 1*&#x200B;内部の[ボックスぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)とHQぼかしを切り替えます。 品質のための速度の貿易。

## サンプル画像

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
