---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-1.html"
breadcrumb-title: ''
description: 「ガウスのスポット1」ノードを使用して、ガウスのスポットパターンを生成し、自然なテクスチャのバリエーションとディテールを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ガウス斑1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# ガウス斑1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ガウスのスポット1 – アイコン](gaussian-spots-1.resources/gaussian-spots-1-01.png "ガウスのスポット1 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

滑らかな<b>ガウス斑</b>のノイズのバリエーションです。\
[ガウスノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)ノードに基づき、グラデーションを狭くします。

関連項目： [ガウススポット2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 生成されるノイズをグレースケールビットマップとして表します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>整数</i> | ノイズタイルの生成に使用するグリッドの区画。    値を大きくすると、描かれるタイルの数が増え、ノイズが高くなります。 |
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>異方性の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの方向の範囲を制御します。値を大きくすると、より狭く、より明確な方向になります。    方向は、<b>Disorder異方性角度</b>パラメーターで制御されます。 |
| <b>anisotropy angleの乱れ</b> <i>フロート</i> | <b>Disorder 異方性</b>パラメーターが0ではない場合に、<b>Disorder</b>パラメーターによって適用されるディスプレイスメントの向きを制御します。 |
| <b>タイルのオフセット</b> <i>浮動小数点2</i> | ノイズのレンダリングに使用される無限平面の部分の位置を制御します。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ガウスのスポット1 – 例1](gaussian-spots-1.resources/gaussian-spots-1-02.png "ガウスのスポット1 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ガウスのスポット1 – 例2](gaussian-spots-1.resources/gaussian-spots-1-03.gif "ガウスのスポット1 – 例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ガウスのスポット1 – 例3](gaussian-spots-1.resources/gaussian-spots-1-04.gif "ガウスのスポット1 – 例3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ガウスのスポット1 – 例4](gaussian-spots-1.resources/gaussian-spots-1-05.gif "ガウスのスポット1 – 例4"){zoomable="yes"}

</td>
</tr>
</table>
