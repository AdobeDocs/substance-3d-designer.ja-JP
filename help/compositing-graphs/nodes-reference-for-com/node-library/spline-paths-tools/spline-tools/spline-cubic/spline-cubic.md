---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: 曲線パスの4つの制御点を持つ滑らかな三次スプラインを作成するには、[スプライン] [三次]ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン（3次）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---


# スプライン（3次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-cubic.resources/spline-cubic-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つの点<b>p1 </b>と<b>p2</b>の間の任意の位置に1つのスプラインを生成します。

スプラインの軌道は、<b>p1</b>の&#39;out&#39; 正接と<b>p2</b>の&#39;in&#39; 正接によって制御されます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

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
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。 |
| <b>入力スプラインを追加</b> <i>ブール値</i> | 生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。 これは均一な分布にも影響を与えます。 |
| <b>Height</b> |  |
| <b>Heightの開始</b> <i>フロート</i> | p1点のHeightを調整します。この値が小さいほど、位置が低くなり、深くなります。 これは、p1でのスプラインのHeightに影響を与えます。 |
| <b>エンドHeight</b> <i>フロート</i> | p2ポイントのHeightを調整します。ここで、値が小さいほど、場所が低くなり、深くなります。 これは、p2でのスプラインのThicknessに影響を与えます。 |
| <b>自動接線Height</b> <i>ブール値</i> | スプライン正接のHeightを自動的に設定し、開始Heightから終了Heightまで直線的に補間します。 |
| <b>p1接線Height</b> <i>浮動小数</i> （&#39;自動正接Height&#39;がTrueの場合に利用可能） | p1ポイントの「out」正接のHeightを調整します。この値が小さいほど、場所が低くなり、深くなります。 これにより、スプラインがp1から離れるときのHeightに影響します。 |
| <b>p2接線Height</b> <i>浮動小数</i> （&#39;自動正接Height&#39;がTrueの場合に利用可能） | p2ポイントの「in」正接のHeightを調整します。この値が小さいほど、場所が低くなり、深くなります。 これにより、スプラインがp2から離れるときのHeightが変化します。 |
| <b>Thickness</b> |  |
| <b>Thicknessの開始</b> <i>フロート</i> | p1点のThicknessを調整します。 これは、p1.<br>のスプラインのThicknessに影響を与えます。注： Thicknessは特定のスプラインノードによって使用されます。 |
| <b>エンドThickness</b> <i>フロート</i> | p2点のThicknessを調整します。 これは、p2.<br>のスプラインのThicknessに影響を与えます。注： Thicknessは特定のスプラインノードによって使用されます。 |
| <b>自動接線Thickness</b> <i>ブール値</i> | 開始Thicknessから終了正接まで直線的に補間するスプラインThicknessのThicknessを自動で設定します。<br>注：Thicknessは特定のスプラインノードによって使用されます。 |
| <b>p1接線Thickness</b> <i>浮動小数</i> （&#39;自動正接Thickness&#39;がTrueの場合に利用可能） | p1の「out」正接のThicknessを補正します。 これは、p1から引き離されるときのスプラインに沿ったThicknessに影響を与えます。<br>注： Thicknessは特定のスプラインノードによって使用されます。 |
| <b>p2接線Thickness</b> <i>浮動小数</i> （&#39;自動正接Thickness&#39;がTrueの場合に利用可能） | p2ポイントの「in」正接のThicknessを調整します。 これは、p2.<br>から引き離されるときのスプラインに沿ったThicknessに影響を与えます。注： Thicknessは特定のスプラインノードによって使用されます。 |
| <b>点の座標</b> |  |
| <b>p1</b> <i>浮動小数点2</i> | テクスチャ空間のp1ポイントの位置を設定します。 |
| <b>p1接線</b> <i>浮動小数点2</i> | テクスチャ空間でのp1ポイントの「out」正接ハンドルの位置を設定します。 |
| <b>p2</b> <i>浮動小数点2</i> | テクスチャ空間のp2ポイントの位置を設定します。 |
| <b>p2接線</b> <i>浮動小数点2</i> | テクスチャ空間でのp2ポイントの&#39;in&#39; 正接ハンドルの位置を設定します。 |
| <b>プレビュー</b> |  |
| <b>接線を表示</b> <i>ブール値</i> | プレビュー出力にp1ポイントの「out」正接とp2ポイントの「in」正接を表示します。 |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインのビジュアライゼーションを描画するために使用するセグメントの数を調整します。 値が大きいほど、線は滑らかになります。 |
| <b>Thickness (px)</b> <i>フロート</i> | プレビュー出力のスプラインビジュアライゼーションのThicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](spline-cubic.resources/SplineCubic-Variant1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-cubic.resources/SplineCubic-Variant2.jpg "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例3](spline-cubic.resources/SplineCubic-Demo.gif "ノードの例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
