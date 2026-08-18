---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: '[異方性反射ノイズ]ノードを使用して、異方性反射テクスチャ効果を作成するための方向性ノイズパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 異方性ノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# 異方性ノイズ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![異方性ノイズ – アイコン](../../../../../../assets/anisotropic_noise_v2.png "異方性ノイズ – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ランダムな色の帯が互いにフェードする水平または垂直のスタック。

ストリップの量は、トランジションのSmoothnessと同様に調整可能です。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 出力

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## 出力

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 生成されるノイズをグレースケールビットマップとして表します。 |

## パラメーター

|  |  |
| --- | --- |
| <b>X量</b>整数 | X軸上のストリップの量。 |
| <b>Y量</b>整数 | Y軸上のストリップの量。 |
| <b>解像度ごとのY量</b>ブール値 | Trueの場合、Y軸上のストリップの数は、その軸上のイメージサイズと等しくなります。 |
| <b>回転</b>ブール値 | ノイズを90度回転します。 |
| <b>Smoothness</b>浮動小数点 | ストリップ間のフェードの量。0はフェードせず、1はストリップ全体でフェードします。 |
| <b>Smoothness補間</b>浮動小数点 | ストリップをフェードするために適用される2つの補間方法の重み付けです。0はリニアで、1はガウスです。 |
| <b>障害</b>浮動小数点 | ノイズの成分を置き換えます。   これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b>浮動小数点 | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。   これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>非正方形の展開</b>ブール値 | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![異方性ノイズ – 例1](../../../../../../assets/anisotropic_noise_v2_1.png "異方性ノイズ – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![異方性ノイズ – 例2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "異方性ノイズ – 例2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
