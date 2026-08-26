---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: パス2Dトランスフォームノードを使用すると、パスを移動、回転、スケールの各操作でトランスフォームできます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パス2D変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# パス2D変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/path-2d-transform-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ギズモを使用してパスを変換します。

</td>
</tr>
</table>

## 入力コネクタ

<b>パス</b> *色*\
エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。

## 出力コネクタ

<b>パス</b> *色*\
変換されたパス。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。

## パラメーター

<b>マトリックスの変形</b> *浮動小数点4*\
スプラインに適用される変換行列。 行列パラメーターを編集するには、次の3つのモードを使用できます。\
*– 変換ギズモ：*&#x200B;スプライン2D変換ノードが選択されている場合、[2Dビュー](../../../../../../interface/2d-view/2d-view.md)に表示されたギズモのハンドルを調整します。\
*– 回転/伸縮：*&#x200B;スプラインの回転と伸縮を個別に制御します。 値は常に現在の変換に対して相対的に適用されることに注意してください。 例えば、50%の幅を2回適用すると、25%の幅になります。\
*– 行列の値：* <b>[行列の値の編集]</b>ボタンをクリックして、行列の生の数値を直接入力します。

<b>オフセット</b> *浮動小数点2*\
位置オフセットをX（水平）およびY（垂直）のスプラインに適用します。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
