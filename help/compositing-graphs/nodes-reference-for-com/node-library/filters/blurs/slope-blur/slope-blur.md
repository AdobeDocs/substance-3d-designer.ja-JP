---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: 勾配ブラーノードを使用して、モーションブラーを作成するためのHeightマップ勾配に基づく方向ブラー効果を適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ぼかし(勾配)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# ぼかし(勾配)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## ぼかし(勾配)

**場所：** *フィルター/ぼかし*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

高度な高品質ブラーを実行します。異方性/方向はグレースケールの「勾配マップ」によって決定されます。 勾配マップの勾配に続く勾配ぼかし効果として、[方向ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)（内部を基準）と似た、高いマップのように表現します。

これは、Designerで最も興味深く、強力なぼかしの1つです。 エッジのチッピングや風化、Dirtや錆のにじみや漏れなど、非常に興味深く予期しない効果を得るために使用できます。

重要：入力に適したバージョンを使用してください。 カラー入力には「勾配ぼかし」を使用し、グレースケール入力には「勾配ぼかしグレースケール」を使用します。

## パラメーター

### 入力

* **勾配**: *グレースケール入力*&#x200B;異方性のドライブ角度に対する勾配マップ。 理想的には、傾斜したグラデーションを含める必要があります。粗い、シャープなトランジションは適切に機能しません。

### パラメーター

* **サンプル**: *0 ～ 32*&#x200B;サンプルの量は、速度を犠牲にして品質に影響します。
* **強度**: *0.0 ～ 16.0*\
  ぼかしの量または強さ。
* **モード**: *ぼかし、最小、最大*|\
  結果としてぼかしのパスとなる描画モード。 「ぼかし」は標準の[異方性反射ぼかし](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)と似ていますが、最小は既存の領域を「食い尽くす」、最大は白い領域を「にじませる」ことができます。

## サンプル画像

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
