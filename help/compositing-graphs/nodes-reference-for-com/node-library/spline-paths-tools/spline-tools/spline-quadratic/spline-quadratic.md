---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: スプライン二次ノードを使用して、3つの制御点を持つ滑らかな二次スプラインを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン（二次）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# スプライン（二次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![スプライン（二次）:アイコン](spline-quadratic.resources/spline-quadratic-icon.png "スプライン（二次）:アイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つの点<b>p1</b>と<b>p3</b>の間の任意の位置に1つのスプラインを生成します。

スプラインの軌道は、<b>p1</b>の「アウト」接線と、<b>p3</b>の「イン」接線によって制御されます。*両方*&#x200B;は、単一の点<b>p3</b>によって制御されます。

スプラインによって形成される円弧のスパンは&#x200B;*調整可能*&#x200B;です。そのため、端からの軌道の一部がまっすぐに残ります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ：<br><b>R</b> - 正接 X<br><b>G</b> - 正接 Y<br><b>B</b> - 正接 Z<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）または開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ：<br><b>R</b> - 正接 X<br><b>G</b> - 正接 Y<br><b>B</b> - 正接 Z<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。 |
| <b>均一な分布</b> <i>ブール値</i> | <i>True</i>の場合、スプラインの点は始点から終点まで等間隔になります。 |
| <b>入力スプラインを追加</b> <i>ブール値</i> | 生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。 これは均一な分布にも影響を与えます。 |
| <b>Smoothness</b> <i>フロート</i> | スプラインによって形成される円弧</i>の<i>スパンを調整します。ここで、1はスプラインの全長が弧を描くことを意味し、0はスプラインが完全にまっすぐであることを意味します。 円弧は、スプラインに沿って点<b>p3</b>から端まで進行します。 |
| <b>Height</b> |  |
| <b>Heightの開始</b> <i>フロート</i> | <b>p1</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。<br>これは<b>p1</b>のスプラインのHeightに影響します。 |
| <b>エンドHeight</b> <i>フロート</i> | <b>p3</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。<br>これは<b>p3</b>のスプラインのThicknessに影響します。 |
| <b>自動接線Height</b> <i>ブール値</i> | <b>p3</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。<br>これは<b>p3</b>のスプラインのThicknessに影響します。 |
| <b>接線Height</b> <i>フロート</i> | <b>p2</b>点で制御される正接によって駆動されるHeightを調整します。<br>これは、<b>p1</b>から引き離され、<b>p3</b>に入る際に、スプラインに沿ったHeightに影響を与えます。<br><i>注意：</i>このパラメーターは、<b>自動正接Height</b>が&#39;False&#39;に設定されている場合にのみ使用できます。 |
| <b>Thickness</b> |  |
| <b>Thicknessの開始</b> <i>フロート</i> | <b>p1</b>ポイントのThicknessを調整します。 これは、<b>p1</b>のスプラインのThicknessに影響を与えます。<br><i>注：</i> Thicknessは、特定のスプラインノードによって使用されます。 |
| <b>エンドThickness</b> <i>フロート</i> | <b>p3</b>ポイントのThicknessを調整します。 これは、<b>p3</b>のスプラインのThicknessに影響を与えます。<br><i>注：</i> Thicknessは、特定のスプラインノードによって使用されます。 |
| <b>自動接線Thickness</b> <i>ブール値</i> | スプライン正接のThicknessを自動的に設定し、<b>開始Thickness</b>から<b>終了Thickness</b>まで直線的に補間します。<br><i>注：</i> Thicknessは特定のスプラインノードによって使用されます。 |
| <b>接線Thickness</b> <i>フロート</i> | <b>p2</b>点で制御される正接によって駆動されるThicknessを調整します。<br>これは、<b>p1</b>から引き離され、<b>p3</b>に入る際に、スプラインに沿ったThicknessに影響を与えます。<br><i>注：</i> Thicknessは、特定のスプラインノードによって使用されます。<br><i>注意2:</i>このパラメーターは、<b>自動Thickness</b>が&#39;False&#39;に設定されている場合にのみ使用できます。 |
| <b>点の座標</b> |  |
| <b>p1</b> <i>浮動小数点2</i> | テクスチャ空間の<b>p1</b>ポイントの位置を設定します。 |
| <b>p2</b> <i>浮動小数点2</i> | テクスチャ領域の<b>p2</b>ポイントの位置を設定します。<br><b>p2</b>ポイントは、<b>p1</b>ポイントと<b>p3</b>ポイントの両方の<i>正接</i>を制御します。 |
| <b>p3</b> <i>浮動小数点2</i> | テクスチャ空間の<b>p3</b>ポイントの位置を設定します。 |
| <b>プレビュー</b> |  |
| <b>接線を表示</b> <i>ブール値</i> | <b>プレビュー</b>出力の<b>p1</b>ポイントの&#39;out&#39; 正接と<b>p3</b>ポイントの&#39;in&#39; 正接を表示します。 スプラインの方向を反転します。 |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | <b>プレビュー</b>出力のスプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>セグメント数</b> <i>整数</i> | <b>プレビュー</b>出力でスプラインの可視化に使用されるセグメントの数を調整します。<br>値を大きくすると、より滑らかな線になります。 |
| <b>Thickness (px)</b> <i>フロート</i> | <b>プレビュー</b>出力のスプラインビジュアライゼーションのThicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![スプライン（二次）：例1](spline-quadratic.resources/spline-quadratic-example-1.png "スプライン（二次）：例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![スプライン（二次）：例2](spline-quadratic.resources/spline-quadratic-example-2.png "スプライン（二次）：例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![スプライン（二次）:デモ](spline-quadratic.resources/spline-quadratic-demo.gif "スプライン（二次）:デモ"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
