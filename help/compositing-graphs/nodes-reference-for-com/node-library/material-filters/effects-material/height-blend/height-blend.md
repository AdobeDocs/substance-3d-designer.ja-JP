---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: ブレンドノードを使用すると、高さマップに基づいてテクスチャをブレンドし、リアルなマテリアル効果を作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Heightブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Heightブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend-01.png){width="128px"}

<b>内：</b> マテリアルフィルター >エフェクト

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Height情報に基づいて2つのハイトマップを組み合わせます。 ブレンドされたHeightmapだけでなく、他の場所で使用できる黒と白のマスクも生成します。

これは、[マテリアルのHeightブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)に必要なマテリアル全体ではなく、組み合わせる高品質のハイトマップが2つある場合に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Heightのトップ</b> <i>グレースケール入力</i> |  |
| <b>下のHeight</b> <i>グレースケール入力</i> |  |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>Heightオフセット</b> <i>0.0 - 1.0</i> | 軸に沿ってブレンドレベルが動くように、高さマップをオフセットします。 これは、ブレンドのメインコントロールです。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | ブレンドのコントラストを調整し、トランジションをよりシャープにします。 |
| <b>モード</b> <i>バランスの取れたHeight、下位Heightの優先度</i> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景Heightの描画の不透明度を調整して、フェードインまたはフェードアウトさせます。 |
