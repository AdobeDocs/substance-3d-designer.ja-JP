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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# スプライン（二次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![スプライン（二次）:アイコン](../../../../../../assets/spline-quadratic-icon.png "スプライン（二次）:アイコン")

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

## 入力コネクタ

|  |  |
| --- | --- |
| <b>プレビュー</b> *グレースケール* | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> *色* | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標： <b>R</b> - X位置<b>G</b> - Y位置<b>B</b> - Height <b>A</b> – パックデータ： – 記号：スプラインが閉じている（負）または開いている（正）; – 絶対値： Thickness + 1。 |
| <b>スプラインデータ</b> *色* | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ： <b>R</b> – 接線X <b>G</b> – 接線Y <b>B</b> – 接線Z <b>A</b> – 未使用 |
| <b>スプラインの量</b> *整数* | 入力スプラインの数。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>プレビュー</b> *グレースケール* | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> *色* | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの点の座標： <b>R</b> - X位置<b>G</b> - Y位置<b>B</b> - Height <b>A</b> – パックデータ： – 記号：スプラインが閉じている（負）または開いている（正）; – 絶対値： Thickness + 1。 |
| <b>スプラインデータ</b> *色* | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ： <b>R</b> – 接線X <b>G</b> – 接線Y <b>B</b> – 接線Z <b>A</b> – 未使用 |
| <b>スプラインの量</b> *整数* | 出力スプラインの数。 |

## パラメーター

|  |  |
| --- | --- |
| <b>方向を反転</b> *ブール値* | スプラインの方向を反転します。 |
| <b>均一な分布</b> *ブール値* | *True*&#x200B;の場合、スプラインの点は始点から終点まで等間隔になります。 |
| <b>入力スプラインを追加</b> *ブール値* | 生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。 |
| <b>非正方形の修正</b> *ブール値* | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。 これは均一な分布にも影響を与えます。 |
| <b>Smoothness</b> *フロート* | スプラインによって形成される円弧&#x200B;*の*&#x200B;スパンを調整します。ここで、1はスプラインの全長が弧を描くことを意味し、0はスプラインが完全にまっすぐであることを意味します。 円弧は、スプラインに沿って点<b>p3</b>から端まで進行します。 |

+++高さ

|  |  |
| --- | --- |
| <b>Heightの開始</b> *フロート* | <b>p1</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。  これは、<b>p1</b>のスプラインのHeightに影響します。 |
| <b>エンドHeight</b> *フロート* | <b>p3</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。  これは、<b>p3</b>のスプラインのThicknessに影響を与えます。 |
| <b>自動接線Height</b> *ブール値* | <b>p3</b>ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。  これは、<b>p3</b>のスプラインのThicknessに影響を与えます。 |
| <b>接線Height</b> *フロート* | <b>p2</b>点で制御される接線によって駆動されるHeightを調整します。  これは、<b>p1</b>から引き離され、<b>p3</b>に入る際に、スプラインに沿ったHeightに影響を与えます。   *注意：*&#x200B;このパラメーターは、<b>自動接線Height</b>が&#39;False&#39;に設定されている場合にのみ使用できます。 |


+++

+++厚み

|  |  |
| --- | --- |
| <b>Thicknessの開始</b> *フロート* | <b>p1</b>ポイントのThicknessを調整します。 これは、<b>p1</b>のスプラインのThicknessに影響します。   *注：* Thicknessは特定のスプラインノードによって使用されています。 |
| <b>エンドThickness</b> *フロート* | <b>p3</b>ポイントのThicknessを調整します。 これは、<b>p3</b>のスプラインのThicknessに影響を与えます。   *注：* Thicknessは特定のスプラインノードによって使用されています。 |
| <b>自動接線Thickness</b> *ブール値* | <b>開始Thickness</b>から<b>終了Thickness</b>まで直線的に補間するスプライン接線のThicknessを自動設定します。   *注：* Thicknessは特定のスプラインノードによって使用されています。 |
| <b>接線Thickness</b> *フロート* | <b>p2</b>点で制御される接線によって駆動されるThicknessを調整します。  これは、<b>p1</b>から引き離され、<b>p3</b>に入る際に、スプラインに沿ったThicknessに影響を与えます。   *注：* Thicknessは特定のスプラインノードによって使用されています。  *注2:*&#x200B;このパラメーターは、<b>自動接線Thickness</b>が&#39;False&#39;に設定されている場合にのみ使用できます。 |


+++

+++点の座標

|  |  |
| --- | --- |
| <b>p1</b> *浮動小数点2* | テクスチャ空間の<b>p1</b>ポイントの位置を設定します。 |
| <b>p2</b> *浮動小数点2* | テクスチャ空間の<b>p2</b>ポイントの位置を設定します。  <b>p2</b>ポイントは、<b>p1</b>ポイントと<b>p3</b>ポイントの両方の&#x200B;*接線*&#x200B;を制御します。 |
| <b>p3</b> *浮動小数点2* | テクスチャ空間の<b>p3</b>ポイントの位置を設定します。 |


+++

+++プレビュー

|  |  |
| --- | --- |
| <b>接線を表示</b> *ブール値* | <b>プレビュー</b>出力の<b>p1</b>ポイント&#39;out&#39;接線と<b>p3</b>ポイント&#39;in&#39;接線を表示します。スプラインの方向を反転します。 |
| <b>方向ヘルパーの表示</b> *ブール値* | <b>プレビュー</b>出力のスプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> *ブール値* | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>セグメント数</b> *整数* | <b>プレビュー</b>出力でスプラインの視覚化を描画するために使用するセグメントの数を調整します。  値が大きいほど、線は滑らかになります。 |
| <b>Thickness (px)</b> *フロート* | <b>プレビュー</b>出力のスプラインビジュアライゼーションのThicknessをピクセル単位で調整します。 |


+++

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![スプライン（二次）：例1](../../../../../../assets/spline-quadratic-example-1.png "スプライン（二次）：例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![スプライン（二次）：例2](../../../../../../assets/spline-quadratic-example-2.png "スプライン（二次）：例2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![スプライン（二次）:デモ](../../../../../../assets/spline-quadratic-demo.gif "スプライン（二次）:デモ"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
