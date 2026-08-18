---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Heightブレンドノードを使用すると、リアルなマテリアルトランジションを作成するためのHeightマップに基づいてテクスチャをブレンドできます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Heightブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Heightブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Heightブレンド

**内：** *マテリアルフィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

Height情報に基づいて2つのハイトマップを組み合わせます。 ブレンドされたHeightmapだけでなく、他の場所で使用できる白黒マスクを生成します。

これは、[マテリアルHeightブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)に必要な高品質のハイトマップが2つある場合に便利です。ただし、必ずしも完全なマテリアルである必要はありません。

## パラメーター

### 入力

* **Heightトップ**: *グレースケール入力*
* **Heightの下**: *グレースケール入力*
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **Heightオフセット**: *0.0 ～ 1.0* Height軸に沿ってブレンドレベルが動くように、Heightmapsをオフセットします。 これは、ブレンドのメインコントロールです。
* **コントラスト**: *0.0 ～ 1.0*\
  ブレンドのコントラストを調整し、トランジションをよりシャープにします。
* **モード**: *バランスの取れたHeight、下のHeightの優先度* 2つの異なる描画モードを切り替えます。
* **不透明度**: *0.0 ～ 1.0*\
  前景Heightの描画の不透明度を調整して、フェードインまたはフェードアウトさせます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
