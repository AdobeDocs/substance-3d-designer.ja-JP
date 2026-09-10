---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: 3D Voronoiノードを使用すると、3Dワールドポジションに基づいてボロノイパターンを生成し、体積細胞テクスチャを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3dvoronoi.png){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>3D Voronoi</b>ノードは、<b>Position Map</b>の入力に基づいて、3D空間でVoronoi ノイズを生成します。

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
| <b>スケール</b> <i>フロート</i> | 3Dボロノイノイズのスケールを制御します。<br><br><i>注意</i>: <b>タイリング</b>が<i>任意の軸</i>で有効になっている場合、スケール調整は<i>段階的</i>です。 これは予期される動作です。 |
| <b>サイズ</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸の3Dボロノイノイズのサイズを制御します。 値が均一でないと、<i>伸縮または収縮</i>効果が発生します。<br><br><i>注意</i>: <i>任意の軸</i>で<b>タイリング</b>が有効になっている場合、サイズの調整は<i>段階的</i>になります。 これは予期される動作です。 |
| <b>オフセット</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸の3D Voronoiノイズの<i>position</i>にオフセットを適用します。 |
| <b>障害</b> <i>浮動小数点3</i> | <i>ランダムオフセット</i>の強度は、<b>X</b>、<b>Y</b>および<b>Z</b>軸のノイズの各点に適用されます。 |
| <b>ゆがみの適用度</b> <i>フロート</i> | 3Dボロノイノイズに適用される<i>ワープ効果</i>の強さを制御します。 |
| <b>ゆがみスケール乗数</b> <i>フロート</i> | <b>ゆがみの強さ</b>で制御されるワープ効果で使用される<i>変形パターン</i>のスケールを制御します。 |
| <b>角丸曲線</b> <i>フロート</i> | ノイズの各点の周りに<i>勾配</i>を丸めて<i>凸型</i>にします。<br><br><i>注意</i>: <b>Style</b>パラメーターが<i>Edge</i>に設定されている場合、このパラメーターは使用できません。 |
| <b>距離スケール</b> <i>フロート</i> | ノイズの各点の周囲の<i>グラデーションの距離</i>を調整します。 |
| <b>距離モード</b> <i>整数</i> | ノイズの各点の周囲の<i>グラデーションの計算</i>に設定します：<br><br>- <i>ユークリッド</i><br>- <i>マンハッタン</i><br>- <i>チェビシェフ</i><br>- <i>ミンコフスキー</i> |
| <b>ミンコフスキー数</b> <i>フロート</i> | ミンコフスキー距離の次数<i>p</i>。 距離グラデーションを象限に分割すると、この数は次のように象限に影響します。<br><br>- pは<i>正確</i> 1：直線<br>- pは<i>低</i> 1より：凹<br>- pは<i>大</i> 1より：凸<br><br>対象の値：<br>- <i>1.0</i>:マンハッタン距離<br>- <i>2.0</i>:ユークリッド距離<i>無限大</i>:チェビシェフ距離<br><br><i>注意</i>：このパラメーターは、<b>距離モード</b>パラメーターが<i>ミンコフスキー</i>に設定されている場合にのみ使用できます。<br> |
| <b>スタイル</b> <i>整数</i> | 3Dボロノイノイズのデータ</i>をレンダリングするノイズを設定します。このメソッドは、3Dスペースの一連の点に基づいています：<br><br>- <i>F1</i>: 3Dスペースの<i>最も近い点</i>までの距離<br>- <i>F2</i>: 3Dスペースの<i>2番目に近い点</i>までの距離<br>- <i>F2-F1\* f2</i><br>- <i>F1/F2</i><br>- <i>エッジ</i>: 3Dスペースのノイズの各セル</i>の間の<i>エッジ<br>- <i>ランダム色</i>: <i>ランダムなフラット色</i>を3Dスペースのノイズの各セルに割り当てます<i></i><br><i> |
| <b>エッジThickness</b> <i>フロート</i> | 3Dボロノイノイズのセル間で検出されるエッジのThicknessを調整します。 X、Y、およびZ軸で辺が検出されました。セルの<i>深度</i>によっては、一部の太さが他よりも速く増加する場合があります。<br><br><i>注意</i>：このパラメーターは、<b>Style</b>パラメーターが<i>Edge</i>に設定されている場合にのみ使用できます。 |
| <b>タイリングを有効にする</b> <i>ブール値</i> | 3Dボロノイノイズを調整して、結果のパターンがX、Y、Z軸に<i>繰り返す</i>ようにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant2.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant6.jpg" />
        </td>
    </tr>
</table>
