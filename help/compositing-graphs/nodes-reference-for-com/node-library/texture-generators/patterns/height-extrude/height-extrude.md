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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# 高さ押し出し

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## 高さ押し出し

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

高さ押し出しは、入力高さマップから3D Z深度をレンダリングします。 [シェイプの押し出し](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)や[Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)と同様に、2D ビュー内でカメラをスピンさせることができます。 主な目的は、平坦な高さマップから3D回転したシェイプを作成するためのジェネレータとして機能することです。 これらの図形は、[図形のスプラッタ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)と共に使用できます。

[シェイプの押し出し](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md)との主な違いは、入力マップがバイナリ「アルファ」タイプのマップである必要がなく、フルレンジのグレースケールマップである必要があることです。 つまり、押し出しのHeight（有機的で複雑なシェイプ）をより細かく制御できますが、ベベルプロファイル（ハードサーフェス、単純なシェイプ）のようなものは制御できません。

## パラメーター

* **カメラ角度**:\
  カメラのオイラー角を半回転で表したもの。 水平方向の回転と拡大・縮小は、入力に直接適用されることに注意してください。
* **カメラスケール**: *0.001 - 3.0*\
  出力に適用されるグローバルスケール。
* **Heightスケール**: *0.0 ～ 2.0*\
  入力Height値にグローバル係数を適用します。
* **垂直オフセット**: *-1.0 - 1.0*\
  最終出力を上下に移動します。
* **地面**: *オフ/オン*\
  Groundがオフの場合、入力がグラウンドのようなプレーンではなく0の場所に黒い背景が表示されます。
* **標準の形式**: *DirectX/OpenGL*\
  **標準形式**&#x200B;パラメーターは、法線マップのY座標を反転します。
* **法線の強度**: *0.0 ～ 256.0*\
  **Normal**&#x200B;ノードの&#x200B;**Intensity**&#x200B;パラメーターと同じです。 回転中にシャールのない法線を取得するには、256に設定します。

## サンプル画像

</td>
</tr>
</table>
