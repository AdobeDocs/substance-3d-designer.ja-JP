---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: 高さ押し出しノードを使用して、テクスチャで3Dのような深度効果を生み出すための高さマップに基づいてシェイプを押し出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高さ押し出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# 高さ押し出し

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude-01.png){width="200px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さ押し出しは、入力高さマップから3D Z深度をレンダリングします。 [シェイプの押し出し](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)や[Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)と同様に、2D ビュー内でカメラをスピンさせることができます。 主な目的は、平坦な高さマップから3D回転したシェイプを作成するためのジェネレータとして機能することです。 これらの図形は、[図形のスプラッタ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)と共に使用できます。

[シェイプの押し出し](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)との主な違いは、入力マップがバイナリ「アルファ」タイプのマップである必要がなく、フルレンジのグレースケールマップである必要があることです。 つまり、押し出しのHeight（有機的で複雑なシェイプ）をより細かく制御できますが、ベベルプロファイル（ハードサーフェス、単純なシェイプ）のようなものは制御できません。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>カメラ角度</b> | カメラのオイラー角を半回転で表したもの。 水平方向の回転と拡大・縮小は、入力に直接適用されることに注意してください。 |
| <b>カメラスケール</b> <i>0.001 - 3.0</i> | 出力に適用されるグローバルスケール。 |
| <b>Heightスケール</b> <i>0.0 - 2.0</i> | 入力Height値にグローバル係数を適用します。 |
| <b>垂直方向のオフセット</b> <i>-1.0 - 1.0</i> | 最終出力を上下に移動します。 |
| <b>地面</b> <i>オフ/オン</i> | Groundがオフの場合、入力がグラウンドのようなプレーンではなく0の場所に黒い背景が表示されます。 |
| <b>標準の形式</b> <i>DirectX/OpenGL</i> | <b>標準形式</b>パラメーターは、法線マップのY座標を反転します。 |
| <b>法線の強度</b> <i>0.0 - 256.0</i> | <b>Normal</b>ノードの<b>Intensity</b>パラメーターと同じです。 回転中にシャールのない法線を取得するには、256に設定します。 |
