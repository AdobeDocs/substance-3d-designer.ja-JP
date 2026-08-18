---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: マテリアルHeightのブレンドノードを使用すると、レイヤ化されたマテリアル効果を作成するためのHeightマップに基づいて、複数のマテリアルをブレンドできます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルHeightブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# マテリアルHeightブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## マテリアルHeightブレンド

**内：** *マテリアルフィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、Heightmapsに基づいて2つのマテリアルをブレンドする[Heightブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md)のより高度なバージョンです。 ユーザ定義のマスクがないので、各マテリアルに1つずつ、少なくとも1つが均一な値ではない2つのHeightmapが必要です。

これは、高品質なブレンドマスクを使用せずに2つの異なる高品質のマテリアルを組み合わせる場合に便利です。

水や雪に溶け込ませたい場合は、代わりにノード[Snowカバー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)と[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)を使用できます。

## パラメーター

### パラメーター

* **チャネル**\
  この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **Heightオフセット**: *0.0 ～ 1.0* Height軸に沿ってブレンドレベルが動くように、Heightmapsをオフセットします。 これは、ブレンドのメインコントロールです。
* **コントラスト**: *0.0 ～ 1.0*\
  ブレンドのコントラストを調整し、トランジションをよりシャープにします。
* **モード**: *バランスの取れたHeight、下のHeightの優先度* 2つの異なる描画モードを切り替えます。
* **不透明度**: *0.0 ～ 1.0*\
  前景Heightの描画の不透明度を調整して、フェードインまたはフェードアウトさせます。
* **アルベドの一致**: *0.0 ～ 1.0*&#x200B;アルベドの色の間で行う内部色の一致の量です。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
