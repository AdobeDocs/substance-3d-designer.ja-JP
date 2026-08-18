---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: ライトノードを使用して、メッシュの照明条件に基づいてマスクを生成し、リアルなマテリアルのバリエーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライト
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# ライト

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## ライト

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは他のジェネレータとは少し異なります。これは、ワールド空間の法線マップに基づいて純粋に偽の照明を行い、白黒の「ライトマップ」マスクを返します。

## パラメーター

* **水平角度**: *0.0 ～ 1.0*&#x200B;フェイクライトの水平角度を設定します。
* **頂角**: *0.0 ～ 1.0*&#x200B;フェイクライトの頂角を設定します。
* **光沢度のハイライト**: *0.0 - 0.999*&#x200B;ハイライト領域のフォールオフの広がりを設定します。
* **ハイライトレベル**: *0.0 ～ 1.0*&#x200B;ハイライト領域の明るさのレベルを設定します。

## サンプル画像

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
