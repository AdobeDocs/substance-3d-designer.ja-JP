---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: '[3Dシンプレックスノイズ]ノードを使用して、滑らかで自然に見えるボリュームテクスチャを作成するためのシンプレックスノイズパターンを3D生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dシンプレックスノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 3Dシンプレックスノイズ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## 3Dシンプレックスノイズ

**インチ：** *テクスチャジェネレーター**/ノイズ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイクした位置マップが入力スロットに接続されると、手続き型ノイズが発生します。 これは、GPUエンジンでのみ使用します。\
[3Dパーリンノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)と似ていますが、パフォーマンスと速度が重要な場合はより速く、簡単になります。

このノイズは、実際のノイズではなく、[Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers)を入力としてテストできます（下図の例を参照）。

## パラメーター

* **スケール**: *0.0 ～ 64.0*\
  エフェクトのグローバルスケールを設定します。
* **サイズ**: *0.0 ～ 2.0* X、Y、Z軸に対して個別に不均等なスケーリングを実行します。

## サンプル画像

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
