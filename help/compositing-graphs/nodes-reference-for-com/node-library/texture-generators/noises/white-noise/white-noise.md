---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: ホワイトノイズノードを使用して、テクスチャのバリエーションやランダムな効果を作成するためのホワイトノイズパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ホワイトノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# ホワイトノイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ホワイトノイズ – アイコン](../../../../../../assets/white_noise_v2.png "ホワイトノイズ – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

異なるヒストグラム形状（均一、ガウス、三角形）をターゲットとする3つの方法のいずれかを使用して、ホワイトノイズを生成します。

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
| <b>ノイズ配布</b> <i>整数</i> | ヒストグラムのシェイプを対象に成分を配分する方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>均一：</i>均一なヒストグラムです。</li> <li data-preserve-html="true"><i>ガウス：</i>ベル曲線に似た正規分布を表すヒストグラムです。</li> <li data-preserve-html="true"><i>三角形：</i>三角形のヒストグラムです。</li> </ul> |
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ホワイトノイズ – 例1](../../../../../../assets/white_noise_v2_1.png "ホワイトノイズ – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ホワイトノイズ – 例2](../../../../../../assets/white_noise_v2_speed0.6_aniso0.gif "ホワイトノイズ – 例2"){zoomable="yes"}

</td>
</tr>
</table>
