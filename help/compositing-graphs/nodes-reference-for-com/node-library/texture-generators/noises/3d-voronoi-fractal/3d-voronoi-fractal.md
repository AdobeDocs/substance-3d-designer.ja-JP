---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: 3D Voronoi Fractalノードを使用して、ボリュームテクスチャの3Dポジションに基づいてフラクタルボロノイパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 3D Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal.png){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>3D Voronoi Fractal</b>ノードは、<b>位置マップ</b>の入力に基づいて、3D空間で<i>フラクタル</i>ボロノイノイズを発生させます。

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
| <b>スケール</b> <i>フロート</i> | フラクタル3Dボロノイノイズのスケールを制御します。<br><br><i>注意</i>: <b>タイリング</b>が<i>任意の軸</i>で有効になっている場合、スケール調整は<i>ステップ</i>です。 これは予期される動作です。 |
| <b>サイズ</b> <i>浮動小数点3</i> | フラクタル3Dボロノイノイズの<b>X</b>、<b>Y</b>および<b>Z</b>軸のサイズを制御します。 値が均一でないと、<i>伸縮または収縮</i>効果が発生します。<br><br><i>注意</i>: <i>任意の軸</i>で<b>タイリング</b>が有効になっている場合、サイズの調整は<i>段階的</i>になります。 これは予期される動作です。 |
| <b>オフセット</b> <i>浮動小数点3</i> | <b>X</b>、<b>Y</b>および<b>Z</b>軸のフラクタル3Dボロノイノイズの<i>位置</i>にオフセットを適用します。 |
| <b>障害</b> <i>浮動小数点3</i> | <i>ランダムオフセット</i>の強さは、<b>X</b>、<b>Y</b>および<b>Z</b>軸のノイズの各ポイントに適用されます。 |
| <b>ゆがみの適用度</b> <i>浮動小数</i> | フラクタル3Dボロノイノイズに適用される<i>ワープ効果</i>の強さを制御します。 |
| <b>ゆがみスケール乗数</b> <i>浮動小数</i> | <b>ゆがみの強さ</b>で制御されるワープ効果で使用される<i>変形パターン</i>のスケールを制御します。 |
| <b>最小レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最小<i>レベル</i>です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる<i>豊富なパターン</i>になります。 |
| <b>最大レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最大<i>レベル</i>です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる<i>豊富なパターン</i>になります。 |
| <b>ラフネス</b> <i>浮動小数</i> | フラクタルパターンでの<i>バランス</i>の低い繰り返しと高い繰り返し<i>レベル</i>を制御します。<br><br><i>注意</i>: <b>0</b>の値を指定すると、<i>行にない</i>出力で、その後に他の低い値が続きます。 これは予期される動作です。<br><br><i>注意2</i>：このパラメーターは、<b>ブレンドモード</b>パラメーターが<i>追加</i>に設定されている場合にのみ使用できます。 |
| <b>空隙性</b> <i>浮動小数</i> | 適用されたフラクタルパターン<i>がスペースを塗りつぶす方法</i>を制御します。 <i>高い</i>値を指定すると、パターンのギャップが<i>少なくなり</i>ノイズが<i>密になります。</i> |
| <b>グローバル不透明度</b> <i>フロート</i> | フラクタル3Dパーリンノイズ値の<i>範囲</i>を0から制御します。 |
| <b>角丸曲線</b> <i>フロート</i> | ノイズの各点の周りに<i>勾配</i>を丸めて<i>凸型</i>にします。<br><br><i>注意</i>: <b>Style</b>パラメーターが<i>Edge</i>に設定されている場合、このパラメーターは使用できません。 |
| <b>距離スケール</b> <i>フロート</i> | ノイズの各点の周囲の<i>グラデーションの距離</i>を調整します。 |
| <b>距離モード</b> <i>整数</i> | ノイズの各点の周囲の<i>グラデーションの計算</i>に設定します：<br><br>- <i>ユークリッド</i><br>- <i>マンハッタン</i><br>- <i>チェビシェフ</i><br>- <i>ミンコフスキー</i> |
| <b>ミンコフスキー数</b> <i>フロート</i> | ミンコフスキー距離の次数<i>p</i>。 距離グラデーションを象限に分割すると、この数は次のように象限に影響します。<br><br>- pは<i>正確</i> 1：直線<br>- pは<i>低</i> 1より：凹<br>- pは<i>大</i> 1より：凸<br><br>対象の値：<br>- <i>1.0</i>:マンハッタン距離<br>- <i>2.0</i>:ユークリッド距離<i>無限大</i>:チェビシェフ距離<br><br><i>注意</i>：このパラメーターは、<b>距離モード</b>パラメーターが<i>ミンコフスキー</i>に設定されている場合にのみ使用できます。<br> |
| <b>描画モード</b> <i>整数</i> | 3D空間で<i>重なり合うセル</i>の値をブレンドする方法を設定します：<br><br>- <i>追加</i>：値を追加します<br>- <i>最大</i>: <i>最高</i>の値を保持します<br>- <i>最小</i>: <i>最低</i>の値を保持します |
| <b>スタイル</b> <i>整数</i> | フラクタル3Dボロノイノイズのデータ</i>をレンダリングするノイズを設定します。このメソッドは、3D空間の一連の点に基づいて決定されます：<br><br>- <i>F1</i>: 3D空間の<i>最も近い点</i>までの距離<br>- <i>F2</i>: 3D空間の<br>- <i>F2-F1</i><br>- <i>F1\*F f2</i><br>- <i>F1/F2</i><br>- <i>エッジ</i>: 3Dスペースのノイズの各セル</i>の間の<i>エッジ<br>- <i>ランダム色</i>: <i>ランダムなフラット色</i>を3Dスペースのノイズの各セルに割り当てます<i><i></i> |
| <b>エッジThickness</b> <i>フロート</i> | フラクタル3Dボロノイノイズのセル間で検出されるエッジのThicknessを調整します。 X、Y、およびZ軸で辺が検出されました。セルの<i>深度</i>によっては、一部の太さが他よりも速く増加する場合があります。<br><br><i>注意</i>：このパラメーターは、<b>Style</b>パラメーターが<i>Edge</i>に設定されている場合にのみ使用できます。 |
| <b>タイリングを有効にする</b> <i>ブール値</i> | フラクタル3Dボロノイノイズを調整して、結果のパターンがX、Y、Z軸に<i>繰り返す</i>ようにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant4.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvoronoifractal-variant3.jpg" />
        </td>
    </tr>
</table>
