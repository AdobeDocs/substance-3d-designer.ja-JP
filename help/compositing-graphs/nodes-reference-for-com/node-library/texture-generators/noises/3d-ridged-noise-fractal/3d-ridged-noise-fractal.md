---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: 3D空間で山のようなノイズを作成するためのリッジフラクタルノイズパターンを作成するには、「3Dリッジフラクタル」ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dリッジノイズフラクタル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 3Dリッジノイズフラクタル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-01.png){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>3Dブリッジノイズフラクタル</b>ノードは、<b>位置マップ</b>の入力に基づいて、3D空間で<i>フラクタル</i>ブリッジノイズを生成します。

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
| <b>スケール</b> <i>フロート</i> | フラクタル3Dリッジノイズのスケールを制御します。 |
| <b>サイズ</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸のフラクタル3D浮彫りノイズのサイズを制御します。 値が均一でないと、<i>伸縮または収縮</i>効果が発生します。 |
| <b>オフセット</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸のフラクタル3D浮彫りノイズの<i>位置</i>にオフセットを適用します。 |
| <b>ゆがみの適用度</b> <i>フロート</i> | フラクタル3Dリッジノイズに適用される<i>ワープ効果</i>の強さを制御します。 |
| <b>ゆがみスケール乗数</b> <i>フロート</i> | <b>ゆがみの強さ</b>で制御されるワープ効果で使用される<i>変形パターン</i>のスケールを制御します。 |
| <b>最小レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最小<i>レベル</i>です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる<i>豊富なパターン</i>になります。 |
| <b>最大レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最大<i>レベル</i>です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる<i>豊富なパターン</i>になります。 |
| <b>粗さ</b> <i>フロート</i> | フラクタルパターンでの<i>バランス</i>の低い繰り返しと高い繰り返し<i>レベル</i>を制御します。<br><br><i>注意</i>: <b>0</b>の値を指定すると、<i>行にない</i>出力で、その後に他の低い値が続きます。 これは予期される動作です。 |
| <b>空隙性</b> <i>フロート</i> | 適用されたフラクタルパターン<i>がスペースを塗りつぶす方法</i>を制御します。 <i>高い</i>値を指定すると、パターンのギャップが<i>少なくなり</i>、ノイズが<i>密度が高く</i>なります。 |
| <b>グローバル不透明度</b> <i>フロート</i> | フラクタル3Dリッジノイズ値の<i>範囲</i>を制御します。<b>ベースライン</b>値<i>前後</i> |
| <b>ベースライン</b> <i>フロート</i> | <i>オフセット</i>を、3Dリッジノイズ値の分布の基準<i>輝度</i>値に適用します。 |
| <b>コントラスト</b> <i>フロート</i> | 3Dブリッジノイズのコントラストを補正します。 |
| <b>タイリングを有効にする</b> <i>ブール値</i> | 3D仕上げのノイズを調整して、結果のパターン<i>がX、Y、Z軸に</i>繰り返されるようにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3d-ridged-noise-fractal-03.jpg" />
        </td>
    </tr>
</table>
