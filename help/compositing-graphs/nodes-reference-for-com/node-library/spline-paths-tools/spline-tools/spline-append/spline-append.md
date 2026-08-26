---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: '[スプライン追加]ノードを使用して、複数のスプラインを一緒に追加し、長い連続パスを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン追加
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# スプライン追加

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-append-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

スプラインはリストとしてパッケージ化されます。 このノードは、入力スプラインのリスト(set #2)を既存のリスト(set #1)に追加します。

リストの順序は保持されます。つまり、リストA-B-CにリストD-E-Fを追加すると、リストA-B-C-D-E-Fになります。

</td>
</tr>
</table>

>[!TIP]
>
> スプラインを追加する順番は、[スプラインの散乱](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md)、[スプラインブリッジ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md)ノードなど、他のノードでこの順番が考慮されるため、注意してください。

## 入力コネクタ

<b>プレビュー#1</b> *グレースケール*&#x200B;入力スプラインの最初のセットをグレースケールイメージとしてプレビューします。

<b>スプライン#1座標</b> *色*&#x200B;入力スプラインの最初のセットの座標です。カラー画像のRGBAチャンネルでエンコードされます。\
<b>R</b> - X位置\
<b>G</b> - Y位置\
<b>B</b> -Height\
<b>A</b> – パックされたデータ：\
*記号：スプラインが閉じている（負）か、開いている（正）;\
*絶対値：Thickness + 1。

<b>スプライン#1データ</b> *色*&#x200B;カラー画像のRGBAチャンネルでエンコードされた入力スプラインの最初のセットの追加データ。\
<b>R</b> – 接線X\
<b>G</b> – 接線Y\
<b>B</b> – 未使用\
<b>A</b> – 未使用

<b>スプライン#1量</b> *整数*&#x200B;最初のセット内の入力スプラインの数です。

<b>プレビュー#2</b> *グレースケール*&#x200B;入力スプラインの2番目のセットのプレビューをグレースケールイメージとして表示します。

<b>スプライン#2座標</b> *色*&#x200B;入力スプラインの2番目のセットの座標です。カラー画像のRGBAチャンネルでエンコードされています。\
<b>R</b> - X位置\
<b>G</b> - Y位置\
<b>B</b> -Height\
<b>A</b> – パックされたデータ：\
*記号：スプラインが閉じている（負）か、開いている（正）;\
*絶対値：Thickness + 1。

<b>スプライン#2データ</b> *色*&#x200B;カラー画像のRGBAチャンネルでエンコードされた2番目の入力スプラインセットの追加データです。\
<b>R</b> – 接線X\
<b>G</b> – 接線Y\
<b>B</b> – 未使用\
<b>A</b> – 未使用

<b>スプライン#2量</b> *整数* 2番目のセット内の入力スプラインの数です。

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

<b>スプラインの方向#1反転&#x200B;</b>*ブール値*&#x200B;最初のセットのスプラインの方向を反転します。

<b>スプライン#2方向を反転&#x200B;</b>*ブール値* 2番目のセットのスプラインの方向を反転します。

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

![ノードの例1](../../../../../../assets/SplineAppend-Demo.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineAppend-Graph.jpg "ノードの例2")

</td>
</tr>
</table>

![ノードデモ](../../../../../../assets/SplineAppend-Demo2.gif "ノードデモ")
