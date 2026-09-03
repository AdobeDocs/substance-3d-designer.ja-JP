---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# スプライン追加

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-append.resources/spline-append-01.png "ノードアイコン")

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

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー#1</b> <i>グレースケール</i> | 最初の入力スプラインセットのプレビューをグレースケールイメージとして表示します。 |
| <b>スプライン#1座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの最初のセットの座標です。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプライン#1データ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの最初のセットの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプライン#1量</b> <i>整数</i> | 最初のセット内の入力スプラインの数。 |
| <b>プレビュー#2</b> <i>グレースケール</i> | 2番目の入力スプラインのセットのプレビューをグレースケールイメージとして表示します。 |
| <b>スプライン#2座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの2番目のセットの座標です。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプライン#2データ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた2番目の入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプライン#2量</b> <i>整数</i> | 2番目のセット内の入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | 出力スプラインの座標がカラー画像のRGBAチャンネルにエンコードされました。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スプライン#1方向を反転</b> <i>ブール値</i> | 最初のセットのスプラインの方向を反転します。 |
| <b>スプライン#2方向を反転</b> <i>ブール値</i> | 2番目のセットのスプラインの方向を反転します。 |
| <b>プレビュー</b> |  |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインのビジュアライゼーションを描画するために使用するセグメントの数を調整します。 値が大きいほど、線は滑らかになります。 |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>Thickness (px)</b> <i>フロート</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](spline-append.resources/spline-append-02.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-append.resources/spline-append-03.jpg "ノードの例2")

</td>
</tr>
</table>

![ノードデモ](spline-append.resources/spline-append-04.gif "ノードデモ")
