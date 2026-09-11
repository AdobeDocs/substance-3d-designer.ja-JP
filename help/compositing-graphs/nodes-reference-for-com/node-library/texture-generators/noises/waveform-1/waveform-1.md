---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: 波形1ノードを使用して、有機的なテクスチャやプロシージャルなバリエーションを作成するための波形パターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 波形1
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# 波形1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![波形1 – アイコン](waveform-1.resources/waveform_01_v2.png "波形1 – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ユーザーが選択したパターンの水平方向の配置で、波形に似たシェイプにスタックされます。

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
| <b>サンプル</b> <i>整数</i> | 波形を描画するためにX軸に沿って配置されるパターンの量。値を小さくすると、段階的な外観になります。 |
| <b>関数</b> <i>整数</i> | 波形の描画に使用する関数。   これにより、各サンプルに配置されるパターンの垂直方向のサイズが制御されます。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>値のノイズ：</i>値のランダム分布</li> <li data-preserve-html="true"><i>コサイン：</i>値はコサイン関数の進行に従います</li> <li data-preserve-html="true"><i>カスタム関数：</i>ユーザーが作成した関数を使用して値を制御します</li> </ul> |
| <b>カスタム関数</b> <i>フロート</i>   *&#39;Function&#39;が&#39;Custom function&#39;に設定されている場合に使用可能* | 各サンプルに配置されたパターンの垂直サイズを計算します。   使用可能な変数：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) X軸上のパターンの位置です。 これは、パターンの選択に使用できます。</li> </ul> |
| <b>粗さ</b> <i>フロート</i> | クリーンで滑らかな波形を、より粗く均等に分布した波形で補間します。    これは、ホワイトノイズに対するクリーンな信号と考えることができます。 |
| <b>スケール</b> <i>整数</i> | 画像に表示される波形の水平方向の範囲です。 |
| <b>最小振幅</b> <i>フロート</i> | 波形の最小値（またはThickness）。 |
| <b>最大振幅</b> <i>フロート</i> | 波形の最大値（またはThickness）。 |
| <b>ノイズ</b> <i>フロート</i> | 波形にノイズを適用します。ノイズは、垂直スパンからランダムに差し引かれます。 |
| <b>位置</b> <i>整数</i> | 画像内での波形の位置です。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>中央：</i>原点は画像の垂直方向の中心です</li> <li data-preserve-html="true"><i>下：</i>原点は画像の下部です</li> </ul> |
| <b>パターン</b> <i>整数</i> | 波形の各サンプルに配置されるパターン。 |
| <b>パターンバリエーション</b> <i>フロート</i> | 一部のパターンに使用できる追加の調整。 |
| <b>障害</b> <i>フロート</i> | 波形値を置き換えます。    これを使用してアニメーション化できます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、波形をアニメーション化するときのディスプレイスメント速度を制御できます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![波形1 – 例1](waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif "波形1 – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
