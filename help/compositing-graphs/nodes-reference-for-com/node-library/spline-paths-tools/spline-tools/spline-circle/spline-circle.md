---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: '[スプライン円]ノードを使用して、丸いパターンとシェイプを生成するための円形スプラインを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン円
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# スプライン円

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-circle-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

円のシェイプの単一のスプラインを生成します。

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

<b>円の半径</b> *フロート*\
テクスチャ空間の円の半径を調整します。

<b>円の事前回転</b> *フロート*\
「サイズ」を適用する前に、基準円に回転を適用します。

<b>円のサイズ</b> *浮動小数点2*\
円の水平方向のサイズ(X)と垂直方向のサイズ(Y)を調整します。

<b>回転後の円</b> *フロート*\
[サイズ]を適用した後で、ベース円に回転を適用します。

<b>円の位置</b> *浮動小数点2*\
テクスチャ空間の円の中心の位置を設定します。

<b>Thicknessの開始</b> *フロート*&#x200B;円の始点のThicknessを調整します。\
このThicknessは、スプラインに沿って終了Thicknessまで補間されます。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>エンドThickness</b> *フロート*&#x200B;円の終点のThicknessを調整します。\
このThicknessは、スプラインに沿って開始Thicknessまで補間されます。\
注記： Thicknessは特定のスプラインノードで使用されます。

<b>Heightの開始</b> *フロート*&#x200B;円の開始点のHeightを調整します。ここで、値が小さいほど位置が低くなり、値が大きいほど位置が深くなります。\
このHeightは、スプラインに沿って終了Heightまで補間されます。

<b>エンドHeight</b> *フロート*&#x200B;円の終点のHeightを調整します。ここで、値が小さいほど位置が低くなり、値が大きいほど位置が深くなります。\
このHeightは、開始Heightからスプラインに沿って補間されます。

<b>トリミング</b> *フロート2*&#x200B;スプラインの始点と終点を円に沿ってオフセットします。\
これらの値は正規化されます。

<b>らせん状</b> *フロート*&#x200B;円の始点を半径から中心に移動します。\
次に、中心からの距離がスプラインに沿ってスプラインの終点まで補間されます。\
この値は正規化されます。

<b>らせん旋回</b> *浮動小数*&#x200B;緩和曲線の中心を中心とした回転の回数を定義します。

<b>スパイラルパワー</b> *片側固定曲線*&#x200B;緩和曲線の描画に使用した中心からの距離に対してパワーカーブを適用します。\
1より大きい値を指定すると、緩和曲線の大部分が中心に近い状態を維持します。

<b>方向を反転</b> *ブール値*\
スプラインの方向を反転します。

<b>均一な分布</b> *ブール値*\
Trueの場合、スプラインの点は始点から終点まで等間隔になります。

<b>入力スプラインを追加</b> *ブール値*\
生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。

<b>非正方形の補正&#x200B;</b>*ブール値*&#x200B;ポイントの位置とThicknessを調整して、非正方形の解像度でスプラインのシェイプを保持します。\
これは均一な分布にも影響を与えます。

+++プレビュー
<b>方向ヘルパーの表示</b> *ブール値*&#x200B;プレビュー出力のスプラインの始点に点を表示し、終点に矢印を表示します。

<b>Thicknessの封筒を表示</b> *ブール値*\
スプラインのThicknessのエッジに追加の線分を表示します。

<b>セグメント数</b> *整数*&#x200B;プレビュー出力でスプラインの視覚化を描画するために使用するセグメントの数を調整します。\
値が大きいほど、線は滑らかになります。

<b>Thickness (px)</b> *フロート*&#x200B;プレビュー出力のスプラインの表示のThicknessをピクセル単位で調整します。

+++

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](../../../../../../assets/SplineCircle-Variant1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineCircle-Demo.gif "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![例3](../../../../../../assets/SplineCircle-Variant2.jpg "例3")

</td>
<td style="border: 0;" valign="top">

![例4](../../../../../../assets/SplineCircle-Variant3.jpg "例4")

</td>
</tr>
</table>
