---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 「3Dパーリンのノイズ」ノードを使用すると、自然な外観のボリューム感を持つテクスチャを作成するために、3D空間でスムーズなパーリンのノイズパターンを生成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dパーリンノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# 3Dパーリンノイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3d-perlin-noise-01.png){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>3Dパーリンノイズ</b>ノードは、<b>位置マップ</b>の入力に基づいて、3D空間でパーリンノイズを生成します。

このノードは、実際のベイク済みマップではなく、[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)を入力としてテストできます（下図の例を参照）。

</td>
</tr>
</table>

>[!WARNING]
>
> このノイズは、<i>GPUエンジンのみ</i> （<b>Direct3D</b>または<b>OpenGL</b>）で使用することを目的としています。 <b>ツール/エンジンの切り替え…</b>に移動するか、<b>F9</b>キーを押して、目的のエンジンを選択します。

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>反転</b> <i>ブール値</i> | 出力イメージを反転します。 |
| <b>スケール</b> <i>フロート</i> | 3Dパーリンノイズの尺度をコントロールします。 |
| <b>サイズ</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸の3Dパーリンノイズのサイズを制御します。 値が均一でないと、<i>伸縮</i>効果が発生します。 |
| <b>オフセット</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸の3Dパーリンノイズの<i>位置</i>にオフセットを適用します。 |
| <b>ゆがみの適用度</b> <i>フロート</i> | 3Dパーリンノイズに適用される<i>ワープ効果</i>の強さを制御します。 |
| <b>ゆがみスケール乗数</b> <i>フロート</i> | <b>ゆがみの強さ</b>で制御されるワープ効果で使用される<i>変形パターン</i>のスケールを制御します。 |
| <b>ベースライン</b> <i>フロート</i> | <i>オフセット</i>を、3Dパーリンノイズ値の分布の基準<i>輝度</i>値に適用します。 |
| <b>コントラスト</b> <i>フロート</i> | 3Dパーリンノイズのコントラストを調整します。 |
| <b>絶対</b> <i>ブール値</i> | 3Dパーリンノイズの絶対値を使用します。 これにより、値<i>が0.5</i>未満の場合に、値の分布が<i>反転</i>します。 |
| <b>タイリングを有効にする</b> <i>ブール値</i> | 3Dパーリンのノイズを調整して、結果のパターンがX、Y、Z軸で<i>繰り返される</i>ようにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3d-perlin-noise-04.jpg" />
        </td>
    </tr>
</table>
