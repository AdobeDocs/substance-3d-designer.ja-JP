---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: '[スプライン2D変換]ノードを使用すると、移動、回転、およびスケーリング操作でスプラインを変換できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン2D変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# スプライン2D変換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-2d-transform-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

方向の反転を含むすべての入力スプラインにグローバル変換を適用します。

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

<b>方向を反転</b> *ブール値*&#x200B;スプラインの方向を反転します。

<b>マトリックスの変形</b> *Float4*&#x200B;スプラインに適用される変換行列です。\
行列パラメーターを編集するには、次の3つのモードを使用できます。\
*– 変換ギズモ*:スプライン2D変換ノードが選択されている場合、2Dビューに表示されたギズモのハンドルを微調整します。\
*– 回転/ストレッチ*:スプラインの回転とストレッチを個別に制御します。 値は常に現在の変換に対して相対的に適用されることに注意してください。 例えば、50%の幅を2回適用すると、25%の幅になります。\
*– 行列の値*: [行列の値の編集]ボタンをクリックして、行列の生の数値を直接入力します。

<b>オフセット</b> *Float2*&#x200B;位置オフセットをX （水平）およびY （垂直）方向のスプラインに適用します。

+++プレビュー
<b>方向ヘルパーの表示</b> *ブール値*&#x200B;プレビュー出力のスプラインの始点に点を表示し、終点に矢印を表示します。

<b>Thicknessの封筒を表示</b> *ブール値*\
スプラインのThicknessのエッジに追加の線分を表示します。

<b>セグメント数</b> *整数*&#x200B;プレビュー出力でスプラインの視覚化を描画するために使用するセグメントの数を調整します。\
値が大きいほど、線は滑らかになります。

<b>Thickness (px)</b> *フロート*&#x200B;プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。

+++

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant2-After.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
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

![ノードの例1](../../../../../../assets/Spline2DTransform-Demo1.gif "ノードの例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
