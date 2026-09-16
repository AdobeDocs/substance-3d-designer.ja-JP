---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: ワープノードを使用して、テクスチャにゆがみエフェクトを適用し、ワープやディスプレイスメントエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ワープ
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 9%
---

# ワープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：ワープ](warp.resources/comp_warp_1.png "原子ノード：ワープ"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

別のグラデーション入力から計算されたスロープに従って入力画像のピクセル値を移動し、結果として変形を行います。

ディレクショナルワープとは異なり、このノードは、グラデーション入力の勾配またはグラデーションで定義される方向に、白い領域を均一に押し出します。

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="warp.resources/warp-tooltip.gif" alt="ワープツールヒント" /></div>

このノードは、エフェクトの結果がグラデーション入力に大きく依存するため、少し扱いにくいことがあります。グラデーションをわずかに微調整すると、同じ強度値で視覚的に大きな違いが生じる可能性があります。 グラデーション入力のコントラスト、輝度、スケール、およびこのノードの強度スライダーを試してください。

法線マップを使い慣れている場合、このノードの動作は、グラデーション入力を[法線マップ](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)に変換し、法線マップベクトルで定義される方向にベース入力を変形させる動作に似ていると考えられます。 実際、[ベクターワープ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)でも同じことが可能です。 同様の効果は、[ぼかし(勾配)](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)でも見つけることができます。



## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *フロート* | ワープの強さを設定します。 |
| <b>入力フィルターモード</b> *ブール値* | 入力のサンプリングにニアレストフィルタとバイリニアフィルタのどちらを使用するかをコントロールします。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | カラー画像またはグレースケール画像。 |
| <b>グラデーション入力</b> *グレースケール* | グレースケールの入力画像のグラデーションの勾配によって、出力画像のワープエフェクトが決まります。 |


## 例

*近日公開。*
