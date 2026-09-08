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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# マテリアルHeightブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

<b>内：</b> マテリアルフィルター >エフェクト

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、Heightmapsに基づいて2つのマテリアルをブレンドする[Heightブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md)のより高度なバージョンです。 ユーザ定義のマスクがないので、各マテリアルに1つずつ、少なくとも1つが均一な値ではない2つのHeightmapが必要です。

これは、高品質なブレンドマスクを使用せずに2つの異なる高品質のマテリアルを組み合わせる場合に便利です。

水や雪に溶け込ませたい場合は、代わりにノード[Snowカバー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)と[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)を使用できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>Heightオフセット</b> <i>0.0 - 1.0</i> | 軸に沿ってブレンドレベルが動くように、高さマップをオフセットします。 これは、ブレンドのメインコントロールです。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | ブレンドのコントラストを調整し、トランジションをよりシャープにします。 |
| <b>モード</b> <i>バランスの取れたHeight、下位Heightの優先度</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景Heightの描画の不透明度を調整して、フェードインまたはフェードアウトさせます。 |
| <b>アルベドの一致</b> <i>0.0 - 1.0</i> | アルベドカラー間で行う内部カラーマッチングの量。 |
