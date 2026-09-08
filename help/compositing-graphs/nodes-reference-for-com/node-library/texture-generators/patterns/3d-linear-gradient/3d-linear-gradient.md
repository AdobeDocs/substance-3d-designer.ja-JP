---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 3D Linear gradientノードを使用して、空間効果の3Dワールド位置に基づいて線形グラデーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D Linear gradient

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力の位置マップに基づいてボリュームグラデーションを作成します。 3D空間の2点間で黒から白へのトランジションを効果的に生成します。 GPU エンジンでのみ使用されます。

同様の効果については、[3Dボリュームマスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)も参照してください。

## パラメーター

* **ポイントの配置モード**: *UV位置、ワールド空間位置*&#x200B;グラデーションポイントは、手動で正確な位置を設定する場合に、UVスペース（2D ビューに設定する場合に最適）または3D座標のどちらで機能するかを選択します。
* **ポイント1**:\
  グラデーションの開始点。 位置モードに基づいて2D座標または3D座標を指定できます。
* **ポイント2**:\
  グラデーションの終点です。 位置モードに基づいて2D座標または3D座標を指定できます。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。

## サンプル画像

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
