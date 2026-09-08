---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: フラクタル和ベースノードを使用して、複雑な有機的テクスチャを作成するためのベースフラクタルノイズパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: フラクタル和ベース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# フラクタル和ベース

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![フラクタル和ベース – アイコン](../../../../../../assets/fractal_sum_base.png "フラクタル和ベース – アイコン"){width="200px"}

<b>In:</b>テクスチャジェネレーター>ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

オクターブの範囲とバランスを調整できる、カスタマイズ可能なフラクタルノイズです。

<b>フラクタル和</b>ファミリのノイズはすべて、このノードに基づいています。

参照： [フラクタル和 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md)、[フラクタル和 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md)、[フラクタル和 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)、[フラクタル和 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>粗さ</b> <i>フロート</i> | ノイズのバランスがオクターブになります。    値を大きくすると、高い周波数のオクターブがより見やすくなります。 |
| <b>分 レベル</b> <i>整数</i> | ノイズで使用される最小オクターブです。    値が大きいほど、ノイズ周波数は高くなります。 |
| <b>最大 レベル</b> <i>整数</i> | ノイズで使用される最大オクターブです。    値が大きいほど、ノイズ周波数は高くなります。 |
| <b>障害</b> <i>フロート</i> | ノイズの成分を置き換えます。    これを使用してノイズをアニメートできます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、ノイズをアニメートするときのディスプレイスメント速度をコントロールできます。 |
| <b>コントラスト</b> <i>フロート</i> | 最終結果のコントラスト。 |
| <b>グローバル不透明度</b> <i>フロート</i> | 最終的な結果では、ノイズの不透明度が一緒に追加されます。    値を大きくすると、領域が白く焼ける場合があります。 |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたタイルを正方形に保ち、ノイズの生成を画像の境界まで拡張します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![フラクタル和ベース – 例1](../../../../../../assets/fractal_sum_base_1.png "フラクタル和ベース – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![フラクタル和ベース – 例2](../../../../../../assets/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "フラクタル和ベース – 例2"){zoomable="yes"}

</td>
</tr>
</table>
