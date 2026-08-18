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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---


# スプラインサンプルThickness

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-sample-thickness-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力Thicknessマップを入力スプラインにマッピングして、入力スプラインのThicknessを変更します。

マップされたHeightマップの効果は、描画モードとその効果の不透明度を変更することで調整できます。

</td>
</tr>
</table>

## 入力コネクタ

<b>プレビュー</b> *グレースケール*&#x200B;入力スプラインをグレースケールイメージとしてプレビューします。

<b>スプライン座標</b> *色*&#x200B;入力スプラインの点の座標は、カラー画像のRGBAチャンネルでエンコードされています：\
<b> R</b> - X位置\
<b> G</b> - Y位置\
<b> B</b> - Height\
    <b>A</b> – パックされたデータ：\
        *記号：スプラインが閉じている（負）か、開いている（正）;\
        *絶対値：Thickness + 1。

<b>スプラインデータ</b> *色*&#x200B;カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データです。\
<b> R</b> – 接線X\
<b> G</b> – 接線Y\
<b> B</b> – 未使用\
<b> A</b> – 未使用

<b>スプラインの量</b> *整数*&#x200B;入力スプラインの数です。

<b>Thicknessマップ</b> *グレースケール*&#x200B;入力スプラインのThicknessを変えるために使用される入力グレースケールイメージです。

## 出力コネクタ

<b>プレビュー</b> *グレースケール*&#x200B;出力スプラインをグレースケールイメージとしてプレビューします。

<b>スプライン座標</b> *色*&#x200B;出力スプラインの点の座標は、色画像のRGBAチャンネルでエンコードされます。\
    <b>R</b> - X位置\
    <b>G</b> - Y位置\
    <b>B</b> -Height\
    <b>A</b> – パックされたデータ：\
        *記号：スプラインが閉じている（負）か、開いている（正）;\
        *絶対値：Thickness + 1。

<b>スプラインデータ</b> *カラー*&#x200B;カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。\
    <b>R</b> – 接線X\
    <b>G</b> – 接線Y\
    <b>B</b> – 未使用\
    <b>A</b> – 未使用

<b>スプラインの量</b> *整数*&#x200B;出力スプラインの数です。

## パラメーター

<b>サンプリングモード</b> *整数* Thicknessマップの値をスプラインにマッピングする方法：\
*– テクスチャ空間*：値は、テクスチャのUV座標を使用してテクスチャに配置されるスプラインに適用されます。 これによって、スプラインに値が「その場で」適用されます。\
*– スプラインに沿った水平*：値は、エンコードされたスプラインの座標に直接適用されます（「スプライン座標」の入力を参照）。各行は上から下に異なるスプラインに適用されます。\
*– 時間 スプラインに沿って（ランダム偏差） オフセットX)*：値は、エンコードされたスプラインの座標に直接（スプライン座標の入力を参照）適用され、各スプラインのスケールマップ内のランダムな水平オフセット（スプライン座標の各行）を伴います。\
*– 時間 スプラインに沿って（ランダム偏差） オフセットY)*：値は、エンコードされたスプラインの座標に直接適用され（スプライン座標の入力を参照）、各スプラインのスケールマップ内のランダムな垂直オフセット（スプライン座標の各行）を伴います。

<b>不透明度</b> *浮動小数* Thicknessマップ入力のスプラインのThicknessに対する影響度の乗数です。<b></b>

<b>描画モード</b> *整数* Thicknessマップのデータと入力スプラインの<span id="_Hlk135820484"></span>Thicknessを合成する方法：\
*– コピー*:スプラインのThicknessをHeightマップ値で上書きします。\
*- Add*: Thicknessマップの値をスプラインのThicknessに追加します。\
*– 削除*: Thicknessマップの値をスプラインのThicknessに削除します。\
*- Multiply*:スプラインのThicknessに対してThicknessマップの値を乗算します。

+++プレビュー
<b>セグメント数</b> *整数*&#x200B;プレビュー出力でスプラインの視覚化を描画するために使用するセグメントの数を調整します。\
値が大きいほど、線は滑らかになります。

<b>方向ヘルパーの表示</b> *ブール値*&#x200B;プレビュー出力のスプラインの始点に点を表示し、終点に矢印を表示します。

<b>Thicknessの封筒を表示</b> *ブール値*\
スプラインのThicknessのエッジに追加の線分を表示します。

<b>Thickness (px)</b> *フロート*&#x200B;プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。

+++

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
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

![ノードの例1](../../../../../../assets/SplineSampleThickness-Variant1-After1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineSampleThickness-Demo.gif "ノードの例2")

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
