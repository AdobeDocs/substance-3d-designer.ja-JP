---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: Voronoi Fractalノードを使用して、有機細胞テクスチャを作成するためのフラクタルVoronoiパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ボロノイフラクタル
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# ボロノイフラクタル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi-fractal.resources/voronoifractal.png){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**ボロノイフラクタル**&#x200B;ノードは、*Zダウン投影*&#x200B;を使用して2Dイメージにマップされた&#x200B;*フラクタル* 3Dボロノイノイズを生成します。

このノードは、実際のノードではなく、[Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)を入力としてテストできます（以下の図の例を参照）。

>[!WARNING]
>
> このノイズは、*GPUエンジンのみ* （**Direct**&#x200B;または&#x200B;**OpenGL**）で使用することを目的としています。 **ツール/エンジンの切り替え…**&#x200B;に移動するか、**F9**&#x200B;キーを押して、目的のエンジンを選択します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>反転</b> <i>ブール値</i> | 出力イメージを反転します。 |
| <b>スケール</b> <i>フロート</i> | フラクタルボロノイノイズのスケールを制御します。<br><br>*注意*: **タイリング**&#x200B;が&#x200B;*任意の軸*&#x200B;で有効になっている場合、スケール調整は&#x200B;*ステップ*&#x200B;です。 これは予期される動作です。 |
| <b>サイズ</b> <i>浮動小数点3</i> | **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のフラクタルボロノイノイズのサイズを制御します。 値が均一でないと、*伸縮または収縮*&#x200B;効果が発生します。<br><br>*注意*: *任意の軸*&#x200B;で&#x200B;**タイリング**&#x200B;が有効になっている場合、サイズの調整は&#x200B;*段階的*&#x200B;になります。 これは予期される動作です。 |
| <b>オフセット</b> <i>浮動小数点3</i> | **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のフラクタルボロノイノイズの&#x200B;*position*&#x200B;にオフセットを適用します。 |
| <b>障害</b> <i>浮動小数点3</i> | *ランダムオフセット*&#x200B;の強度は、**X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のノイズの各点に適用されます。 |
| <b>ゆがみの適用度</b> <i>フロート</i> | フラクタルボロノイノイズに適用される&#x200B;*ワープエフェクト*&#x200B;の強度を制御します。 |
| <b>ゆがみスケール乗数</b> <i>フロート</i> | **ゆがみの強さ**&#x200B;で制御されるワープ効果で使用される&#x200B;*変形パターン*&#x200B;のスケールを制御します。 |
| <b>最小レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最小&#x200B;*レベル*&#x200B;です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる&#x200B;*豊富なパターン*&#x200B;になります。 |
| <b>最大レベル</b> <i>整数</i> | フラクタルパターンで使用される繰り返しの最大&#x200B;*レベル*&#x200B;です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる&#x200B;*豊富なパターン*&#x200B;になります。 |
| <b>粗さ</b> <i>フロート</i> | フラクタルパターンでの&#x200B;*バランス*&#x200B;の低い繰り返しと高い繰り返し&#x200B;*レベル*&#x200B;を制御します。<br><br>*注意*: **0**&#x200B;の値を指定すると、*行にない*&#x200B;出力で、その後に他の低い値が続きます。 これは予期される動作です。<br><br>*注意2*：このパラメーターは、**描画モード**&#x200B;パラメーターが&#x200B;*追加*&#x200B;に設定されている場合にのみ使用できます。 |
| <b>空隙性</b> <i>フロート</i> | 適用されたフラクタルパターン&#x200B;*がスペースを塗りつぶす方法*&#x200B;を制御します。 *高い*&#x200B;値を指定すると、パターンのギャップが&#x200B;*少なくなり*、ノイズが&#x200B;*密度が高く*&#x200B;なります。 |
| <b>グローバル不透明度</b> <i>フロート</i> | フラクタルパーリンノイズ値の&#x200B;*範囲*&#x200B;を0から制御します。 |
| <b>角丸曲線</b> <i>フロート</i> | ノイズの各点の周りに&#x200B;*勾配*&#x200B;を丸めて&#x200B;*凸型*&#x200B;にします。<br><br>*注意*: **Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合、このパラメーターは使用できません。 |
| <b>距離スケール</b> <i>フロート</i> | ノイズの各点の周囲の&#x200B;*グラデーションの距離*&#x200B;を調整します。 |
| <b>距離モード</b> <i>整数</i> | ノイズの各点の周囲の&#x200B;*グラデーションの計算*&#x200B;に設定します：<br><br>- *ユークリッド*<br>- *マンハッタン*<br>- *チェビシェフ*<br>- *ミンコフスキー* |
| <b>ミンコフスキー数</b> <i>フロート</i> | ミンコフスキー距離の次数&#x200B;*p*。 距離グラデーションを象限に分割すると、この数は次のように象限に影響します。<br><br>- pは&#x200B;*正確* 1：直線<br>- pは&#x200B;*低* 1より：凹<br>- pは&#x200B;*大* 1より：凸<br><br>対象の値：<br><br>- *1.0*:マンハッタン距離<br>- *2.0*:ユークリッド距離&#x200B;*無限大*:チェビシェフ距離&#x200B;<br><br>*注意*：このパラメーターは、**距離モード**&#x200B;パラメーターが&#x200B;*ミンコフスキー*&#x200B;に設定されている場合にのみ使用できます。<br> |
| <b>描画モード</b> <i>整数</i> | *重なり合うセル*&#x200B;の値を<br><br>- *加算*&#x200B;の間でブレンドする方法を設定します：値の加算<br>- *最大値*: *最大値*&#x200B;の値<br>- *最小値*: *最小値*&#x200B;の値を保持 |
| <b>スタイル</b> <i>整数</i> | フラクタルボロノイノイズのデータ&#x200B;*をレンダリングするノイズを設定します。このメソッドは、空間内の一連の点に基づいて決定されます。<br><br>-* F1 *：空間内の*&#x200B;最も近い点&#x200B;*までの距離<br>-* F2 *：空間内の* 2番目に近い点&#x200B;*までの距離<br>-* F2-F1\*F2*<br>- *f1/F2*<br>- *エッジ*：空間内のノイズの各セル&#x200B;*の間にある*&#x200B;エッジ<br>- *ランダムな色*: *ランダムなフラットな色*&#x200B;を空間内のノイズの各セルに割り当てます&#x200B;**<br>* |
| <b>エッジThickness</b> <i>フロート</i> | フラクタルボロノイノイズのセル間で検出されるエッジのThicknessを調整します。 X、Y、およびZ軸で辺が検出されました。セルの&#x200B;*深度*&#x200B;によっては、一部の太さが他よりも速く増加する場合があります。<br><br>*注意*：このパラメーターは、**Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合にのみ使用できます。 |
| <b>ランダムカラーシードモード</b> <i>整数</i> | セルごとのカラー選択のランダムシードを&#x200B;*取得*&#x200B;するメソッドを設定します： <br><br>- *グローバルランダムシード*:ノードから継承&#x200B;*シードを使用します<br>-*&#x200B;手動シード&#x200B;*:*&#x200B;個別&#x200B;*シードを使用します<br><br>*&#x200B;注意&#x200B;*：このパラメーターは、**Style**&#x200B;パラメーターが*&#x200B;ランダムカラー&#x200B;*に設定されている場合にのみ使用できます。* |
| <b>ランダムカラーシード</b> <i>整数</i> | セルごとのカラー選択に使用する個別のランダムシードです。<br><br>*注意*：このパラメーターは、**Style**&#x200B;パラメーターが&#x200B;*ランダムカラー*&#x200B;に設定されていて、**ランダムカラーシードモード**&#x200B;パラメーターが&#x200B;*手動シード*&#x200B;に設定されている場合にのみ使用できます。 |
| <b>タイリングを有効にする</b> <i>ブール値</i> | フラクタルボロノイノイズを調整して、結果のパターンがX、Y、Z軸で&#x200B;*繰り返す*&#x200B;ようにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/fractal-voronoi-sea.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/fractal-voronoi-scifi-panel.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant4.jpg" />
        </td>
    </tr>
</table>
