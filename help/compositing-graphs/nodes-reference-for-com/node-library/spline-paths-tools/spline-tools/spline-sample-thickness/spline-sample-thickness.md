---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: '[スプラインサンプル]Thicknessノードを使用して、手続き型の効果を得るためにスプラインに沿ってThickness値をサンプリングします。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインサンプルThickness
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# スプラインサンプルThickness

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-sample-thickness.resources/spline-sample-thickness-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力Thicknessマップを入力スプラインにマッピングして、入力スプラインのThicknessを変更します。

マップされたHeightマップの効果は、描画モードとその効果の不透明度を変更することで調整できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |
| <b>Thicknessマップ</b> <i>グレースケール</i> | 入力スプラインのThicknessを変えるために使用される入力グレースケールイメージ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | 出力スプラインの座標がカラー画像のRGBAチャンネルにエンコードされました。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>サンプリングモード</b> <i>整数</i> | 厚みマップの値をスプラインにマッピングする方式：<br>- <i>テクスチャ空間</i>：値は、テクスチャのUV座標を使用してテクスチャに配置する場合にスプラインに適用されます。 これにより、値がスプラインに「その場で」適用されます。<br>- <i>スプラインに沿った水平</i>：値は、エンコードされたスプラインの座標に直接適用されます（「スプライン座標」の入力を参照）。ここで、各行は上から下まで異なるスプラインに適用されます。<br>- <i>Hor。 スプラインに沿って（ランダム偏差） オフセットX)</i>：値は、エンコードされたスプラインの座標に直接適用され（スプライン座標の入力を参照）、各スプラインのスケールマップ内のランダムな水平オフセット（スプライン座標の各行）で使用されます。<br>- <i>水平 スプラインに沿って（ランダム偏差） オフセットY)</i>：値は、エンコードされたスプラインの座標に直接適用され（スプライン座標の入力を参照）、各スプラインのスケールマップ内のランダムな垂直オフセット（スプライン座標の各行）を伴います。 |
| <b>不透明度</b> <i>浮動小数</i> | 厚みマップ入力がスプラインのThicknessに与える影響の強さを表す乗数。 |
| <b>描画モード</b> <i>整数</i> | 厚みマップのデータと入力スプラインの<span id="_Hlk135820484"></span>Thicknessをブレンドする方式：<br>- <i>コピー</i>:スプラインのThicknessを高さマップ値でオーバーライドします；<br>- <i>追加</i>:スプラインのThicknessに厚みマップ値を加えます；<br>- <i>減算</i>: 厚みマップ値をスプラインのThicknessに減算します；<br>- <i>乗算</i>:スプラインのThicknessに対して厚みマップ値を乗算します。 |
| <b>プレビュー</b> |  |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインの視覚化に使用するセグメントの数を調整します。<br>値を大きくすると、より滑らかな線になります。 |
| <b>方向のヘルパーを表示</b> <i>ブーリアン</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブーリアン</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>Thickness (px)</b> <i>浮動小数</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](spline-sample-thickness.resources/SplineSampleThickness-Variant1-After1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-sample-thickness.resources/SplineSampleThickness-Demo.gif "ノードの例2")

</td>
</tr>
</table>
