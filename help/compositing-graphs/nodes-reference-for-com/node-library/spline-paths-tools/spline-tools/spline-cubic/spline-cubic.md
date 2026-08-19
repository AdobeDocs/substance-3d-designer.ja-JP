---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# スプライン（3次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-cubic-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つの点<b>p1 </b>と<b>p2</b>の間の任意の位置に1つのスプラインを生成します。

スプラインの軌道は、<b>p1</b>の「アウト」接線と<b>p2</b>の「イン」接線によって制御されます。

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

<b>方向を反転</b> *ブール値*\
スプラインの方向を反転します。

<b>入力スプラインを追加</b> *ブール値*\
生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。

<b>非正方形の補正&#x200B;</b>*ブール値*&#x200B;ポイントの位置とThicknessを調整して、非正方形の解像度でスプラインのシェイプを保持します。\
これは均一な分布にも影響を与えます。

+++高さ
<b>Heightの開始</b> *フロート* p1ポイントのHeightを調整します。ここで、値が小さいほど、位置が低くなり、深くなります。\
これは、p1でのスプラインのHeightに影響を与えます。

<b>エンドHeight</b> *フロート* p2ポイントのHeightを調整します。このポイントの値が小さいほど、位置が低くなり、深くなります。\
これは、p2でのスプラインのThicknessに影響を与えます。

<b>自動接線Height</b> *ブール値*&#x200B;開始Heightから終了Heightまで直線的に補間するスプライン接線のHeightを自動的に設定します。

<b>p1接線Height</b> *Float* （&#39;Auto Tangent Height&#39;がTrueの場合に使用可能）\
p1点の「out」接線のHeightを調整します。この接線では、値が小さいほど位置が低くなり、値が小さいほど位置が深くなります。\
これにより、スプラインがp1から離れるときのHeightに影響します。

<b>p2接線Height</b> *Float* （&#39;Auto Tangent Height&#39;がTrueの場合に使用可能）\
P2点の「in」接線のHeightを調整します。ここで、値が小さいほど位置が低くなり、深くなります。\
これにより、スプラインがp2から離れるときのHeightが変化します。

+++

+++厚み
<b>Thicknessの開始</b> *フロート* p1の点のThicknessを調整します。\
これは、p1でのスプラインのThicknessに影響を与えます。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>エンドThickness</b> *浮動小数点* p2のThicknessを調整します。\
これは、p2でのスプラインのThicknessに影響を与えます。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>自動接線Thickness</b> *ブール値*&#x200B;開始Thicknessから終了Thicknessまで直線的に補間するスプライン接線のThicknessを自動的に設定します。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>p1接線Thickness</b> *Float* （&#39;Auto Tangent Thickness&#39;がTrueの場合に使用可能）\
p1点の「アウト」接線のThicknessを調整します。\
これにより、スプラインがp1から離れるときのThicknessに影響します。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>p2接線Thickness</b> *Float* （&#39;Auto Tangent Thickness&#39;がTrueの場合に使用可能）\
p2点の&#39;in&#39;接線のThicknessを調整します。\
これにより、スプラインがp2から離れるときのThicknessが変化します。\
注記： Thicknessは特定のスプラインノードで使用されます。

+++

+++点の座標
<b>p1</b> *フロート2*&#x200B;テクスチャ空間のp1ポイントの位置を設定します。

<b>p1接線</b> *Float2*&#x200B;テクスチャ空間のp1ポイントの&#39;out&#39;接線ハンドルの位置を設定します。

<b>p2</b> *浮動小数点2*&#x200B;テクスチャ空間のp2ポイントの位置を設定します。

<b>p2接線</b> *Float2*&#x200B;テクスチャ空間のP2ポイント&#39;in&#39;接線ハンドルの位置を設定します。

+++

+++プレビュー
<b>接線を表示</b> *ブール値*&#x200B;プレビュー出力にp1点&#39;out&#39;接線とp2点&#39;in&#39;接線を表示します。

<b>方向ヘルパーの表示</b> *ブール値*&#x200B;プレビュー出力のスプラインの始点に点を表示し、終点に矢印を表示します。

<b>セグメント数</b> *整数*&#x200B;プレビュー出力でスプラインの視覚化を描画するために使用するセグメントの数を調整します。\
値が大きいほど、線は滑らかになります。

<b>Thickness (px)</b> *フロート*&#x200B;プレビュー出力のスプラインの表示のThicknessをピクセル単位で調整します。

+++

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](../../../../../../assets/SplineCubic-Variant1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineCubic-Variant2.jpg "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例3](../../../../../../assets/SplineCubic-Demo.gif "ノードの例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
